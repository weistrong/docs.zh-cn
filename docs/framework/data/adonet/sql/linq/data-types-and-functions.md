---
description: 了解更多相关信息：数据类型和函数
title: 数据类型和函数
ms.date: 03/30/2017
ms.assetid: 683413c5-0312-4e60-8619-9a97bdc6e62a
ms.openlocfilehash: 5a718d5fd4b110d35153e4486e42cee0b8a215bd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786142"
---
# <a name="data-types-and-functions"></a>数据类型和函数

下表列出的主题介绍了对公共语言运行库 (CLR) 的成员、构造和强制转换的 LINQ to SQL 支持。 受支持的成员和构造可以在 LINQ to SQL 查询中使用。  
  
 表中不受支持的项表示 LINQ to SQL 无法转换 CLR 成员、构造或强制转换以供在 SQL Server 上执行。 您可能仍可以在您的代码中使用这些项，但是在查询转换为 Transact-SQL 之前或结果已经从数据库中检索后必须对其进行计算。  
  
|主题|说明|  
|-----------|-----------------|  
|[SQL-CLR 类型映射](sql-clr-type-mapping.md)|提供 CLR 类型和 SQL Server 类型之间的详细映射矩阵。|  
|[基本数据类型](basic-data-types.md)|汇总了 .NET Framework 的行为差异。|  
|[Boolean 数据类型](boolean-data-types.md)|汇总了 .NET Framework 的行为差异。|  
|[Null 语义](null-semantics.md)|提供指向讨论 null 和可以为 null 问题的 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 主题的链接。|  
|[数值和比较运算符](numeric-and-comparison-operators.md)|汇总了 .NET Framework 的行为差异。|  
|[序列运算符](sequence-operators.md)|汇总了 .NET Framework 的行为差异。|  
|[System.Convert 方法](system-convert-methods.md)|汇总了 .NET Framework 的行为差异。|  
|[System.DateTime 方法](system-datetime-methods.md)|介绍对 <xref:System.DateTime?displayProperty=nameWithType> 结构的成员的 LINQ to SQL 支持。|  
|[System.DateTimeOffset 方法](system-datetimeoffset-methods.md)|介绍对 <xref:System.DateTimeOffset?displayProperty=nameWithType> 结构的成员的 LINQ to SQL 支持。|  
|[System.Math 方法](system-math-methods.md)|汇总了 .NET Framework 的行为差异。|  
|[System.Object 方法](system-object-methods.md)|汇总了 .NET Framework 的行为差异。|  
|[System.String 方法](system-string-methods.md)|汇总了 .NET Framework 的行为差异。|  
|[System.TimeSpan 方法](system-timespan-methods.md)|介绍对 <xref:System.TimeSpan?displayProperty=nameWithType> 结构的成员的 LINQ to SQL 支持。|  
|[不支持的功能](unsupported-functionality.md)|介绍 [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] 不支持的功能。|  
  
## <a name="see-also"></a>请参阅

- [SQL-CLR 类型不匹配](sql-clr-type-mismatches.md)
- [引用](reference.md)
