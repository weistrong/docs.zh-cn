---
description: '了解详细信息：变量 (实体 SQL) '
title: 变量 (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 3eed222a-f8f6-46b6-9cd5-220cc0e4e5d8
ms.openlocfilehash: 134fee8f61c8e87a18520e6622f6a6a5cceb0076
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795035"
---
# <a name="variables-entity-sql"></a>变量 (Entity SQL)

## <a name="variable"></a>变量  

 变量表达式是对当前作用域中定义的命名表达式的引用。 变量引用必须是 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] [标识符](identifiers-entity-sql.md)中定义的有效标识符。  
  
 以下示例演示如何在表达式中使用变量。 FROM 子句中的 `c` 是变量定义。 在 SELECT 子句中使用的 `c` 表示变量引用。  
  
```sql  
select c
from LOB.customers as c  
```  
  
## <a name="see-also"></a>请参阅

- [标识符](identifiers-entity-sql.md)
- [参数](parameters-entity-sql.md)
- [Entity SQL 概述](entity-sql-overview.md)
