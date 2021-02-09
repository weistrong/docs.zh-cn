---
description: 详细了解：在 .NET Framework 文件 I/O 和文件系统中使用的类 (Visual Basic)
title: 在 .NET Framework 文件 I/O 和文件系统中使用的类
ms.date: 07/20/2015
helpviewer_keywords:
- file I/O classes
ms.assetid: 4a5ca924-eea8-4a95-a5f0-6ac10de276a3
ms.openlocfilehash: a8cbe476044df92fcdbdd0421b91f3c7c098e063
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99666324"
---
# <a name="classes-used-in-net-framework-file-io-and-the-file-system-visual-basic"></a><span data-ttu-id="06268-103">在 .NET Framework 文件 I/O 和文件系统中使用的类 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="06268-103">Classes Used in .NET Framework File I/O and the File System (Visual Basic)</span></span>

<span data-ttu-id="06268-104">下列各表列出了常用于 .NET Framework 文件 I/O 的类，将这些类分为文件 I/O 类、用于创建流的类和用于读取和写入流的类。</span><span class="sxs-lookup"><span data-stu-id="06268-104">The following tables list the classes commonly used for .NET Framework file I/O, categorized into file I/O classes, classes used for creating streams, and classes used to read and write to streams.</span></span>  
  
<span data-ttu-id="06268-105">要获取更完整的列表，请参阅[类库概述](../../../../standard/class-library-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="06268-105">For a more comprehensive listing, see [Class Library Overview](../../../../standard/class-library-overview.md).</span></span>  
  
## <a name="basic-io-classes-for-files-drives-and-directories"></a><span data-ttu-id="06268-106">用于文件、驱动器和目录的基本 I/O 类</span><span class="sxs-lookup"><span data-stu-id="06268-106">Basic I/O Classes for Files, Drives, and Directories</span></span>  

 <span data-ttu-id="06268-107">下表列出并说明了用于文件 I/O 的主类。</span><span class="sxs-lookup"><span data-stu-id="06268-107">The following table lists and describes the main classes used for file I/O.</span></span>  
  
|<span data-ttu-id="06268-108">类</span><span class="sxs-lookup"><span data-stu-id="06268-108">Class</span></span>|<span data-ttu-id="06268-109">说明</span><span class="sxs-lookup"><span data-stu-id="06268-109">Description</span></span>|  
|-----------|-----------------|  
|<xref:System.IO.Directory?displayProperty=nameWithType>|<span data-ttu-id="06268-110">提供用于创建、移动和枚举目录和子目录的静态方法。</span><span class="sxs-lookup"><span data-stu-id="06268-110">Provides static methods for creating, moving, and enumerating through directories and subdirectories.</span></span>|  
|<xref:System.IO.DirectoryInfo?displayProperty=nameWithType>|<span data-ttu-id="06268-111">提供用于创建、移动和枚举目录和子目录的实例方法。</span><span class="sxs-lookup"><span data-stu-id="06268-111">Provides instance methods for creating, moving, and enumerating through directories and subdirectories.</span></span>|  
|<xref:System.IO.DriveInfo?displayProperty=nameWithType>|<span data-ttu-id="06268-112">提供通过驱动器用于创建、移动和枚举的实例方法。</span><span class="sxs-lookup"><span data-stu-id="06268-112">Provides instance methods for creating, moving, and enumerating through drives.</span></span>|  
|<xref:System.IO.File?displayProperty=nameWithType>|<span data-ttu-id="06268-113">提供用于创建、复制、删除、移动和打开文件的静态方法，并可帮助创建 `FileStream`。</span><span class="sxs-lookup"><span data-stu-id="06268-113">Provides static methods for creating, copying, deleting, moving, and opening files, and aids in the creation of a `FileStream`.</span></span>|  
|<xref:System.IO.FileAccess?displayProperty=nameWithType>|<span data-ttu-id="06268-114">定义文件的读取、写入或读/写访问权限的常量。</span><span class="sxs-lookup"><span data-stu-id="06268-114">Defines constants for read, write, or read/write access to a file.</span></span>|  
|<xref:System.IO.FileAttributes?displayProperty=nameWithType>|<span data-ttu-id="06268-115">提供文件和目录的属性，例如 `Archive`、`Hidden` 和 `ReadOnly`。</span><span class="sxs-lookup"><span data-stu-id="06268-115">Provides attributes for files and directories such as `Archive`, `Hidden`, and `ReadOnly`.</span></span>|  
|<xref:System.IO.FileInfo?displayProperty=nameWithType>|<span data-ttu-id="06268-116">提供用于创建、复制、删除、移动和打开文件的静态方法，并可帮助创建 `FileStream`。</span><span class="sxs-lookup"><span data-stu-id="06268-116">Provides static methods for creating, copying, deleting, moving, and opening files, and aids in the creation of a `FileStream`.</span></span>|  
|<xref:System.IO.FileMode?displayProperty=nameWithType>|<span data-ttu-id="06268-117">控制打开文件的方式。</span><span class="sxs-lookup"><span data-stu-id="06268-117">Controls how a file is opened.</span></span> <span data-ttu-id="06268-118">在多个 `FileStream` 和 `IsolatedStorageFileStream` 的构造函数中指定此参数，此参数用于 <xref:System.IO.File> 和 <xref:System.IO.FileInfo> 的 `Open` 方法。</span><span class="sxs-lookup"><span data-stu-id="06268-118">This parameter is specified in many of the constructors for `FileStream` and `IsolatedStorageFileStream`, and for the `Open` methods of <xref:System.IO.File> and <xref:System.IO.FileInfo>.</span></span>|  
|<xref:System.IO.FileShare?displayProperty=nameWithType>|<span data-ttu-id="06268-119">定义用于控制其他文件流可以对同一文件进行何种类型的访问的常量。</span><span class="sxs-lookup"><span data-stu-id="06268-119">Defines constants for controlling the type of access other file streams can have to the same file.</span></span>|  
|<xref:System.IO.Path?displayProperty=nameWithType>|<span data-ttu-id="06268-120">提供用于处理目录字符串的方法和属性。</span><span class="sxs-lookup"><span data-stu-id="06268-120">Provides methods and properties for processing directory strings.</span></span>|  
|<xref:System.Security.Permissions.FileIOPermission?displayProperty=nameWithType>|<span data-ttu-id="06268-121">通过定义 <xref:System.Security.Permissions.FileIOPermissionAttribute.Read%2A>、<xref:System.Security.Permissions.FileIOPermissionAttribute.Write%2A>、<xref:System.Security.Permissions.FileIOPermissionAttribute.Append%2A> 和 <xref:System.Security.Permissions.FileIOPermissionAttribute.PathDiscovery%2A> 权限来控制对文件和文件夹的访问。</span><span class="sxs-lookup"><span data-stu-id="06268-121">Controls the access of files and folders by defining <xref:System.Security.Permissions.FileIOPermissionAttribute.Read%2A>, <xref:System.Security.Permissions.FileIOPermissionAttribute.Write%2A>, <xref:System.Security.Permissions.FileIOPermissionAttribute.Append%2A> and <xref:System.Security.Permissions.FileIOPermissionAttribute.PathDiscovery%2A> permissions.</span></span>|  
  
## <a name="classes-used-to-create-streams"></a><span data-ttu-id="06268-122">用于创建流的类</span><span class="sxs-lookup"><span data-stu-id="06268-122">Classes Used to Create Streams</span></span>  

 <span data-ttu-id="06268-123">下表列出并说明了用于创建流的主类。</span><span class="sxs-lookup"><span data-stu-id="06268-123">The following table lists and describes the main classes used to create streams.</span></span>  
  
|<span data-ttu-id="06268-124">类</span><span class="sxs-lookup"><span data-stu-id="06268-124">Class</span></span>|<span data-ttu-id="06268-125">说明</span><span class="sxs-lookup"><span data-stu-id="06268-125">Description</span></span>|  
|-----------|-----------------|  
|<xref:System.IO.BufferedStream?displayProperty=nameWithType>|<span data-ttu-id="06268-126">将缓冲层添加到另一个流上的读取和写入操作。</span><span class="sxs-lookup"><span data-stu-id="06268-126">Adds a buffering layer to read and write operations on another stream.</span></span>|  
|<xref:System.IO.FileStream?displayProperty=nameWithType>|<span data-ttu-id="06268-127">支持通过文件的 <xref:System.IO.FileStream.Seek%2A> 方法对其进行随机访问。</span><span class="sxs-lookup"><span data-stu-id="06268-127">Supports random access to files through its <xref:System.IO.FileStream.Seek%2A> method.</span></span> <span data-ttu-id="06268-128">默认情况下 <xref:System.IO.FileStream> 同步打开文件，但也支持异步操作。</span><span class="sxs-lookup"><span data-stu-id="06268-128"><xref:System.IO.FileStream> opens files synchronously by default but also supports asynchronous operation.</span></span>|  
|<xref:System.IO.MemoryStream?displayProperty=nameWithType>|<span data-ttu-id="06268-129">创建一个流，其后备存储为内存而非文件。</span><span class="sxs-lookup"><span data-stu-id="06268-129">Creates a stream whose backing store is memory, rather than a file.</span></span>|  
|<xref:System.Net.Sockets.NetworkStream?displayProperty=nameWithType>|<span data-ttu-id="06268-130">为网络访问提供数据的基础流。</span><span class="sxs-lookup"><span data-stu-id="06268-130">Provides the underlying stream of data for network access.</span></span>|  
|<xref:System.Security.Cryptography.CryptoStream?displayProperty=nameWithType>|<span data-ttu-id="06268-131">定义将数据流链接到加密转换的流。</span><span class="sxs-lookup"><span data-stu-id="06268-131">Defines a stream that links data streams to cryptographic transformations.</span></span>|  
  
## <a name="classes-used-to-read-from-and-write-to-streams"></a><span data-ttu-id="06268-132">用于读取和写入到流的类</span><span class="sxs-lookup"><span data-stu-id="06268-132">Classes Used to Read from and Write to Streams</span></span>  

 <span data-ttu-id="06268-133">下表显示使用流读取和写入到文件的特定类。</span><span class="sxs-lookup"><span data-stu-id="06268-133">The following table shows the specific classes used for reading from and writing to files with streams.</span></span>  
  
|<span data-ttu-id="06268-134">**类**</span><span class="sxs-lookup"><span data-stu-id="06268-134">**Class**</span></span>|<span data-ttu-id="06268-135">**说明**</span><span class="sxs-lookup"><span data-stu-id="06268-135">**Description**</span></span>|  
|---------------|---------------------|  
|<xref:System.IO.BinaryReader?displayProperty=nameWithType>|<span data-ttu-id="06268-136">从 <xref:System.IO.FileStream> 读取编码字符串和基元数据类型。</span><span class="sxs-lookup"><span data-stu-id="06268-136">Reads encoded strings and primitive data types from a <xref:System.IO.FileStream>.</span></span>|  
|<xref:System.IO.BinaryWriter?displayProperty=nameWithType>|<span data-ttu-id="06268-137">将编码字符串和基元数据类型写入 <xref:System.IO.FileStream>。</span><span class="sxs-lookup"><span data-stu-id="06268-137">Writes encoded strings and primitive data types to a <xref:System.IO.FileStream>.</span></span>|  
|<xref:System.IO.StreamReader?displayProperty=nameWithType>|<span data-ttu-id="06268-138">从 <xref:System.IO.FileStream> 读取字符，使用 <xref:System.IO.StreamReader.CurrentEncoding%2A> 将字符转换为字节，或将字节转换为字符。</span><span class="sxs-lookup"><span data-stu-id="06268-138">Reads characters from a <xref:System.IO.FileStream>, using <xref:System.IO.StreamReader.CurrentEncoding%2A> to convert characters to and from bytes.</span></span> <span data-ttu-id="06268-139">对于给定的流，<xref:System.IO.StreamReader> 的构造函数基于特定 <xref:System.IO.StreamReader.CurrentEncoding%2A> 报头的状态，尝试确定正确的 <xref:System.IO.StreamReader.CurrentEncoding%2A>，如字节顺序标记。</span><span class="sxs-lookup"><span data-stu-id="06268-139"><xref:System.IO.StreamReader> has a constructor that attempts to ascertain the correct <xref:System.IO.StreamReader.CurrentEncoding%2A> for a given stream, based on the presence of a <xref:System.IO.StreamReader.CurrentEncoding%2A>-specific preamble, such as a byte order mark.</span></span>|  
|<xref:System.IO.StreamWriter?displayProperty=nameWithType>|<span data-ttu-id="06268-140">将字符写入 `FileStream`，使用 <xref:System.IO.StreamWriter.Encoding%2A> 将字符转换为字节。</span><span class="sxs-lookup"><span data-stu-id="06268-140">Writes characters to a `FileStream`, using <xref:System.IO.StreamWriter.Encoding%2A> to convert characters to bytes.</span></span>|  
|<xref:System.IO.StringReader?displayProperty=nameWithType>|<span data-ttu-id="06268-141">从 `String` 读取字符。</span><span class="sxs-lookup"><span data-stu-id="06268-141">Reads characters from a `String`.</span></span> <span data-ttu-id="06268-142">输出可以是任意编码中的流或 `String`。</span><span class="sxs-lookup"><span data-stu-id="06268-142">Output can be either a stream in any encoding or a `String`.</span></span>|  
|<xref:System.IO.StringWriter?displayProperty=nameWithType>|<span data-ttu-id="06268-143">将字符写入 `String`。</span><span class="sxs-lookup"><span data-stu-id="06268-143">Writes characters to a `String`.</span></span> <span data-ttu-id="06268-144">输出可以是任意编码中的流或 `String`。</span><span class="sxs-lookup"><span data-stu-id="06268-144">Output can be either a stream in any encoding or a `String`.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="06268-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="06268-145">See also</span></span>

- [<span data-ttu-id="06268-146">撰写流</span><span class="sxs-lookup"><span data-stu-id="06268-146">Composing Streams</span></span>](../../../../standard/io/composing-streams.md)
- [<span data-ttu-id="06268-147">文件和流 I/O</span><span class="sxs-lookup"><span data-stu-id="06268-147">File and Stream I/O</span></span>](../../../../standard/io/index.md)
- [<span data-ttu-id="06268-148">异步文件 I/O</span><span class="sxs-lookup"><span data-stu-id="06268-148">Asynchronous File I/O</span></span>](../../../../standard/io/asynchronous-file-i-o.md)
- [<span data-ttu-id="06268-149">.NET Framework 文件 I/O 和文件系统基础知识 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="06268-149">Basics of .NET Framework File I/O and the File System (Visual Basic)</span></span>](basics-of-net-framework-file-io-and-the-file-system.md)
