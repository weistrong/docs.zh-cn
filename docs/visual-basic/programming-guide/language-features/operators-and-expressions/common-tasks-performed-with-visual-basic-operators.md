---
description: 了解更多：通过 Visual Basic 运算符执行的常见任务
title: 使用 Visual Basic 运算符执行的常规任务
ms.date: 07/20/2015
helpviewer_keywords:
- operators [Visual Basic], logical
- operators [Visual Basic], string concatenation
- operators [Visual Basic], bitwise
- operators [Visual Basic], bit-shift
- operators [Visual Basic], arithmetic
- operators [Visual Basic], string comparison
- operators [Visual Basic], concatenation
- Visual Basic code, operators
- operators [Visual Basic], comparison
- operators [Visual Basic], short-circuiting logical
ms.assetid: d181afe5-fafa-460f-a13b-81203f6f4587
ms.openlocfilehash: 5103241c7c92ffe7264178e9abb6a56ba03d4b52
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100465257"
---
# <a name="common-tasks-performed-with-visual-basic-operators"></a><span data-ttu-id="a4ca0-103">使用 Visual Basic 运算符执行的常规任务</span><span class="sxs-lookup"><span data-stu-id="a4ca0-103">Common Tasks Performed with Visual Basic Operators</span></span>

<span data-ttu-id="a4ca0-104">运算符执行涉及一个或多个称为 *操作数* 的表达式的许多常见任务。</span><span class="sxs-lookup"><span data-stu-id="a4ca0-104">Operators perform many common tasks involving one or more expressions called *operands*.</span></span>  
  
## <a name="arithmetic-and-bit-shift-tasks"></a><span data-ttu-id="a4ca0-105">算术和移位任务</span><span class="sxs-lookup"><span data-stu-id="a4ca0-105">Arithmetic and Bit-shift Tasks</span></span>  

 <span data-ttu-id="a4ca0-106">下表总结了可用的算术和移位运算。</span><span class="sxs-lookup"><span data-stu-id="a4ca0-106">The following table summarizes the available arithmetic and bit-shift operations.</span></span>  
  
|<span data-ttu-id="a4ca0-107">功能</span><span class="sxs-lookup"><span data-stu-id="a4ca0-107">To</span></span>|<span data-ttu-id="a4ca0-108">查看</span><span class="sxs-lookup"><span data-stu-id="a4ca0-108">See</span></span>|  
|---|---|  
|<span data-ttu-id="a4ca0-109">向另一个数值添加一个数值</span><span class="sxs-lookup"><span data-stu-id="a4ca0-109">Add one numeric value to another</span></span>|[<span data-ttu-id="a4ca0-110">+ 运算符</span><span class="sxs-lookup"><span data-stu-id="a4ca0-110">+ Operator</span></span>](../../../language-reference/operators/addition-operator.md)|  
|<span data-ttu-id="a4ca0-111">从一个数值中减去另一个数值</span><span class="sxs-lookup"><span data-stu-id="a4ca0-111">Subtract one numeric value from another</span></span>|[<span data-ttu-id="a4ca0-112">- 运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a4ca0-112">- Operator (Visual Basic)</span></span>](../../../language-reference/operators/subtraction-operator.md)|  
|<span data-ttu-id="a4ca0-113">反转数值的符号</span><span class="sxs-lookup"><span data-stu-id="a4ca0-113">Reverse the sign of a numeric value</span></span>|[<span data-ttu-id="a4ca0-114">- 运算符 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="a4ca0-114">- Operator (Visual Basic)</span></span>](../../../language-reference/operators/subtraction-operator.md)|  
|<span data-ttu-id="a4ca0-115">将一个数值乘以另一个数值</span><span class="sxs-lookup"><span data-stu-id="a4ca0-115">Multiply one numeric value by another</span></span>|[<span data-ttu-id="a4ca0-116">\* 运算符</span><span class="sxs-lookup"><span data-stu-id="a4ca0-116">\* Operator</span></span>](../../../language-reference/operators/multiplication-operator.md)|  
|<span data-ttu-id="a4ca0-117">将一个数值除以另一个数值</span><span class="sxs-lookup"><span data-stu-id="a4ca0-117">Divide one numeric value into another</span></span>|[<span data-ttu-id="a4ca0-118">/Operator (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="a4ca0-118">/ Operator (Visual Basic)</span></span>](../../../language-reference/operators/floating-point-division-operator.md)|  
|<span data-ttu-id="a4ca0-119">查找一个数值除以另 (一个数值的商，而不包含余数) </span><span class="sxs-lookup"><span data-stu-id="a4ca0-119">Find the quotient of one numeric value divided by another (without the remainder)</span></span>|[<span data-ttu-id="a4ca0-120">\ 运算符 (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="a4ca0-120">\ Operator (Visual Basic)</span></span>](../../../language-reference/operators/integer-division-operator.md)|  
|<span data-ttu-id="a4ca0-121">查找一个数值除以另一个数值相除后的余数 (不包含商) </span><span class="sxs-lookup"><span data-stu-id="a4ca0-121">Find the remainder of one numeric value divided by another (without the quotient)</span></span>|[<span data-ttu-id="a4ca0-122">Mod 运算符</span><span class="sxs-lookup"><span data-stu-id="a4ca0-122">Mod Operator</span></span>](../../../language-reference/operators/mod-operator.md)|  
|<span data-ttu-id="a4ca0-123">向一个数值增加另一个数值</span><span class="sxs-lookup"><span data-stu-id="a4ca0-123">Raise one numeric value to the power of another</span></span>|[<span data-ttu-id="a4ca0-124">^ 运算符</span><span class="sxs-lookup"><span data-stu-id="a4ca0-124">^ Operator</span></span>](../../../language-reference/operators/exponentiation-operator.md)|  
|<span data-ttu-id="a4ca0-125">将数值的位模式向左移动</span><span class="sxs-lookup"><span data-stu-id="a4ca0-125">Shift the bit pattern of a numeric value to the left</span></span>|[<span data-ttu-id="a4ca0-126"><\< 操作员</span><span class="sxs-lookup"><span data-stu-id="a4ca0-126"><\< Operator</span></span>](../../../language-reference/operators/left-shift-operator.md)|  
|<span data-ttu-id="a4ca0-127">将数值的位模式向右移位</span><span class="sxs-lookup"><span data-stu-id="a4ca0-127">Shift the bit pattern of a numeric value to the right</span></span>|[<span data-ttu-id="a4ca0-128">>> 运算符</span><span class="sxs-lookup"><span data-stu-id="a4ca0-128">>> Operator</span></span>](../../../language-reference/operators/right-shift-operator.md)|  
  
## <a name="comparison-tasks"></a><span data-ttu-id="a4ca0-129">比较任务</span><span class="sxs-lookup"><span data-stu-id="a4ca0-129">Comparison Tasks</span></span>  

 <span data-ttu-id="a4ca0-130">下表总结了可用的比较运算。</span><span class="sxs-lookup"><span data-stu-id="a4ca0-130">The following table summarizes the available comparison operations.</span></span>  
  
|<span data-ttu-id="a4ca0-131">功能</span><span class="sxs-lookup"><span data-stu-id="a4ca0-131">To</span></span>|<span data-ttu-id="a4ca0-132">查看</span><span class="sxs-lookup"><span data-stu-id="a4ca0-132">See</span></span>|  
|---|---|  
|<span data-ttu-id="a4ca0-133">确定两个值是否相等</span><span class="sxs-lookup"><span data-stu-id="a4ca0-133">Determine whether two values are equal</span></span>|<span data-ttu-id="a4ca0-134">`=` 运算符 [在 Visual Basic 中 (比较运算符](comparison-operators.md)) </span><span class="sxs-lookup"><span data-stu-id="a4ca0-134">`=` Operator ([Comparison Operators in Visual Basic](comparison-operators.md))</span></span>|  
|<span data-ttu-id="a4ca0-135">确定两个值是否不相等</span><span class="sxs-lookup"><span data-stu-id="a4ca0-135">Determine whether two values are unequal</span></span>|<span data-ttu-id="a4ca0-136">`<>` 运算符 [在 Visual Basic 中 (比较运算符](comparison-operators.md)) </span><span class="sxs-lookup"><span data-stu-id="a4ca0-136">`<>` Operator ([Comparison Operators in Visual Basic](comparison-operators.md))</span></span>|  
|<span data-ttu-id="a4ca0-137">确定一个值是否小于另一个值</span><span class="sxs-lookup"><span data-stu-id="a4ca0-137">Determine whether one value is less than another</span></span>|<span data-ttu-id="a4ca0-138">`<` 运算符 [在 Visual Basic 中 (比较运算符](comparison-operators.md)) </span><span class="sxs-lookup"><span data-stu-id="a4ca0-138">`<` Operator ([Comparison Operators in Visual Basic](comparison-operators.md))</span></span>|  
|<span data-ttu-id="a4ca0-139">确定一个值是否大于另一个值</span><span class="sxs-lookup"><span data-stu-id="a4ca0-139">Determine whether one value is greater than another</span></span>|<span data-ttu-id="a4ca0-140">`>` 运算符 [在 Visual Basic 中 (比较运算符](comparison-operators.md)) </span><span class="sxs-lookup"><span data-stu-id="a4ca0-140">`>` Operator ([Comparison Operators in Visual Basic](comparison-operators.md))</span></span>|  
|<span data-ttu-id="a4ca0-141">确定一个值是否小于或等于另一个值</span><span class="sxs-lookup"><span data-stu-id="a4ca0-141">Determine whether one value is less than or equal to another</span></span>|<span data-ttu-id="a4ca0-142">`<=` 运算符 [在 Visual Basic 中 (比较运算符](comparison-operators.md)) </span><span class="sxs-lookup"><span data-stu-id="a4ca0-142">`<=` Operator ([Comparison Operators in Visual Basic](comparison-operators.md))</span></span>|  
|<span data-ttu-id="a4ca0-143">确定一个值是否大于或等于另一个值</span><span class="sxs-lookup"><span data-stu-id="a4ca0-143">Determine whether one value is greater than or equal to another</span></span>|<span data-ttu-id="a4ca0-144">`>=` 运算符 [在 Visual Basic 中 (比较运算符](comparison-operators.md)) </span><span class="sxs-lookup"><span data-stu-id="a4ca0-144">`>=` Operator ([Comparison Operators in Visual Basic](comparison-operators.md))</span></span>|  
|<span data-ttu-id="a4ca0-145">确定两个对象变量是否引用相同的对象实例</span><span class="sxs-lookup"><span data-stu-id="a4ca0-145">Determine whether two object variables refer to the same object instance</span></span>|[<span data-ttu-id="a4ca0-146">Is 运算符</span><span class="sxs-lookup"><span data-stu-id="a4ca0-146">Is Operator</span></span>](../../../language-reference/operators/is-operator.md)|  
|<span data-ttu-id="a4ca0-147">确定两个对象变量是否引用不同的对象实例</span><span class="sxs-lookup"><span data-stu-id="a4ca0-147">Determine whether two object variables refer to different object instances</span></span>|[<span data-ttu-id="a4ca0-148">IsNot 运算符</span><span class="sxs-lookup"><span data-stu-id="a4ca0-148">IsNot Operator</span></span>](../../../language-reference/operators/isnot-operator.md)|  
|<span data-ttu-id="a4ca0-149">确定对象是否为特定类型</span><span class="sxs-lookup"><span data-stu-id="a4ca0-149">Determine whether an object is of a specific type</span></span>|[<span data-ttu-id="a4ca0-150">TypeOf 运算符</span><span class="sxs-lookup"><span data-stu-id="a4ca0-150">TypeOf Operator</span></span>](../../../language-reference/operators/typeof-operator.md)|  
  
## <a name="concatenation-tasks"></a><span data-ttu-id="a4ca0-151">串联任务</span><span class="sxs-lookup"><span data-stu-id="a4ca0-151">Concatenation Tasks</span></span>  

 <span data-ttu-id="a4ca0-152">下表总结了可用的串联运算。</span><span class="sxs-lookup"><span data-stu-id="a4ca0-152">The following table summarizes the available concatenation operations.</span></span>  
  
|<span data-ttu-id="a4ca0-153">功能</span><span class="sxs-lookup"><span data-stu-id="a4ca0-153">To</span></span>|<span data-ttu-id="a4ca0-154">查看</span><span class="sxs-lookup"><span data-stu-id="a4ca0-154">See</span></span>|  
|---|---|  
|<span data-ttu-id="a4ca0-155">将多个字符串联接为一个字符串</span><span class="sxs-lookup"><span data-stu-id="a4ca0-155">Join multiple strings into a single string</span></span>|<span data-ttu-id="a4ca0-156">`&` 运算符 [在 Visual Basic 中 (串联运算符](concatenation-operators.md)) </span><span class="sxs-lookup"><span data-stu-id="a4ca0-156">`&` Operator ([Concatenation Operators in Visual Basic](concatenation-operators.md))</span></span>|  
|<span data-ttu-id="a4ca0-157">用字符串值联接数值</span><span class="sxs-lookup"><span data-stu-id="a4ca0-157">Join numeric values with string values</span></span>|<span data-ttu-id="a4ca0-158">`+` 运算符 [在 Visual Basic 中 (串联运算符](concatenation-operators.md)) </span><span class="sxs-lookup"><span data-stu-id="a4ca0-158">`+` Operator ([Concatenation Operators in Visual Basic](concatenation-operators.md))</span></span>|  
  
## <a name="logical-and-bitwise-tasks"></a><span data-ttu-id="a4ca0-159">逻辑和按位任务</span><span class="sxs-lookup"><span data-stu-id="a4ca0-159">Logical and Bitwise Tasks</span></span>  

 <span data-ttu-id="a4ca0-160">下表总结了可用的逻辑和按位运算。</span><span class="sxs-lookup"><span data-stu-id="a4ca0-160">The following table summarizes the available logical and bitwise operations.</span></span>  
  
|<span data-ttu-id="a4ca0-161">功能</span><span class="sxs-lookup"><span data-stu-id="a4ca0-161">To</span></span>|<span data-ttu-id="a4ca0-162">查看</span><span class="sxs-lookup"><span data-stu-id="a4ca0-162">See</span></span>|  
|---|---|  
|<span data-ttu-id="a4ca0-163">对布尔值执行逻辑非运算</span><span class="sxs-lookup"><span data-stu-id="a4ca0-163">Perform logical negation on a Boolean value</span></span>|[<span data-ttu-id="a4ca0-164">Not 运算符</span><span class="sxs-lookup"><span data-stu-id="a4ca0-164">Not Operator</span></span>](../../../language-reference/operators/not-operator.md)|  
|<span data-ttu-id="a4ca0-165">对两个布尔值执行逻辑与运算</span><span class="sxs-lookup"><span data-stu-id="a4ca0-165">Perform logical conjunction on two Boolean values</span></span>|[<span data-ttu-id="a4ca0-166">And 运算符</span><span class="sxs-lookup"><span data-stu-id="a4ca0-166">And Operator</span></span>](../../../language-reference/operators/and-operator.md)|  
|<span data-ttu-id="a4ca0-167">对两个布尔值执行包含逻辑析取</span><span class="sxs-lookup"><span data-stu-id="a4ca0-167">Perform inclusive logical disjunction on two Boolean values</span></span>|[<span data-ttu-id="a4ca0-168">Or 运算符</span><span class="sxs-lookup"><span data-stu-id="a4ca0-168">Or Operator</span></span>](../../../language-reference/operators/or-operator.md)|  
|<span data-ttu-id="a4ca0-169">对两个布尔值执行独占逻辑析取</span><span class="sxs-lookup"><span data-stu-id="a4ca0-169">Perform exclusive logical disjunction on two Boolean values</span></span>|[<span data-ttu-id="a4ca0-170">Xor 运算符</span><span class="sxs-lookup"><span data-stu-id="a4ca0-170">Xor Operator</span></span>](../../../language-reference/operators/xor-operator.md)|  
|<span data-ttu-id="a4ca0-171">对两个布尔值执行短路逻辑与运算</span><span class="sxs-lookup"><span data-stu-id="a4ca0-171">Perform short-circuited logical conjunction on two Boolean values</span></span>|[<span data-ttu-id="a4ca0-172">AndAlso 运算符</span><span class="sxs-lookup"><span data-stu-id="a4ca0-172">AndAlso Operator</span></span>](../../../language-reference/operators/andalso-operator.md)|  
|<span data-ttu-id="a4ca0-173">对两个布尔值执行短路包含逻辑析取</span><span class="sxs-lookup"><span data-stu-id="a4ca0-173">Perform short-circuited inclusive logical disjunction on two Boolean values</span></span>|[<span data-ttu-id="a4ca0-174">OrElse 运算符</span><span class="sxs-lookup"><span data-stu-id="a4ca0-174">OrElse Operator</span></span>](../../../language-reference/operators/orelse-operator.md)|  
|<span data-ttu-id="a4ca0-175">对两个整数值执行按位逻辑与运算</span><span class="sxs-lookup"><span data-stu-id="a4ca0-175">Perform bit-by-bit logical conjunction on two integral values</span></span>|[<span data-ttu-id="a4ca0-176">And 运算符</span><span class="sxs-lookup"><span data-stu-id="a4ca0-176">And Operator</span></span>](../../../language-reference/operators/and-operator.md)|  
|<span data-ttu-id="a4ca0-177">对两个整数值执行逐位包含逻辑析取</span><span class="sxs-lookup"><span data-stu-id="a4ca0-177">Perform bit-by-bit inclusive logical disjunction on two integral values</span></span>|[<span data-ttu-id="a4ca0-178">Or 运算符</span><span class="sxs-lookup"><span data-stu-id="a4ca0-178">Or Operator</span></span>](../../../language-reference/operators/or-operator.md)|  
|<span data-ttu-id="a4ca0-179">对两个整数值执行按位异或逻辑析取</span><span class="sxs-lookup"><span data-stu-id="a4ca0-179">Perform bit-by-bit exclusive logical disjunction on two integral values</span></span>|[<span data-ttu-id="a4ca0-180">Xor 运算符</span><span class="sxs-lookup"><span data-stu-id="a4ca0-180">Xor Operator</span></span>](../../../language-reference/operators/xor-operator.md)|  
|<span data-ttu-id="a4ca0-181">对整数值执行按位逻辑求反</span><span class="sxs-lookup"><span data-stu-id="a4ca0-181">Perform bit-by-bit logical negation on an integral value</span></span>|[<span data-ttu-id="a4ca0-182">Not 运算符</span><span class="sxs-lookup"><span data-stu-id="a4ca0-182">Not Operator</span></span>](../../../language-reference/operators/not-operator.md)|  
  
## <a name="see-also"></a><span data-ttu-id="a4ca0-183">请参阅</span><span class="sxs-lookup"><span data-stu-id="a4ca0-183">See also</span></span>

- [<span data-ttu-id="a4ca0-184">运算符和表达式</span><span class="sxs-lookup"><span data-stu-id="a4ca0-184">Operators and Expressions</span></span>](index.md)
- [<span data-ttu-id="a4ca0-185">按功能列出的运算符</span><span class="sxs-lookup"><span data-stu-id="a4ca0-185">Operators Listed by Functionality</span></span>](../../../language-reference/operators/operators-listed-by-functionality.md)
