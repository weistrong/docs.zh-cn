---
description: 了解更多：不支持的表达式
title: 不支持的表达式 (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 5e79da7e-e78a-413c-8fb0-f3f9cd84f579
dev_langs:
- sql
ms.openlocfilehash: ceb57dc78f9685a79de987d15f7fd57a583b75a0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99673292"
---
# <a name="unsupported-expressions"></a><span data-ttu-id="4aeef-103">不支持的表达式</span><span class="sxs-lookup"><span data-stu-id="4aeef-103">Unsupported expressions</span></span>

<span data-ttu-id="4aeef-104">本主题介绍中不支持的 Transact-sql 表达式 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 。</span><span class="sxs-lookup"><span data-stu-id="4aeef-104">This topic describes Transact-SQL expressions that are not supported in [!INCLUDE[esql](../../../../../../includes/esql-md.md)].</span></span> <span data-ttu-id="4aeef-105">有关详细信息，请参阅 [实体 SQL 与 transact-sql 的不同之处](how-entity-sql-differs-from-transact-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="4aeef-105">For more information, see [How Entity SQL Differs from Transact-SQL](how-entity-sql-differs-from-transact-sql.md).</span></span>

## <a name="quantified-predicates"></a><span data-ttu-id="4aeef-106">量化谓词</span><span class="sxs-lookup"><span data-stu-id="4aeef-106">Quantified predicates</span></span>

<span data-ttu-id="4aeef-107">Transact-sql 允许构造以下形式：</span><span class="sxs-lookup"><span data-stu-id="4aeef-107">Transact-SQL allows constructs of the following form:</span></span>

```sql
sal > all (select salary from employees)
sal > any (select salary from employees)
```

<span data-ttu-id="4aeef-108">但 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 不支持此这样的构造。</span><span class="sxs-lookup"><span data-stu-id="4aeef-108">[!INCLUDE[esql](../../../../../../includes/esql-md.md)], however, does not support such constructs.</span></span> <span data-ttu-id="4aeef-109">在 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 中的等效表达式可以写为如下形式：</span><span class="sxs-lookup"><span data-stu-id="4aeef-109">Equivalent expressions can be written in [!INCLUDE[esql](../../../../../../includes/esql-md.md)] as follows:</span></span>

```sql
not exists(select 0 from employees as e where sal <= e.salary)
exists(select 0 from employees as e where sal > e.salary)
```

## <a name="-operator"></a><span data-ttu-id="4aeef-110">\* 运算符</span><span class="sxs-lookup"><span data-stu-id="4aeef-110">\* operator</span></span>

<span data-ttu-id="4aeef-111">Transact-sql 支持在 SELECT 子句中使用 \* 运算符，以指示应提取所有列。这在中不受支持 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 。</span><span class="sxs-lookup"><span data-stu-id="4aeef-111">Transact-SQL supports the use of the \* operator in the SELECT clause to indicate that all columns should be projected out. This is not supported in [!INCLUDE[esql](../../../../../../includes/esql-md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="4aeef-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="4aeef-112">See also</span></span>

- [<span data-ttu-id="4aeef-113">Entity SQL 概述</span><span class="sxs-lookup"><span data-stu-id="4aeef-113">Entity SQL Overview</span></span>](entity-sql-overview.md)
- [<span data-ttu-id="4aeef-114">Entity SQL 与 Transact-SQL 有何不同</span><span class="sxs-lookup"><span data-stu-id="4aeef-114">How Entity SQL Differs from Transact-SQL</span></span>](how-entity-sql-differs-from-transact-sql.md)
