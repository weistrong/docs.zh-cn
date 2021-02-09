---
description: 详细了解：操作说明：在 Visual Basic 中移动文件
title: 如何：移动文件
ms.date: 07/20/2015
helpviewer_keywords:
- files [Visual Basic], moving
ms.assetid: 53a7457b-5815-41ad-b37d-28537c1fb77a
ms.openlocfilehash: 31049d2b7f0516c056fc1f1620a3ad8c1f0a2e1c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797518"
---
# <a name="how-to-move-a-file-in-visual-basic"></a><span data-ttu-id="332be-103">如何：在 Visual Basic 中移动文件</span><span class="sxs-lookup"><span data-stu-id="332be-103">How to: Move a File in Visual Basic</span></span>

<span data-ttu-id="332be-104">`My.Computer.FileSystem.MoveFile` 方法可以用于将文件移到另一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="332be-104">The `My.Computer.FileSystem.MoveFile` method can be used to move a file to another folder.</span></span> <span data-ttu-id="332be-105">如果目标结构不存在，则将创建它。</span><span class="sxs-lookup"><span data-stu-id="332be-105">If the target structure does not exist, it will be created.</span></span>  
  
### <a name="to-move-a-file"></a><span data-ttu-id="332be-106">移动文件</span><span class="sxs-lookup"><span data-stu-id="332be-106">To move a file</span></span>  
  
- <span data-ttu-id="332be-107">使用 `MoveFile` 方法来移动文件，并指定源文件和目标文件的文件名和位置。</span><span class="sxs-lookup"><span data-stu-id="332be-107">Use the `MoveFile` method to move the file, specifying the file name and location for both the source file and the target file.</span></span> <span data-ttu-id="332be-108">本示例将名为 `test.txt` 的文件从 `TestDir1` 移动到 `TestDir2`。</span><span class="sxs-lookup"><span data-stu-id="332be-108">This example moves the file named `test.txt` from `TestDir1` to `TestDir2`.</span></span> <span data-ttu-id="332be-109">请注意，即使目标文件名与源文件名相同，也要指定目标文件名。</span><span class="sxs-lookup"><span data-stu-id="332be-109">Note that the target file name is specified even though it is the same as the source file name.</span></span>  
  
     [!code-vb[VbVbcnMyFileSystem#24](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/Class1.vb#24)]  
  
### <a name="to-move-a-file-and-rename-it"></a><span data-ttu-id="332be-110">移动文件并对其重命名</span><span class="sxs-lookup"><span data-stu-id="332be-110">To move a file and rename it</span></span>  
  
- <span data-ttu-id="332be-111">使用 `MoveFile` 方法来移动文件，指定源文件名和位置、目标位置以及在目标位置中的新名称。</span><span class="sxs-lookup"><span data-stu-id="332be-111">Use the `MoveFile` method to move the file, specifying the source file name and location, the target location, and the new name at the target location.</span></span> <span data-ttu-id="332be-112">本示例将名为 `test.txt` 的文件从 `TestDir1` 移动到 `TestDir2` 并将其重命名为 `nexttest.txt`。</span><span class="sxs-lookup"><span data-stu-id="332be-112">This example moves the file named `test.txt` from `TestDir1` to `TestDir2` and renames it `nexttest.txt`.</span></span>  
  
     [!code-vb[VbVbcnMyFileSystem#25](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/Class1.vb#25)]  
  
## <a name="robust-programming"></a><span data-ttu-id="332be-113">可靠编程</span><span class="sxs-lookup"><span data-stu-id="332be-113">Robust Programming</span></span>  

 <span data-ttu-id="332be-114">以下情况可能会导致异常：</span><span class="sxs-lookup"><span data-stu-id="332be-114">The following conditions may cause an exception:</span></span>  
  
- <span data-ttu-id="332be-115">路径由于以下原因之一而无效：是零长度字符串；仅为空白；包含无效字符；是一个设备路径（开头字符为 \\\\.\\）(<xref:System.ArgumentException>)。</span><span class="sxs-lookup"><span data-stu-id="332be-115">The path is not valid for one of the following reasons: it is a zero-length string, it contains only white space, it contains invalid characters, or it is a device path (starts with \\\\.\\) (<xref:System.ArgumentException>).</span></span>  
  
- <span data-ttu-id="332be-116">路径无效，因为它是 `Nothing` (<xref:System.ArgumentNullException>)。</span><span class="sxs-lookup"><span data-stu-id="332be-116">The path is not valid because it is `Nothing` (<xref:System.ArgumentNullException>).</span></span>  
  
- <span data-ttu-id="332be-117">`destinationFileName` 为 `Nothing` 或空字符串 (<xref:System.ArgumentNullException>)。</span><span class="sxs-lookup"><span data-stu-id="332be-117">`destinationFileName` is `Nothing` or an empty string (<xref:System.ArgumentNullException>).</span></span>  
  
- <span data-ttu-id="332be-118">源文件无效或不存在 (<xref:System.IO.FileNotFoundException>)。</span><span class="sxs-lookup"><span data-stu-id="332be-118">The source file is not valid or does not exist (<xref:System.IO.FileNotFoundException>).</span></span>  
  
- <span data-ttu-id="332be-119">组合路径指向现有目录、目标文件已存在并且 `overwrite` 已设置为 `False`、具有相同名称的目标目录中的文件正在使用，或用户没有足够的权限访问该文件 (<xref:System.IO.IOException>)。</span><span class="sxs-lookup"><span data-stu-id="332be-119">The combined path points to an existing directory, the destination file exists and `overwrite` is set to `False`, a file in the target directory with the same name is in use, or the user does not have sufficient permissions to access the file (<xref:System.IO.IOException>).</span></span>  
  
- <span data-ttu-id="332be-120">路径中的文件名或目录名包含冒号 (:)，或格式无效 (<xref:System.NotSupportedException>)。</span><span class="sxs-lookup"><span data-stu-id="332be-120">A file or directory name in the path contains a colon (:) or is in an invalid format (<xref:System.NotSupportedException>).</span></span>  
  
- <span data-ttu-id="332be-121">`showUI` 已设置为 `True`、 `onUserCancel` 已设置为 `ThrowException`，并且用户已取消该操作或发生了未指定的 I/O 错误 (<xref:System.OperationCanceledException>)。</span><span class="sxs-lookup"><span data-stu-id="332be-121">`showUI` is set to `True`, `onUserCancel` is set to `ThrowException`, and either the user has cancelled the operation or an unspecified I/O error occurs (<xref:System.OperationCanceledException>).</span></span>  
  
- <span data-ttu-id="332be-122">路径超过了系统定义的最大长度 (<xref:System.IO.PathTooLongException>)。</span><span class="sxs-lookup"><span data-stu-id="332be-122">The path exceeds the system-defined maximum length (<xref:System.IO.PathTooLongException>).</span></span>  
  
- <span data-ttu-id="332be-123">该用户缺少查看该路径所必需的权限 (<xref:System.Security.SecurityException>)。</span><span class="sxs-lookup"><span data-stu-id="332be-123">The user lacks necessary permissions to view the path (<xref:System.Security.SecurityException>).</span></span>  
  
- <span data-ttu-id="332be-124">用户没有必需的权限 (<xref:System.UnauthorizedAccessException>)。</span><span class="sxs-lookup"><span data-stu-id="332be-124">The user does not have required permission (<xref:System.UnauthorizedAccessException>).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="332be-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="332be-125">See also</span></span>

- <xref:Microsoft.VisualBasic.FileIO.FileSystem.MoveFile%2A>
- [<span data-ttu-id="332be-126">如何：重命名文件</span><span class="sxs-lookup"><span data-stu-id="332be-126">How to: Rename a File</span></span>](how-to-rename-a-file.md)
- [<span data-ttu-id="332be-127">如何：在不同的目录中创建文件的副本</span><span class="sxs-lookup"><span data-stu-id="332be-127">How to: Create a Copy of a File in a Different Directory</span></span>](how-to-create-a-copy-of-a-file-in-a-different-directory.md)
- [<span data-ttu-id="332be-128">如何：分析文件路径</span><span class="sxs-lookup"><span data-stu-id="332be-128">How to: Parse File Paths</span></span>](how-to-parse-file-paths.md)
