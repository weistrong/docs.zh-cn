---
description: '了解有关以下方面的详细信息：权限被拒绝 (Visual Basic) '
title: 权限被拒绝
ms.date: 07/20/2015
f1_keywords:
- vbrID70
ms.assetid: 71f46756-f522-4814-aab4-492bf9924245
ms.openlocfilehash: dcd7f69c1294d22510a3600a3feb045da30faf17
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795412"
---
# <a name="permission-denied-visual-basic"></a><span data-ttu-id="3a433-103">权限被拒绝 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="3a433-103">Permission denied (Visual Basic)</span></span>

<span data-ttu-id="3a433-104">尝试写入到写保护的磁盘或访问锁定的文件。</span><span class="sxs-lookup"><span data-stu-id="3a433-104">An attempt was made to write to a write-protected disk or to access a locked file.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="3a433-105">更正此错误</span><span class="sxs-lookup"><span data-stu-id="3a433-105">To correct this error</span></span>  
  
1. <span data-ttu-id="3a433-106">若要打开写保护的文件，请更改文件的写保护特性。</span><span class="sxs-lookup"><span data-stu-id="3a433-106">To open a write-protected file, change the write-protection attribute of the file.</span></span>  
  
2. <span data-ttu-id="3a433-107">请确保其他进程未锁定该文件，并等待打开该文件，直到另一个进程释放它。</span><span class="sxs-lookup"><span data-stu-id="3a433-107">Make sure that another process has not locked the file, and wait to open the file until the other process releases it.</span></span>  
  
3. <span data-ttu-id="3a433-108">若要访问注册表，请检查你的用户权限是否包括此类型的注册表访问权限。</span><span class="sxs-lookup"><span data-stu-id="3a433-108">To access the registry, check that your user permissions include this type of registry access.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3a433-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="3a433-109">See also</span></span>

- [<span data-ttu-id="3a433-110">错误类型</span><span class="sxs-lookup"><span data-stu-id="3a433-110">Error Types</span></span>](../../programming-guide/language-features/error-types.md)
