---
description: 详细了解：操作说明：在 Visual Basic 中向文本文件追加内容
title: 如何：向文本文件追加内容
ms.date: 07/20/2015
helpviewer_keywords:
- I/O [Visual Basic], appending to files
- I/O [Visual Basic], My.Computer.FileSystem.WriteAllText method
- I/O [Visual Basic], WriteAllText method
ms.assetid: bbbd7fb5-f169-41a9-b53f-520ea9613913
ms.openlocfilehash: f66e1cb4ba299ee89f0d84d17d01af67650c9340
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797661"
---
# <a name="how-to-append-to-text-files-in-visual-basic"></a><span data-ttu-id="7f2e8-103">如何：在 Visual Basic 中向文本文件追加内容</span><span class="sxs-lookup"><span data-stu-id="7f2e8-103">How to: Append to Text Files in Visual Basic</span></span>

<span data-ttu-id="7f2e8-104">通过指定将 `append` 参数设置为 `True`，可使用 <xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllText%2A> 方法向文本文件追加内容。</span><span class="sxs-lookup"><span data-stu-id="7f2e8-104">The <xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllText%2A> method can be used to append to a text file by specifying that the `append` parameter is set to `True`.</span></span>  
  
### <a name="to-append-to-a-text-file"></a><span data-ttu-id="7f2e8-105">向文本文件追加内容</span><span class="sxs-lookup"><span data-stu-id="7f2e8-105">To append to a text file</span></span>  
  
- <span data-ttu-id="7f2e8-106">使用 `WriteAllText` 方法，指定目标文件以及要追加的字符串，并将 `append` 参数设置为 `True`。</span><span class="sxs-lookup"><span data-stu-id="7f2e8-106">Use the `WriteAllText` method, specifying the target file and string to be appended and setting the `append` parameter to `True`.</span></span>  
  
     <span data-ttu-id="7f2e8-107">此示例将字符串 `"This is a test string."` 写入名为 `Testfile.txt` 的文件中。</span><span class="sxs-lookup"><span data-stu-id="7f2e8-107">This example writes the string `"This is a test string."` to the file named `Testfile.txt`.</span></span>  
  
     [!code-vb[VbFileIOWrite#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbFileIOWrite/VB/Class1.vb#6)]  
  
## <a name="robust-programming"></a><span data-ttu-id="7f2e8-108">可靠编程</span><span class="sxs-lookup"><span data-stu-id="7f2e8-108">Robust Programming</span></span>  

 <span data-ttu-id="7f2e8-109">以下情况可能会导致异常：</span><span class="sxs-lookup"><span data-stu-id="7f2e8-109">The following conditions may cause an exception:</span></span>  
  
- <span data-ttu-id="7f2e8-110">路径由于以下原因之一而无效：是零长度字符串；仅为空白；包含无效字符；是一个设备路径（开头字符为 \\\\.\\）(<xref:System.ArgumentException>)。</span><span class="sxs-lookup"><span data-stu-id="7f2e8-110">The path is not valid for one of the following reasons: it is a zero-length string, it contains only white space, it contains invalid characters, or it is a device path (starts with \\\\.\\) (<xref:System.ArgumentException>).</span></span>  
  
- <span data-ttu-id="7f2e8-111">路径无效，因为它是 `Nothing` (<xref:System.ArgumentNullException>)。</span><span class="sxs-lookup"><span data-stu-id="7f2e8-111">The path is not valid because it is `Nothing` (<xref:System.ArgumentNullException>).</span></span>  
  
- <span data-ttu-id="7f2e8-112">`File` 指向不存在的路径（<xref:System.IO.FileNotFoundException> 或 <xref:System.IO.DirectoryNotFoundException>）。</span><span class="sxs-lookup"><span data-stu-id="7f2e8-112">`File` points to a path that does not exist (<xref:System.IO.FileNotFoundException> or <xref:System.IO.DirectoryNotFoundException>).</span></span>  
  
- <span data-ttu-id="7f2e8-113">文件正由另一个进程使用，或者出现 I/O 错误 (<xref:System.IO.IOException>)。</span><span class="sxs-lookup"><span data-stu-id="7f2e8-113">The file is in use by another process, or an I/O error occurs (<xref:System.IO.IOException>).</span></span>  
  
- <span data-ttu-id="7f2e8-114">路径超过了系统定义的最大长度 (<xref:System.IO.PathTooLongException>)。</span><span class="sxs-lookup"><span data-stu-id="7f2e8-114">The path exceeds the system-defined maximum length (<xref:System.IO.PathTooLongException>).</span></span>  
  
- <span data-ttu-id="7f2e8-115">路径中的文件名或目录名包含冒号 (:)，或格式无效 (<xref:System.NotSupportedException>)。</span><span class="sxs-lookup"><span data-stu-id="7f2e8-115">A file or directory name in the path contains a colon (:) or is in an invalid format (<xref:System.NotSupportedException>).</span></span>  
  
- <span data-ttu-id="7f2e8-116">该用户缺少查看该路径所必需的权限 (<xref:System.Security.SecurityException>)。</span><span class="sxs-lookup"><span data-stu-id="7f2e8-116">The user lacks necessary permissions to view the path (<xref:System.Security.SecurityException>).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7f2e8-117">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7f2e8-117">See also</span></span>

- <xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllText%2A>
- <xref:Microsoft.VisualBasic.FileIO.FileSystem>
- [<span data-ttu-id="7f2e8-118">写入文件</span><span class="sxs-lookup"><span data-stu-id="7f2e8-118">Writing to Files</span></span>](writing-to-files.md)
