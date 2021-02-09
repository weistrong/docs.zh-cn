---
description: 详细了解：操作说明：在 Visual Basic 中查找具有特定模式的文件
title: 如何：查找具有特定模式的文件
ms.date: 07/20/2015
helpviewer_keywords:
- files [Visual Basic], finding
- pattern matching
- patterns, matching
ms.assetid: 25e3b71d-b844-4293-9e4e-f06c5836b5cc
ms.openlocfilehash: 42266ad354e1ac8e3920663447e4d39fe7ad1b8f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797557"
---
# <a name="how-to-find-files-with-a-specific-pattern-in-visual-basic"></a><span data-ttu-id="dd82a-103">如何：在 Visual Basic 中查找具有特定模式的文件</span><span class="sxs-lookup"><span data-stu-id="dd82a-103">How to: Find Files with a Specific Pattern in Visual Basic</span></span>

<span data-ttu-id="dd82a-104"><xref:Microsoft.VisualBasic.MyServices.FileSystemProxy.GetFiles%2A> 方法返回表示文件的路径名的只读字符串集合。</span><span class="sxs-lookup"><span data-stu-id="dd82a-104">The <xref:Microsoft.VisualBasic.MyServices.FileSystemProxy.GetFiles%2A> method returns a read-only collection of strings representing the path names for the files.</span></span> <span data-ttu-id="dd82a-105">可以使用 `wildCards` 参数来指定特定模式。</span><span class="sxs-lookup"><span data-stu-id="dd82a-105">You can use the `wildCards` parameter to specify a specific pattern.</span></span> <span data-ttu-id="dd82a-106">若要在搜索中包括子目录，请将 `searchType` 参数设置为 `SearchOption.SearchAllSubDirectories`。</span><span class="sxs-lookup"><span data-stu-id="dd82a-106">If you would like to include subdirectories in the search, set the `searchType` parameter to `SearchOption.SearchAllSubDirectories`.</span></span>  
  
 <span data-ttu-id="dd82a-107">如果没有找到与指定模式匹配的文件，则返回一个空集合。</span><span class="sxs-lookup"><span data-stu-id="dd82a-107">An empty collection is returned if no files matching the specified pattern are found.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="dd82a-108">有关使用 `System.IO` 命名空间的 `DirectoryInfo` 类返回文件列表的信息，请参阅 <xref:System.IO.DirectoryInfo.GetFiles%2A>。</span><span class="sxs-lookup"><span data-stu-id="dd82a-108">For information about returning a file list by using the `DirectoryInfo` class of the `System.IO` namespace, see <xref:System.IO.DirectoryInfo.GetFiles%2A>.</span></span>  
  
### <a name="to-find-files-with-a-specified-pattern"></a><span data-ttu-id="dd82a-109">查找具有指定模式的文件</span><span class="sxs-lookup"><span data-stu-id="dd82a-109">To find files with a specified pattern</span></span>  
  
- <span data-ttu-id="dd82a-110">使用 `GetFiles` 方法，同时提供要搜索的目录的名称和路径并指定模式。</span><span class="sxs-lookup"><span data-stu-id="dd82a-110">Use the `GetFiles` method, supplying the name and path of the directory you want to search and specifying the pattern.</span></span> <span data-ttu-id="dd82a-111">以下示例返回目录中扩展名为 `.dll` 的所有文件，并将其添加到 `ListBox1`。</span><span class="sxs-lookup"><span data-stu-id="dd82a-111">The following example returns all files with the extension `.dll` in the directory and adds them to `ListBox1`.</span></span>  
  
     [!code-vb[VbFileIOMisc#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbFileIOMisc/VB/Class1.vb#4)]  
  
## <a name="net-framework-security"></a><span data-ttu-id="dd82a-112">.NET Framework 安全性</span><span class="sxs-lookup"><span data-stu-id="dd82a-112">.NET Framework Security</span></span>  

 <span data-ttu-id="dd82a-113">以下情况可能会导致异常：</span><span class="sxs-lookup"><span data-stu-id="dd82a-113">The following conditions may cause an exception:</span></span>  
  
- <span data-ttu-id="dd82a-114">路径由于以下原因之一而无效：是零长度字符串；仅为空白；包含无效字符；是一个设备路径（开头字符为 \\\\.\\）(<xref:System.ArgumentException>)。</span><span class="sxs-lookup"><span data-stu-id="dd82a-114">The path is not valid for one of the following reasons: it is a zero-length string, it contains only white space, it contains invalid characters, or it is a device path (starts with \\\\.\\) (<xref:System.ArgumentException>).</span></span>  
  
- <span data-ttu-id="dd82a-115">路径无效，因为它是 `Nothing` (<xref:System.ArgumentNullException>)。</span><span class="sxs-lookup"><span data-stu-id="dd82a-115">The path is not valid because it is `Nothing` (<xref:System.ArgumentNullException>).</span></span>  
  
- <span data-ttu-id="dd82a-116">`directory` 不存在 (<xref:System.IO.DirectoryNotFoundException>)。</span><span class="sxs-lookup"><span data-stu-id="dd82a-116">`directory` does not exist (<xref:System.IO.DirectoryNotFoundException>).</span></span>  
  
- <span data-ttu-id="dd82a-117">`directory` 指向某个现有文件 (<xref:System.IO.IOException>)。</span><span class="sxs-lookup"><span data-stu-id="dd82a-117">`directory` points to an existing file (<xref:System.IO.IOException>).</span></span>  
  
- <span data-ttu-id="dd82a-118">路径超过了系统定义的最大长度 (<xref:System.IO.PathTooLongException>)。</span><span class="sxs-lookup"><span data-stu-id="dd82a-118">The path exceeds the system-defined maximum length (<xref:System.IO.PathTooLongException>).</span></span>  
  
- <span data-ttu-id="dd82a-119">路径中的文件名或文件夹名包含冒号 (:)，或其格式无效 (<xref:System.NotSupportedException>)。</span><span class="sxs-lookup"><span data-stu-id="dd82a-119">A file or folder name in the path contains a colon (:) or is in an invalid format (<xref:System.NotSupportedException>).</span></span>  
  
- <span data-ttu-id="dd82a-120">该用户缺少查看该路径所必需的权限 (<xref:System.Security.SecurityException>)。</span><span class="sxs-lookup"><span data-stu-id="dd82a-120">The user lacks necessary permissions to view the path (<xref:System.Security.SecurityException>).</span></span>  
  
- <span data-ttu-id="dd82a-121">该用户缺少必要的权限 (<xref:System.UnauthorizedAccessException>)。</span><span class="sxs-lookup"><span data-stu-id="dd82a-121">The user lacks necessary permissions (<xref:System.UnauthorizedAccessException>).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dd82a-122">另请参阅</span><span class="sxs-lookup"><span data-stu-id="dd82a-122">See also</span></span>

- <xref:Microsoft.VisualBasic.MyServices.FileSystemProxy.GetFiles%2A>
- [<span data-ttu-id="dd82a-123">如何：查找具有特定模式的子目录</span><span class="sxs-lookup"><span data-stu-id="dd82a-123">How to: Find Subdirectories with a Specific Pattern</span></span>](how-to-find-subdirectories-with-a-specific-pattern.md)
- [<span data-ttu-id="dd82a-124">疑难解答：读取和写入文本文件</span><span class="sxs-lookup"><span data-stu-id="dd82a-124">Troubleshooting: Reading from and Writing to Text Files</span></span>](troubleshooting-reading-from-and-writing-to-text-files.md)
- [<span data-ttu-id="dd82a-125">如何：获取目录中的文件集合</span><span class="sxs-lookup"><span data-stu-id="dd82a-125">How to: Get the Collection of Files in a Directory</span></span>](how-to-get-the-collection-of-files-in-a-directory.md)
