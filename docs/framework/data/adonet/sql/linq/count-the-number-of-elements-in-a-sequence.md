---
description: 了解详细信息：计算序列中的元素数
title: 对序列中元素的数目进行计数
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: ccbe5d54-c9eb-4b14-b0ab-f628483c5f99
ms.openlocfilehash: 91030516098e900229a1e131ea0c9a7d8bef4034
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99663074"
---
# <a name="count-the-number-of-elements-in-a-sequence"></a>对序列中元素的数目进行计数

使用 <xref:System.Linq.Enumerable.Count%2A> 运算符可计算序列中的元素数目。  
  
 对 Northwind 示例数据库运行此查询产生的输出为 `91`。  
  
## <a name="example"></a>示例  

 下面的示例计算数据库中的 `Customers` 数目。  
  
 [!code-csharp[DLinqQueryExamples#4](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#4)]
 [!code-vb[DLinqQueryExamples#4](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#4)]  
  
## <a name="example"></a>示例  

 下面的示例计算数据库中尚未停产的产品数目。  
  
 对 Northwind 示例数据库运行此示例产生的输出为 `69`。  
  
 [!code-csharp[DLinqQueryExamples#5](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#5)]
 [!code-vb[DLinqQueryExamples#5](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#5)]  
  
## <a name="see-also"></a>请参阅

- [聚合查询](aggregate-queries.md)
- [下载示例数据库](downloading-sample-databases.md)
