---
description: '了解详细信息：扩大和收缩转换 (Visual Basic) '
title: Widening and Narrowing Conversions
ms.date: 07/20/2015
helpviewer_keywords:
- widening conversions [Visual Basic]
- narrowing conversions [Visual Basic]
- conversions [Visual Basic], type
- data types [Visual Basic], changing
- variables [Visual Basic], changing data type
- conversions [Visual Basic], exceptions during conversion
- type conversion [Visual Basic], exceptions during conversion
- conversions [Visual Basic], data type
- conversions [Visual Basic], narrowing
- type conversion [Visual Basic], narrowing
- data type conversion [Visual Basic], widening
- data type conversion [Visual Basic], narrowing
- changing data types [Visual Basic]
- type conversion [Visual Basic], widening
- data type conversion [Visual Basic], exceptions during conversion
- conversions [Visual Basic], widening
ms.assetid: 058c3152-6c28-4268-af44-2209e774f0bd
ms.openlocfilehash: 2ccd7d51b811aaf0f3e29dc0dc1730dffad2106b
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100468429"
---
# <a name="widening-and-narrowing-conversions-visual-basic"></a><span data-ttu-id="d8485-103">扩大转换和收缩转换 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d8485-103">Widening and Narrowing Conversions (Visual Basic)</span></span>

<span data-ttu-id="d8485-104">类型转换的一个重要注意事项是转换的结果是否在目标数据类型的范围内。</span><span class="sxs-lookup"><span data-stu-id="d8485-104">An important consideration with a type conversion is whether the result of the conversion is within the range of the destination data type.</span></span>  
  
 <span data-ttu-id="d8485-105">*扩大转换* 将值更改为数据类型，可允许原始数据的任何可能值。</span><span class="sxs-lookup"><span data-stu-id="d8485-105">A *widening conversion* changes a value to a data type that can allow for any possible value of the original data.</span></span>  <span data-ttu-id="d8485-106">扩大转换保留源值，但可以更改其表示形式。</span><span class="sxs-lookup"><span data-stu-id="d8485-106">Widening conversions preserve the source value but can change its representation.</span></span> <span data-ttu-id="d8485-107">如果从整型转换为或从整型转换为，则会发生这种情况 `Decimal` `Char` `String` 。</span><span class="sxs-lookup"><span data-stu-id="d8485-107">This occurs if you convert from an integral type to `Decimal`, or from `Char` to `String`.</span></span>  
  
 <span data-ttu-id="d8485-108">*“收缩转换”* 将值更改为可能无法保存某些可能值的数据类型。</span><span class="sxs-lookup"><span data-stu-id="d8485-108">A *narrowing conversion* changes a value to a data type that might not be able to hold some of the possible values.</span></span> <span data-ttu-id="d8485-109">例如，当将小数值转换为整型时，将对其进行舍入，并且将转换为的数值类型 `Boolean` 减小为 `True` 或 `False` 。</span><span class="sxs-lookup"><span data-stu-id="d8485-109">For example, a fractional value is rounded when it is converted to an integral type, and a numeric type being converted to `Boolean` is reduced to either `True` or `False`.</span></span>  
  
## <a name="widening-conversions"></a><span data-ttu-id="d8485-110">扩大转换</span><span class="sxs-lookup"><span data-stu-id="d8485-110">Widening Conversions</span></span>  

 <span data-ttu-id="d8485-111">下表显示了标准扩大转换。</span><span class="sxs-lookup"><span data-stu-id="d8485-111">The following table shows the standard widening conversions.</span></span>  
  
|<span data-ttu-id="d8485-112">数据类型</span><span class="sxs-lookup"><span data-stu-id="d8485-112">Data type</span></span>|<span data-ttu-id="d8485-113">扩大到数据类型 <sup>1</sup></span><span class="sxs-lookup"><span data-stu-id="d8485-113">Widens to data types <sup>1</sup></span></span>|  
|---|---|  
|[<span data-ttu-id="d8485-114">SByte</span><span class="sxs-lookup"><span data-stu-id="d8485-114">SByte</span></span>](../../../language-reference/data-types/sbyte-data-type.md)|<span data-ttu-id="d8485-115">`SByte`, `Short`, `Integer`, `Long`, `Decimal`, `Single`, `Double`</span><span class="sxs-lookup"><span data-stu-id="d8485-115">`SByte`, `Short`, `Integer`, `Long`, `Decimal`, `Single`, `Double`</span></span>|  
|[<span data-ttu-id="d8485-116">Byte</span><span class="sxs-lookup"><span data-stu-id="d8485-116">Byte</span></span>](../../../language-reference/data-types/byte-data-type.md)|<span data-ttu-id="d8485-117">`Byte`, `Short`, `UShort`, `Integer`, `UInteger`, `Long`, `ULong`, `Decimal`, `Single`, `Double`</span><span class="sxs-lookup"><span data-stu-id="d8485-117">`Byte`, `Short`, `UShort`, `Integer`, `UInteger`, `Long`, `ULong`, `Decimal`, `Single`, `Double`</span></span>|  
|[<span data-ttu-id="d8485-118">Short</span><span class="sxs-lookup"><span data-stu-id="d8485-118">Short</span></span>](../../../language-reference/data-types/short-data-type.md)|<span data-ttu-id="d8485-119">`Short`, `Integer`, `Long`, `Decimal`, `Single`, `Double`</span><span class="sxs-lookup"><span data-stu-id="d8485-119">`Short`, `Integer`, `Long`, `Decimal`, `Single`, `Double`</span></span>|  
|[<span data-ttu-id="d8485-120">UShort</span><span class="sxs-lookup"><span data-stu-id="d8485-120">UShort</span></span>](../../../language-reference/data-types/ushort-data-type.md)|<span data-ttu-id="d8485-121">`UShort`, `Integer`, `UInteger`, `Long`, `ULong`, `Decimal`, `Single`, `Double`</span><span class="sxs-lookup"><span data-stu-id="d8485-121">`UShort`, `Integer`, `UInteger`, `Long`, `ULong`, `Decimal`, `Single`, `Double`</span></span>|  
|[<span data-ttu-id="d8485-122">Integer</span><span class="sxs-lookup"><span data-stu-id="d8485-122">Integer</span></span>](../../../language-reference/data-types/integer-data-type.md)|<span data-ttu-id="d8485-123">`Integer`、 `Long` 、 `Decimal` 、 `Single` 、 `Double` <sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="d8485-123">`Integer`, `Long`, `Decimal`, `Single`, `Double`<sup>2</sup></span></span>|  
|[<span data-ttu-id="d8485-124">UInteger</span><span class="sxs-lookup"><span data-stu-id="d8485-124">UInteger</span></span>](../../../language-reference/data-types/uinteger-data-type.md)|<span data-ttu-id="d8485-125">`UInteger`、 `Long` 、 `ULong` 、 `Decimal` 、 `Single` 、 `Double` <sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="d8485-125">`UInteger`, `Long`, `ULong`, `Decimal`, `Single`, `Double`<sup>2</sup></span></span>|  
|[<span data-ttu-id="d8485-126">Long</span><span class="sxs-lookup"><span data-stu-id="d8485-126">Long</span></span>](../../../language-reference/data-types/long-data-type.md)|<span data-ttu-id="d8485-127">`Long`， `Decimal` ， `Single` ， `Double` <sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="d8485-127">`Long`, `Decimal`, `Single`, `Double`<sup>2</sup></span></span>|  
|[<span data-ttu-id="d8485-128">ULong</span><span class="sxs-lookup"><span data-stu-id="d8485-128">ULong</span></span>](../../../language-reference/data-types/ulong-data-type.md)|<span data-ttu-id="d8485-129">`ULong`， `Decimal` ， `Single` ， `Double` <sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="d8485-129">`ULong`, `Decimal`, `Single`, `Double`<sup>2</sup></span></span>|  
|<span data-ttu-id="d8485-130">十进制 </span><span class="sxs-lookup"><span data-stu-id="d8485-130">[Decimal](../../../language-reference/data-types/decimal-data-type.md)</span></span>|<span data-ttu-id="d8485-131">`Decimal`， `Single` ， `Double` <sup>2</sup></span><span class="sxs-lookup"><span data-stu-id="d8485-131">`Decimal`, `Single`, `Double`<sup>2</sup></span></span>|  
|[<span data-ttu-id="d8485-132">单精度</span><span class="sxs-lookup"><span data-stu-id="d8485-132">Single</span></span>](../../../language-reference/data-types/single-data-type.md)|<span data-ttu-id="d8485-133">`Single`, `Double`</span><span class="sxs-lookup"><span data-stu-id="d8485-133">`Single`, `Double`</span></span>|  
|[<span data-ttu-id="d8485-134">双精度</span><span class="sxs-lookup"><span data-stu-id="d8485-134">Double</span></span>](../../../language-reference/data-types/double-data-type.md)|`Double`|  
|<span data-ttu-id="d8485-135">枚举类型 ([枚举](../../../language-reference/statements/enum-statement.md)) </span><span class="sxs-lookup"><span data-stu-id="d8485-135">Any enumerated type ([Enum](../../../language-reference/statements/enum-statement.md))</span></span>|<span data-ttu-id="d8485-136">它的基础整型类型和基础类型扩展到的任何类型。</span><span class="sxs-lookup"><span data-stu-id="d8485-136">Its underlying integral type and any type to which the underlying type widens.</span></span>|  
|[<span data-ttu-id="d8485-137">Char</span><span class="sxs-lookup"><span data-stu-id="d8485-137">Char</span></span>](../../../language-reference/data-types/char-data-type.md)|<span data-ttu-id="d8485-138">`Char`, `String`</span><span class="sxs-lookup"><span data-stu-id="d8485-138">`Char`, `String`</span></span>|  
|<span data-ttu-id="d8485-139">`Char` 数组</span><span class="sxs-lookup"><span data-stu-id="d8485-139">`Char` array</span></span>|<span data-ttu-id="d8485-140">`Char` 组成 `String`</span><span class="sxs-lookup"><span data-stu-id="d8485-140">`Char` array, `String`</span></span>|  
|<span data-ttu-id="d8485-141">任何类型</span><span class="sxs-lookup"><span data-stu-id="d8485-141">Any type</span></span>|[<span data-ttu-id="d8485-142">对象</span><span class="sxs-lookup"><span data-stu-id="d8485-142">Object</span></span>](../../../language-reference/data-types/object-data-type.md)|  
|<span data-ttu-id="d8485-143">任何派生类型</span><span class="sxs-lookup"><span data-stu-id="d8485-143">Any derived type</span></span>|<span data-ttu-id="d8485-144">它派生自的任何基类型 <sup>3</sup>。</span><span class="sxs-lookup"><span data-stu-id="d8485-144">Any base type from which it is derived <sup>3</sup>.</span></span>|  
|<span data-ttu-id="d8485-145">任何类型</span><span class="sxs-lookup"><span data-stu-id="d8485-145">Any type</span></span>|<span data-ttu-id="d8485-146">它所实现的任何接口。</span><span class="sxs-lookup"><span data-stu-id="d8485-146">Any interface it implements.</span></span>|  
|[<span data-ttu-id="d8485-147">无</span><span class="sxs-lookup"><span data-stu-id="d8485-147">Nothing</span></span>](../../../language-reference/nothing.md)|<span data-ttu-id="d8485-148">任何数据类型或对象类型。</span><span class="sxs-lookup"><span data-stu-id="d8485-148">Any data type or object type.</span></span>|  
  
 <span data-ttu-id="d8485-149"><sup>1</sup> 根据定义，每个数据类型扩大到自身。</span><span class="sxs-lookup"><span data-stu-id="d8485-149"><sup>1</sup> By definition, every data type widens to itself.</span></span>  
  
 <span data-ttu-id="d8485-150"><sup>2</sup> 从、、、 `Integer` `UInteger` `Long` `ULong` 或 `Decimal` 到或的 `Single` 转换 `Double` 可能会导致精度损失，但绝不会损失。</span><span class="sxs-lookup"><span data-stu-id="d8485-150"><sup>2</sup> Conversions from `Integer`, `UInteger`, `Long`, `ULong`, or `Decimal` to `Single` or `Double` might result in loss of precision, but never in loss of magnitude.</span></span> <span data-ttu-id="d8485-151">在这种意义上，它们不会导致信息丢失。</span><span class="sxs-lookup"><span data-stu-id="d8485-151">In this sense they do not incur information loss.</span></span>  
  
 <span data-ttu-id="d8485-152"><sup>3</sup> 从派生类型到它的某个基类型的转换都是扩大的。</span><span class="sxs-lookup"><span data-stu-id="d8485-152"><sup>3</sup> It might seem surprising that a conversion from a derived type to one of its base types is widening.</span></span> <span data-ttu-id="d8485-153">理由是，派生类型包含基类型的所有成员，因此它限定为基类型的实例。</span><span class="sxs-lookup"><span data-stu-id="d8485-153">The justification is that the derived type contains all the members of the base type, so it qualifies as an instance of the base type.</span></span> <span data-ttu-id="d8485-154">相反，基类型不包含由派生类型定义的任何新成员。</span><span class="sxs-lookup"><span data-stu-id="d8485-154">In the opposite direction, the base type does not contain any new members defined by the derived type.</span></span>  
  
 <span data-ttu-id="d8485-155">扩大转换始终会在运行时成功，不会导致数据丢失。</span><span class="sxs-lookup"><span data-stu-id="d8485-155">Widening conversions always succeed at run time and never incur data loss.</span></span> <span data-ttu-id="d8485-156">无论 [选项 Strict 语句](../../../language-reference/statements/option-strict-statement.md) 是否将类型检查开关设置为或，都可以始终隐式执行它们 `On` `Off` 。</span><span class="sxs-lookup"><span data-stu-id="d8485-156">You can always perform them implicitly, whether the [Option Strict Statement](../../../language-reference/statements/option-strict-statement.md) sets the type checking switch to `On` or to `Off`.</span></span>  
  
## <a name="narrowing-conversions"></a><span data-ttu-id="d8485-157">收缩转换</span><span class="sxs-lookup"><span data-stu-id="d8485-157">Narrowing Conversions</span></span>  

 <span data-ttu-id="d8485-158">标准收缩转换包括：</span><span class="sxs-lookup"><span data-stu-id="d8485-158">The standard narrowing conversions include the following:</span></span>  
  
- <span data-ttu-id="d8485-159">上表中的扩大转换的反向方向 (除了每个类型扩大到自身) </span><span class="sxs-lookup"><span data-stu-id="d8485-159">The reverse directions of the widening conversions in the preceding table (except that every type widens to itself)</span></span>  
  
- <span data-ttu-id="d8485-160">[布尔值](../../../language-reference/data-types/boolean-data-type.md)和任何数值类型之间的任意方向转换</span><span class="sxs-lookup"><span data-stu-id="d8485-160">Conversions in either direction between [Boolean](../../../language-reference/data-types/boolean-data-type.md) and any numeric type</span></span>  
  
- <span data-ttu-id="d8485-161">从任何数值类型到任何枚举类型的转换都 (`Enum`) </span><span class="sxs-lookup"><span data-stu-id="d8485-161">Conversions from any numeric type to any enumerated type (`Enum`)</span></span>  
  
- <span data-ttu-id="d8485-162">在[字符串](../../../language-reference/data-types/string-data-type.md)和任何数值类型、 `Boolean` 或[日期](../../../language-reference/data-types/date-data-type.md)之间的任意方向转换</span><span class="sxs-lookup"><span data-stu-id="d8485-162">Conversions in either direction between [String](../../../language-reference/data-types/string-data-type.md) and any numeric type, `Boolean`, or [Date](../../../language-reference/data-types/date-data-type.md)</span></span>  
  
- <span data-ttu-id="d8485-163">从数据类型或对象类型转换为派生自它的类型</span><span class="sxs-lookup"><span data-stu-id="d8485-163">Conversions from a data type or object type to a type derived from it</span></span>  
  
 <span data-ttu-id="d8485-164">收缩转换在运行时并不总是成功，可能会失败或导致数据丢失。</span><span class="sxs-lookup"><span data-stu-id="d8485-164">Narrowing conversions do not always succeed at run time, and can fail or incur data loss.</span></span> <span data-ttu-id="d8485-165">如果目标数据类型无法接收正在转换的值，则会发生错误。</span><span class="sxs-lookup"><span data-stu-id="d8485-165">An error occurs if the destination data type cannot receive the value being converted.</span></span> <span data-ttu-id="d8485-166">例如，数字转换可能会导致溢出。</span><span class="sxs-lookup"><span data-stu-id="d8485-166">For example, a numeric conversion can result in an overflow.</span></span> <span data-ttu-id="d8485-167">编译器不允许隐式执行收缩转换，除非 [Option Strict 语句](../../../language-reference/statements/option-strict-statement.md) 将类型检查开关设置为 `Off` 。</span><span class="sxs-lookup"><span data-stu-id="d8485-167">The compiler does not allow you to perform narrowing conversions implicitly unless the [Option Strict Statement](../../../language-reference/statements/option-strict-statement.md) sets the type checking switch to `Off`.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="d8485-168">禁止将从集合中的元素转换 `For Each…Next` 为循环控制变量的收缩转换错误。</span><span class="sxs-lookup"><span data-stu-id="d8485-168">The narrowing-conversion error is suppressed for conversions from the elements in a `For Each…Next` collection to the loop control variable.</span></span> <span data-ttu-id="d8485-169">有关详细信息和示例，请参阅中的 "收缩转换" 一节 [。下一语句](../../../language-reference/statements/for-each-next-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="d8485-169">For more information and examples, see the "Narrowing Conversions" section in [For Each...Next Statement](../../../language-reference/statements/for-each-next-statement.md).</span></span>  
  
### <a name="when-to-use-narrowing-conversions"></a><span data-ttu-id="d8485-170">何时使用收缩转换</span><span class="sxs-lookup"><span data-stu-id="d8485-170">When to Use Narrowing Conversions</span></span>  

 <span data-ttu-id="d8485-171">如果知道源值可转换为目标数据类型，而不会出错或丢失数据，则可以使用收缩转换。</span><span class="sxs-lookup"><span data-stu-id="d8485-171">You use a narrowing conversion when you know the source value can be converted to the destination data type without error or data loss.</span></span> <span data-ttu-id="d8485-172">例如，如果你有一个 `String` 知道包含 "True" 或 "False" 的，则可以使用 `CBool` 关键字将其转换为 `Boolean` 。</span><span class="sxs-lookup"><span data-stu-id="d8485-172">For example, if you have a `String` that you know contains either "True" or "False," you can use the `CBool` keyword to convert it to `Boolean`.</span></span>  
  
## <a name="exceptions-during-conversion"></a><span data-ttu-id="d8485-173">转换过程中的异常</span><span class="sxs-lookup"><span data-stu-id="d8485-173">Exceptions During Conversion</span></span>  

 <span data-ttu-id="d8485-174">因为扩大转换始终会成功，所以它们不会引发异常。</span><span class="sxs-lookup"><span data-stu-id="d8485-174">Because widening conversions always succeed, they do not throw exceptions.</span></span> <span data-ttu-id="d8485-175">收缩转换在失败时，通常会引发以下异常：</span><span class="sxs-lookup"><span data-stu-id="d8485-175">Narrowing conversions, when they fail, most commonly throw the following exceptions:</span></span>  
  
- <span data-ttu-id="d8485-176"><xref:System.InvalidCastException> -如果在这两个类型之间未定义转换</span><span class="sxs-lookup"><span data-stu-id="d8485-176"><xref:System.InvalidCastException> — if no conversion is defined between the two types</span></span>  
  
- <span data-ttu-id="d8485-177"><xref:System.OverflowException> - (整型类型仅) 转换后的值对于目标类型来说太大</span><span class="sxs-lookup"><span data-stu-id="d8485-177"><xref:System.OverflowException> — (integral types only) if the converted value is too large for the target type</span></span>  
  
 <span data-ttu-id="d8485-178">如果某个类或结构定义一个 [CType 函数](../../../language-reference/functions/ctype-function.md) ，该函数将充当与该类或结构之间的转换运算符， `CType` 则可能会引发它认为合适的任何异常。</span><span class="sxs-lookup"><span data-stu-id="d8485-178">If a class or structure defines a [CType Function](../../../language-reference/functions/ctype-function.md) to serve as a conversion operator to or from that class or structure, that `CType` can throw any exception it deems appropriate.</span></span> <span data-ttu-id="d8485-179">此外，这 `CType` 可能会调用 Visual Basic 函数或 .NET Framework 方法，进而可能引发各种异常。</span><span class="sxs-lookup"><span data-stu-id="d8485-179">In addition, that `CType` might call Visual Basic functions or .NET Framework methods, which in turn could throw a variety of exceptions.</span></span>  
  
## <a name="changes-during-reference-type-conversions"></a><span data-ttu-id="d8485-180">引用类型转换期间的更改</span><span class="sxs-lookup"><span data-stu-id="d8485-180">Changes During Reference Type Conversions</span></span>  

 <span data-ttu-id="d8485-181">从 *引用类型* 进行的转换只复制指向值的指针。</span><span class="sxs-lookup"><span data-stu-id="d8485-181">A conversion from a *reference type* copies only the pointer to the value.</span></span> <span data-ttu-id="d8485-182">值本身既不会进行复制，也不会更改。</span><span class="sxs-lookup"><span data-stu-id="d8485-182">The value itself is neither copied nor changed in any way.</span></span> <span data-ttu-id="d8485-183">唯一可以更改的是保存指针的变量的数据类型。</span><span class="sxs-lookup"><span data-stu-id="d8485-183">The only thing that can change is the data type of the variable holding the pointer.</span></span> <span data-ttu-id="d8485-184">在下面的示例中，数据类型从派生类转换为其基类，但这两个变量现在指向的对象是不变的。</span><span class="sxs-lookup"><span data-stu-id="d8485-184">In the following example, the data type is converted from the derived class to its base class, but the object that both variables now point to is unchanged.</span></span>  
  
```vb  
' Assume class cSquare inherits from class cShape.  
Dim shape As cShape  
Dim square As cSquare = New cSquare  
' The following statement performs a widening  
' conversion from a derived class to its base class.  
shape = square  
```  
  
## <a name="see-also"></a><span data-ttu-id="d8485-185">请参阅</span><span class="sxs-lookup"><span data-stu-id="d8485-185">See also</span></span>

- [<span data-ttu-id="d8485-186">数据类型</span><span class="sxs-lookup"><span data-stu-id="d8485-186">Data Types</span></span>](index.md)
- [<span data-ttu-id="d8485-187">Visual Basic 中的类型转换</span><span class="sxs-lookup"><span data-stu-id="d8485-187">Type Conversions in Visual Basic</span></span>](type-conversions.md)
- [<span data-ttu-id="d8485-188">隐式转换和显式转换</span><span class="sxs-lookup"><span data-stu-id="d8485-188">Implicit and Explicit Conversions</span></span>](implicit-and-explicit-conversions.md)
- [<span data-ttu-id="d8485-189">字符串和其他类型之间的转换</span><span class="sxs-lookup"><span data-stu-id="d8485-189">Conversions Between Strings and Other Types</span></span>](conversions-between-strings-and-other-types.md)
- [<span data-ttu-id="d8485-190">如何：在 Visual Basic 中将一个对象转换为其他类型</span><span class="sxs-lookup"><span data-stu-id="d8485-190">How to: Convert an Object to Another Type in Visual Basic</span></span>](how-to-convert-an-object-to-another-type.md)
- [<span data-ttu-id="d8485-191">数组转换</span><span class="sxs-lookup"><span data-stu-id="d8485-191">Array Conversions</span></span>](array-conversions.md)
- [<span data-ttu-id="d8485-192">数据类型</span><span class="sxs-lookup"><span data-stu-id="d8485-192">Data Types</span></span>](../../../language-reference/data-types/index.md)
- [<span data-ttu-id="d8485-193">Type Conversion Functions</span><span class="sxs-lookup"><span data-stu-id="d8485-193">Type Conversion Functions</span></span>](../../../language-reference/functions/type-conversion-functions.md)
