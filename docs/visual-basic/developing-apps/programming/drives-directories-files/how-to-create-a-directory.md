---
description: 详细了解：操作说明：在 Visual Basic 中创建目录
title: 如何：创建目录
ms.date: 07/20/2015
helpviewer_keywords:
- directories [Visual Basic], creating
- folders [Visual Basic], creating
ms.assetid: 0351a2ca-24d8-43b5-bb39-9b99e6401cff
ms.openlocfilehash: 39a0f1b2f482b27b6f207f0ca8a498db198e9d59
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99797596"
---
# <a name="how-to-create-a-directory-in-visual-basic"></a><span data-ttu-id="09936-103">如何：在 Visual Basic 中创建目录</span><span class="sxs-lookup"><span data-stu-id="09936-103">How to: Create a Directory in Visual Basic</span></span>

<span data-ttu-id="09936-104">使用 `My.Computer.FileSystem` 对象的 `CreateDirectory` 方法来创建目录。</span><span class="sxs-lookup"><span data-stu-id="09936-104">Use the `CreateDirectory` method of the `My.Computer.FileSystem` object to create directories.</span></span>  
  
 <span data-ttu-id="09936-105">如果该目录已存在，则不引发任何异常。</span><span class="sxs-lookup"><span data-stu-id="09936-105">If the directory already exists, no exception is thrown.</span></span>  
  
### <a name="to-create-a-directory"></a><span data-ttu-id="09936-106">创建目录</span><span class="sxs-lookup"><span data-stu-id="09936-106">To create a directory</span></span>  
  
- <span data-ttu-id="09936-107">使用 `CreateDirectory` 方法，指定将在其中创建目录的位置的完整路径。</span><span class="sxs-lookup"><span data-stu-id="09936-107">Use the `CreateDirectory` method by specifying the full path of the location where the directory should be created.</span></span> <span data-ttu-id="09936-108">此示例在 `NewDirectory` 中创建目录 `C:\Documents and Settings\All Users\Documents`。</span><span class="sxs-lookup"><span data-stu-id="09936-108">This example creates the directory `NewDirectory` in `C:\Documents and Settings\All Users\Documents`.</span></span>  
  
     [!code-vb[VbVbcnMyFileSystem#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnMyFileSystem/VB/Class1.vb#2)]  
  
## <a name="robust-programming"></a><span data-ttu-id="09936-109">可靠编程</span><span class="sxs-lookup"><span data-stu-id="09936-109">Robust Programming</span></span>  

 <span data-ttu-id="09936-110">以下情况可能会导致异常：</span><span class="sxs-lookup"><span data-stu-id="09936-110">The following conditions may cause an exception:</span></span>  
  
- <span data-ttu-id="09936-111">目录名称格式不正确。</span><span class="sxs-lookup"><span data-stu-id="09936-111">The directory name is malformed.</span></span> <span data-ttu-id="09936-112">例如，它包含非法字符或仅为空白 (<xref:System.ArgumentException>)。</span><span class="sxs-lookup"><span data-stu-id="09936-112">For example, it contains illegal characters or is only white space (<xref:System.ArgumentException>).</span></span>  
  
- <span data-ttu-id="09936-113">要创建的目录的父目录为只读 (<xref:System.IO.IOException>)。</span><span class="sxs-lookup"><span data-stu-id="09936-113">The parent directory of the directory to be created is read-only (<xref:System.IO.IOException>).</span></span>  
  
- <span data-ttu-id="09936-114">目录名称为 `Nothing` (<xref:System.ArgumentNullException>)。</span><span class="sxs-lookup"><span data-stu-id="09936-114">The directory name is `Nothing` (<xref:System.ArgumentNullException>).</span></span>  
  
- <span data-ttu-id="09936-115">目录名称过长 (<xref:System.IO.PathTooLongException>)。</span><span class="sxs-lookup"><span data-stu-id="09936-115">The directory name is too long (<xref:System.IO.PathTooLongException>).</span></span>  
  
- <span data-ttu-id="09936-116">目录名称是一个冒号“:”(<xref:System.NotSupportedException>)。</span><span class="sxs-lookup"><span data-stu-id="09936-116">The directory name is a colon ":" (<xref:System.NotSupportedException>).</span></span>  
  
- <span data-ttu-id="09936-117">用户无权创建目录 (<xref:System.UnauthorizedAccessException>)。</span><span class="sxs-lookup"><span data-stu-id="09936-117">The user does not have permission to create the directory (<xref:System.UnauthorizedAccessException>).</span></span>  
  
- <span data-ttu-id="09936-118">用户在部分信任情况下缺少权限 (<xref:System.Security.SecurityException>)。</span><span class="sxs-lookup"><span data-stu-id="09936-118">The user lacks permissions in a partial-trust situation (<xref:System.Security.SecurityException>).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="09936-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="09936-119">See also</span></span>

- <xref:Microsoft.VisualBasic.FileIO.FileSystem.CreateDirectory%2A>
- [<span data-ttu-id="09936-120">创建、删除和移动文件和目录</span><span class="sxs-lookup"><span data-stu-id="09936-120">Creating, Deleting, and Moving Files and Directories</span></span>](creating-deleting-and-moving-files-and-directories.md)
