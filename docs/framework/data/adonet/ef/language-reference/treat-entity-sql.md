---
description: '了解详细信息：处理 (实体 SQL) '
title: TREAT (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 5b77f156-55de-4cb4-8154-87f707d4c635
ms.openlocfilehash: 3f014cac631d246b35d145cdb80c9aa6ac401524
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99673422"
---
# <a name="treat-entity-sql"></a><span data-ttu-id="f5c32-103">TREAT (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="f5c32-103">TREAT (Entity SQL)</span></span>

<span data-ttu-id="f5c32-104">将特定基类型的对象视为指定派生类型的对象。</span><span class="sxs-lookup"><span data-stu-id="f5c32-104">Treats an object of a particular base type as an object of the specified derived type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f5c32-105">语法</span><span class="sxs-lookup"><span data-stu-id="f5c32-105">Syntax</span></span>  
  
```sql  
TREAT ( expression as type)  
```  
  
## <a name="arguments"></a><span data-ttu-id="f5c32-106">参数</span><span class="sxs-lookup"><span data-stu-id="f5c32-106">Arguments</span></span>  

 `expression`  
 <span data-ttu-id="f5c32-107">任何返回实体的有效查询表达式。</span><span class="sxs-lookup"><span data-stu-id="f5c32-107">Any valid query expression that returns an entity.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="f5c32-108">指定表达式的类型必须为指定数据类型的子类型，或者该数据类型必须为表达式的类型的子类型。</span><span class="sxs-lookup"><span data-stu-id="f5c32-108">The type of the specified expression must be a subtype of the specified data type, or the data type must be a subtype of the type of expression.</span></span>  
  
 `type`  
 <span data-ttu-id="f5c32-109">一个实体类型。</span><span class="sxs-lookup"><span data-stu-id="f5c32-109">An entity type.</span></span> <span data-ttu-id="f5c32-110">该类型必须由命名空间进行限定。</span><span class="sxs-lookup"><span data-stu-id="f5c32-110">The type must be qualified by a namespace.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="f5c32-111">指定表达式必须为指定数据类型的子类型，或者该数据类型必须为该表达式的子类型。</span><span class="sxs-lookup"><span data-stu-id="f5c32-111">The specified expression must be a subtype of the specified data type, or the data type must be a subtype of the expression.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f5c32-112">返回值</span><span class="sxs-lookup"><span data-stu-id="f5c32-112">Return Value</span></span>  

 <span data-ttu-id="f5c32-113">一个具有指定数据类型的值。</span><span class="sxs-lookup"><span data-stu-id="f5c32-113">A value of the specified data type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f5c32-114">备注</span><span class="sxs-lookup"><span data-stu-id="f5c32-114">Remarks</span></span>  

 <span data-ttu-id="f5c32-115">TREAT 用于在相关类之间执行向上转换。</span><span class="sxs-lookup"><span data-stu-id="f5c32-115">TREAT is used to perform upcasting between related classes.</span></span> <span data-ttu-id="f5c32-116">例如，如果 `Employee` 派生自 `Person` 且 p 的类型为 `Person`，则 `TREAT(p AS NamespaceName.Employee)` 会将泛型 `Person` 实例向上转换为 `Employee`；即，使您可以将 p 视为 `Employee`。</span><span class="sxs-lookup"><span data-stu-id="f5c32-116">For example, if `Employee` derives from `Person` and p is of type `Person`, `TREAT(p AS NamespaceName.Employee)` upcasts a generic `Person` instance to `Employee`; that is, it allows you to treat p as `Employee`.</span></span>  
  
 <span data-ttu-id="f5c32-117">TREAT 用于可以执行类似于以下查询的继承方案：</span><span class="sxs-lookup"><span data-stu-id="f5c32-117">TREAT is used in inheritance scenarios where you can do a query like the following:</span></span>  
  
```sql  
SELECT TREAT(p AS NamespaceName.Employee)  
FROM ContainerName.Person AS p  
WHERE p IS OF (NamespaceName.Employee)
```  
  
 <span data-ttu-id="f5c32-118">此查询将 `Person` 实体向上转换为 `Employee` 类型。</span><span class="sxs-lookup"><span data-stu-id="f5c32-118">This query upcasts `Person` entities to the `Employee` type.</span></span> <span data-ttu-id="f5c32-119">如果 p 的值的实际类型不是 `Employee`，则表达式会生成值 `null`。</span><span class="sxs-lookup"><span data-stu-id="f5c32-119">If the value of p is not actually of type `Employee`, the expression yields the value `null`.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="f5c32-120">指定的表达式 `Employee` 必须为指定数据类型的子类型 `Person` ，或者该数据类型必须为该表达式的子类型。</span><span class="sxs-lookup"><span data-stu-id="f5c32-120">The specified expression `Employee` must be a subtype of the specified data type `Person`, or the data type must be a subtype of the expression.</span></span> <span data-ttu-id="f5c32-121">否则，表达式会导致编译时错误。</span><span class="sxs-lookup"><span data-stu-id="f5c32-121">Otherwise, the expression will result in a compile-time error.</span></span>  
  
 <span data-ttu-id="f5c32-122">下表显示了 TREAT 在某些典型模式和非常见模式下的行为。</span><span class="sxs-lookup"><span data-stu-id="f5c32-122">The following table shows the behavior of treat over some typical patterns and some less common patterns.</span></span> <span data-ttu-id="f5c32-123">所有异常都在调用提供程序之前从客户端引发：</span><span class="sxs-lookup"><span data-stu-id="f5c32-123">All exceptions are thrown from the client side before the provider gets invoked:</span></span>  
  
|<span data-ttu-id="f5c32-124">模式</span><span class="sxs-lookup"><span data-stu-id="f5c32-124">Pattern</span></span>|<span data-ttu-id="f5c32-125">行为</span><span class="sxs-lookup"><span data-stu-id="f5c32-125">Behavior</span></span>|  
|-------------|--------------|  
|`TREAT (null AS EntityType)`|<span data-ttu-id="f5c32-126">返回 `DbNull`。</span><span class="sxs-lookup"><span data-stu-id="f5c32-126">Returns `DbNull`.</span></span>|  
|`TREAT (null AS ComplexType)`|<span data-ttu-id="f5c32-127">引发异常。</span><span class="sxs-lookup"><span data-stu-id="f5c32-127">Throws an exception.</span></span>|  
|`TREAT (null AS RowType)`|<span data-ttu-id="f5c32-128">引发异常。</span><span class="sxs-lookup"><span data-stu-id="f5c32-128">Throws an exception/</span></span>|  
|`TREAT (EntityType AS EntityType)`|<span data-ttu-id="f5c32-129">返回 `EntityType` 或 `null`。</span><span class="sxs-lookup"><span data-stu-id="f5c32-129">Returns `EntityType` or `null`.</span></span>|  
|`TREAT (ComplexType AS ComplexType)`|<span data-ttu-id="f5c32-130">引发异常。</span><span class="sxs-lookup"><span data-stu-id="f5c32-130">Throws an exception.</span></span>|  
|`TREAT (RowType AS RowType)`|<span data-ttu-id="f5c32-131">引发异常。</span><span class="sxs-lookup"><span data-stu-id="f5c32-131">Throws an exception.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="f5c32-132">示例</span><span class="sxs-lookup"><span data-stu-id="f5c32-132">Example</span></span>  

 <span data-ttu-id="f5c32-133">下面的 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 查询使用 TREAT 运算符将类型为 Course 的对象转换为类型为 OnsiteCourse 的对象的集合。</span><span class="sxs-lookup"><span data-stu-id="f5c32-133">The following [!INCLUDE[esql](../../../../../../includes/esql-md.md)] query uses the TREAT operator to convert an object of the type Course to a collection of objects of the type OnsiteCourse.</span></span> <span data-ttu-id="f5c32-134">该查询基于 [School 模型](/previous-versions/dotnet/netframework-4.0/bb896300(v=vs.100))。</span><span class="sxs-lookup"><span data-stu-id="f5c32-134">The query is based on the [School Model](/previous-versions/dotnet/netframework-4.0/bb896300(v=vs.100)).</span></span>  
  
 [!code-sql[DP EntityServices Concepts#TREAT_ISOF](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#treat_isof)]  
  
## <a name="see-also"></a><span data-ttu-id="f5c32-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="f5c32-135">See also</span></span>

- [<span data-ttu-id="f5c32-136">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="f5c32-136">Entity SQL Reference</span></span>](entity-sql-reference.md)
- [<span data-ttu-id="f5c32-137">可以为 NULL 的结构化类型</span><span class="sxs-lookup"><span data-stu-id="f5c32-137">Nullable Structured Types</span></span>](nullable-structured-types-entity-sql.md)
