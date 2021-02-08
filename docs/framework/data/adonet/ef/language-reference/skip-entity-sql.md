---
description: '了解详细信息：跳过 (实体 SQL) '
title: SKIP (Entity SQL)
ms.date: 03/30/2017
ms.assetid: e2139412-8ea4-451b-8f10-91af18dfa3ec
ms.openlocfilehash: f4924acae6e351e076b5795cf47d63966ebdcb43
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99768007"
---
# <a name="skip-entity-sql"></a><span data-ttu-id="d4c15-103">SKIP (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="d4c15-103">SKIP (Entity SQL)</span></span>

<span data-ttu-id="d4c15-104">在 ORDER BY 子句中使用 SKIP 子子句可执行物理分页。</span><span class="sxs-lookup"><span data-stu-id="d4c15-104">You can perform physical paging by using the SKIP sub-clause in the ORDER BY clause.</span></span> <span data-ttu-id="d4c15-105">SKIP 不能脱离 ORDER BY 子句单独使用。</span><span class="sxs-lookup"><span data-stu-id="d4c15-105">SKIP cannot be used separately from the ORDER BY clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4c15-106">语法</span><span class="sxs-lookup"><span data-stu-id="d4c15-106">Syntax</span></span>

```sql
[ SKIP n ]
```

## <a name="arguments"></a><span data-ttu-id="d4c15-107">参数</span><span class="sxs-lookup"><span data-stu-id="d4c15-107">Arguments</span></span>

`n` \
<span data-ttu-id="d4c15-108">要跳过的项数。</span><span class="sxs-lookup"><span data-stu-id="d4c15-108">The number of items to skip.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4c15-109">备注</span><span class="sxs-lookup"><span data-stu-id="d4c15-109">Remarks</span></span>

<span data-ttu-id="d4c15-110">如果 ORDER BY 子句中存在 SKIP 表达式子子句，则将根据排序规范对结果排序，结果集将包含从紧接着 SKIP 表达式之后的下一行开始的行。</span><span class="sxs-lookup"><span data-stu-id="d4c15-110">If a SKIP expression sub-clause is present in an ORDER BY clause, the results will be sorted according the sort specification and the result set will include rows starting from the next row immediately after the SKIP expression.</span></span> <span data-ttu-id="d4c15-111">例如，SKIP 5 将跳过前五行，并返回第六行以及后续行。</span><span class="sxs-lookup"><span data-stu-id="d4c15-111">For example, SKIP 5 will skip the first five rows and return from the sixth row forward.</span></span>

> [!NOTE]
> <span data-ttu-id="d4c15-112">如果 TOP 修饰符和 SKIP 子子句同时出现在同一个查询表达式中， [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 查询将无效。</span><span class="sxs-lookup"><span data-stu-id="d4c15-112">An [!INCLUDE[esql](../../../../../../includes/esql-md.md)] query is invalid if both the TOP modifier and the SKIP sub-clause are present in the same query expression.</span></span> <span data-ttu-id="d4c15-113">应重写查询，将 TOP 表达式更改为 LIMIT 表达式。</span><span class="sxs-lookup"><span data-stu-id="d4c15-113">The query should be rewritten by changing the TOP expression to the LIMIT expression.</span></span>

> [!NOTE]
> <span data-ttu-id="d4c15-114">在 SQL Server 2000 中，对非键列使用 SKIP 和 ORDER BY 可能会返回不正确的结果。</span><span class="sxs-lookup"><span data-stu-id="d4c15-114">In SQL Server 2000, using SKIP with ORDER BY on non-key columns might return incorrect results.</span></span> <span data-ttu-id="d4c15-115">如果非键列中有重复数据，那么跳过的行数可能多于指定的行数。</span><span class="sxs-lookup"><span data-stu-id="d4c15-115">More than the specified number of rows might be skipped if the non-key column has duplicate data in it.</span></span> <span data-ttu-id="d4c15-116">这是因为如何为 SQL Server 2000 转换 SKIP。</span><span class="sxs-lookup"><span data-stu-id="d4c15-116">This is due to how SKIP is translated for SQL Server 2000.</span></span> <span data-ttu-id="d4c15-117">例如，在下面的代码中，如果 `E.NonKeyColumn` 有重复值，则跳过的行可能超过 5 行：</span><span class="sxs-lookup"><span data-stu-id="d4c15-117">For example, in the following code more than five rows might be skipped if `E.NonKeyColumn` has duplicate values:</span></span>
>
> ```sql
> SELECT [E] FROM Container.EntitySet AS [E] ORDER BY [E].[NonKeyColumn] DESC SKIP 5L
> ```

<span data-ttu-id="d4c15-118">[!INCLUDE[esql](../../../../../../includes/esql-md.md)][如何：对查询结果进行分页](/previous-versions/dotnet/netframework-4.0/bb738702(v=vs.100))的查询使用 ORDER BY 运算符与 SKIP 来指定 SELECT 语句中返回的对象所使用的排序顺序。</span><span class="sxs-lookup"><span data-stu-id="d4c15-118">The [!INCLUDE[esql](../../../../../../includes/esql-md.md)] query in [How to: Page Through Query Results](/previous-versions/dotnet/netframework-4.0/bb738702(v=vs.100)) uses the ORDER BY operator with SKIP to specify the sort order used on objects returned in a SELECT statement.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4c15-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="d4c15-119">See also</span></span>

- [<span data-ttu-id="d4c15-120">ORDER BY</span><span class="sxs-lookup"><span data-stu-id="d4c15-120">ORDER BY</span></span>](order-by-entity-sql.md)
- <span data-ttu-id="d4c15-121">[如何：按页查看查询结果](/previous-versions/dotnet/netframework-4.0/bb738702(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="d4c15-121">[How to: Page Through Query Results](/previous-versions/dotnet/netframework-4.0/bb738702(v=vs.100))</span></span>
- [<span data-ttu-id="d4c15-122">分页</span><span class="sxs-lookup"><span data-stu-id="d4c15-122">Paging</span></span>](paging-entity-sql.md)
- [<span data-ttu-id="d4c15-123">TOP</span><span class="sxs-lookup"><span data-stu-id="d4c15-123">TOP</span></span>](top-entity-sql.md)
