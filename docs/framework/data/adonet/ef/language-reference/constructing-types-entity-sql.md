---
description: '了解详细信息：构造类型 (实体 SQL) '
title: 构造类型 (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 41fa7bde-8d20-4a3f-a3d2-fb791e128010
ms.openlocfilehash: 5963c34ffd8e9273d400cc16ba93f72ded2ede46
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99724838"
---
# <a name="constructing-types-entity-sql"></a><span data-ttu-id="e4c4b-103">构造类型 (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="e4c4b-103">Constructing Types (Entity SQL)</span></span>

<!-- markdownlint-disable DOCSMD001 -->
[!INCLUDE[esql](../../../../../../includes/esql-md.md)] <span data-ttu-id="e4c4b-104">提供了三种构造函数：行构造函数、命名类型构造函数和集合构造函数。</span><span class="sxs-lookup"><span data-stu-id="e4c4b-104">provides three kinds of constructors: row constructors, named type constructors, and collection constructors.</span></span>

## <a name="row-constructors"></a><span data-ttu-id="e4c4b-105">行构造函数</span><span class="sxs-lookup"><span data-stu-id="e4c4b-105">Row Constructors</span></span>

<span data-ttu-id="e4c4b-106">使用 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 中的行构造函数可以从一个或多个值构造结构上类型化的匿名记录。</span><span class="sxs-lookup"><span data-stu-id="e4c4b-106">You use row constructors in [!INCLUDE[esql](../../../../../../includes/esql-md.md)] to construct anonymous, structurally typed records from one or more values.</span></span> <span data-ttu-id="e4c4b-107">行构造函数的结果类型为行类型，其字段类型对应于用于构造该行的值的类型。</span><span class="sxs-lookup"><span data-stu-id="e4c4b-107">The result type of a row constructor is a row type whose field types correspond to the types of the values used to construct the row.</span></span> <span data-ttu-id="e4c4b-108">例如，下面的表达式构造一个类型为的值 `Record(a int, b string, c int)` ：</span><span class="sxs-lookup"><span data-stu-id="e4c4b-108">For example, the following expression constructs a value of type `Record(a int, b string, c int)`:</span></span>

`ROW(1 AS a, "abc" AS b, a + 34 AS c)`

<span data-ttu-id="e4c4b-109">如果没有为行构造函数中的表达式提供别名，则实体框架会尝试生成一个别名。</span><span class="sxs-lookup"><span data-stu-id="e4c4b-109">If you do not provide an alias for an expression in a row constructor, the Entity Framework will try to generate one.</span></span> <span data-ttu-id="e4c4b-110">有关详细信息，请参阅 [标识符](identifiers-entity-sql.md)中的 "别名规则" 一节。</span><span class="sxs-lookup"><span data-stu-id="e4c4b-110">For more information, see the "Aliasing Rules" section in [Identifiers](identifiers-entity-sql.md).</span></span>

<span data-ttu-id="e4c4b-111">以下规则适用于在行构造函数中指定表达式别名：</span><span class="sxs-lookup"><span data-stu-id="e4c4b-111">The following rules apply to expression aliasing in a row constructor:</span></span>

- <span data-ttu-id="e4c4b-112">行构造函数中的表达式不能引用同一构造函数中的其他别名。</span><span class="sxs-lookup"><span data-stu-id="e4c4b-112">Expressions in a row constructor cannot refer to other aliases in the same constructor.</span></span>
- <span data-ttu-id="e4c4b-113">同一行构造函数中的两个表达式不能具有相同别名。</span><span class="sxs-lookup"><span data-stu-id="e4c4b-113">Two expressions in the same row constructor cannot have the same alias.</span></span>

<span data-ttu-id="e4c4b-114">有关行构造函数的详细信息，请参阅 [row](row-entity-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="e4c4b-114">For more information about row constructors, see [ROW](row-entity-sql.md).</span></span>

## <a name="collection-constructors"></a><span data-ttu-id="e4c4b-115">集合构造函数</span><span class="sxs-lookup"><span data-stu-id="e4c4b-115">Collection Constructors</span></span>

<span data-ttu-id="e4c4b-116">使用 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 中的集合构造函数可以从值列表创建多重集实例。</span><span class="sxs-lookup"><span data-stu-id="e4c4b-116">You use collection constructors in [!INCLUDE[esql](../../../../../../includes/esql-md.md)] to create an instance of a multiset from a list of values.</span></span> <span data-ttu-id="e4c4b-117">该构造函数中的所有值都必须为互兼容的 `T` 类型，并且该构造函数生成 `Multiset<T>` 类型的集合。</span><span class="sxs-lookup"><span data-stu-id="e4c4b-117">All the values in the constructor must be of mutually compatible type `T`, and the constructor produces a collection of type `Multiset<T>`.</span></span> <span data-ttu-id="e4c4b-118">例如，下面的表达式创建整数集合：</span><span class="sxs-lookup"><span data-stu-id="e4c4b-118">For example, the following expression creates a collection of integers:</span></span>

`Multiset(1, 2, 3)`

`{1, 2, 3}`

<span data-ttu-id="e4c4b-119">因为无法确定元素类型，所以不能使用空的多重集构造函数。</span><span class="sxs-lookup"><span data-stu-id="e4c4b-119">Empty multiset constructors are not allowed because the type of the elements cannot be determined.</span></span> <span data-ttu-id="e4c4b-120">下面的表达式无效：</span><span class="sxs-lookup"><span data-stu-id="e4c4b-120">The following is not valid:</span></span>

`multiset() {}`

<span data-ttu-id="e4c4b-121">有关详细信息，请参阅 [多重集](multiset-entity-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="e4c4b-121">For more information, see [MULTISET](multiset-entity-sql.md).</span></span>

## <a name="named-type-constructors-namedtype-initializers"></a><span data-ttu-id="e4c4b-122">命名类型构造函数（NamedType 初始值设定项）</span><span class="sxs-lookup"><span data-stu-id="e4c4b-122">Named Type Constructors (NamedType Initializers)</span></span>

[!INCLUDE[esql](../../../../../../includes/esql-md.md)] <span data-ttu-id="e4c4b-123">允许类型构造函数（初始值设定项）创建命名复杂类型和命名实体类型的实例。</span><span class="sxs-lookup"><span data-stu-id="e4c4b-123">allows type constructors (initializers) to create instances of named complex types and entity types.</span></span> <span data-ttu-id="e4c4b-124">例如，下面的表达式创建 `Person` 类型的实例。</span><span class="sxs-lookup"><span data-stu-id="e4c4b-124">For example, the following expression creates an instance of a `Person` type.</span></span>

`Person("abc", 12)`

<span data-ttu-id="e4c4b-125">下面的表达式创建复杂类型的实例。</span><span class="sxs-lookup"><span data-stu-id="e4c4b-125">The following expression creates an instance of a complex type.</span></span>

`MyModel.ZipCode(‘98118’, ‘4567’)`

<span data-ttu-id="e4c4b-126">下面的表达式创建嵌套复杂类型的实例。</span><span class="sxs-lookup"><span data-stu-id="e4c4b-126">The following expression creates an instance of a nested complex type.</span></span>

`MyModel.AddressInfo('My street address', 'Seattle', 'WA', MyModel.ZipCode('98118', '4567'))`

<span data-ttu-id="e4c4b-127">下面的表达式创建具有嵌套复杂类型的实体的实例。</span><span class="sxs-lookup"><span data-stu-id="e4c4b-127">The following expression creates an instance of an entity with a nested complex type.</span></span>

`MyModel.Person("Bill", MyModel.AddressInfo('My street address', 'Seattle', 'WA', MyModel.ZipCode('98118', '4567')))`

<span data-ttu-id="e4c4b-128">下面的示例演示如何将复杂类型的属性初始化为 null。</span><span class="sxs-lookup"><span data-stu-id="e4c4b-128">The following example shows how to initialize a property of a complex type to null.</span></span> `MyModel.ZipCode(‘98118’, null)`

<span data-ttu-id="e4c4b-129">假定该构造函数的参数的顺序与该类型的属性的声明顺序相同。</span><span class="sxs-lookup"><span data-stu-id="e4c4b-129">The arguments to the constructor are assumed to be in the same order as the declaration of the attributes of the type.</span></span>

<span data-ttu-id="e4c4b-130">有关详细信息，请参阅 [命名类型构造函数](named-type-constructor-entity-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="e4c4b-130">For more information, see [Named Type Constructor](named-type-constructor-entity-sql.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e4c4b-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="e4c4b-131">See also</span></span>

- [<span data-ttu-id="e4c4b-132">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="e4c4b-132">Entity SQL Reference</span></span>](entity-sql-reference.md)
- [<span data-ttu-id="e4c4b-133">Entity SQL 概述</span><span class="sxs-lookup"><span data-stu-id="e4c4b-133">Entity SQL Overview</span></span>](entity-sql-overview.md)
- [<span data-ttu-id="e4c4b-134">类型系统</span><span class="sxs-lookup"><span data-stu-id="e4c4b-134">Type System</span></span>](type-system-entity-sql.md)
