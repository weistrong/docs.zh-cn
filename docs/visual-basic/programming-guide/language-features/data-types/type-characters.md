---
description: '了解详细信息：键入字符 (Visual Basic) '
title: 类型字符
ms.date: 01/31/2018
helpviewer_keywords:
- '&H prefix for hexadecimal values'
- hexadecimal literals [Visual Basic]
- F literal type character [Visual Basic]
- '& identifier type character'
- type characters [Visual Basic]
- octal literals [Visual Basic]
- literals [Visual Basic], hexadecimal
- '&O prefix for octal values'
- literals [Visual Basic], default types
- defaults, literal types
- C literal type character [Visual Basic]
- type characters [Visual Basic], literal
- $ identifier type character
- L literal type character [Visual Basic]
- UI literal type characters [Visual Basic]
- default literal types [Visual Basic]
- D literal type character [Visual Basic]
- literals [Visual Basic], octal
- S literal type character [Visual Basic]
- '! identifier type character'
- US literal type characters [Visual Basic]
- '% identifier type character'
- data types [Visual Basic], type characters
- characters [Visual Basic], identifier type
- type characters [Visual Basic], identifier
- '# identifier type character'
- identifier type characters [Visual Basic]
- literal type characters [Visual Basic]
- I literal type character [Visual Basic]
- R literal type character [Visual Basic]
- '@ identifier type character'
- UL literal type characters [Visual Basic]
- literal types [Visual Basic], default
ms.assetid: 6353cb9b-6ee4-4af6-a5a8-88ce39f90cc5
ms.openlocfilehash: d1afccb821d2ffb4dfabe3c38e0db4a7f902c164
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100454542"
---
# <a name="type-characters-visual-basic"></a><span data-ttu-id="58bde-103">键入字符 (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="58bde-103">Type characters (Visual Basic)</span></span>

<span data-ttu-id="58bde-104">除了在声明语句中指定数据类型之外，还可以使用 *类型字符* 强制某些编程元素的数据类型。</span><span class="sxs-lookup"><span data-stu-id="58bde-104">In addition to specifying a data type in a declaration statement, you can force the data type of some programming elements with a *type character*.</span></span> <span data-ttu-id="58bde-105">类型字符必须紧跟在元素之后，无任何类型的插入字符。</span><span class="sxs-lookup"><span data-stu-id="58bde-105">The type character must immediately follow the element, with no intervening characters of any kind.</span></span>

<span data-ttu-id="58bde-106">类型字符不是元素名称的一部分。</span><span class="sxs-lookup"><span data-stu-id="58bde-106">The type character is not part of the name of the element.</span></span> <span data-ttu-id="58bde-107">在不使用类型字符的情况下，可以引用使用类型字符定义的元素。</span><span class="sxs-lookup"><span data-stu-id="58bde-107">An element defined with a type character can be referenced without the type character.</span></span>

## <a name="identifier-type-characters"></a><span data-ttu-id="58bde-108">标识符类型字符</span><span class="sxs-lookup"><span data-stu-id="58bde-108">Identifier type characters</span></span>

<span data-ttu-id="58bde-109">Visual Basic 提供一组 *标识符类型字符* ，可以在声明中使用这些字符来指定变量或常量的数据类型。</span><span class="sxs-lookup"><span data-stu-id="58bde-109">Visual Basic supplies a set of *identifier type characters* that you can use in a declaration to specify the data type of a variable or constant.</span></span> <span data-ttu-id="58bde-110">下表显示了可用的标识符类型字符和用法示例。</span><span class="sxs-lookup"><span data-stu-id="58bde-110">The following table shows the available identifier type characters with examples of usage.</span></span>
  
|<span data-ttu-id="58bde-111">标识符类型字符</span><span class="sxs-lookup"><span data-stu-id="58bde-111">Identifier type character</span></span>|<span data-ttu-id="58bde-112">数据类型</span><span class="sxs-lookup"><span data-stu-id="58bde-112">Data type</span></span>|<span data-ttu-id="58bde-113">示例</span><span class="sxs-lookup"><span data-stu-id="58bde-113">Example</span></span>|  
|-------------------------------|---------------|-------------|  
|`%`|`Integer`|`Dim L%`|  
|`&`|`Long`|`Dim M&`|  
|`@`|`Decimal`|`Const W@ = 37.5`|  
|`!`|`Single`|`Dim Q!`|  
|`#`|`Double`|`Dim X#`|  
|`$`|`String`|`Dim V$ = "Secret"`|  
  
 <span data-ttu-id="58bde-114">对于、、、、、、、、 `Boolean` `Byte` `Char` `Date` `Object` `SByte` `Short` `UInteger` `ULong` 或 `UShort` 数据类型，或任何复合数据类型（例如数组或结构），都不存在标识符类型字符。</span><span class="sxs-lookup"><span data-stu-id="58bde-114">No identifier type characters exist for the `Boolean`, `Byte`, `Char`, `Date`, `Object`, `SByte`, `Short`, `UInteger`, `ULong`, or `UShort` data types, or for any composite data types such as arrays or structures.</span></span>

<span data-ttu-id="58bde-115">在某些情况下，可以将该 `$` 字符追加到 Visual Basic 函数，例如 `Left$` 而不是 `Left` ，以获取类型的返回值 `String` 。</span><span class="sxs-lookup"><span data-stu-id="58bde-115">In some cases, you can append the `$` character to a Visual Basic function, for example `Left$` instead of `Left`, to obtain a returned value of type `String`.</span></span>

<span data-ttu-id="58bde-116">在所有情况下，标识符类型字符都必须紧跟在标识符名称后面。</span><span class="sxs-lookup"><span data-stu-id="58bde-116">In all cases, the identifier type character must immediately follow the identifier name.</span></span>

## <a name="literal-type-characters"></a><span data-ttu-id="58bde-117">文本类型字符</span><span class="sxs-lookup"><span data-stu-id="58bde-117">Literal type characters</span></span>

<span data-ttu-id="58bde-118">*文本* 是数据类型的特定值的文本表示形式。</span><span class="sxs-lookup"><span data-stu-id="58bde-118">A *literal* is a textual representation of a particular value of a data type.</span></span>  

### <a name="default-literal-types"></a><span data-ttu-id="58bde-119">默认文本类型</span><span class="sxs-lookup"><span data-stu-id="58bde-119">Default literal types</span></span>

<span data-ttu-id="58bde-120">在代码中显示的文本形式通常会确定其数据类型。</span><span class="sxs-lookup"><span data-stu-id="58bde-120">The form of a literal as it appears in your code ordinarily determines its data type.</span></span> <span data-ttu-id="58bde-121">下表显示了这些默认类型。</span><span class="sxs-lookup"><span data-stu-id="58bde-121">The following table shows these default types.</span></span>  
  
|<span data-ttu-id="58bde-122">文本格式的文本</span><span class="sxs-lookup"><span data-stu-id="58bde-122">Textual form of literal</span></span>|<span data-ttu-id="58bde-123">默认数据类型</span><span class="sxs-lookup"><span data-stu-id="58bde-123">Default data type</span></span>|<span data-ttu-id="58bde-124">示例</span><span class="sxs-lookup"><span data-stu-id="58bde-124">Example</span></span>|  
|-----------------------------|-----------------------|-------------|  
|<span data-ttu-id="58bde-125">数值，无小数部分</span><span class="sxs-lookup"><span data-stu-id="58bde-125">Numeric, no fractional part</span></span>|`Integer`|`2147483647`|  
|<span data-ttu-id="58bde-126">数值，没有小数部分，太大，无法 `Integer`</span><span class="sxs-lookup"><span data-stu-id="58bde-126">Numeric, no fractional part, too large for `Integer`</span></span>|`Long`|`2147483648`|  
|<span data-ttu-id="58bde-127">数值，小数部分</span><span class="sxs-lookup"><span data-stu-id="58bde-127">Numeric, fractional part</span></span>|`Double`|`1.2`|  
|<span data-ttu-id="58bde-128">包含在双引号内</span><span class="sxs-lookup"><span data-stu-id="58bde-128">Enclosed in double quotation marks</span></span>|`String`|`"A"`|  
|<span data-ttu-id="58bde-129">括在数字符号内</span><span class="sxs-lookup"><span data-stu-id="58bde-129">Enclosed within number signs</span></span>|`Date`|`#5/17/1993 9:32 AM#`|  

### <a name="forced-literal-types"></a><span data-ttu-id="58bde-130">强制文本类型</span><span class="sxs-lookup"><span data-stu-id="58bde-130">Forced literal types</span></span>

<span data-ttu-id="58bde-131">Visual Basic 提供一组 *文本类型字符*，您可以使用这些字符强制文本采用其形式所指示的数据类型之外的数据类型。</span><span class="sxs-lookup"><span data-stu-id="58bde-131">Visual Basic supplies a set of *literal type characters*, which you can use to force a literal to assume a data type other than the one its form indicates.</span></span> <span data-ttu-id="58bde-132">为此，可将字符追加到文本末尾。</span><span class="sxs-lookup"><span data-stu-id="58bde-132">You do this by appending the character to the end of the literal.</span></span> <span data-ttu-id="58bde-133">下表显示了可用的文本类型字符，其中包含用法的示例。</span><span class="sxs-lookup"><span data-stu-id="58bde-133">The following table shows the available literal type characters with examples of usage.</span></span>
  
|<span data-ttu-id="58bde-134">文本类型字符</span><span class="sxs-lookup"><span data-stu-id="58bde-134">Literal type character</span></span>|<span data-ttu-id="58bde-135">数据类型</span><span class="sxs-lookup"><span data-stu-id="58bde-135">Data type</span></span>|<span data-ttu-id="58bde-136">示例</span><span class="sxs-lookup"><span data-stu-id="58bde-136">Example</span></span>|  
|----------------------------|---------------|-------------|  
|`S`|`Short`|`I = 347S`|
|`I`|`Integer`|`J = 347I`|
|`L`|`Long`|`K = 347L`|
|`D`|`Decimal`|`X = 347D`|
|`F`|`Single`|`Y = 347F`|
|`R`|`Double`|`Z = 347R`|
|`US`|`UShort`|`L = 347US`|
|`UI`|`UInteger`|`M = 347UI`|
|`UL`|`ULong`|`N = 347UL`|
|`C`|`Char`|`Q = "."C`|

<span data-ttu-id="58bde-137">对于、、、 `Boolean` `Byte` `Date` `Object` 、 `SByte` 或 `String` 数据类型，或任何复合数据类型（例如数组或结构），不存在文本类型字符。</span><span class="sxs-lookup"><span data-stu-id="58bde-137">No literal type characters exist for the `Boolean`, `Byte`, `Date`, `Object`, `SByte`, or `String` data types, or for any composite data types such as arrays or structures.</span></span>

<span data-ttu-id="58bde-138">文本还可以使用标识符类型字符 (`%` 、 `&` 、 `@` 、 `!` 、 `#` 、) ，也可以 `$` 是变量、常量和表达式。</span><span class="sxs-lookup"><span data-stu-id="58bde-138">Literals can also use the identifier type characters (`%`, `&`, `@`, `!`, `#`, `$`), as can variables, constants, and expressions.</span></span> <span data-ttu-id="58bde-139">但 (、、、、、、) 文本类型字符只能 `S` `I` `L` `D` `F` `R` `C` 与文本一起使用。</span><span class="sxs-lookup"><span data-stu-id="58bde-139">However, the literal type characters (`S`, `I`, `L`, `D`, `F`, `R`, `C`) can be used only with literals.</span></span>

<span data-ttu-id="58bde-140">在所有情况下，文本类型字符都必须紧跟在文本值之后。</span><span class="sxs-lookup"><span data-stu-id="58bde-140">In all cases, the literal type character must immediately follow the literal value.</span></span>

## <a name="hexadecimal-binary-and-octal-literals"></a><span data-ttu-id="58bde-141">十六进制、二进制和八进制文本</span><span class="sxs-lookup"><span data-stu-id="58bde-141">Hexadecimal, binary, and octal literals</span></span>

<span data-ttu-id="58bde-142">编译器通常将整数文本解释为十进制 (以10为底) 号系统。</span><span class="sxs-lookup"><span data-stu-id="58bde-142">The compiler normally interprets an integer literal to be in the decimal (base 10) number system.</span></span> <span data-ttu-id="58bde-143">你还可以将整数文本定义为带有前缀的十六进制 (以16为基数的) 号 `&H` ，作为二进制 (以前缀形式表示的以2为基的) 号 `&B` ，以及作为带有前缀的八进制 (基数 8) 号 `&O` 。</span><span class="sxs-lookup"><span data-stu-id="58bde-143">You can also define an integer literal as a hexadecimal (base 16) number with the `&H` prefix, as a binary (base 2) number with the `&B` prefix, and as an octal (base 8) number with the `&O` prefix.</span></span> <span data-ttu-id="58bde-144">前缀后面的数字必须适用于数字系统。</span><span class="sxs-lookup"><span data-stu-id="58bde-144">The digits that follow the prefix must be appropriate for the number system.</span></span> <span data-ttu-id="58bde-145">下表对此进行了说明。</span><span class="sxs-lookup"><span data-stu-id="58bde-145">The following table illustrates this.</span></span>  
  
|<span data-ttu-id="58bde-146">数字基数</span><span class="sxs-lookup"><span data-stu-id="58bde-146">Number base</span></span>|<span data-ttu-id="58bde-147">前缀</span><span class="sxs-lookup"><span data-stu-id="58bde-147">Prefix</span></span>|<span data-ttu-id="58bde-148">有效的数字值</span><span class="sxs-lookup"><span data-stu-id="58bde-148">Valid digit values</span></span>|<span data-ttu-id="58bde-149">示例</span><span class="sxs-lookup"><span data-stu-id="58bde-149">Example</span></span>|
|-----------------|------------|------------------------|-------------|
|<span data-ttu-id="58bde-150">十六进制（以 16 为基数）</span><span class="sxs-lookup"><span data-stu-id="58bde-150">Hexadecimal (base 16)</span></span>|`&H`|<span data-ttu-id="58bde-151">0-9 和 A-f</span><span class="sxs-lookup"><span data-stu-id="58bde-151">0-9 and A-F</span></span>|`&HFFFF`|
|<span data-ttu-id="58bde-152">二进制 (基数 2) </span><span class="sxs-lookup"><span data-stu-id="58bde-152">Binary (base 2)</span></span>|`&B`|<span data-ttu-id="58bde-153">0-1</span><span class="sxs-lookup"><span data-stu-id="58bde-153">0-1</span></span>|`&B01111100`|
|<span data-ttu-id="58bde-154">八进制（以 8 为基数）</span><span class="sxs-lookup"><span data-stu-id="58bde-154">Octal (base 8)</span></span>|`&O`|<span data-ttu-id="58bde-155">0-7</span><span class="sxs-lookup"><span data-stu-id="58bde-155">0-7</span></span>|`&O77`|

<span data-ttu-id="58bde-156">从 Visual Basic 2017 开始，可以使用下划线字符 (`_`) 作为组分隔符，以增强整型文本的可读性。</span><span class="sxs-lookup"><span data-stu-id="58bde-156">Starting in Visual Basic 2017, you can use the underscore character (`_`) as a group separator to enhance the readability of an integral literal.</span></span> <span data-ttu-id="58bde-157">下面的示例使用 `_` 字符将二进制文本分组到8位组中：</span><span class="sxs-lookup"><span data-stu-id="58bde-157">The following example uses the `_` character to group a binary literal into 8-bit groups:</span></span>

```vb
Dim number As Integer = &B00100010_11000101_11001111_11001101
```

<span data-ttu-id="58bde-158">您可以在文本类型为字符的后面跟有前缀的文本。</span><span class="sxs-lookup"><span data-stu-id="58bde-158">You can follow a prefixed literal with a literal type character.</span></span> <span data-ttu-id="58bde-159">下面的示例显示了这种情况。</span><span class="sxs-lookup"><span data-stu-id="58bde-159">The following example shows this.</span></span>

```vb
Dim counter As Short = &H8000S
Dim flags As UShort = &H8000US
```

<span data-ttu-id="58bde-160">在上面的示例中，的 `counter` 十进制值为-32768，其 `flags` 十进制值为 + 32768。</span><span class="sxs-lookup"><span data-stu-id="58bde-160">In the previous example, `counter` has the decimal value of -32768, and `flags` has the decimal value of +32768.</span></span>

<span data-ttu-id="58bde-161">从 Visual Basic 15.5 开始，还可以使用下划线字符 (`_`) 作为前缀和十六进制、二进制或八进制数字之间的前导分隔符。</span><span class="sxs-lookup"><span data-stu-id="58bde-161">Starting with Visual Basic 15.5, you can also use the underscore character (`_`) as a leading separator between the prefix and the hexadecimal, binary, or octal digits.</span></span> <span data-ttu-id="58bde-162">例如：</span><span class="sxs-lookup"><span data-stu-id="58bde-162">For example:</span></span>

```vb
Dim number As Integer = &H_C305_F860
```

[!INCLUDE [supporting-underscores](../../../../../includes/vb-separator-langversion.md)]

## <a name="see-also"></a><span data-ttu-id="58bde-163">请参阅</span><span class="sxs-lookup"><span data-stu-id="58bde-163">See also</span></span>

- [<span data-ttu-id="58bde-164">数据类型</span><span class="sxs-lookup"><span data-stu-id="58bde-164">Data Types</span></span>](index.md)
- [<span data-ttu-id="58bde-165">基本数据类型</span><span class="sxs-lookup"><span data-stu-id="58bde-165">Elementary Data Types</span></span>](elementary-data-types.md)
- [<span data-ttu-id="58bde-166">Value Types and Reference Types</span><span class="sxs-lookup"><span data-stu-id="58bde-166">Value Types and Reference Types</span></span>](value-types-and-reference-types.md)
- [<span data-ttu-id="58bde-167">Visual Basic 中的类型转换</span><span class="sxs-lookup"><span data-stu-id="58bde-167">Type Conversions in Visual Basic</span></span>](type-conversions.md)
- [<span data-ttu-id="58bde-168">数据类型疑难解答</span><span class="sxs-lookup"><span data-stu-id="58bde-168">Troubleshooting Data Types</span></span>](troubleshooting-data-types.md)
- [<span data-ttu-id="58bde-169">变量声明</span><span class="sxs-lookup"><span data-stu-id="58bde-169">Variable Declaration</span></span>](../variables/variable-declaration.md)
- [<span data-ttu-id="58bde-170">数据类型</span><span class="sxs-lookup"><span data-stu-id="58bde-170">Data Types</span></span>](../../../language-reference/data-types/index.md)
