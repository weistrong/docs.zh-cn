---
description: '了解详细信息：类型定义 (实体 SQL) '
title: 类型定义 (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 306b204a-ade5-47ef-95b5-c785d2da4a7e
ms.openlocfilehash: e5a66ed9ea456733bab9c68d96ef5c176dad5651
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99673409"
---
# <a name="type-definitions-entity-sql"></a><span data-ttu-id="7bbba-103">类型定义 (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="7bbba-103">Type Definitions (Entity SQL)</span></span>

<span data-ttu-id="7bbba-104">类型定义用在 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 内联函数的声明语句中。</span><span class="sxs-lookup"><span data-stu-id="7bbba-104">A type definition is used in the declaration statement of an [!INCLUDE[esql](../../../../../../includes/esql-md.md)] Inline function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7bbba-105">备注</span><span class="sxs-lookup"><span data-stu-id="7bbba-105">Remarks</span></span>  

 <span data-ttu-id="7bbba-106">内联函数的声明语句包含 [函数](function-entity-sql.md) 关键字，后跟表示函数名称的标识符 (例如，"MyAvg" ) 后跟括号中的参数定义列表 (例如，"拥有的集合 (Decimal) " ) 。</span><span class="sxs-lookup"><span data-stu-id="7bbba-106">The declaration statement for an inline function consists of the [FUNCTION](function-entity-sql.md) keyword followed by the identifier representing the function name (for example, "MyAvg") followed by a parameter definition list in parenthesis (for example, "dues Collection(Decimal)").</span></span>  
  
 <span data-ttu-id="7bbba-107">参数定义列表由零个或多个参数定义组成。</span><span class="sxs-lookup"><span data-stu-id="7bbba-107">The parameter definition list consists of zero or more parameter definitions.</span></span> <span data-ttu-id="7bbba-108">每个参数定义均由一个标识符（该函数的参数的名称，例如“dues”）后跟类型定义（例如，“Collection(Decimal)”）组成。</span><span class="sxs-lookup"><span data-stu-id="7bbba-108">Each parameter definition consists of an identifier (the name of the parameter to the function, for example, "dues") followed by a type definition (for example, "Collection(Decimal)").</span></span>  
  
 <span data-ttu-id="7bbba-109">类型定义可以为以下任一情况：</span><span class="sxs-lookup"><span data-stu-id="7bbba-109">The type definitions can be either:</span></span>  
  
- <span data-ttu-id="7bbba-110">标识符的类型（例如，“Int32”或“AdventureWorks.Order”）。</span><span class="sxs-lookup"><span data-stu-id="7bbba-110">The type of the identifier (for example, "Int32" or "AdventureWorks.Order").</span></span>  
  
- <span data-ttu-id="7bbba-111">关键字 `COLLECTION` 后跟放在括号中的另一个类型定义（例如，“Collection(AdventureWorks.Order)”）。</span><span class="sxs-lookup"><span data-stu-id="7bbba-111">The keyword `COLLECTION` followed by another type definition in parenthesis (for example, "Collection(AdventureWorks.Order)").</span></span>  
  
- <span data-ttu-id="7bbba-112">关键字 ROW 后跟放在括号中的属性定义列表（例如，“Row(x AdventureWorks.Order)”）。</span><span class="sxs-lookup"><span data-stu-id="7bbba-112">The keyword ROW followed by a list of property definitions in parenthesis (for example, "Row(x AdventureWorks.Order)").</span></span> <span data-ttu-id="7bbba-113">属性定义具有格式，如 " `identifier type_definition` ， `identifier type_definition` ，..."。</span><span class="sxs-lookup"><span data-stu-id="7bbba-113">Property definitions have a format such as "`identifier type_definition`, `identifier type_definition`, ...".</span></span>  
  
- <span data-ttu-id="7bbba-114">关键字 REF 后跟放在括号中的标识符类型（例如，“Ref(AdventureWorks.Order)”）。</span><span class="sxs-lookup"><span data-stu-id="7bbba-114">The keyword REF followed by the type of the identifier in parenthesis (for example, "Ref(AdventureWorks.Order)").</span></span> <span data-ttu-id="7bbba-115">REF 类型定义运算符要求将实体类型作为自变量。</span><span class="sxs-lookup"><span data-stu-id="7bbba-115">The REF type definition operator requires an entity type as the argument.</span></span> <span data-ttu-id="7bbba-116">您不能指定基元类型作为参数。</span><span class="sxs-lookup"><span data-stu-id="7bbba-116">You cannot specify a primitive type as the argument.</span></span>  
  
 <span data-ttu-id="7bbba-117">还可以嵌套类型定义（例如，“Collection(Row(x Ref(AdventureWorks.Order)))”）。</span><span class="sxs-lookup"><span data-stu-id="7bbba-117">You can also nest type definitions (for example, "Collection(Row(x Ref(AdventureWorks.Order)))").</span></span>  
  
 <span data-ttu-id="7bbba-118">类型定义选项为：</span><span class="sxs-lookup"><span data-stu-id="7bbba-118">The type definition options are:</span></span>  
  
- <span data-ttu-id="7bbba-119">`IdentifierName supported_type` 或</span><span class="sxs-lookup"><span data-stu-id="7bbba-119">`IdentifierName supported_type`, or</span></span>  
  
- <span data-ttu-id="7bbba-120">`IdentifierName` COLLECTION(`type_definition`) 或</span><span class="sxs-lookup"><span data-stu-id="7bbba-120">`IdentifierName` COLLECTION(`type_definition`), or</span></span>  
  
- <span data-ttu-id="7bbba-121">`IdentifierName` ROW(`property_definition`) 或</span><span class="sxs-lookup"><span data-stu-id="7bbba-121">`IdentifierName` ROW(`property_definition`), or</span></span>  
  
- <span data-ttu-id="7bbba-122">`IdentifierName` REF(`supported_entity_type`)</span><span class="sxs-lookup"><span data-stu-id="7bbba-122">`IdentifierName` REF(`supported_entity_type`)</span></span>  
  
 <span data-ttu-id="7bbba-123">属性定义选项为 `IdentifierName type_definition`。</span><span class="sxs-lookup"><span data-stu-id="7bbba-123">The property definition option is `IdentifierName type_definition`.</span></span>  
  
 <span data-ttu-id="7bbba-124">支持的类型为当前命名空间中的任何类型。</span><span class="sxs-lookup"><span data-stu-id="7bbba-124">Supported types are any types in the current namespace.</span></span> <span data-ttu-id="7bbba-125">它们包括基元类型和实体类型。</span><span class="sxs-lookup"><span data-stu-id="7bbba-125">These include both primitive and entity types.</span></span>  
  
 <span data-ttu-id="7bbba-126">支持的实体类型仅仅是当前命名空间中的实体类型。</span><span class="sxs-lookup"><span data-stu-id="7bbba-126">Supported entity types refer to only entity types in the current namespace.</span></span> <span data-ttu-id="7bbba-127">而不包括基元类型。</span><span class="sxs-lookup"><span data-stu-id="7bbba-127">They do not include primitive types.</span></span>  
  
## <a name="examples"></a><span data-ttu-id="7bbba-128">示例</span><span class="sxs-lookup"><span data-stu-id="7bbba-128">Examples</span></span>  

 <span data-ttu-id="7bbba-129">下面是一个简单类型定义的示例。</span><span class="sxs-lookup"><span data-stu-id="7bbba-129">The following is an example of a simple type definition.</span></span>  
  
```sql  
USING Microsoft.Samples.Entity  
Function MyRound(p1 EDM.Decimal) AS (  
   Round(p1)  
)  
MyRound(CAST(1.7 as EDM.Decimal))  
```  
  
 <span data-ttu-id="7bbba-130">下面是 COLLECTION 类型定义的示例。</span><span class="sxs-lookup"><span data-stu-id="7bbba-130">The following is an example of a COLLECTION type definition.</span></span>  
  
```sql  
USING Microsoft.Samples.Entity  
Function MyRound(p1 Collection(EDM.Decimal)) AS (  
   Select Round(p1) from p1  
)  
MyRound({CAST(1.7 as EDM.Decimal), CAST(2.7 as EDM.Decimal)})  
```  
  
 <span data-ttu-id="7bbba-131">下面是 ROW 类型定义的示例。</span><span class="sxs-lookup"><span data-stu-id="7bbba-131">The following is an example of a ROW type definition.</span></span>  
  
```sql  
USING Microsoft.Samples.Entity  
Function MyRound(p1 Row(x EDM.Decimal)) AS (  
   Round(p1.x)  
)  
select MyRound(row(a as x)) from {CAST(1.7 as EDM.Decimal), CAST(2.7 as EDM.Decimal)} as a  
```  
  
 <span data-ttu-id="7bbba-132">下面是 REF 类型定义的示例。</span><span class="sxs-lookup"><span data-stu-id="7bbba-132">The following is an example of a REF type definition.</span></span>  
  
```sql  
USING Microsoft.Samples.Entity  
Function UnReference(p1 Ref(AdventureWorks.Order)) AS (  
   Deref(p1)  
)  
select Ref(x) from AdventureWorksEntities.SalesOrderHeaders as x  
```  
  
## <a name="see-also"></a><span data-ttu-id="7bbba-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="7bbba-133">See also</span></span>

- [<span data-ttu-id="7bbba-134">Entity SQL 概述</span><span class="sxs-lookup"><span data-stu-id="7bbba-134">Entity SQL Overview</span></span>](entity-sql-overview.md)
- [<span data-ttu-id="7bbba-135">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="7bbba-135">Entity SQL Reference</span></span>](entity-sql-reference.md)
