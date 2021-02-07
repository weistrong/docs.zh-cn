---
description: 了解详细信息：如何：检测和解决冲突的提交
title: 如何：检测到并解决冲突的提交
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 91e27206-01fb-4c7a-8afc-1383a6ac5067
ms.openlocfilehash: 7ccfc9aeba8a21c3f5e950569d7650af087416a4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99739035"
---
# <a name="how-to-detect-and-resolve-conflicting-submissions"></a><span data-ttu-id="9e76f-103">如何：检测到并解决冲突的提交</span><span class="sxs-lookup"><span data-stu-id="9e76f-103">How to: Detect and Resolve Conflicting Submissions</span></span>

[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <span data-ttu-id="9e76f-104">提供了许多资源，用于检测和解决因多个用户更改数据库而产生的冲突。</span><span class="sxs-lookup"><span data-stu-id="9e76f-104">provides many resources for detecting and resolving conflicts that stem from multi-user changes to the database.</span></span> <span data-ttu-id="9e76f-105">有关详细信息，请参阅 [如何：管理更改冲突](how-to-manage-change-conflicts.md)。</span><span class="sxs-lookup"><span data-stu-id="9e76f-105">For more information, see [How to: Manage Change Conflicts](how-to-manage-change-conflicts.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="9e76f-106">示例</span><span class="sxs-lookup"><span data-stu-id="9e76f-106">Example</span></span>  

 <span data-ttu-id="9e76f-107">下面的示例演示 `try` / `catch` 捕获异常的块 <xref:System.Data.Linq.ChangeConflictException> 。</span><span class="sxs-lookup"><span data-stu-id="9e76f-107">The following example shows a `try`/`catch` block that catches a <xref:System.Data.Linq.ChangeConflictException> exception.</span></span> <span data-ttu-id="9e76f-108">每个冲突的实体和成员信息会显示在控制台窗口中。</span><span class="sxs-lookup"><span data-stu-id="9e76f-108">Entity and member information for each conflict is displayed in the console window.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="9e76f-109">您必须将 `using System.Reflection` 指令（在 Visual Basic 中为 `Imports System.Reflection`）包含在内，以支持信息检索。</span><span class="sxs-lookup"><span data-stu-id="9e76f-109">You must include the `using System.Reflection` directive (`Imports System.Reflection` in Visual Basic) to support the information retrieval.</span></span> <span data-ttu-id="9e76f-110">有关详细信息，请参阅 <xref:System.Reflection>。</span><span class="sxs-lookup"><span data-stu-id="9e76f-110">For more information, see <xref:System.Reflection>.</span></span>  
  
 [!code-csharp[DLinqSubmittingChanges#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqSubmittingChanges/cs/Program.cs#2)]
 [!code-vb[DLinqSubmittingChanges#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqSubmittingChanges/vb/Module1.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="9e76f-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="9e76f-111">See also</span></span>

- [<span data-ttu-id="9e76f-112">进行和提交数据更改</span><span class="sxs-lookup"><span data-stu-id="9e76f-112">Making and Submitting Data Changes</span></span>](making-and-submitting-data-changes.md)
- [<span data-ttu-id="9e76f-113">如何：管理更改冲突</span><span class="sxs-lookup"><span data-stu-id="9e76f-113">How to: Manage Change Conflicts</span></span>](how-to-manage-change-conflicts.md)
