---
description: 了解详细信息：从序列中消除重复元素
title: 从序列中消除重复的元素
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 2b224a84-bad5-4843-adcc-14e784d280f5
ms.openlocfilehash: f371fc27794361e3ea92d342f845996d9291d30c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786090"
---
# <a name="eliminate-duplicate-elements-from-a-sequence"></a>从序列中消除重复的元素

使用 <xref:System.Linq.Queryable.Distinct%2A> 运算符可从序列中消除重复元素。  
  
## <a name="example"></a>示例  

 下面的示例使用 <xref:System.Linq.Queryable.Distinct%2A> 来选择有客户的唯一城市序列。  
  
 [!code-csharp[DLinqQueryExamples#36](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#36)]
 [!code-vb[DLinqQueryExamples#36](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#36)]  
  
## <a name="see-also"></a>请参阅

- [查询示例](query-examples.md)
