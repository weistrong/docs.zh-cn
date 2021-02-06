---
description: 了解详细信息：返回两个序列的并集
title: 返回两个序列的并集
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 8b8bd3cb-86d4-4a3b-9906-61f68726dd1f
ms.openlocfilehash: 5541316560c05712e22c54f706b02d868fadb381
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662957"
---
# <a name="return-the-set-union-of-two-sequences"></a>返回两个序列的并集

使用 <xref:System.Linq.Queryable.Union%2A> 运算符可返回两个序列的并集。  
  
## <a name="example"></a>示例  

 此示例使用 <xref:System.Linq.Queryable.Union%2A> 返回有或的所有国家/地区的序列 `Customers` `Employees` 。  
  
 [!code-csharp[DLinqQueryExamples#43](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#43)]
 [!code-vb[DLinqQueryExamples#43](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#43)]  
  
 在中 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] ， <xref:System.Linq.Queryable.Union%2A> 运算符是为多重集定义的，因为多重集的无序串联 (实际上是 [`UNION ALL`](/sql/t-sql/language-elements/set-operators-union-transact-sql) SQL) 中子句的结果。

有关详细信息和示例，请参阅 <xref:System.Linq.Queryable.Union%2A?displayProperty=nameWithType> 。
  
## <a name="see-also"></a>请参阅

- [查询示例](query-examples.md)
- [标准查询运算符转换](standard-query-operator-translation.md)
