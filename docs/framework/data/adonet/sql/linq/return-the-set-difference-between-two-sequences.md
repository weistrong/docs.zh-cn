---
description: 了解详细信息：返回两个序列之间的差集
title: 返回两个序列之间的差集
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 62efb546-c898-408f-af21-36e7c6fed217
ms.openlocfilehash: 6836195ac4e1ee678fd3e8089e7c341f7dd247e8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662972"
---
# <a name="return-the-set-difference-between-two-sequences"></a>返回两个序列之间的差集

使用 <xref:System.Linq.Queryable.Except%2A> 运算符可返回两个序列之间的差集。  
  
## <a name="example"></a>示例  

 此示例使用 <xref:System.Linq.Queryable.Except%2A> 返回 `Customers` 居住但不居住的所有国家/地区的序列 `Employees` 。  
  
 [!code-csharp[DLinqQueryExamples#41](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#41)]
 [!code-vb[DLinqQueryExamples#41](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#41)]  
  
 在 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 中，<xref:System.Linq.Queryable.Except%2A> 运算仅对集合而言是定义完善的。 针对多重集的语义尚未定义。  
  
## <a name="see-also"></a>请参阅

- [查询示例](query-examples.md)
- [标准查询运算符转换](standard-query-operator-translation.md)
