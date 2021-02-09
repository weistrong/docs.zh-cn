---
description: 详细了解：操作说明：在同一目录中创建文件副本 (Visual Basic)
title: 如何：在同一目录中创建文件副本
ms.date: 07/20/2015
f1_keywords:
- File.Copy
helpviewer_keywords:
- My.Computer.FileSystem.CopyFile method, copying files [Visual Basic]
- files [Visual Basic], copying
- CopyFile method [Visual Basic], copying files in Visual Basic
- I/O [Visual Basic], copying files
ms.assetid: b2fdda86-e666-42c2-9706-9527e9fa68ff
ms.openlocfilehash: 27fecc22a9317dd45e663aa37884c6c1f1e36349
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797609"
---
# <a name="how-to-create-a-copy-of-a-file-in-the-same-directory-in-visual-basic"></a><span data-ttu-id="8db1f-103">如何：在同一目录中创建文件副本 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8db1f-103">How to: Create a Copy of a File in the Same Directory in Visual Basic</span></span>

<span data-ttu-id="8db1f-104">使用 `My.Computer.FileSystem.CopyFile` 方法复制文件。</span><span class="sxs-lookup"><span data-stu-id="8db1f-104">Use the `My.Computer.FileSystem.CopyFile` method to copy files.</span></span> <span data-ttu-id="8db1f-105">使用参数可以覆盖现有文件、重命名文件、显示操作的进度以及允许用户取消操作。</span><span class="sxs-lookup"><span data-stu-id="8db1f-105">The parameters allow you to overwrite existing files, rename the file, show the progress of the operation, and allow the user to cancel the operation.</span></span>  
  
### <a name="to-create-a-copy-of-a-file-in-the-same-folder"></a><span data-ttu-id="8db1f-106">在同一文件夹中创建文件副本</span><span class="sxs-lookup"><span data-stu-id="8db1f-106">To create a copy of a file in the same folder</span></span>  
  
- <span data-ttu-id="8db1f-107">使用 `CopyFile` 方法，提供目标文件和位置。</span><span class="sxs-lookup"><span data-stu-id="8db1f-107">Use the `CopyFile` method, supplying the target file and the location.</span></span> <span data-ttu-id="8db1f-108">下面的示例创建名为 `test2.txt` 的 `test.txt` 副本。</span><span class="sxs-lookup"><span data-stu-id="8db1f-108">The following example creates a copy of `test.txt` called `test2.txt`.</span></span>  
  
     [!code-vb[VbVbcnMyFileSystem#51](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/Class1.vb#51)]  
  
### <a name="to-create-a-copy-of-a-file-in-the-same-folder-overwriting-existing-files"></a><span data-ttu-id="8db1f-109">通过覆盖现有文件在同一文件夹中创建文件副本</span><span class="sxs-lookup"><span data-stu-id="8db1f-109">To create a copy of a file in the same folder, overwriting existing files</span></span>  
  
- <span data-ttu-id="8db1f-110">使用 `CopyFile` 方法，提供目标文件和位置，并将 `overwrite` 设置为 `True`。</span><span class="sxs-lookup"><span data-stu-id="8db1f-110">Use the `CopyFile` method, supplying the target file and location, and setting `overwrite` to `True`.</span></span> <span data-ttu-id="8db1f-111">下面的示例创建名为 `test2.txt` 的 `test.txt` 副本，并用该名称覆盖任何现有文件。</span><span class="sxs-lookup"><span data-stu-id="8db1f-111">The following example creates a copy of `test.txt` called `test2.txt` and overwrites any existing files by that name.</span></span>  
  
     [!code-vb[VbVbcnMyFileSystem#52](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/Class1.vb#52)]  
  
## <a name="robust-programming"></a><span data-ttu-id="8db1f-112">可靠编程</span><span class="sxs-lookup"><span data-stu-id="8db1f-112">Robust Programming</span></span>  

 <span data-ttu-id="8db1f-113">以下情况可能会导致异常：</span><span class="sxs-lookup"><span data-stu-id="8db1f-113">The following conditions may cause an exception to be thrown:</span></span>  
  
- <span data-ttu-id="8db1f-114">路径由于以下原因之一而无效：是零长度字符串；仅为空白；包含无效字符；是一个设备路径（开头字符为 \\\\.\\）(<xref:System.ArgumentException>)。</span><span class="sxs-lookup"><span data-stu-id="8db1f-114">The path is not valid for one of the following reasons: it is a zero-length string, it contains only white space, it contains invalid characters, or it is a device path (starts with \\\\.\\) (<xref:System.ArgumentException>).</span></span>  
  
- <span data-ttu-id="8db1f-115">系统无法检索绝对路径 (<xref:System.ArgumentException>)。</span><span class="sxs-lookup"><span data-stu-id="8db1f-115">The system could not retrieve the absolute path (<xref:System.ArgumentException>).</span></span>  
  
- <span data-ttu-id="8db1f-116">路径无效，因为它是 `Nothing` (<xref:System.ArgumentNullException>)。</span><span class="sxs-lookup"><span data-stu-id="8db1f-116">The path is not valid because it is `Nothing` (<xref:System.ArgumentNullException>).</span></span>  
  
- <span data-ttu-id="8db1f-117">源文件无效或不存在 (<xref:System.IO.FileNotFoundException>)。</span><span class="sxs-lookup"><span data-stu-id="8db1f-117">The source file is not valid or does not exist (<xref:System.IO.FileNotFoundException>).</span></span>  
  
- <span data-ttu-id="8db1f-118">合并路径指向现有目录 (<xref:System.IO.IOException>)。</span><span class="sxs-lookup"><span data-stu-id="8db1f-118">The combined path points to an existing directory (<xref:System.IO.IOException>).</span></span>  
  
- <span data-ttu-id="8db1f-119">存在目标文件，并且 `overwrite` 设置为 `False` (<xref:System.IO.IOException>)。</span><span class="sxs-lookup"><span data-stu-id="8db1f-119">The destination file exists and `overwrite` is set to `False` (<xref:System.IO.IOException>).</span></span>  
  
- <span data-ttu-id="8db1f-120">用户没有足够的权限访问文件 (<xref:System.IO.IOException>)。</span><span class="sxs-lookup"><span data-stu-id="8db1f-120">The user does not have sufficient permissions to access the file (<xref:System.IO.IOException>).</span></span>  
  
- <span data-ttu-id="8db1f-121">目标文件夹中的同名文件正在使用中 (<xref:System.IO.IOException>)。</span><span class="sxs-lookup"><span data-stu-id="8db1f-121">A file in the target folder with the same name is in use (<xref:System.IO.IOException>).</span></span>  
  
- <span data-ttu-id="8db1f-122">路径中的文件名或文件夹名包含冒号 (:)，或其格式无效 (<xref:System.NotSupportedException>)。</span><span class="sxs-lookup"><span data-stu-id="8db1f-122">A file or folder name in the path contains a colon (:) or is in an invalid format (<xref:System.NotSupportedException>).</span></span>  
  
- <span data-ttu-id="8db1f-123">`ShowUI` 设置为 `True`、`onUserCancel` 设置为 `ThrowException`，并且用户已取消操作 (<xref:System.OperationCanceledException>)。</span><span class="sxs-lookup"><span data-stu-id="8db1f-123">`ShowUI` is set to `True`, `onUserCancel` is set to `ThrowException`, and the user has cancelled the operation (<xref:System.OperationCanceledException>).</span></span>  
  
- <span data-ttu-id="8db1f-124">`ShowUI` 设置为 `True`、`onUserCancel` 设置为 `ThrowException`，并出现未指定的 I/O 错误 (<xref:System.OperationCanceledException>)。</span><span class="sxs-lookup"><span data-stu-id="8db1f-124">`ShowUI` is set to `True`, `onUserCancel` is set to `ThrowException`, and an unspecified I/O error occurs (<xref:System.OperationCanceledException>).</span></span>  
  
- <span data-ttu-id="8db1f-125">路径超过了系统定义的最大长度 (<xref:System.IO.PathTooLongException>)。</span><span class="sxs-lookup"><span data-stu-id="8db1f-125">The path exceeds the system-defined maximum length (<xref:System.IO.PathTooLongException>).</span></span>  
  
- <span data-ttu-id="8db1f-126">用户没有必需的权限 (<xref:System.UnauthorizedAccessException>)。</span><span class="sxs-lookup"><span data-stu-id="8db1f-126">The user does not have required permission (<xref:System.UnauthorizedAccessException>).</span></span>  
  
- <span data-ttu-id="8db1f-127">该用户缺少查看该路径所必需的权限 (<xref:System.Security.SecurityException>)。</span><span class="sxs-lookup"><span data-stu-id="8db1f-127">The user lacks necessary permissions to view the path (<xref:System.Security.SecurityException>).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8db1f-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8db1f-128">See also</span></span>

- <xref:Microsoft.VisualBasic.FileIO.FileSystem>
- <xref:Microsoft.VisualBasic.FileIO.FileSystem.CopyFile%2A>
- <xref:Microsoft.VisualBasic.FileIO.UICancelOption>
- [<span data-ttu-id="8db1f-129">如何：将具有特定模式的文件复制到目录中</span><span class="sxs-lookup"><span data-stu-id="8db1f-129">How to: Copy Files with a Specific Pattern to a Directory</span></span>](how-to-copy-files-with-a-specific-pattern-to-a-directory.md)
- [<span data-ttu-id="8db1f-130">如何：在不同的目录中创建文件的副本</span><span class="sxs-lookup"><span data-stu-id="8db1f-130">How to: Create a Copy of a File in a Different Directory</span></span>](how-to-create-a-copy-of-a-file-in-a-different-directory.md)
- [<span data-ttu-id="8db1f-131">如何：将目录复制到另一个目录</span><span class="sxs-lookup"><span data-stu-id="8db1f-131">How to: Copy a Directory to Another Directory</span></span>](how-to-copy-a-directory-to-another-directory.md)
- [<span data-ttu-id="8db1f-132">如何：重命名文件</span><span class="sxs-lookup"><span data-stu-id="8db1f-132">How to: Rename a File</span></span>](how-to-rename-a-file.md)
