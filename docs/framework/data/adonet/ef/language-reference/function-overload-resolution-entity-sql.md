---
description: '了解更多相关信息：函数重载决策 (实体 SQL) '
title: 函数重载解析 (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 9c648054-3808-4a69-9d3e-98e6a4f9c5ca
ms.openlocfilehash: 8fbe0b54ed559d1f962c3e916d25554e0de65737
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786324"
---
# <a name="function-overload-resolution-entity-sql"></a><span data-ttu-id="4d323-103">函数重载解析 (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="4d323-103">Function Overload Resolution (Entity SQL)</span></span>

<span data-ttu-id="4d323-104">本主题描述如何解析 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 函数。</span><span class="sxs-lookup"><span data-stu-id="4d323-104">This topic describes how [!INCLUDE[esql](../../../../../../includes/esql-md.md)] functions are resolved.</span></span>  
  
 <span data-ttu-id="4d323-105">可以使用相同的名称定义一个以上的函数，只要这些函数具有唯一的签名即可。</span><span class="sxs-lookup"><span data-stu-id="4d323-105">More than one function can be defined with the same name, as long as the functions have unique signatures.</span></span>  
  
 <span data-ttu-id="4d323-106">在发生这种情况时，必须应用下面的条件来确定给定的表达式引用哪个函数。</span><span class="sxs-lookup"><span data-stu-id="4d323-106">When this is the case, the following criteria must be applied to determine which function is referenced by a given expression.</span></span> <span data-ttu-id="4d323-107">这些条件是按顺序应用的。</span><span class="sxs-lookup"><span data-stu-id="4d323-107">These criteria are applied in sequence.</span></span> <span data-ttu-id="4d323-108">第一个仅适用于单个函数的条件所对应的函数就是所解析的函数。</span><span class="sxs-lookup"><span data-stu-id="4d323-108">The first criterion that applies only to a single function is the resolved function.</span></span>  
  
1. <span data-ttu-id="4d323-109">**参数编号**。</span><span class="sxs-lookup"><span data-stu-id="4d323-109">**Parameter number**.</span></span> <span data-ttu-id="4d323-110">函数在表达式中指定了相同个数的参数。</span><span class="sxs-lookup"><span data-stu-id="4d323-110">The function has the same number of parameters specified in the expression.</span></span>  
  
2. <span data-ttu-id="4d323-111">**类型完全匹配**。</span><span class="sxs-lookup"><span data-stu-id="4d323-111">**Exact match on type**.</span></span> <span data-ttu-id="4d323-112">函数的每个自变量类型都严格匹配参数类型，或为 null 字面值。</span><span class="sxs-lookup"><span data-stu-id="4d323-112">Each argument type of the function exactly matches the parameter type, or is the null literal.</span></span>  
  
3. <span data-ttu-id="4d323-113">**子类型上的匹配**。</span><span class="sxs-lookup"><span data-stu-id="4d323-113">**Match on subtype**.</span></span> <span data-ttu-id="4d323-114">函数的每个自变量类型都严格匹配参数类型或为参数类型的子类型，或为 null 字面值。</span><span class="sxs-lookup"><span data-stu-id="4d323-114">Each argument type of the function exactly matches or is a sub-type of the parameter type, or the argument is the null literal.</span></span> <span data-ttu-id="4d323-115">如果多个函数的唯一区别是所需的子类型转换的个数，则子类型转换个数最小的函数就是所解析的函数。</span><span class="sxs-lookup"><span data-stu-id="4d323-115">In the event that several functions differ only in the number of sub-type conversions required, the function with the least number of sub-type conversions is the resolved function.</span></span>  
  
4. <span data-ttu-id="4d323-116">**子类型或类型升级的匹配项**。</span><span class="sxs-lookup"><span data-stu-id="4d323-116">**Match on subtype or type promotion**.</span></span> <span data-ttu-id="4d323-117">函数的每个实参类型都严格匹配形参类型，或为形参类型的子类型，或可以提升到形参类型，或为 null 字面值。</span><span class="sxs-lookup"><span data-stu-id="4d323-117">Each argument type of the function exactly matches, is a sub-type of, or can be promoted to the parameter type, or the argument is the null literal.</span></span> <span data-ttu-id="4d323-118">同样，如果多个函数的唯一区别是子类型转换和提升的个数，则子类型转换和提升个数最小的函数就是所解析的函数。</span><span class="sxs-lookup"><span data-stu-id="4d323-118">Again, in the event that several functions differ only in the number of sub-type conversions and promotions, the function with the least number of sub-type conversions and promotions is the resolved function.</span></span>  
  
 <span data-ttu-id="4d323-119">如果上述任何条件都无法导致选择单个函数，则函数调用表达式具有多义性。</span><span class="sxs-lookup"><span data-stu-id="4d323-119">If none of these criteria result in a single function being selected, the function invocation expression is ambiguous.</span></span>  
  
 <span data-ttu-id="4d323-120">即使可以使用上述规则推断出单个函数，实参仍然可能不匹配形参。</span><span class="sxs-lookup"><span data-stu-id="4d323-120">Even if a single function can be extracted using these rules, the arguments still might not match the parameters.</span></span> <span data-ttu-id="4d323-121">在这种情况下，将引发错误。</span><span class="sxs-lookup"><span data-stu-id="4d323-121">An error is raised in this case.</span></span>  
  
 <span data-ttu-id="4d323-122">对于用户定义的函数，内联查询函数的定义将优先，即使当模型定义的函数存在且具有一个更适合用户定义函数的签名也不例外。</span><span class="sxs-lookup"><span data-stu-id="4d323-122">For user-defined functions, the definition for an inline query function takes precedence even when a model-defined function exists with a signature that is a better match for the user-defined function.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4d323-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="4d323-123">See also</span></span>

- [<span data-ttu-id="4d323-124">实体 SQL 引用</span><span class="sxs-lookup"><span data-stu-id="4d323-124">Entity SQL Reference</span></span>](entity-sql-reference.md)
- [<span data-ttu-id="4d323-125">Entity SQL 概述</span><span class="sxs-lookup"><span data-stu-id="4d323-125">Entity SQL Overview</span></span>](entity-sql-overview.md)
- [<span data-ttu-id="4d323-126">函数</span><span class="sxs-lookup"><span data-stu-id="4d323-126">Functions</span></span>](functions-entity-sql.md)
