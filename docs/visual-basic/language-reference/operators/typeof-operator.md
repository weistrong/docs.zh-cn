---
description: '详细了解： TypeOf 运算符 (Visual Basic) '
title: TypeOf 运算符
ms.date: 07/20/2015
f1_keywords:
- TypeOf
- vb.TypeOf
helpviewer_keywords:
- types [Visual Basic], compatible
- comparison operators [Visual Basic]
- TypeOf...Is expression
- data types [Visual Basic], compatible
- TypeOf operator [Visual Basic]
- compatible data types [Visual Basic]
ms.assetid: 33f65296-659a-4b9a-9a29-c2a91cff68b2
ms.openlocfilehash: 59a03095b2abbaa304221b30402b9a058954db63
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99795230"
---
# <a name="typeof-operator-visual-basic"></a><span data-ttu-id="ae742-103">TypeOf 运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ae742-103">TypeOf Operator (Visual Basic)</span></span>

<span data-ttu-id="ae742-104">检查表达式的结果的运行时类型是否与指定的类型兼容。</span><span class="sxs-lookup"><span data-stu-id="ae742-104">Checks whether the runtime type of an expression's result is type-compatible with the specified type.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ae742-105">语法</span><span class="sxs-lookup"><span data-stu-id="ae742-105">Syntax</span></span>  
  
```vb  
result = TypeOf objectexpression Is typename  
```  
  
```vb  
result = TypeOf objectexpression IsNot typename  
```  
  
## <a name="parts"></a><span data-ttu-id="ae742-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="ae742-106">Parts</span></span>  

 `result`  
 <span data-ttu-id="ae742-107">返回。</span><span class="sxs-lookup"><span data-stu-id="ae742-107">Returned.</span></span> <span data-ttu-id="ae742-108">一个 `Boolean` 值。</span><span class="sxs-lookup"><span data-stu-id="ae742-108">A `Boolean` value.</span></span>  
  
 `objectexpression`  
 <span data-ttu-id="ae742-109">必需。</span><span class="sxs-lookup"><span data-stu-id="ae742-109">Required.</span></span> <span data-ttu-id="ae742-110">计算结果为引用类型的任何表达式。</span><span class="sxs-lookup"><span data-stu-id="ae742-110">Any expression that evaluates to a reference type.</span></span>  
  
 `typename`  
 <span data-ttu-id="ae742-111">必需。</span><span class="sxs-lookup"><span data-stu-id="ae742-111">Required.</span></span> <span data-ttu-id="ae742-112">任何数据类型名。</span><span class="sxs-lookup"><span data-stu-id="ae742-112">Any data type name.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ae742-113">备注</span><span class="sxs-lookup"><span data-stu-id="ae742-113">Remarks</span></span>  

 <span data-ttu-id="ae742-114">`TypeOf` 运算符确定 `objectexpression` 的运行时类型是否与 `typename` 兼容。</span><span class="sxs-lookup"><span data-stu-id="ae742-114">The `TypeOf` operator determines whether the run-time type of `objectexpression` is compatible with `typename`.</span></span> <span data-ttu-id="ae742-115">兼容性取决于 `typename` 的类型类别。</span><span class="sxs-lookup"><span data-stu-id="ae742-115">The compatibility depends on the type category of `typename`.</span></span> <span data-ttu-id="ae742-116">下表显示如何确定兼容性。</span><span class="sxs-lookup"><span data-stu-id="ae742-116">The following table shows how compatibility is determined.</span></span>  
  
|<span data-ttu-id="ae742-117">`typename` 的类型类别</span><span class="sxs-lookup"><span data-stu-id="ae742-117">Type category of `typename`</span></span>|<span data-ttu-id="ae742-118">兼容性条件</span><span class="sxs-lookup"><span data-stu-id="ae742-118">Compatibility criterion</span></span>|  
|---------------------------------|-----------------------------|  
|<span data-ttu-id="ae742-119">实例</span><span class="sxs-lookup"><span data-stu-id="ae742-119">Class</span></span>|<span data-ttu-id="ae742-120">`objectexpression` 属于类型 `typename` 或继承自 `typename`</span><span class="sxs-lookup"><span data-stu-id="ae742-120">`objectexpression` is of type `typename` or inherits from `typename`</span></span>|  
|<span data-ttu-id="ae742-121">结构</span><span class="sxs-lookup"><span data-stu-id="ae742-121">Structure</span></span>|<span data-ttu-id="ae742-122">`objectexpression` 属于类型 `typename`</span><span class="sxs-lookup"><span data-stu-id="ae742-122">`objectexpression` is of type `typename`</span></span>|  
|<span data-ttu-id="ae742-123">接口</span><span class="sxs-lookup"><span data-stu-id="ae742-123">Interface</span></span>|<span data-ttu-id="ae742-124">`objectexpression` 实现 `typename` 或继承自实现 `typename` 的类</span><span class="sxs-lookup"><span data-stu-id="ae742-124">`objectexpression` implements `typename` or inherits from a class that implements `typename`</span></span>|  
  
 <span data-ttu-id="ae742-125">如果 `objectexpression` 的运行时类型满足兼容性条件，则 `result` 是 `True`。</span><span class="sxs-lookup"><span data-stu-id="ae742-125">If the run-time type of `objectexpression` satisfies the compatibility criterion, `result` is `True`.</span></span> <span data-ttu-id="ae742-126">否则 `result` 为 `False`。</span><span class="sxs-lookup"><span data-stu-id="ae742-126">Otherwise, `result` is `False`.</span></span>  <span data-ttu-id="ae742-127">如果 `objectexpression` 为 null，则 `TypeOf`...`Is` 返回 `False`，...`IsNot` 返回 `True`。</span><span class="sxs-lookup"><span data-stu-id="ae742-127">If `objectexpression` is null, then `TypeOf`...`Is` returns `False`, and ...`IsNot` returns `True`.</span></span>  
  
 <span data-ttu-id="ae742-128">`TypeOf` 始终与 `Is` 关键字一起使用来构造 `TypeOf`...`Is` 表达式，或与 `IsNot` 关键字一起使用来构造 `TypeOf`...`IsNot` 表达式。</span><span class="sxs-lookup"><span data-stu-id="ae742-128">`TypeOf` is always used with the `Is` keyword to construct a `TypeOf`...`Is` expression, or with the `IsNot` keyword to construct a `TypeOf`...`IsNot` expression.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ae742-129">示例</span><span class="sxs-lookup"><span data-stu-id="ae742-129">Example</span></span>  

 <span data-ttu-id="ae742-130">下面的示例使用 `TypeOf`...`Is` 表达式测试具有不同数据类型的两个对象引用变量的类型兼容性。</span><span class="sxs-lookup"><span data-stu-id="ae742-130">The following example uses `TypeOf`...`Is` expressions to test the type compatibility of two object reference variables with various data types.</span></span>  
  
 [!code-vb[VbVbalrOperators#39](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#39)]  
  
 <span data-ttu-id="ae742-131">变量 `refInteger` 具有运行时类型 `Integer`。</span><span class="sxs-lookup"><span data-stu-id="ae742-131">The variable `refInteger` has a run-time type of `Integer`.</span></span> <span data-ttu-id="ae742-132">它与 `Integer` 兼容，但不与 `Double` 兼容。</span><span class="sxs-lookup"><span data-stu-id="ae742-132">It is compatible with `Integer` but not with `Double`.</span></span> <span data-ttu-id="ae742-133">变量 `refForm` 具有运行时类型 <xref:System.Windows.Forms.Form>。</span><span class="sxs-lookup"><span data-stu-id="ae742-133">The variable `refForm` has a run-time type of <xref:System.Windows.Forms.Form>.</span></span> <span data-ttu-id="ae742-134">它与 <xref:System.Windows.Forms.Form> 兼容因为这是其类型，与 <xref:System.Windows.Forms.Control> 兼容因为 <xref:System.Windows.Forms.Form> 继承自 <xref:System.Windows.Forms.Control>，与 <xref:System.ComponentModel.IComponent> 兼容因为 <xref:System.Windows.Forms.Form> 继承自 <xref:System.ComponentModel.Component>（它实现 <xref:System.ComponentModel.IComponent>）。</span><span class="sxs-lookup"><span data-stu-id="ae742-134">It is compatible with <xref:System.Windows.Forms.Form> because that is its type, with <xref:System.Windows.Forms.Control> because <xref:System.Windows.Forms.Form> inherits from <xref:System.Windows.Forms.Control>, and with <xref:System.ComponentModel.IComponent> because <xref:System.Windows.Forms.Form> inherits from <xref:System.ComponentModel.Component>, which implements <xref:System.ComponentModel.IComponent>.</span></span> <span data-ttu-id="ae742-135">但是，`refForm` 与 <xref:System.Windows.Forms.Label> 不兼容。</span><span class="sxs-lookup"><span data-stu-id="ae742-135">However, `refForm` is not compatible with <xref:System.Windows.Forms.Label>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae742-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="ae742-136">See also</span></span>

- [<span data-ttu-id="ae742-137">Is 运算符</span><span class="sxs-lookup"><span data-stu-id="ae742-137">Is Operator</span></span>](is-operator.md)
- [<span data-ttu-id="ae742-138">IsNot 运算符</span><span class="sxs-lookup"><span data-stu-id="ae742-138">IsNot Operator</span></span>](isnot-operator.md)
- [<span data-ttu-id="ae742-139">Comparison Operators in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="ae742-139">Comparison Operators in Visual Basic</span></span>](../../programming-guide/language-features/operators-and-expressions/comparison-operators.md)
- [<span data-ttu-id="ae742-140">Visual Basic 中的运算符优先级</span><span class="sxs-lookup"><span data-stu-id="ae742-140">Operator Precedence in Visual Basic</span></span>](operator-precedence.md)
- [<span data-ttu-id="ae742-141">按功能列出的运算符</span><span class="sxs-lookup"><span data-stu-id="ae742-141">Operators Listed by Functionality</span></span>](operators-listed-by-functionality.md)
- [<span data-ttu-id="ae742-142">运算符和表达式</span><span class="sxs-lookup"><span data-stu-id="ae742-142">Operators and Expressions</span></span>](../../programming-guide/language-features/operators-and-expressions/index.md)
