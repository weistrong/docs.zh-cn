---
description: 了解详细信息：路径/文件访问错误
title: 路径/文件访问错误
ms.date: 07/20/2015
f1_keywords:
- vbrID75
ms.assetid: 6ce3a161-7316-46bd-a785-0d50e5414020
ms.openlocfilehash: d4fc7e716f025c0a482ab414f4a25a2b521634e6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795438"
---
# <a name="pathfile-access-error"></a><span data-ttu-id="09a1b-103">路径/文件访问错误</span><span class="sxs-lookup"><span data-stu-id="09a1b-103">Path/File access error</span></span>

<span data-ttu-id="09a1b-104">在文件访问或磁盘访问操作期间，操作系统无法在路径和文件名之间建立连接。</span><span class="sxs-lookup"><span data-stu-id="09a1b-104">During a file-access or disk-access operation, the operating system could not make a connection between the path and the file name.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="09a1b-105">更正此错误</span><span class="sxs-lookup"><span data-stu-id="09a1b-105">To correct this error</span></span>  
  
1. <span data-ttu-id="09a1b-106">请确保文件规范格式正确。</span><span class="sxs-lookup"><span data-stu-id="09a1b-106">Make sure the file specification is correctly formatted.</span></span> <span data-ttu-id="09a1b-107">文件名可以包含完全限定的 (绝对) 或相对路径。</span><span class="sxs-lookup"><span data-stu-id="09a1b-107">A file name can contain a fully qualified (absolute) or relative path.</span></span> <span data-ttu-id="09a1b-108">完全限定路径以驱动器名称开头 (如果路径位于另一个驱动器上) 并列出从根到文件的显式路径。</span><span class="sxs-lookup"><span data-stu-id="09a1b-108">A fully qualified path starts with the drive name (if the path is on another drive) and lists the explicit path from the root to the file.</span></span> <span data-ttu-id="09a1b-109">未完全限定的任何路径都是相对于当前驱动器和目录的路径。</span><span class="sxs-lookup"><span data-stu-id="09a1b-109">Any path that is not fully qualified is relative to the current drive and directory.</span></span>  
  
2. <span data-ttu-id="09a1b-110">请确保未尝试保存将替换现有只读文件的文件。</span><span class="sxs-lookup"><span data-stu-id="09a1b-110">Make sure that you did not attempt to save a file that would replace an existing read-only file.</span></span> <span data-ttu-id="09a1b-111">如果是这种情况，请更改目标文件的只读属性，或使用不同的文件名保存该文件。</span><span class="sxs-lookup"><span data-stu-id="09a1b-111">If this is the case, change the read-only attribute of the target file, or save the file with a different file name.</span></span>  
  
3. <span data-ttu-id="09a1b-112">请确保未尝试按顺序或模式打开只读文件 `Output` `Append` 。</span><span class="sxs-lookup"><span data-stu-id="09a1b-112">Make sure you did not attempt to open a read-only file in sequential `Output` or `Append` mode.</span></span> <span data-ttu-id="09a1b-113">如果是这种情况，请在模式下打开该文件 `Input` 或更改该文件的只读属性。</span><span class="sxs-lookup"><span data-stu-id="09a1b-113">If this is the case, open the file in `Input` mode or change the read-only attribute of the file.</span></span>  
  
4. <span data-ttu-id="09a1b-114">请确保未尝试在数据库或文档中更改 Visual Basic 项目。</span><span class="sxs-lookup"><span data-stu-id="09a1b-114">Make sure you did not attempt to change a Visual Basic project within a database or document.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="09a1b-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="09a1b-115">See also</span></span>

- [<span data-ttu-id="09a1b-116">错误类型</span><span class="sxs-lookup"><span data-stu-id="09a1b-116">Error Types</span></span>](../../programming-guide/language-features/error-types.md)
