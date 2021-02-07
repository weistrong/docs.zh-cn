---
description: 了解更多： Null 语义
title: Null 语义
ms.date: 03/30/2017
ms.assetid: a97017ae-d634-4cf3-bbaf-054a528fd683
ms.openlocfilehash: 2326cd20a225f31693260aa038477f1f6090d02f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99695550"
---
# <a name="null-semantics"></a>Null 语义

下表提供了文档的各个部分的链接， [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 其中 `null` `Nothing` 讨论了 Visual Basic) 问题 (。  
  
|主题|说明|  
|-----------|-----------------|  
|[SQL-CLR 类型不匹配](sql-clr-type-mismatches.md)|本主题的 "Null 语义" 部分包括以下内容的讨论：三态 SQL Boolean 与两态公共语言运行时 (CLR) <xref:System.Boolean> 、文本 `Nothing` (Visual Basic) 和 `null` (c # ) ，以及其他类似问题。|  
|[标准查询运算符转换](standard-query-operator-translation.md)|本主题的“Null 语义”部分介绍 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]中的 null 比较语义。|  
|[System.String 方法](system-string-methods.md)|本主题的“与 .NET 的差异”部分说明从 <xref:System.String.LastIndexOf%2A> 返回 0 为何意味着字符串为 null 或找到的位置为 0。|  
|[计算数值序列中值的和](compute-the-sum-of-values-in-a-numeric-sequence.md)|描述运算符如何 <xref:System.Linq.Enumerable.Sum%2A> 计算 `null` (`Nothing` 在 Visual Basic) 而不是0（对于仅包含 null 值或空序列的序列）。|  
  
## <a name="see-also"></a>请参阅

- [数据类型和函数](data-types-and-functions.md)
