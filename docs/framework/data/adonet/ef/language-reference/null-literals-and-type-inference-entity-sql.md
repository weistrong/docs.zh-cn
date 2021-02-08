---
description: '了解详细信息： (实体 SQL 的 Null 文本和类型推理) '
title: Null 文本和类型推理 (Entity SQL)
ms.date: 03/30/2017
ms.assetid: edd56afb-af1b-4e7d-b210-cb8998143426
ms.openlocfilehash: 3b3474ea9841a34970d2269173d263fda2eb1789
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802133"
---
# <a name="null-literals-and-type-inference-entity-sql"></a><span data-ttu-id="8faf2-103">Null 文本和类型推理 (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="8faf2-103">Null Literals and Type Inference (Entity SQL)</span></span>

<span data-ttu-id="8faf2-104">Null 文本与 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 类型系统中的任何类型都兼容。</span><span class="sxs-lookup"><span data-stu-id="8faf2-104">Null literals are compatible with any type in the [!INCLUDE[esql](../../../../../../includes/esql-md.md)] type system.</span></span> <span data-ttu-id="8faf2-105">但是，为了正确进行 Null 文本类型推理，[!INCLUDE[esql](../../../../../../includes/esql-md.md)] 对何处可以使用 Null 文本实施某些约束。</span><span class="sxs-lookup"><span data-stu-id="8faf2-105">However, for the type of a null literal to be inferred correctly, [!INCLUDE[esql](../../../../../../includes/esql-md.md)] imposes certain constraints on where a null literal can be used.</span></span>  
  
## <a name="typed-nulls"></a><span data-ttu-id="8faf2-106">类型化 Null</span><span class="sxs-lookup"><span data-stu-id="8faf2-106">Typed Nulls</span></span>  

 <span data-ttu-id="8faf2-107">类型化 Null 可以在任意位置使用。</span><span class="sxs-lookup"><span data-stu-id="8faf2-107">Typed nulls can be used anywhere.</span></span> <span data-ttu-id="8faf2-108">类型化 Null 是已知的，因此不需要类型推理。</span><span class="sxs-lookup"><span data-stu-id="8faf2-108">Type inference is not required for typed nulls because the type is known.</span></span> <span data-ttu-id="8faf2-109">例如，使用下面的 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 构造可以构造 Int16 类型的 Null。</span><span class="sxs-lookup"><span data-stu-id="8faf2-109">For example, you can construct a null of type Int16 with the following [!INCLUDE[esql](../../../../../../includes/esql-md.md)] construct:</span></span>  
  
 `(cast(null as Int16))`  
  
## <a name="free-floating-null-literals"></a><span data-ttu-id="8faf2-110">自由浮动 Null 文本</span><span class="sxs-lookup"><span data-stu-id="8faf2-110">Free-Floating Null Literals</span></span>  

 <span data-ttu-id="8faf2-111">自由浮动 Null 文本的用法如下：</span><span class="sxs-lookup"><span data-stu-id="8faf2-111">Free-floating null literals can be used in the following contexts:</span></span>  
  
- <span data-ttu-id="8faf2-112">用作 CAST 或 TREAT 表达式的自变量。</span><span class="sxs-lookup"><span data-stu-id="8faf2-112">As an argument to a CAST or TREAT expression.</span></span> <span data-ttu-id="8faf2-113">建议用这种方式生成类型化 Null 表达式。</span><span class="sxs-lookup"><span data-stu-id="8faf2-113">This is the recommended way to produce a typed null expression.</span></span>  
  
- <span data-ttu-id="8faf2-114">用作方法或函数的参数。</span><span class="sxs-lookup"><span data-stu-id="8faf2-114">As an argument to a method or a function.</span></span> <span data-ttu-id="8faf2-115">标准重载规则适用。</span><span class="sxs-lookup"><span data-stu-id="8faf2-115">Standard overload rules apply.</span></span>  
  
- <span data-ttu-id="8faf2-116">用作算术表达式（例如 +、- 或 /）的一个参数。</span><span class="sxs-lookup"><span data-stu-id="8faf2-116">As one of the arguments to an arithmetic expression such as +, -, or /.</span></span> <span data-ttu-id="8faf2-117">其他自变量不能为 Null 文本，否则不能进行类型推理。</span><span class="sxs-lookup"><span data-stu-id="8faf2-117">The other arguments cannot be null literals, otherwise type inference is not possible.</span></span>  
  
- <span data-ttu-id="8faf2-118">用作逻辑表达式（AND、OR 或 NOT）的任何自变量。</span><span class="sxs-lookup"><span data-stu-id="8faf2-118">As any of the arguments to a logical expression (AND, OR, or NOT).</span></span> <span data-ttu-id="8faf2-119">所有自变量都已知为类型 Boolean。</span><span class="sxs-lookup"><span data-stu-id="8faf2-119">All the arguments are known to be of type Boolean.</span></span>  
  
- <span data-ttu-id="8faf2-120">用作 IS NULL 或 IS NOT NULL 表达式的参数。</span><span class="sxs-lookup"><span data-stu-id="8faf2-120">As the argument to an IS NULL or IS NOT NULL expression.</span></span>  
  
- <span data-ttu-id="8faf2-121">用作 LIKE 表达式的一个或多个自变量。</span><span class="sxs-lookup"><span data-stu-id="8faf2-121">As one or more of the arguments to a LIKE expression.</span></span> <span data-ttu-id="8faf2-122">所有参数都应为字符串。</span><span class="sxs-lookup"><span data-stu-id="8faf2-122">All arguments are expected to be strings.</span></span>  
  
- <span data-ttu-id="8faf2-123">用作命名类型构造函数的一个或多个自变量。</span><span class="sxs-lookup"><span data-stu-id="8faf2-123">As one or more of the arguments to a named-type constructor.</span></span>  
  
- <span data-ttu-id="8faf2-124">用作多集构造函数的一个或多个自变量。</span><span class="sxs-lookup"><span data-stu-id="8faf2-124">As one or more of the arguments to a multiset constructor.</span></span> <span data-ttu-id="8faf2-125">多集构造函数至少有一个自变量必须为非 Null 文本的表达式。</span><span class="sxs-lookup"><span data-stu-id="8faf2-125">At least one argument to the multiset constructor must be an expression that is not a null literal.</span></span>  
  
- <span data-ttu-id="8faf2-126">用作 CASE 表达式中的一个或多个 THEN 或 ELSE 表达式。</span><span class="sxs-lookup"><span data-stu-id="8faf2-126">As one or more of the THEN or ELSE expressions in a CASE expression.</span></span> <span data-ttu-id="8faf2-127">CASE 表达式中至少有一个 THEN 或 ELSE 表达式必须为非 Null 文本的表达式。</span><span class="sxs-lookup"><span data-stu-id="8faf2-127">At least one of the THEN or ELSE expressions in the CASE expression must be an expression other than a null literal.</span></span>  
  
 <span data-ttu-id="8faf2-128">其他情况下不能使用自由浮动 Null 文本。</span><span class="sxs-lookup"><span data-stu-id="8faf2-128">Free-floating null literals cannot be used in other scenarios.</span></span> <span data-ttu-id="8faf2-129">例如，它们不能用作行构造函数的自变量。</span><span class="sxs-lookup"><span data-stu-id="8faf2-129">For example,  they cannot be used as arguments to a row constructor.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8faf2-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="8faf2-130">See also</span></span>

- [<span data-ttu-id="8faf2-131">Entity SQL 概述</span><span class="sxs-lookup"><span data-stu-id="8faf2-131">Entity SQL Overview</span></span>](entity-sql-overview.md)
