---
description: '了解详细信息：实体 SQL 参数 () '
title: 参数 (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 8d618edd-0988-4ff2-8263-ce59448af7a5
ms.openlocfilehash: 77b1e6ee95b5d367fec8d99345bbb416c2b9787d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99724526"
---
# <a name="parameters-entity-sql"></a><span data-ttu-id="56e84-103">参数 (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="56e84-103">Parameters (Entity SQL)</span></span>

<span data-ttu-id="56e84-104">参数是在 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 之外（通常通过由主机语言使用的绑定 API）定义的变量。</span><span class="sxs-lookup"><span data-stu-id="56e84-104">Parameters are variables that are defined outside [!INCLUDE[esql](../../../../../../includes/esql-md.md)], usually through a binding API that is used by a host language.</span></span> <span data-ttu-id="56e84-105">每个参数都具有名称和类型。</span><span class="sxs-lookup"><span data-stu-id="56e84-105">Each parameter has a name and a type.</span></span> <span data-ttu-id="56e84-106">参数名称在查询表达式中定义，并以 (@) 符号作为前缀。</span><span class="sxs-lookup"><span data-stu-id="56e84-106">Parameter names are defined in query expressions with the at (@) symbol as a prefix.</span></span> <span data-ttu-id="56e84-107">这可以将它们与属性的名称或在查询中定义的其他名称区分开来。</span><span class="sxs-lookup"><span data-stu-id="56e84-107">This disambiguates them from the names of properties or other names that are defined in the query.</span></span>  
  
 <span data-ttu-id="56e84-108">主机语言绑定 API 提供用于绑定参数的 API。</span><span class="sxs-lookup"><span data-stu-id="56e84-108">The host-language binding API provides APIs for binding parameters.</span></span>  
  
## <a name="example"></a><span data-ttu-id="56e84-109">示例</span><span class="sxs-lookup"><span data-stu-id="56e84-109">Example</span></span>  
  
```sql  
SELECT c
      FROM LOB.Customers AS c
      WHERE c.Name = @name  
```  
  
## <a name="see-also"></a><span data-ttu-id="56e84-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="56e84-110">See also</span></span>

- [<span data-ttu-id="56e84-111">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="56e84-111">Entity SQL Reference</span></span>](entity-sql-reference.md)
- [<span data-ttu-id="56e84-112">Entity SQL 概述</span><span class="sxs-lookup"><span data-stu-id="56e84-112">Entity SQL Overview</span></span>](entity-sql-overview.md)
