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
# <a name="how-to-detect-and-resolve-conflicting-submissions"></a>如何：检测到并解决冲突的提交

[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 提供了许多资源，用于检测和解决因多个用户更改数据库而产生的冲突。 有关详细信息，请参阅 [如何：管理更改冲突](how-to-manage-change-conflicts.md)。  
  
## <a name="example"></a>示例  

 下面的示例演示 `try` / `catch` 捕获异常的块 <xref:System.Data.Linq.ChangeConflictException> 。 每个冲突的实体和成员信息会显示在控制台窗口中。  
  
> [!NOTE]
> 您必须将 `using System.Reflection` 指令（在 Visual Basic 中为 `Imports System.Reflection`）包含在内，以支持信息检索。 有关详细信息，请参阅 <xref:System.Reflection>。  
  
 [!code-csharp[DLinqSubmittingChanges#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqSubmittingChanges/cs/Program.cs#2)]
 [!code-vb[DLinqSubmittingChanges#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqSubmittingChanges/vb/Module1.vb#2)]  
  
## <a name="see-also"></a>请参阅

- [进行和提交数据更改](making-and-submitting-data-changes.md)
- [如何：管理更改冲突](how-to-manage-change-conflicts.md)
