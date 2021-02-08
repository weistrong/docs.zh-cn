---
description: '了解有关以下方面的详细信息：函数 (实体 SQL) '
title: FUNCTION (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 0bb88992-37ed-4991-ace5-55be612a2c4d
ms.openlocfilehash: d61aafce03dc7b82b678f1eb107afb79c6c3ed2f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786311"
---
# <a name="function-entity-sql"></a><span data-ttu-id="b7d10-103">FUNCTION (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="b7d10-103">FUNCTION (Entity SQL)</span></span>

<span data-ttu-id="b7d10-104">在 Entity SQL 查询命令的范围内定义函数。</span><span class="sxs-lookup"><span data-stu-id="b7d10-104">Defines a function in the scope of an Entity SQL query command.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b7d10-105">语法</span><span class="sxs-lookup"><span data-stu-id="b7d10-105">Syntax</span></span>  
  
```sql  
FUNCTION function-name  
( [ { parameter_name <type_definition>
        [ ,...n ]  
  ]  
) AS ( function_expression )
  
<type_definition>::=  
    { data_type | COLLECTION ( <type_definition> )
                | REF ( data_type )
                | ROW ( row_expression )
        }
```  
  
## <a name="arguments"></a><span data-ttu-id="b7d10-106">参数</span><span class="sxs-lookup"><span data-stu-id="b7d10-106">Arguments</span></span>  

 `function-name`  
 <span data-ttu-id="b7d10-107">函数的名称。</span><span class="sxs-lookup"><span data-stu-id="b7d10-107">Name of the function.</span></span>  
  
 `parameter-name`  
 <span data-ttu-id="b7d10-108">函数中参数的名称。</span><span class="sxs-lookup"><span data-stu-id="b7d10-108">Name of a parameter in the function.</span></span>  
  
 `function_expression`  
 <span data-ttu-id="b7d10-109">属于函数的有效 Entity SQL 表达式。</span><span class="sxs-lookup"><span data-stu-id="b7d10-109">A valid Entity SQL expression that is the function.</span></span> <span data-ttu-id="b7d10-110">函数中的命令，可以作用于传递给函数的 `parameter_name` 参数。</span><span class="sxs-lookup"><span data-stu-id="b7d10-110">The command in the function can act on `parameter_name` parameters passed to the function.</span></span>  
  
 `data_type`  
 <span data-ttu-id="b7d10-111">受支持类型的名称。</span><span class="sxs-lookup"><span data-stu-id="b7d10-111">Name of a supported type.</span></span>  
  
 <span data-ttu-id="b7d10-112">集合 ( <type_definition `>` ) </span><span class="sxs-lookup"><span data-stu-id="b7d10-112">COLLECTION ( <type_definition`>` )</span></span>  
 <span data-ttu-id="b7d10-113">一个表达式，返回受支持类型、行或引用的集合。</span><span class="sxs-lookup"><span data-stu-id="b7d10-113">An expression that returns a collection of supported types, rows, or references.</span></span>  
  
 <span data-ttu-id="b7d10-114">引用 **(** `data_type` **)**</span><span class="sxs-lookup"><span data-stu-id="b7d10-114">REF **(**`data_type`**)**</span></span>  
 <span data-ttu-id="b7d10-115">一个表达式，返回对实体类型的引用。</span><span class="sxs-lookup"><span data-stu-id="b7d10-115">An expression that returns a reference to an entity type.</span></span>  
  
 <span data-ttu-id="b7d10-116">行 **(** `row_expression` **)**</span><span class="sxs-lookup"><span data-stu-id="b7d10-116">ROW **(**`row_expression`**)**</span></span>  
 <span data-ttu-id="b7d10-117">一个表达式，从一个或多个值返回结构上类型化的匿名记录。</span><span class="sxs-lookup"><span data-stu-id="b7d10-117">An expression that returns anonymous, structurally typed records from one or more values.</span></span> <span data-ttu-id="b7d10-118">有关更多信息，请参见 [ROW](row-entity-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="b7d10-118">For more information, see [ROW](row-entity-sql.md).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b7d10-119">备注</span><span class="sxs-lookup"><span data-stu-id="b7d10-119">Remarks</span></span>  

 <span data-ttu-id="b7d10-120">可以内联声明具有相同名称的多个函数，只要这些函数的签名不同即可。</span><span class="sxs-lookup"><span data-stu-id="b7d10-120">Multiple functions with the same name can be declared inline, as long as the function signatures are different.</span></span> <span data-ttu-id="b7d10-121">有关详细信息，请参阅 [Function Overload Resolution](function-overload-resolution-entity-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="b7d10-121">For more information, see [Function Overload Resolution](function-overload-resolution-entity-sql.md).</span></span>  
  
 <span data-ttu-id="b7d10-122">只有在 Entity SQL 命令中定义了内联函数后，才可以在该命令中调用内联函数。</span><span class="sxs-lookup"><span data-stu-id="b7d10-122">An inline function can be called in an Entity SQL command only after it has been defined in that command.</span></span> <span data-ttu-id="b7d10-123">但是，在定义被调函数之前或之后，都可以在一个内联函数中调用另一个内联函数。</span><span class="sxs-lookup"><span data-stu-id="b7d10-123">However, an inline function can be called inside another inline function either before or after the called function has been defined.</span></span> <span data-ttu-id="b7d10-124">在下面的示例中，函数 A 在定义函数 B 之前调用函数 B：</span><span class="sxs-lookup"><span data-stu-id="b7d10-124">In the following example, function A calls function B before function B is defined:</span></span>  
  
 `Function A() as ('A calls B. ' + B())`  
  
 `Function B() as ('B was called.')`  
  
 `A()`  
  
 <span data-ttu-id="b7d10-125">有关详细信息，请参阅 [如何：调用用户定义的函数](/previous-versions/dotnet/netframework-4.0/dd490951(v=vs.100))。</span><span class="sxs-lookup"><span data-stu-id="b7d10-125">For more information, see [How to: Call a User-Defined Function](/previous-versions/dotnet/netframework-4.0/dd490951(v=vs.100)).</span></span>  
  
 <span data-ttu-id="b7d10-126">还可以在模型本身中声明函数。</span><span class="sxs-lookup"><span data-stu-id="b7d10-126">Functions can also be declared in the model itself.</span></span> <span data-ttu-id="b7d10-127">在模型中声明的函数的执行方式与在命令中内联声明的函数的执行方式相同。</span><span class="sxs-lookup"><span data-stu-id="b7d10-127">Functions declared in the model are executed in the same way as functions declared inline in the command.</span></span> <span data-ttu-id="b7d10-128">有关详细信息，请参阅 [用户定义函数](user-defined-functions-entity-sql.md)。</span><span class="sxs-lookup"><span data-stu-id="b7d10-128">For more information, see [User-Defined Functions](user-defined-functions-entity-sql.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="b7d10-129">示例</span><span class="sxs-lookup"><span data-stu-id="b7d10-129">Example</span></span>  

 <span data-ttu-id="b7d10-130">下面的 Entity SQL 命令定义一个函数 `Products` ，该函数采用整数值来筛选返回的产品。</span><span class="sxs-lookup"><span data-stu-id="b7d10-130">The following Entity SQL command defines a function `Products` that takes an integer value to filter the returned products.</span></span>  
  
 [!code-sql[DP EntityServices Concepts#FUNCTION1](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#function1)]  
  
## <a name="example"></a><span data-ttu-id="b7d10-131">示例</span><span class="sxs-lookup"><span data-stu-id="b7d10-131">Example</span></span>  

 <span data-ttu-id="b7d10-132">下面的 Entity SQL 命令定义一个函数 `StringReturnsCollection` ，该函数采用字符串集合来筛选返回的联系人。</span><span class="sxs-lookup"><span data-stu-id="b7d10-132">The following Entity SQL command defines a function `StringReturnsCollection` that takes a collection of strings to filter the returned contacts.</span></span>  
  
 [!code-sql[DP EntityServices Concepts#FUNCTION2](~/samples/snippets/tsql/VS_Snippets_Data/dp entityservices concepts/tsql/entitysql.sql#function2)]  
  
## <a name="see-also"></a><span data-ttu-id="b7d10-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="b7d10-133">See also</span></span>

- [<span data-ttu-id="b7d10-134">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="b7d10-134">Entity SQL Reference</span></span>](entity-sql-reference.md)
- [<span data-ttu-id="b7d10-135">Entity SQL 语言</span><span class="sxs-lookup"><span data-stu-id="b7d10-135">Entity SQL Language</span></span>](entity-sql-language.md)
