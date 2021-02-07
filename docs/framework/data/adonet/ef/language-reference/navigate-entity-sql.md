---
description: '了解详细信息：导航 (实体 SQL) '
title: NAVIGATE (Entity SQL)
ms.date: 03/30/2017
ms.assetid: f107f29d-005f-4e39-a898-17f163abb1d0
ms.openlocfilehash: 7fa39a988429fe0a658b01078d2369ad4767f4a7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99696498"
---
# <a name="navigate-entity-sql"></a><span data-ttu-id="5e7ea-103">NAVIGATE (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="5e7ea-103">NAVIGATE (Entity SQL)</span></span>

<span data-ttu-id="5e7ea-104">导航实体之间建立的关系。</span><span class="sxs-lookup"><span data-stu-id="5e7ea-104">Navigates over the relationship established between entities.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e7ea-105">语法</span><span class="sxs-lookup"><span data-stu-id="5e7ea-105">Syntax</span></span>

```sql
navigate(instance-expression, [relationship-type], [to-end [, from-end] ])
```

## <a name="arguments"></a><span data-ttu-id="5e7ea-106">参数</span><span class="sxs-lookup"><span data-stu-id="5e7ea-106">Arguments</span></span>

<span data-ttu-id="5e7ea-107">`instance-expression` 实体的实例。</span><span class="sxs-lookup"><span data-stu-id="5e7ea-107">`instance-expression` An instance of an entity.</span></span>

<span data-ttu-id="5e7ea-108">`relationship-type` 关系的类型名称，从概念架构定义语言 (CSDL) 文件。</span><span class="sxs-lookup"><span data-stu-id="5e7ea-108">`relationship-type` The type name of the relationship, from the conceptual schema definition language (CSDL) file.</span></span> <span data-ttu-id="5e7ea-109">`relationship-type`限定为 \<namespace> 。 \<relationship type name></span><span class="sxs-lookup"><span data-stu-id="5e7ea-109">The `relationship-type` is qualified as \<namespace>.\<relationship type name>.</span></span>

<span data-ttu-id="5e7ea-110">`to` 关系的结束。</span><span class="sxs-lookup"><span data-stu-id="5e7ea-110">`to` The end of the relationship.</span></span>

<span data-ttu-id="5e7ea-111">`from` 关系的开头。</span><span class="sxs-lookup"><span data-stu-id="5e7ea-111">`from` The beginning of the relationship.</span></span>

## <a name="return-value"></a><span data-ttu-id="5e7ea-112">返回值</span><span class="sxs-lookup"><span data-stu-id="5e7ea-112">Return Value</span></span>

<span data-ttu-id="5e7ea-113">如果结束端的基数为 1，返回值将为 `Ref<T>`。</span><span class="sxs-lookup"><span data-stu-id="5e7ea-113">If the cardinality of the to end is 1, the return value will be `Ref<T>`.</span></span> <span data-ttu-id="5e7ea-114">如果结束端的基数为 n，返回值将为 `Collection<Ref<T>>`。</span><span class="sxs-lookup"><span data-stu-id="5e7ea-114">If the cardinality of the to end is n, the return value will be `Collection<Ref<T>>`.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e7ea-115">备注</span><span class="sxs-lookup"><span data-stu-id="5e7ea-115">Remarks</span></span>

<span data-ttu-id="5e7ea-116">关系是实体数据模型 (EDM) 中的第一类构造。</span><span class="sxs-lookup"><span data-stu-id="5e7ea-116">Relationships are first-class constructs in the Entity Data Model (EDM).</span></span> <span data-ttu-id="5e7ea-117">可以在两个或更多实体类型之间建立关系，用户可以通过关系从一端（实体）导航到另一端。</span><span class="sxs-lookup"><span data-stu-id="5e7ea-117">Relationships can be established between two or more entity types, and users can navigate over the relationship from one end (entity) to another.</span></span> <span data-ttu-id="5e7ea-118">当关系中的名称解析没有歧义时，`from` 和 `to` 为有条件可选。</span><span class="sxs-lookup"><span data-stu-id="5e7ea-118">`from` and `to` are conditionally optional when there is no ambiguity in name resolution within the relationship.</span></span>

<span data-ttu-id="5e7ea-119">NAVIGATE 在 O 和 C 空间中有效。</span><span class="sxs-lookup"><span data-stu-id="5e7ea-119">NAVIGATE is valid in O and C space.</span></span>

<span data-ttu-id="5e7ea-120">导航构造的常规形式如下：</span><span class="sxs-lookup"><span data-stu-id="5e7ea-120">The general form of a navigation construct is the following:</span></span>

<span data-ttu-id="5e7ea-121">navigate(`instance-expression`, `relationship-type`, [ `to-end` [, `from-end` ] ] )</span><span class="sxs-lookup"><span data-stu-id="5e7ea-121">navigate(`instance-expression`, `relationship-type`, [ `to-end` [, `from-end` ] ] )</span></span>

<span data-ttu-id="5e7ea-122">例如：</span><span class="sxs-lookup"><span data-stu-id="5e7ea-122">For example:</span></span>

```sql
Select o.Id, navigate(o, OrderCustomer, Customer, Order)
From LOB.Orders as o
```

<span data-ttu-id="5e7ea-123">其中 OrderCustomer 为 `relationship`，Customer 和 Order 为关系的 `to-end` （客户）和 `from-end` （订单）。</span><span class="sxs-lookup"><span data-stu-id="5e7ea-123">Where OrderCustomer is the `relationship`, and Customer and Order are the `to-end` (customer) and `from-end` (order) of the relationship.</span></span> <span data-ttu-id="5e7ea-124">如果 OrderCustomer 是 n：1关系，那么导航表达式的结果类型为 Ref \<Customer> 。</span><span class="sxs-lookup"><span data-stu-id="5e7ea-124">If OrderCustomer was a n:1 relationship, then the result type of the navigate expression is Ref\<Customer>.</span></span>

<span data-ttu-id="5e7ea-125">此表达式的简单形式如下：</span><span class="sxs-lookup"><span data-stu-id="5e7ea-125">The simpler form of this expression is the following:</span></span>

```sql
Select o.Id, navigate(o, OrderCustomer)
From LOB.Orders as o
```

<span data-ttu-id="5e7ea-126">同样，在以下形式的查询中，导航表达式会生成<引用> 的集合 \<Order> 。</span><span class="sxs-lookup"><span data-stu-id="5e7ea-126">Similarly, in a query of the following form, The navigate expression would produce a Collection<Ref\<Order>>.</span></span>

```sql
Select c.Id, navigate(c, OrderCustomer, Order, Customer)
From LOB.Customers as c
```

<span data-ttu-id="5e7ea-127">实例表达式必须为 entity/ref 类型。</span><span class="sxs-lookup"><span data-stu-id="5e7ea-127">The instance-expression must be an entity/ref type.</span></span>

## <a name="example"></a><span data-ttu-id="5e7ea-128">示例</span><span class="sxs-lookup"><span data-stu-id="5e7ea-128">Example</span></span>

<span data-ttu-id="5e7ea-129">下面的 Entity SQL 查询使用 NAVIGATE 运算符来导航建立在 Address 和 SalesOrderHeader 实体类型之间的关系。</span><span class="sxs-lookup"><span data-stu-id="5e7ea-129">The following Entity SQL query uses the NAVIGATE operator to navigate over the relationship established between Address and SalesOrderHeader entity types.</span></span> <span data-ttu-id="5e7ea-130">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="5e7ea-130">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="5e7ea-131">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="5e7ea-131">To compile and run this query, follow these steps:</span></span>

1. <span data-ttu-id="5e7ea-132">执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="5e7ea-132">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>

2. <span data-ttu-id="5e7ea-133">将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="5e7ea-133">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>

 [!code-sql[DP EntityServices Concepts#NAVIGATE](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#navigate)]

## <a name="see-also"></a><span data-ttu-id="5e7ea-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="5e7ea-134">See also</span></span>

- [<span data-ttu-id="5e7ea-135">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="5e7ea-135">Entity SQL Reference</span></span>](entity-sql-reference.md)
- [<span data-ttu-id="5e7ea-136">如何：使用导航运算符导航关系</span><span class="sxs-lookup"><span data-stu-id="5e7ea-136">How to: Navigate Relationships with Navigate Operator</span></span>](navigate-entity-sql.md)
