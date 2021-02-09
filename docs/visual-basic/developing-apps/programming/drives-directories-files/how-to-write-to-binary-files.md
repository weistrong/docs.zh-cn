---
description: 详细了解：操作说明：在 Visual Basic 中写入二进制文件
title: 如何：写入二进制文件
ms.date: 07/20/2015
helpviewer_keywords:
- files [Visual Basic], binary access
- WriteAllBytes method [Visual Basic]
- binary files [Visual Basic], writing in Visual Basic
ms.assetid: 59fae125-de5b-4c96-883c-209f4a55112c
ms.openlocfilehash: a1fe18c9143c26fd40e6a1d9cde36581c2c0be12
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797323"
---
# <a name="how-to-write-to-binary-files-in-visual-basic"></a><span data-ttu-id="9fb04-103">如何：在 Visual Basic 中写入二进制文件</span><span class="sxs-lookup"><span data-stu-id="9fb04-103">How to: Write to Binary Files in Visual Basic</span></span>

<span data-ttu-id="9fb04-104"><xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllBytes%2A> 方法向二进制文件写入数据。</span><span class="sxs-lookup"><span data-stu-id="9fb04-104">The <xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllBytes%2A> method writes data to a binary file.</span></span> <span data-ttu-id="9fb04-105">如果 `append` 参数为 `True`，会将数据追加到文件中；否则将覆盖文件中的数据。</span><span class="sxs-lookup"><span data-stu-id="9fb04-105">If the `append` parameter is `True`, it will append the data to the file; otherwise data in the file is overwritten.</span></span>

<span data-ttu-id="9fb04-106">如果指定的路径（不包括文件名）无效，则将引发 <xref:System.IO.DirectoryNotFoundException> 异常。</span><span class="sxs-lookup"><span data-stu-id="9fb04-106">If the specified path excluding the file name is not valid, a <xref:System.IO.DirectoryNotFoundException> exception will be thrown.</span></span> <span data-ttu-id="9fb04-107">如果该路径有效，但文件不存在，则将创建文件。</span><span class="sxs-lookup"><span data-stu-id="9fb04-107">If the path is valid but the file does not exist, the file will be created.</span></span>

## <a name="to-write-to-a-binary-file"></a><span data-ttu-id="9fb04-108">写入二进制文件</span><span class="sxs-lookup"><span data-stu-id="9fb04-108">To write to a binary file</span></span>

<span data-ttu-id="9fb04-109">使用 `WriteAllBytes` 方法，并提供文件路径和名称以及要写入的字节数。</span><span class="sxs-lookup"><span data-stu-id="9fb04-109">Use the `WriteAllBytes` method, supplying the file path and name and the bytes to be written.</span></span> <span data-ttu-id="9fb04-110">本示例将数据组 `CustomerData` 追加到名为 `CollectedData.dat` 的文件中。</span><span class="sxs-lookup"><span data-stu-id="9fb04-110">This example appends the data array `CustomerData` to the file named `CollectedData.dat`.</span></span>

[!code-vb[VbVbcnMyFileSystem#27](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/Class1.vb#27)]

## <a name="robust-programming"></a><span data-ttu-id="9fb04-111">可靠编程</span><span class="sxs-lookup"><span data-stu-id="9fb04-111">Robust Programming</span></span>

<span data-ttu-id="9fb04-112">以下情况可能会导致异常：</span><span class="sxs-lookup"><span data-stu-id="9fb04-112">The following conditions may create an exception:</span></span>

- <span data-ttu-id="9fb04-113">路径由于以下原因之一而无效：是零长度字符串；仅包含空白；包含无效字符。</span><span class="sxs-lookup"><span data-stu-id="9fb04-113">The path is not valid for one of the following reasons: it is a zero-length string; it contains only white space; or it contains invalid characters.</span></span> <span data-ttu-id="9fb04-114">(<xref:System.ArgumentException>).</span><span class="sxs-lookup"><span data-stu-id="9fb04-114">(<xref:System.ArgumentException>).</span></span>

- <span data-ttu-id="9fb04-115">路径无效，因为它是 `Nothing` (<xref:System.ArgumentNullException>)。</span><span class="sxs-lookup"><span data-stu-id="9fb04-115">The path is not valid because it is `Nothing` (<xref:System.ArgumentNullException>).</span></span>

- <span data-ttu-id="9fb04-116">`File` 指向不存在的路径（<xref:System.IO.FileNotFoundException> 或 <xref:System.IO.DirectoryNotFoundException>）。</span><span class="sxs-lookup"><span data-stu-id="9fb04-116">`File` points to a path that does not exist (<xref:System.IO.FileNotFoundException> or <xref:System.IO.DirectoryNotFoundException>).</span></span>

- <span data-ttu-id="9fb04-117">文件正由另一个进程使用，或者出现 I/O 错误 (<xref:System.IO.IOException>)。</span><span class="sxs-lookup"><span data-stu-id="9fb04-117">The file is in use by another process, or an I/O error occurs (<xref:System.IO.IOException>).</span></span>

- <span data-ttu-id="9fb04-118">路径超过了系统定义的最大长度 (<xref:System.IO.PathTooLongException>)。</span><span class="sxs-lookup"><span data-stu-id="9fb04-118">The path exceeds the system-defined maximum length (<xref:System.IO.PathTooLongException>).</span></span>

- <span data-ttu-id="9fb04-119">路径中的文件名或目录名包含冒号 (:)，或格式无效 (<xref:System.NotSupportedException>)。</span><span class="sxs-lookup"><span data-stu-id="9fb04-119">A file or directory name in the path contains a colon (:) or is in an invalid format (<xref:System.NotSupportedException>).</span></span>

- <span data-ttu-id="9fb04-120">该用户缺少查看该路径所必需的权限 (<xref:System.Security.SecurityException>)。</span><span class="sxs-lookup"><span data-stu-id="9fb04-120">The user lacks necessary permissions to view the path (<xref:System.Security.SecurityException>).</span></span>

## <a name="see-also"></a><span data-ttu-id="9fb04-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9fb04-121">See also</span></span>

- <xref:Microsoft.VisualBasic.FileIO.FileSystem.WriteAllBytes%2A>
- [<span data-ttu-id="9fb04-122">如何：向文件写入文本</span><span class="sxs-lookup"><span data-stu-id="9fb04-122">How to: Write Text to Files</span></span>](how-to-write-text-to-files.md)
