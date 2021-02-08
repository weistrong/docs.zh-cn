---
description: 了解有关以下内容的详细信息： FILESTREAM 数据
title: FILESTREAM 数据
ms.date: 03/30/2017
ms.assetid: bd8b845c-0f09-4295-b466-97ef106eefa8
ms.openlocfilehash: 0110be6b867a07ec1cd204e2a3de371367bbfa36
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802042"
---
# <a name="filestream-data"></a><span data-ttu-id="368db-103">FILESTREAM 数据</span><span class="sxs-lookup"><span data-stu-id="368db-103">FILESTREAM Data</span></span>

<span data-ttu-id="368db-104">FILESTREAM 存储属性可用于 varbinary(max) 列中存储的二进制 (BLOB) 数据。</span><span class="sxs-lookup"><span data-stu-id="368db-104">The FILESTREAM storage attribute is for binary (BLOB) data stored in a varbinary(max) column.</span></span> <span data-ttu-id="368db-105">在使用 FILESTREAM 之前，存储二进制数据需要经过特殊处理。</span><span class="sxs-lookup"><span data-stu-id="368db-105">Before FILESTREAM, storing binary data required special handling.</span></span> <span data-ttu-id="368db-106">非结构化数据（例如文本文档、图像和视频）通常存储在数据库外部，因此难以管理。</span><span class="sxs-lookup"><span data-stu-id="368db-106">Unstructured data, such as text documents, images and video, is often stored outside of the database, making it difficult to manage.</span></span>

> [!NOTE]
> <span data-ttu-id="368db-107">您必须安装 .NET Framework 3.5 SP1（或更高版本）才能使用 SqlClient 处理 FILESTREAM 数据。</span><span class="sxs-lookup"><span data-stu-id="368db-107">You must install the .NET Framework 3.5 SP1 (or later) to work with FILESTREAM data using SqlClient.</span></span>

<span data-ttu-id="368db-108">在 varbinary(max) 列上指定 FILESTREAM 特性会致使 SQL Server 将数据存储在本地 NTFS 文件系统中，而不是存储在数据库文件中。</span><span class="sxs-lookup"><span data-stu-id="368db-108">Specifying the FILESTREAM attribute on a varbinary(max) column causes SQL Server to store the data on the local NTFS file system instead of in the database file.</span></span> <span data-ttu-id="368db-109">虽然数据是单独存储的，但可以使用受支持的相同 Transact-SQL 语句处理存储在数据库中的 varbinary(max) 数据。</span><span class="sxs-lookup"><span data-stu-id="368db-109">Although it is stored separately, you can use the same Transact-SQL statements that are supported for working with varbinary(max) data that is stored in the database.</span></span>

## <a name="sqlclient-support-for-filestream"></a><span data-ttu-id="368db-110">SqlClient 对 FILESTREAM 的支持</span><span class="sxs-lookup"><span data-stu-id="368db-110">SqlClient Support for FILESTREAM</span></span>

<span data-ttu-id="368db-111">用于 SQL Server 的 .NET Framework 数据提供程序 <xref:System.Data.SqlClient> 支持使用 <xref:System.Data.SqlTypes.SqlFileStream> 在命名空间中定义的类读取和写入 FILESTREAM 数据 <xref:System.Data.SqlTypes> 。</span><span class="sxs-lookup"><span data-stu-id="368db-111">The .NET Framework Data Provider for SQL Server, <xref:System.Data.SqlClient>, supports reading and writing to FILESTREAM data using the <xref:System.Data.SqlTypes.SqlFileStream> class defined in the <xref:System.Data.SqlTypes> namespace.</span></span> <span data-ttu-id="368db-112">`SqlFileStream` 继承自 <xref:System.IO.Stream> 类，该类提供了用于读写数据流的方法。</span><span class="sxs-lookup"><span data-stu-id="368db-112">`SqlFileStream` inherits from the <xref:System.IO.Stream> class, which provides methods for reading and writing to streams of data.</span></span> <span data-ttu-id="368db-113">从流中读取会将数据从流传输到数据结构（如字节数组）中。</span><span class="sxs-lookup"><span data-stu-id="368db-113">Reading from a stream transfers data from the stream into a data structure, such as an array of bytes.</span></span> <span data-ttu-id="368db-114">写入数据会将数据从数据结构传输到流中。</span><span class="sxs-lookup"><span data-stu-id="368db-114">Writing transfers the data from the data structure into a stream.</span></span>

### <a name="creating-the-sql-server-table"></a><span data-ttu-id="368db-115">创建 SQL Server 表</span><span class="sxs-lookup"><span data-stu-id="368db-115">Creating the SQL Server Table</span></span>

<span data-ttu-id="368db-116">下列 Transact-SQL 语句将创建一个名为 employees 的表并插入一行数据。</span><span class="sxs-lookup"><span data-stu-id="368db-116">The following Transact-SQL statements creates a table named employees and inserts a row of data.</span></span> <span data-ttu-id="368db-117">启用 FILESTREAM 存储后，可以将此表与下面的代码示例结合使用。</span><span class="sxs-lookup"><span data-stu-id="368db-117">Once you have enabled FILESTREAM storage, you can use this table in conjunction with the code examples that follow.</span></span> <span data-ttu-id="368db-118">本主题末尾提供了 SQL Server 联机丛书中资源的链接。</span><span class="sxs-lookup"><span data-stu-id="368db-118">The links to resources in SQL Server Books Online are located at the end of this topic.</span></span>

```sql
CREATE TABLE employees
(
  EmployeeId INT  NOT NULL  PRIMARY KEY,
  Photo VARBINARY(MAX) FILESTREAM  NULL,
  RowGuid UNIQUEIDENTIFIER  NOT NULL  ROWGUIDCOL
  UNIQUE DEFAULT NEWID()
)
GO
Insert into employees
Values(1, 0x00, default)
GO
```

### <a name="example-reading-overwriting-and-inserting-filestream-data"></a><span data-ttu-id="368db-119">示例：读取、覆盖和插入 FILESTREAM 数据</span><span class="sxs-lookup"><span data-stu-id="368db-119">Example: Reading, Overwriting, and Inserting FILESTREAM Data</span></span>

<span data-ttu-id="368db-120">下面的示例演示如何从 FILESTREAM 读取数据。</span><span class="sxs-lookup"><span data-stu-id="368db-120">The following sample demonstrates how to read data from a FILESTREAM.</span></span> <span data-ttu-id="368db-121">该代码获取文件的逻辑路径，将 `FileAccess` 设置为 `Read`，并将 `FileOptions` 设置为 `SequentialScan`。</span><span class="sxs-lookup"><span data-stu-id="368db-121">The code gets the logical path to the file, setting the `FileAccess` to `Read` and the `FileOptions` to `SequentialScan`.</span></span> <span data-ttu-id="368db-122">然后，该代码将 SqlFileStream 中的字节读取到缓冲区中。</span><span class="sxs-lookup"><span data-stu-id="368db-122">The code then reads the bytes from the SqlFileStream into the buffer.</span></span> <span data-ttu-id="368db-123">然后，将字节写入控制台窗口。</span><span class="sxs-lookup"><span data-stu-id="368db-123">The bytes are then written to the console window.</span></span>

<span data-ttu-id="368db-124">该示例还演示了如何将数据写入到 FILESTREAM（其中现有的所有数据将被覆盖）。</span><span class="sxs-lookup"><span data-stu-id="368db-124">The sample also demonstrates how to write data to a FILESTREAM in which all existing data is overwritten.</span></span> <span data-ttu-id="368db-125">该代码获取文件的逻辑路径，并创建 `SqlFileStream`，将 `FileAccess` 设置为 `Write`，将 `FileOptions` 设置为 `SequentialScan`。</span><span class="sxs-lookup"><span data-stu-id="368db-125">The code gets the logical path to the file and creates the `SqlFileStream`, setting the `FileAccess` to `Write` and the `FileOptions` to `SequentialScan`.</span></span> <span data-ttu-id="368db-126">将一个字节写入 `SqlFileStream`，替换文件中的所有数据。</span><span class="sxs-lookup"><span data-stu-id="368db-126">A single byte is written to the `SqlFileStream`, replacing any data in the file.</span></span>

<span data-ttu-id="368db-127">示例还演示了如何通过使用 Seek 方法将数据附加到 FILESTREAM 文件的结尾，以将数据写入到其中。</span><span class="sxs-lookup"><span data-stu-id="368db-127">The sample also demonstrates how to write data to a FILESTREAM by using the Seek method to append data to the end of the file.</span></span> <span data-ttu-id="368db-128">该代码获取文件的逻辑路径，并创建 `SqlFileStream`，将 `FileAccess` 设置为 `ReadWrite`，将 `FileOptions` 设置为 `SequentialScan`。</span><span class="sxs-lookup"><span data-stu-id="368db-128">The code gets the logical path to the file and creates the `SqlFileStream`, setting the `FileAccess` to `ReadWrite` and the `FileOptions` to `SequentialScan`.</span></span> <span data-ttu-id="368db-129">此代码使用 Seek 方法查找到文件的末尾，并向现有文件追加一个字节。</span><span class="sxs-lookup"><span data-stu-id="368db-129">The code uses the Seek method to seek to the end of the file, appending a single byte to the existing file.</span></span>

```csharp
using System;
using System.Data.SqlClient;
using System.Data.SqlTypes;
using System.Data;
using System.IO;

namespace FileStreamTest
{
    class Program
    {
        static void Main(string[] args)
        {
            SqlConnectionStringBuilder builder = new SqlConnectionStringBuilder("server=(local);integrated security=true;database=myDB");
            ReadFileStream(builder);
            OverwriteFileStream(builder);
            InsertFileStream(builder);

            Console.WriteLine("Done");
        }

        private static void ReadFileStream(SqlConnectionStringBuilder connStringBuilder)
        {
            using (SqlConnection connection = new SqlConnection(connStringBuilder.ToString()))
            {
                connection.Open();
                SqlCommand command = new SqlCommand("SELECT TOP(1) Photo.PathName(), GET_FILESTREAM_TRANSACTION_CONTEXT() FROM employees", connection);

                SqlTransaction tran = connection.BeginTransaction(IsolationLevel.ReadCommitted);
                command.Transaction = tran;

                using (SqlDataReader reader = command.ExecuteReader())
                {
                    while (reader.Read())
                    {
                        // Get the pointer for the file
                        string path = reader.GetString(0);
                        byte[] transactionContext = reader.GetSqlBytes(1).Buffer;

                        // Create the SqlFileStream
                        using (Stream fileStream = new SqlFileStream(path, transactionContext, FileAccess.Read, FileOptions.SequentialScan, allocationSize: 0))
                        {
                            // Read the contents as bytes and write them to the console
                            for (long index = 0; index < fileStream.Length; index++)
                            {
                                Console.WriteLine(fileStream.ReadByte());
                            }
                        }
                    }
                }
                tran.Commit();
            }
        }

        private static void OverwriteFileStream(SqlConnectionStringBuilder connStringBuilder)
        {
            using (SqlConnection connection = new SqlConnection(connStringBuilder.ToString()))
            {
                connection.Open();

                SqlCommand command = new SqlCommand("SELECT TOP(1) Photo.PathName(), GET_FILESTREAM_TRANSACTION_CONTEXT() FROM employees", connection);

                SqlTransaction tran = connection.BeginTransaction(IsolationLevel.ReadCommitted);
                command.Transaction = tran;

                using (SqlDataReader reader = command.ExecuteReader())
                {
                    while (reader.Read())
                    {
                        // Get the pointer for file
                        string path = reader.GetString(0);
                        byte[] transactionContext = reader.GetSqlBytes(1).Buffer;

                        // Create the SqlFileStream
                        using (Stream fileStream = new SqlFileStream(path, transactionContext, FileAccess.Write, FileOptions.SequentialScan, allocationSize: 0))
                        {
                            // Write a single byte to the file. This will
                            // replace any data in the file.
                            fileStream.WriteByte(0x01);
                        }
                    }
                }
                tran.Commit();
            }
        }

        private static void InsertFileStream(SqlConnectionStringBuilder connStringBuilder)
        {
            using (SqlConnection connection = new SqlConnection(connStringBuilder.ToString()))
            {
                connection.Open();

                SqlCommand command = new SqlCommand("SELECT TOP(1) Photo.PathName(), GET_FILESTREAM_TRANSACTION_CONTEXT() FROM employees", connection);

                SqlTransaction tran = connection.BeginTransaction(IsolationLevel.ReadCommitted);
                command.Transaction = tran;

                using (SqlDataReader reader = command.ExecuteReader())
                {
                    while (reader.Read())
                    {
                        // Get the pointer for file
                        string path = reader.GetString(0);
                        byte[] transactionContext = reader.GetSqlBytes(1).Buffer;

                        using (Stream fileStream = new SqlFileStream(path, transactionContext, FileAccess.ReadWrite, FileOptions.SequentialScan, allocationSize: 0))
                        {
                            // Seek to the end of the file
                            fileStream.Seek(0, SeekOrigin.End);

                            // Append a single byte
                            fileStream.WriteByte(0x01);
                        }
                    }
                }
                tran.Commit();
            }

        }
    }
}
```

<span data-ttu-id="368db-130">关于另一个示例，请参见[如何将二进制数据存储和提取到文件流列中](https://www.codeproject.com/Articles/32216/How-to-store-and-fetch-binary-data-into-a-file-str)。</span><span class="sxs-lookup"><span data-stu-id="368db-130">For another sample, see [How to store and fetch binary data into a file stream column](https://www.codeproject.com/Articles/32216/How-to-store-and-fetch-binary-data-into-a-file-str).</span></span>

## <a name="resources-in-sql-server-books-online"></a><span data-ttu-id="368db-131">SQL Server 联机丛书中的资源</span><span class="sxs-lookup"><span data-stu-id="368db-131">Resources in SQL Server Books Online</span></span>

<span data-ttu-id="368db-132">FILESTREAM 的完整文档位于 SQL Server 联机丛书中的以下各节中。</span><span class="sxs-lookup"><span data-stu-id="368db-132">The complete documentation for FILESTREAM is located in the following sections in SQL Server Books Online.</span></span>

|<span data-ttu-id="368db-133">主题</span><span class="sxs-lookup"><span data-stu-id="368db-133">Topic</span></span>|<span data-ttu-id="368db-134">说明</span><span class="sxs-lookup"><span data-stu-id="368db-134">Description</span></span>|
|-----------|-----------------|
|[<span data-ttu-id="368db-135">FILESTREAM (SQL Server)</span><span class="sxs-lookup"><span data-stu-id="368db-135">FILESTREAM (SQL Server)</span></span>](/sql/relational-databases/blob/filestream-sql-server)|<span data-ttu-id="368db-136">介绍何时使用 FILESTREAM 存储以及它如何将 SQL Server 数据库引擎与 NTFS 文件系统集成。</span><span class="sxs-lookup"><span data-stu-id="368db-136">Describes when to use FILESTREAM storage and how it integrates the SQL Server Database Engine with an NTFS file system.</span></span>|
|[<span data-ttu-id="368db-137">为 FILESTREAM 数据创建客户端应用程序</span><span class="sxs-lookup"><span data-stu-id="368db-137">Create Client Applications for FILESTREAM Data</span></span>](/sql/relational-databases/blob/create-client-applications-for-filestream-data)|<span data-ttu-id="368db-138">介绍用于处理 FILESTREAM 数据的 Windows API 函数。</span><span class="sxs-lookup"><span data-stu-id="368db-138">Describes the Windows API functions for working with FILESTREAM data.</span></span>|
|[<span data-ttu-id="368db-139">FILESTREAM 与其他 SQL Server 功能</span><span class="sxs-lookup"><span data-stu-id="368db-139">FILESTREAM and Other SQL Server Features</span></span>](/sql/relational-databases/blob/filestream-compatibility-with-other-sql-server-features)|<span data-ttu-id="368db-140">提供将 FILESTREAM 数据与 SQL Server 的其他功能一起使用时的注意事项、准则和限制。</span><span class="sxs-lookup"><span data-stu-id="368db-140">Provides considerations, guidelines and limitations for using FILESTREAM data with other features of SQL Server.</span></span>|

## <a name="see-also"></a><span data-ttu-id="368db-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="368db-141">See also</span></span>

- [<span data-ttu-id="368db-142">SQL Server 数据类型和 ADO.NET</span><span class="sxs-lookup"><span data-stu-id="368db-142">SQL Server Data Types and ADO.NET</span></span>](sql-server-data-types.md)
- [<span data-ttu-id="368db-143">在 ADO.NET 中检索和修改数据</span><span class="sxs-lookup"><span data-stu-id="368db-143">Retrieving and Modifying Data in ADO.NET</span></span>](../retrieving-and-modifying-data.md)
- [<span data-ttu-id="368db-144">代码访问安全性和 ADO.NET</span><span class="sxs-lookup"><span data-stu-id="368db-144">Code Access Security and ADO.NET</span></span>](../code-access-security.md)
- [<span data-ttu-id="368db-145">SQL Server 二进制和大值数据</span><span class="sxs-lookup"><span data-stu-id="368db-145">SQL Server Binary and Large-Value Data</span></span>](sql-server-binary-and-large-value-data.md)
- [<span data-ttu-id="368db-146">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="368db-146">ADO.NET Overview</span></span>](../ado-net-overview.md)
