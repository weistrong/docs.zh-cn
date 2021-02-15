---
description: 详细了解：运算符重载
title: 运算符重载
ms.date: 10/22/2008
helpviewer_keywords:
- operators [.NET Framework], overloads
- names [.NET Framework], overloaded operators
- member design guidelines, operators
- overloaded operators
ms.assetid: 37585bf2-4c27-4dee-849a-af70e3338cc1
ms.openlocfilehash: e6552f35081afa542e4dc14239206a63c7c1bd59
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99713320"
---
# <a name="operator-overloads"></a><span data-ttu-id="63cf7-103">运算符重载</span><span class="sxs-lookup"><span data-stu-id="63cf7-103">Operator Overloads</span></span>

<span data-ttu-id="63cf7-104">运算符重载可以使框架类型看起来像是内置语言基元一样。</span><span class="sxs-lookup"><span data-stu-id="63cf7-104">Operator overloads allow framework types to appear as if they were built-in language primitives.</span></span>

 <span data-ttu-id="63cf7-105">尽管运算符重载在某些情况下是允许使用的，而且很有用，但还是应该谨慎使用它们。</span><span class="sxs-lookup"><span data-stu-id="63cf7-105">Although allowed and useful in some situations, operator overloads should be used cautiously.</span></span> <span data-ttu-id="63cf7-106">在许多情况下，运算符重载被滥用，例如当框架设计者开始使用运算符来执行本应是简单方法的运算时。</span><span class="sxs-lookup"><span data-stu-id="63cf7-106">There are many cases in which operator overloading has been abused, such as when framework designers started to use operators for operations that should be simple methods.</span></span> <span data-ttu-id="63cf7-107">以下准则应该可帮助你决定何时以及如何使用运算符重载。</span><span class="sxs-lookup"><span data-stu-id="63cf7-107">The following guidelines should help you decide when and how to use operator overloading.</span></span>

 <span data-ttu-id="63cf7-108">❌ 请避免定义运算符重载，除非在感觉像是基元（内置）类型的类型中。</span><span class="sxs-lookup"><span data-stu-id="63cf7-108">❌ AVOID defining operator overloads, except in types that should feel like primitive (built-in) types.</span></span>

 <span data-ttu-id="63cf7-109">✔️ 请考虑在一个感觉像是基元类型的类型中定义运算符重载。</span><span class="sxs-lookup"><span data-stu-id="63cf7-109">✔️ CONSIDER defining operator overloads in a type that should feel like a primitive type.</span></span>

 <span data-ttu-id="63cf7-110">例如，<xref:System.String?displayProperty=nameWithType> 定义了 `operator==` 和 `operator!=`。</span><span class="sxs-lookup"><span data-stu-id="63cf7-110">For example, <xref:System.String?displayProperty=nameWithType> has `operator==` and `operator!=` defined.</span></span>

 <span data-ttu-id="63cf7-111">✔️ 请务必在表示数字的结构（如 <xref:System.Decimal?displayProperty=nameWithType>）中定义运算符重载。</span><span class="sxs-lookup"><span data-stu-id="63cf7-111">✔️ DO define operator overloads in structs that represent numbers (such as <xref:System.Decimal?displayProperty=nameWithType>).</span></span>

 <span data-ttu-id="63cf7-112">❌ 在定义运算符重载时请勿太刻意。</span><span class="sxs-lookup"><span data-stu-id="63cf7-112">❌ DO NOT be cute when defining operator overloads.</span></span>

 <span data-ttu-id="63cf7-113">运算符重载在运算结果显而易见的情况下非常有用。</span><span class="sxs-lookup"><span data-stu-id="63cf7-113">Operator overloading is useful in cases in which it is immediately obvious what the result of the operation will be.</span></span> <span data-ttu-id="63cf7-114">例如，能够从另一个 `DateTime` 中减去一个 <xref:System.DateTime> 并得到一个 <xref:System.TimeSpan>，这是有意义的。</span><span class="sxs-lookup"><span data-stu-id="63cf7-114">For example, it makes sense to be able to subtract one <xref:System.DateTime> from another `DateTime` and get a <xref:System.TimeSpan>.</span></span> <span data-ttu-id="63cf7-115">但是，以下操作是不恰当的：使用逻辑 union 运算符来联合两个数据库查询或使用 shift 运算符写入到流中。</span><span class="sxs-lookup"><span data-stu-id="63cf7-115">However, it is not appropriate to use the logical union operator to union two database queries, or to use the shift operator to write to a stream.</span></span>

 <span data-ttu-id="63cf7-116">❌ 除非至少有一个操作数属于定义重载的类型，否则请勿提供运算符重载。</span><span class="sxs-lookup"><span data-stu-id="63cf7-116">❌ DO NOT provide operator overloads unless at least one of the operands is of the type defining the overload.</span></span>

 <span data-ttu-id="63cf7-117">✔️ 请确保以对称方式重载运算符。</span><span class="sxs-lookup"><span data-stu-id="63cf7-117">✔️ DO overload operators in a symmetric fashion.</span></span>

 <span data-ttu-id="63cf7-118">例如，如果你重载了 `operator==`，则还应重载 `operator!=`。</span><span class="sxs-lookup"><span data-stu-id="63cf7-118">For example, if you overload the `operator==`, you should also overload the `operator!=`.</span></span> <span data-ttu-id="63cf7-119">同样，如果你重载了 `operator<`，则还应重载 `operator>`，诸如此类。</span><span class="sxs-lookup"><span data-stu-id="63cf7-119">Similarly, if you overload the `operator<`, you should also overload the `operator>`, and so on.</span></span>

 <span data-ttu-id="63cf7-120">✔️ 请考虑为方法提供与每个重载的运算符相对应的友好名称。</span><span class="sxs-lookup"><span data-stu-id="63cf7-120">✔️ CONSIDER providing methods with friendly names that correspond to each overloaded operator.</span></span>

 <span data-ttu-id="63cf7-121">许多语言不支持运算符重载。</span><span class="sxs-lookup"><span data-stu-id="63cf7-121">Many languages do not support operator overloading.</span></span> <span data-ttu-id="63cf7-122">出于此原因，建议重载运算符的类型包含一个辅助方法，该方法具有适当的特定于域的名称且提供等效功能。</span><span class="sxs-lookup"><span data-stu-id="63cf7-122">For this reason, it is recommended that types that overload operators include a secondary method with an appropriate domain-specific name that provides equivalent functionality.</span></span>

 <span data-ttu-id="63cf7-123">下表包含一个运算符列表及相应的友好方法名称。</span><span class="sxs-lookup"><span data-stu-id="63cf7-123">The following table contains a list of operators and the corresponding friendly method names.</span></span>

|<span data-ttu-id="63cf7-124">C# 运算符符号</span><span class="sxs-lookup"><span data-stu-id="63cf7-124">C# Operator Symbol</span></span>|<span data-ttu-id="63cf7-125">元数据名称</span><span class="sxs-lookup"><span data-stu-id="63cf7-125">Metadata Name</span></span>|<span data-ttu-id="63cf7-126">友好名称</span><span class="sxs-lookup"><span data-stu-id="63cf7-126">Friendly Name</span></span>|
|-------------------------|-------------------|-------------------|
|`N/A`|`op_Implicit`|`To<TypeName>/From<TypeName>`|
|`N/A`|`op_Explicit`|`To<TypeName>/From<TypeName>`|
|`+ (binary)`|`op_Addition`|`Add`|
|`- (binary)`|`op_Subtraction`|`Subtract`|
|`* (binary)`|`op_Multiply`|`Multiply`|
|`/`|`op_Division`|`Divide`|
|`%`|`op_Modulus`|`Mod or Remainder`|
|`^`|`op_ExclusiveOr`|`Xor`|
|`& (binary)`|`op_BitwiseAnd`|`BitwiseAnd`|
|<code>&#124;</code>|`op_BitwiseOr`|`BitwiseOr`|
|`&&`|`op_LogicalAnd`|`And`|
|<code>&#124;&#124;</code>|`op_LogicalOr`|`Or`|
|`=`|`op_Assign`|`Assign`|
|`<<`|`op_LeftShift`|`LeftShift`|
|`>>`|`op_RightShift`|`RightShift`|
|`N/A`|`op_SignedRightShift`|`SignedRightShift`|
|`N/A`|`op_UnsignedRightShift`|`UnsignedRightShift`|
|`==`|`op_Equality`|`Equals`|
|`!=`|`op_Inequality`|`Equals`|
|`>`|`op_GreaterThan`|`CompareTo`|
|`<`|`op_LessThan`|`CompareTo`|
|`>=`|`op_GreaterThanOrEqual`|`CompareTo`|
|`<=`|`op_LessThanOrEqual`|`CompareTo`|
|`*=`|`op_MultiplicationAssignment`|`Multiply`|
|`-=`|`op_SubtractionAssignment`|`Subtract`|
|`^=`|`op_ExclusiveOrAssignment`|`Xor`|
|`<<=`|`op_LeftShiftAssignment`|`LeftShift`|
|`%=`|`op_ModulusAssignment`|`Mod`|
|`+=`|`op_AdditionAssignment`|`Add`|
|`&=`|`op_BitwiseAndAssignment`|`BitwiseAnd`|
|<code>&#124;=</code>|`op_BitwiseOrAssignment`|`BitwiseOr`|
|`,`|`op_Comma`|`Comma`|
|`/=`|`op_DivisionAssignment`|`Divide`|
|`--`|`op_Decrement`|`Decrement`|
|`++`|`op_Increment`|`Increment`|
|`- (unary)`|`op_UnaryNegation`|`Negate`|
|`+ (unary)`|`op_UnaryPlus`|`Plus`|
|`~`|`op_OnesComplement`|`OnesComplement`|

### <a name="overloading-operator-"></a><span data-ttu-id="63cf7-127">重载运算符 ==</span><span class="sxs-lookup"><span data-stu-id="63cf7-127">Overloading Operator ==</span></span>

 <span data-ttu-id="63cf7-128">重载 `operator ==` 非常复杂。</span><span class="sxs-lookup"><span data-stu-id="63cf7-128">Overloading `operator ==` is quite complicated.</span></span> <span data-ttu-id="63cf7-129">该运算符的语义需要与其他一些成员（如 <xref:System.Object.Equals%2A?displayProperty=nameWithType>）兼容。</span><span class="sxs-lookup"><span data-stu-id="63cf7-129">The semantics of the operator need to be compatible with several other members, such as <xref:System.Object.Equals%2A?displayProperty=nameWithType>.</span></span>

### <a name="conversion-operators"></a><span data-ttu-id="63cf7-130">转换运算符</span><span class="sxs-lookup"><span data-stu-id="63cf7-130">Conversion Operators</span></span>

 <span data-ttu-id="63cf7-131">转换运算符是允许从一种类型转换为另一种类型的一元运算符。</span><span class="sxs-lookup"><span data-stu-id="63cf7-131">Conversion operators are unary operators that allow conversion from one type to another.</span></span> <span data-ttu-id="63cf7-132">该运算符必须对操作数或返回类型定义为静态成员。</span><span class="sxs-lookup"><span data-stu-id="63cf7-132">The operators must be defined as static members on either the operand or the return type.</span></span> <span data-ttu-id="63cf7-133">有两种类型的转换运算符：隐式和显式。</span><span class="sxs-lookup"><span data-stu-id="63cf7-133">There are two types of conversion operators: implicit and explicit.</span></span>

 <span data-ttu-id="63cf7-134">❌ 如果最终用户没有明确期望进行此类转换，请勿提供转换运算符。</span><span class="sxs-lookup"><span data-stu-id="63cf7-134">❌ DO NOT provide a conversion operator if such conversion is not clearly expected by the end users.</span></span>

 <span data-ttu-id="63cf7-135">❌ 请勿在类型的域外定义转换运算符。</span><span class="sxs-lookup"><span data-stu-id="63cf7-135">❌ DO NOT define conversion operators outside of a type’s domain.</span></span>

 <span data-ttu-id="63cf7-136">例如，<xref:System.Int32>、<xref:System.Double> 和 <xref:System.Decimal> 均为数值类型，而 <xref:System.DateTime> 则不是。</span><span class="sxs-lookup"><span data-stu-id="63cf7-136">For example, <xref:System.Int32>, <xref:System.Double>, and <xref:System.Decimal> are all numeric types, whereas <xref:System.DateTime> is not.</span></span> <span data-ttu-id="63cf7-137">因此，应该没有转换运算符能够将 `Double(long)` 转换为 `DateTime`。</span><span class="sxs-lookup"><span data-stu-id="63cf7-137">Therefore, there should be no conversion operator to convert a `Double(long)` to a `DateTime`.</span></span> <span data-ttu-id="63cf7-138">在这种情况下，首选使用构造函数。</span><span class="sxs-lookup"><span data-stu-id="63cf7-138">A constructor is preferred in such a case.</span></span>

 <span data-ttu-id="63cf7-139">❌ 如果转换可能有损，请勿提供隐式转换运算符。</span><span class="sxs-lookup"><span data-stu-id="63cf7-139">❌ DO NOT provide an implicit conversion operator if the conversion is potentially lossy.</span></span>

 <span data-ttu-id="63cf7-140">例如，不应存在从 `Double` 到 `Int32` 的隐式转换，因为 `Double` 的范围比 `Int32` 大。</span><span class="sxs-lookup"><span data-stu-id="63cf7-140">For example, there should not be an implicit conversion from `Double` to `Int32` because `Double` has a wider range than `Int32`.</span></span> <span data-ttu-id="63cf7-141">即使转换可能会有损，也可以提供显式转换运算符。</span><span class="sxs-lookup"><span data-stu-id="63cf7-141">An explicit conversion operator can be provided even if the conversion is potentially lossy.</span></span>

 <span data-ttu-id="63cf7-142">❌ 请勿从隐式强制转换引发异常。</span><span class="sxs-lookup"><span data-stu-id="63cf7-142">❌ DO NOT throw exceptions from implicit casts.</span></span>

 <span data-ttu-id="63cf7-143">最终用户很难了解发生的情况，因为他们可能没有意识到正在进行转换。</span><span class="sxs-lookup"><span data-stu-id="63cf7-143">It is very difficult for end users to understand what is happening, because they might not be aware that a conversion is taking place.</span></span>

 <span data-ttu-id="63cf7-144">✔️ 如果对强制转换运算符的调用导致有损转换，而该运算符的协定不允许有损转换，请务必引发 <xref:System.InvalidCastException?displayProperty=nameWithType>。</span><span class="sxs-lookup"><span data-stu-id="63cf7-144">✔️ DO throw <xref:System.InvalidCastException?displayProperty=nameWithType> if a call to a cast operator results in a lossy conversion and the contract of the operator does not allow lossy conversions.</span></span>

 <span data-ttu-id="63cf7-145">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="63cf7-145">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="63cf7-146">在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。</span><span class="sxs-lookup"><span data-stu-id="63cf7-146">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="63cf7-147">请参阅</span><span class="sxs-lookup"><span data-stu-id="63cf7-147">See also</span></span>

- [<span data-ttu-id="63cf7-148">成员设计准则</span><span class="sxs-lookup"><span data-stu-id="63cf7-148">Member Design Guidelines</span></span>](member.md)
- [<span data-ttu-id="63cf7-149">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="63cf7-149">Framework Design Guidelines</span></span>](index.md)
