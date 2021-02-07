---
description: '了解详细信息：行 (实体 SQL) '
title: ROW (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 06da96e8-55d7-486c-991a-4e514d837ff9
ms.openlocfilehash: 2d0bcf3c5be8ef3b67e170af5159ae7dd8744630
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99739269"
---
# <a name="row-entity-sql"></a><span data-ttu-id="737e8-103">ROW (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="737e8-103">ROW (Entity SQL)</span></span>

<span data-ttu-id="737e8-104">从一个或多个值构造结构上类型化的匿名记录。</span><span class="sxs-lookup"><span data-stu-id="737e8-104">Constructs anonymous, structurally typed records from one or more values.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="737e8-105">语法</span><span class="sxs-lookup"><span data-stu-id="737e8-105">Syntax</span></span>  
  
```sql  
ROW ( expression [ AS alias ] [,...] )  
```  
  
## <a name="arguments"></a><span data-ttu-id="737e8-106">参数</span><span class="sxs-lookup"><span data-stu-id="737e8-106">Arguments</span></span>  

 `expression`  
 <span data-ttu-id="737e8-107">任何有效的查询表达式，该表达式返回要在行类型中构造的值。</span><span class="sxs-lookup"><span data-stu-id="737e8-107">Any valid query expression that returns a value to construct in a row type.</span></span>  
  
 `alias`  
 <span data-ttu-id="737e8-108">为在行类型中指定的值指定别名。</span><span class="sxs-lookup"><span data-stu-id="737e8-108">Specifies an alias for the value specified in a row type.</span></span> <span data-ttu-id="737e8-109">如果未提供别名，则 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 会尝试基于 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 别名生成规则来生成别名。</span><span class="sxs-lookup"><span data-stu-id="737e8-109">If an alias is not provided, [!INCLUDE[esql](../../../../../../includes/esql-md.md)] tries to generate an alias based on the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] alias generation rules.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="737e8-110">返回值</span><span class="sxs-lookup"><span data-stu-id="737e8-110">Return Value</span></span>  

 <span data-ttu-id="737e8-111">一个行类型。</span><span class="sxs-lookup"><span data-stu-id="737e8-111">A row type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="737e8-112">备注</span><span class="sxs-lookup"><span data-stu-id="737e8-112">Remarks</span></span>  

 <span data-ttu-id="737e8-113">使用 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 中的行构造函数可以从一个或多个值构造结构上类型化的匿名记录。</span><span class="sxs-lookup"><span data-stu-id="737e8-113">You use row constructors in the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] to construct anonymous, structurally typed records from one or more values.</span></span> <span data-ttu-id="737e8-114">行构造函数的结果类型为行类型，其字段类型对应于用于构造该行的值的类型。</span><span class="sxs-lookup"><span data-stu-id="737e8-114">The result type of a row constructor is a row type whose field types correspond to the types of the values that were used to construct the row.</span></span> <span data-ttu-id="737e8-115">例如，下面的表达式构造一个类型为 `Record(a int, b string, c int)`的值。</span><span class="sxs-lookup"><span data-stu-id="737e8-115">For example, the following expression constructs a value of type `Record(a int, b string, c int)`.</span></span>  
  
```sql  
ROW(1 AS a, "abc" AS b, a+34 AS c)  
```  
  
 <span data-ttu-id="737e8-116">如果没有为行构造函数中的表达式提供别名，则实体框架会尝试生成一个别名。</span><span class="sxs-lookup"><span data-stu-id="737e8-116">If you do not provide an alias for an expression in a row constructor, the Entity Framework will try to generate one.</span></span> <span data-ttu-id="737e8-117">有关更多信息，请参见 [标识符](identifiers-entity-sql.md) 主题中的“别名规则”一节。</span><span class="sxs-lookup"><span data-stu-id="737e8-117">For more information, see the "Aliasing Rules" section of the [Identifiers](identifiers-entity-sql.md) topic.</span></span>  
  
 <span data-ttu-id="737e8-118">以下规则适用于在行构造函数中指定表达式别名：</span><span class="sxs-lookup"><span data-stu-id="737e8-118">The following rules apply to expression aliasing in a row constructor:</span></span>  
  
- <span data-ttu-id="737e8-119">行构造函数中的表达式不能引用同一构造函数中的其他别名。</span><span class="sxs-lookup"><span data-stu-id="737e8-119">Expressions in a row constructor cannot refer to other aliases in the same constructor.</span></span>  
  
- <span data-ttu-id="737e8-120">同一行构造函数中的两个表达式不能具有相同别名。</span><span class="sxs-lookup"><span data-stu-id="737e8-120">Two expressions in the same row constructor cannot have the same alias.</span></span>  
  
 <span data-ttu-id="737e8-121">有关查询构造函数的详细信息，请参阅 [构造类型](constructing-types-entity-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="737e8-121">For more information about query constructors, see [Constructing Types](constructing-types-entity-sql.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="737e8-122">示例</span><span class="sxs-lookup"><span data-stu-id="737e8-122">Example</span></span>  

 <span data-ttu-id="737e8-123">下面的 Entity SQL 查询使用 ROW 运算符构造结构上类型化的匿名记录。</span><span class="sxs-lookup"><span data-stu-id="737e8-123">The following Entity SQL query uses the ROW operator to construct anonymous, structurally typed records.</span></span> <span data-ttu-id="737e8-124">此查询基于 AdventureWorks 销售模型。</span><span class="sxs-lookup"><span data-stu-id="737e8-124">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="737e8-125">若要编译并运行此查询，请执行下列步骤：</span><span class="sxs-lookup"><span data-stu-id="737e8-125">To compile and run this query, follow these steps:</span></span>  
  
1. <span data-ttu-id="737e8-126">执行 [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md)中的过程。</span><span class="sxs-lookup"><span data-stu-id="737e8-126">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2. <span data-ttu-id="737e8-127">将以下查询作为参数传递给 `ExecuteStructuralTypeQuery` 方法：</span><span class="sxs-lookup"><span data-stu-id="737e8-127">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-sql[DP EntityServices Concepts#ROW](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#row)]  
  
## <a name="see-also"></a><span data-ttu-id="737e8-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="737e8-128">See also</span></span>

- [<span data-ttu-id="737e8-129">构造类型</span><span class="sxs-lookup"><span data-stu-id="737e8-129">Constructing Types</span></span>](constructing-types-entity-sql.md)
- [<span data-ttu-id="737e8-130">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="737e8-130">Entity SQL Reference</span></span>](entity-sql-reference.md)
- [<span data-ttu-id="737e8-131">类型定义</span><span class="sxs-lookup"><span data-stu-id="737e8-131">Type Definitions</span></span>](type-definitions-entity-sql.md)
