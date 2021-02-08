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
# <a name="variables-entity-sql"></a><span data-ttu-id="d7f6f-103">变量 (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="d7f6f-103">Variables (Entity SQL)</span></span>

## <a name="variable"></a><span data-ttu-id="d7f6f-104">变量</span><span class="sxs-lookup"><span data-stu-id="d7f6f-104">Variable</span></span>  

 <span data-ttu-id="d7f6f-105">变量表达式是对当前作用域中定义的命名表达式的引用。</span><span class="sxs-lookup"><span data-stu-id="d7f6f-105">A variable expression is a reference to a named expression defined in the current scope.</span></span> <span data-ttu-id="d7f6f-106">变量引用必须是 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] [标识符](identifiers-entity-sql.md)中定义的有效标识符。</span><span class="sxs-lookup"><span data-stu-id="d7f6f-106">A variable reference must be a valid [!INCLUDE[esql](../../../../../../includes/esql-md.md)] identifier, as defined in [Identifiers](identifiers-entity-sql.md).</span></span>  
  
 <span data-ttu-id="d7f6f-107">以下示例演示如何在表达式中使用变量。</span><span class="sxs-lookup"><span data-stu-id="d7f6f-107">The following example shows the use of a variable in the expression.</span></span> <span data-ttu-id="d7f6f-108">FROM 子句中的 `c` 是变量定义。</span><span class="sxs-lookup"><span data-stu-id="d7f6f-108">The `c` in the FROM clause is the definition of the variable.</span></span> <span data-ttu-id="d7f6f-109">在 SELECT 子句中使用的 `c` 表示变量引用。</span><span class="sxs-lookup"><span data-stu-id="d7f6f-109">The use of `c` in the SELECT clause represents the variable reference.</span></span>  
  
```sql  
select c
from LOB.customers as c  
```  
  
## <a name="see-also"></a><span data-ttu-id="d7f6f-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="d7f6f-110">See also</span></span>

- [<span data-ttu-id="d7f6f-111">标识符</span><span class="sxs-lookup"><span data-stu-id="d7f6f-111">Identifiers</span></span>](identifiers-entity-sql.md)
- [<span data-ttu-id="d7f6f-112">参数</span><span class="sxs-lookup"><span data-stu-id="d7f6f-112">Parameters</span></span>](parameters-entity-sql.md)
- [<span data-ttu-id="d7f6f-113">Entity SQL 概述</span><span class="sxs-lookup"><span data-stu-id="d7f6f-113">Entity SQL Overview</span></span>](entity-sql-overview.md)
