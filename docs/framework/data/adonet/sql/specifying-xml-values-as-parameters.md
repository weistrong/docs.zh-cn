---
description: 了解详细信息：将 XML 值指定为参数
title: 将 XML 值指定为参数
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 2c4d08b8-fc29-4614-97fa-29c8ff7ca5b3
ms.openlocfilehash: 9c5b81270eeaec1fc0b3992971c9285863c92466
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99767448"
---
# <a name="specifying-xml-values-as-parameters"></a><span data-ttu-id="74819-103">将 XML 值指定为参数</span><span class="sxs-lookup"><span data-stu-id="74819-103">Specifying XML Values as Parameters</span></span>

<span data-ttu-id="74819-104">如果查询需要值为 XML 字符串的参数，开发人员可以使用 SqlXml 数据类型的实例提供该值。</span><span class="sxs-lookup"><span data-stu-id="74819-104">If a query requires a parameter whose value is an XML string, developers can supply that value using an instance of the **SqlXml** data type.</span></span> <span data-ttu-id="74819-105">真的没有任何窍门；SQL Server 中的 XML 列接受参数值的方式与其他数据类型完全相同。</span><span class="sxs-lookup"><span data-stu-id="74819-105">There really are no tricks; XML columns in SQL Server accept parameter values in exactly the same way as other data types.</span></span>  
  
## <a name="example"></a><span data-ttu-id="74819-106">示例</span><span class="sxs-lookup"><span data-stu-id="74819-106">Example</span></span>  

 <span data-ttu-id="74819-107">以下控制台应用程序在 AdventureWorks 数据库中新建一个表。</span><span class="sxs-lookup"><span data-stu-id="74819-107">The following console application creates a new table in the **AdventureWorks** database.</span></span> <span data-ttu-id="74819-108">新表包括一个名为 SalesID 的列和一个名为 SalesInfo 的 XML 列。</span><span class="sxs-lookup"><span data-stu-id="74819-108">The new table includes a column named **SalesID** and an XML column named **SalesInfo**.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="74819-109">默认情况下，在安装 SQL Server 时不安装 AdventureWorks 示例数据库。</span><span class="sxs-lookup"><span data-stu-id="74819-109">The **AdventureWorks** sample database is not installed by default when you install SQL Server.</span></span> <span data-ttu-id="74819-110">可以通过运行 SQL Server 安装程序来安装它。</span><span class="sxs-lookup"><span data-stu-id="74819-110">You can install it by running SQL Server Setup.</span></span>  
  
 <span data-ttu-id="74819-111">该示例准备一个 <xref:System.Data.SqlClient.SqlCommand> 对象以在新表中插入行。</span><span class="sxs-lookup"><span data-stu-id="74819-111">The example prepares a <xref:System.Data.SqlClient.SqlCommand> object to insert a row in the new table.</span></span> <span data-ttu-id="74819-112">保存的文件为 SalesInfo 列提供所需的 XML 数据。</span><span class="sxs-lookup"><span data-stu-id="74819-112">A saved file provides the XML data needed for the **SalesInfo** column.</span></span>  
  
 <span data-ttu-id="74819-113">若要创建运行示例所需的文件，请在与项目相同的文件夹中创建一个新的文本文件。</span><span class="sxs-lookup"><span data-stu-id="74819-113">To create the file needed for the example to run, create a new text file in the same folder as your project.</span></span> <span data-ttu-id="74819-114">将文件命名为 MyTestStoreData.xml。</span><span class="sxs-lookup"><span data-stu-id="74819-114">Name the file MyTestStoreData.xml.</span></span> <span data-ttu-id="74819-115">在记事本中打开该文件，然后复制并粘贴以下文本：</span><span class="sxs-lookup"><span data-stu-id="74819-115">Open the file in Notepad and copy and paste the following text:</span></span>  
  
```xml  
<StoreSurvey xmlns="http://schemas.microsoft.com/sqlserver/2004/07/adventure-works/StoreSurvey">  
  <AnnualSales>300000</AnnualSales>  
  <AnnualRevenue>30000</AnnualRevenue>  
  <BankName>International Bank</BankName>  
  <BusinessType>BM</BusinessType>  
  <YearOpened>1970</YearOpened>  
  <Specialty>Road</Specialty>  
  <SquareFeet>7000</SquareFeet>  
  <Brands>3</Brands>  
  <Internet>T1</Internet>  
  <NumberEmployees>2</NumberEmployees>  
</StoreSurvey>  
```  
  
```vb  
Imports System  
Imports System.Data.SqlClient  
Imports System.Data.SqlTypes  
Imports System.Xml  
  
Module Module1  
    Sub Main()  
  
        Using connection As SqlConnection = New SqlConnection(GetConnectionString())  
        connection.Open()  
  
        ' Create a sample table (dropping first if it already  
        ' exists.)  
        Dim commandNewTable As String = _  
         "IF EXISTS (SELECT * FROM dbo.sysobjects " & _  
         "WHERE id = object_id(N'[dbo].[XmlDataTypeSample]') " & _  
         "AND OBJECTPROPERTY(id, N'IsUserTable') = 1) " & _  
         "DROP TABLE [dbo].[XmlDataTypeSample];" & _  
         "CREATE TABLE [dbo].[XmlDataTypeSample](" & _  
         "[SalesID] [int] IDENTITY(1,1) NOT NULL, " & _  
         "[SalesInfo] [xml])"  
  
        Dim commandAdd As New _  
         SqlCommand(commandNewTable, connection)  
        commandAdd.ExecuteNonQuery()  
  
        Dim commandText As String = _  
         "INSERT INTO [dbo].[XmlDataTypeSample] " & _  
           "([SalesInfo] ) " & _  
           "VALUES(@xmlParameter )"  
  
        Dim command As New SqlCommand(commandText, connection)  
  
        ' Read the saved XML document as a
        ' SqlXml-data typed variable.  
        Dim newXml As SqlXml = _  
         New SqlXml(New XmlTextReader("MyTestStoreData.xml"))  
  
        ' Supply the SqlXml value for the value of the parameter.  
        command.Parameters.AddWithValue("@xmlParameter", newXml)  
  
        Dim result As Integer = command.ExecuteNonQuery()  
        Console.WriteLine(result & " row was added.")  
        Console.WriteLine("Press Enter to continue.")  
        Console.ReadLine()  
    End Using  
End Sub  
  
    Private Function GetConnectionString() As String  
        ' To avoid storing the connection string in your code,
        ' you can retrieve it from a configuration file.
        Return "Data Source=(local);Integrated Security=SSPI;" & _  
          "Initial Catalog=AdventureWorks"  
    End Function  
End Module  
```  
  
```csharp  
using System;  
using System.Data;  
using System.Data.SqlClient;  
using System.Xml;  
using System.Data.SqlTypes;  
  
class Class1  
{  
    static void Main()  
    {  
        using (SqlConnection connection = new SqlConnection(GetConnectionString()))  
       {  
        connection.Open();  
        //  Create a sample table (dropping first if it already  
        //  exists.)  
  
        string commandNewTable =
            "IF EXISTS (SELECT * FROM dbo.sysobjects " +
            "WHERE id = " +  
                  "object_id(N'[dbo].[XmlDataTypeSample]') " +
            "AND OBJECTPROPERTY(id, N'IsUserTable') = 1) " +
            "DROP TABLE [dbo].[XmlDataTypeSample];" +
            "CREATE TABLE [dbo].[XmlDataTypeSample](" +
            "[SalesID] [int] IDENTITY(1,1) NOT NULL, " +
            "[SalesInfo] [xml])";  
        SqlCommand commandAdd =
                   new SqlCommand(commandNewTable, connection);  
        commandAdd.ExecuteNonQuery();  
        string commandText =
            "INSERT INTO [dbo].[XmlDataTypeSample] " +
            "([SalesInfo] ) " +
            "VALUES(@xmlParameter )";  
        SqlCommand command =
                  new SqlCommand(commandText, connection);  
  
        //  Read the saved XML document as a
        //  SqlXml-data typed variable.  
        SqlXml newXml =
            new SqlXml(new XmlTextReader("MyTestStoreData.xml"));  
  
        //  Supply the SqlXml value for the value of the parameter.  
        command.Parameters.AddWithValue("@xmlParameter", newXml);  
  
        int result = command.ExecuteNonQuery();  
        Console.WriteLine(result + " row was added.");  
        Console.WriteLine("Press Enter to continue.");  
        Console.ReadLine();  
    }  
  }  
  
    private static string GetConnectionString()  
    {  
        // To avoid storing the connection string in your code,
        // you can retrieve it from a configuration file.
        return "Data Source=(local);Integrated Security=true;" +  
        "Initial Catalog=AdventureWorks; ";  
    }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="74819-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="74819-116">See also</span></span>

- <xref:System.Data.SqlTypes.SqlXml>
- [<span data-ttu-id="74819-117">SQL Server 中的 XML 数据</span><span class="sxs-lookup"><span data-stu-id="74819-117">XML Data in SQL Server</span></span>](xml-data-in-sql-server.md)
- [<span data-ttu-id="74819-118">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="74819-118">ADO.NET Overview</span></span>](../ado-net-overview.md)
