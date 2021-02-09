---
description: 详细了解：操作说明：在 Visual Basic 中删除文件
title: 如何：删除文件
ms.date: 07/20/2015
helpviewer_keywords:
- Delete method [Visual Basic]
- files [Visual Basic], deleting
- files [Visual Basic], manipulating
- File object
ms.assetid: 4b721769-3e45-4be7-b7fe-b08dc4141b44
ms.openlocfilehash: 49bfe2e4a0d9114e2f653ae14dab303e35e2dfeb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797570"
---
# <a name="how-to-delete-a-file-in-visual-basic"></a><span data-ttu-id="8e1fe-103">如何：在 Visual Basic 中删除文件</span><span class="sxs-lookup"><span data-stu-id="8e1fe-103">How to: Delete a File in Visual Basic</span></span>

<span data-ttu-id="8e1fe-104">通过 `My.Computer.FileSystem` 对象的 `DeleteFile` 方法，可以删除文件。</span><span class="sxs-lookup"><span data-stu-id="8e1fe-104">The `DeleteFile` method of the `My.Computer.FileSystem` object allows you to delete a file.</span></span> <span data-ttu-id="8e1fe-105">它提供的选项包括：是否将已删除的文件发送到“回收站”、是否要求用户确认应删除该文件，以及当用户取消操作时要执行的操作。</span><span class="sxs-lookup"><span data-stu-id="8e1fe-105">Among the options it offers are: whether to send the deleted file to the **Recycle Bin**, whether to ask the user to confirm that the file should be deleted, and what to do when the user cancels the operation.</span></span>  
  
### <a name="to-delete-a-text-file"></a><span data-ttu-id="8e1fe-106">删除文本文件</span><span class="sxs-lookup"><span data-stu-id="8e1fe-106">To delete a text file</span></span>  
  
- <span data-ttu-id="8e1fe-107">使用 `DeleteFile` 方法删除文件。</span><span class="sxs-lookup"><span data-stu-id="8e1fe-107">Use the `DeleteFile` method to delete the file.</span></span> <span data-ttu-id="8e1fe-108">以下代码演示如何删除名为 `test.txt` 的文件。</span><span class="sxs-lookup"><span data-stu-id="8e1fe-108">The following code demonstrates how to delete the file named `test.txt`.</span></span>  
  
     [!code-vb[VbVbcnMyFileSystem#22](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/Class1.vb#22)]  
  
### <a name="to-delete-a-text-file-and-ask-the-user-to-confirm-that-the-file-should-be-deleted"></a><span data-ttu-id="8e1fe-109">删除文本文件，并要求用户确认应删除该文件</span><span class="sxs-lookup"><span data-stu-id="8e1fe-109">To delete a text file and ask the user to confirm that the file should be deleted</span></span>  
  
- <span data-ttu-id="8e1fe-110">使用 `DeleteFile` 方法删除文件，同时将 `showUI` 设置为 `AllDialogs`。</span><span class="sxs-lookup"><span data-stu-id="8e1fe-110">Use the `DeleteFile` method to delete the file, setting `showUI` to `AllDialogs`.</span></span> <span data-ttu-id="8e1fe-111">以下代码演示如何删除名为 `test.txt` 的文件，并允许用户确认是否应删除该文件。</span><span class="sxs-lookup"><span data-stu-id="8e1fe-111">The following code demonstrates how to delete the file named `test.txt` and allow the user to confirm that the file should be deleted.</span></span>  
  
     [!code-vb[VbFileIOMisc#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbFileIOMisc/VB/Class1.vb#9)]  
  
### <a name="to-delete-a-text-file-and-send-it-to-the-recycle-bin"></a><span data-ttu-id="8e1fe-112">删除文本文件并将其发送到“回收站”</span><span class="sxs-lookup"><span data-stu-id="8e1fe-112">To delete a text file and send it to the Recycle Bin</span></span>  
  
- <span data-ttu-id="8e1fe-113">使用 `DeleteFile` 方法删除文件，并为 `recycle` 参数指定 `SendToRecycleBin`。</span><span class="sxs-lookup"><span data-stu-id="8e1fe-113">Use the `DeleteFile` method to delete the file, specifying `SendToRecycleBin` for the `recycle` parameter.</span></span> <span data-ttu-id="8e1fe-114">以下代码演示如何删除名为 `test.txt` 的文件并将其发送到“回收站”。</span><span class="sxs-lookup"><span data-stu-id="8e1fe-114">The following code demonstrates how to delete the file named `test.txt` and send it to the **Recycle Bin**.</span></span>  
  
     [!code-vb[VbFileIOMisc#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbFileIOMisc/VB/Class1.vb#10)]  
  
## <a name="robust-programming"></a><span data-ttu-id="8e1fe-115">可靠编程</span><span class="sxs-lookup"><span data-stu-id="8e1fe-115">Robust Programming</span></span>  

 <span data-ttu-id="8e1fe-116">以下情况可能会导致异常：</span><span class="sxs-lookup"><span data-stu-id="8e1fe-116">The following conditions may cause an exception:</span></span>  
  
- <span data-ttu-id="8e1fe-117">路径由于以下原因之一而无效：是零长度字符串；仅为空白；包含无效字符；是一个设备路径（开头字符为 \\\\.\\）(<xref:System.ArgumentException>)。</span><span class="sxs-lookup"><span data-stu-id="8e1fe-117">The path is not valid for one of the following reasons: it is a zero-length string, it contains only white space, it contains invalid characters, or it is a device path (starts with \\\\.\\) (<xref:System.ArgumentException>).</span></span>  
  
- <span data-ttu-id="8e1fe-118">路径无效，因为它是 `Nothing` (<xref:System.ArgumentNullException>)。</span><span class="sxs-lookup"><span data-stu-id="8e1fe-118">The path is not valid because it is `Nothing` (<xref:System.ArgumentNullException>).</span></span>  
  
- <span data-ttu-id="8e1fe-119">路径超过了系统定义的最大长度 (<xref:System.IO.PathTooLongException>)。</span><span class="sxs-lookup"><span data-stu-id="8e1fe-119">The path exceeds the system-defined maximum length (<xref:System.IO.PathTooLongException>).</span></span>  
  
- <span data-ttu-id="8e1fe-120">路径中的文件名或文件夹名包含冒号 (:)，或其格式无效 (<xref:System.NotSupportedException>)。</span><span class="sxs-lookup"><span data-stu-id="8e1fe-120">A file or folder name in the path contains a colon (:) or is in an invalid format (<xref:System.NotSupportedException>).</span></span>  
  
- <span data-ttu-id="8e1fe-121">该文件正在使用中 (<xref:System.IO.IOException>)。</span><span class="sxs-lookup"><span data-stu-id="8e1fe-121">The file is in use (<xref:System.IO.IOException>).</span></span>  
  
- <span data-ttu-id="8e1fe-122">该用户缺少查看该路径所必需的权限 (<xref:System.Security.SecurityException>)。</span><span class="sxs-lookup"><span data-stu-id="8e1fe-122">The user lacks necessary permissions to view the path (<xref:System.Security.SecurityException>).</span></span>  
  
- <span data-ttu-id="8e1fe-123">该文件不存在 (<xref:System.IO.FileNotFoundException>)。</span><span class="sxs-lookup"><span data-stu-id="8e1fe-123">The file does not exist (<xref:System.IO.FileNotFoundException>).</span></span>  
  
- <span data-ttu-id="8e1fe-124">用户无权删除文件，或文件为只读 (<xref:System.UnauthorizedAccessException>)。</span><span class="sxs-lookup"><span data-stu-id="8e1fe-124">The user does not have permission to delete the file, or the file is read-only (<xref:System.UnauthorizedAccessException>).</span></span>  
  
- <span data-ttu-id="8e1fe-125">存在部分信任的情况，在此情况下用户没有足够的权限 (<xref:System.Security.SecurityException>)。</span><span class="sxs-lookup"><span data-stu-id="8e1fe-125">A partial-trust situation exists in which the user does not have sufficient permissions (<xref:System.Security.SecurityException>).</span></span>  
  
- <span data-ttu-id="8e1fe-126">用户取消了该操作，并且 `onUserCancel` 设置为 `ThrowException` (<xref:System.OperationCanceledException>)。</span><span class="sxs-lookup"><span data-stu-id="8e1fe-126">The user cancelled the operation and `onUserCancel` is set to `ThrowException` (<xref:System.OperationCanceledException>).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8e1fe-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8e1fe-127">See also</span></span>

- <xref:Microsoft.VisualBasic.FileIO.UICancelOption>
- <xref:Microsoft.VisualBasic.FileIO.FileSystem>
- <xref:Microsoft.VisualBasic.FileIO.UIOption>
- <xref:Microsoft.VisualBasic.FileIO.RecycleOption>
- [<span data-ttu-id="8e1fe-128">如何：获取目录中的文件集合</span><span class="sxs-lookup"><span data-stu-id="8e1fe-128">How to: Get the Collection of Files in a Directory</span></span>](how-to-get-the-collection-of-files-in-a-directory.md)
