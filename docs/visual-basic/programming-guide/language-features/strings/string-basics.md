---
description: 了解详细信息： Visual Basic 中的字符串基础
title: 字符串基础
ms.date: 07/20/2015
helpviewer_keywords:
- strings [Visual Basic], Like operator
- strings [Visual Basic], Visual Basic
- strings [Visual Basic], regular expressions
ms.assetid: 5674418d-f00d-4f72-9f98-d15897793350
ms.openlocfilehash: 25d76ee177e5b3eaaa8aa6b2b1b1787dc29095a1
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100424354"
---
# <a name="string-basics-in-visual-basic"></a><span data-ttu-id="686c6-103">字符串基础 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="686c6-103">String Basics in Visual Basic</span></span>

<span data-ttu-id="686c6-104">`String` 数据类型表示一系列字符（每个字符都进而表示 `Char` 数据类型的一个实例）。</span><span class="sxs-lookup"><span data-stu-id="686c6-104">The `String` data type represents a series of characters (each representing in turn an instance of the `Char` data type).</span></span> <span data-ttu-id="686c6-105">本主题介绍 Visual Basic 中的字符串的基本概念。</span><span class="sxs-lookup"><span data-stu-id="686c6-105">This topic introduces the basic concepts of strings in Visual Basic.</span></span>  
  
## <a name="string-variables"></a><span data-ttu-id="686c6-106">字符串变量</span><span class="sxs-lookup"><span data-stu-id="686c6-106">String Variables</span></span>  

 <span data-ttu-id="686c6-107">可以向字符串的实例分配表示一系列字符的文本值。</span><span class="sxs-lookup"><span data-stu-id="686c6-107">An instance of a string can be assigned a literal value that represents a series of characters.</span></span> <span data-ttu-id="686c6-108">例如：</span><span class="sxs-lookup"><span data-stu-id="686c6-108">For example:</span></span>  
  
 [!code-vb[VbVbalrStrings#63](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#63)]  
  
 <span data-ttu-id="686c6-109">`String` 变量还可以接受计算结果为字符串的任何表达式。</span><span class="sxs-lookup"><span data-stu-id="686c6-109">A `String` variable can also accept any expression that evaluates to a string.</span></span> <span data-ttu-id="686c6-110">示例如下所示：</span><span class="sxs-lookup"><span data-stu-id="686c6-110">Examples are shown below:</span></span>  
  
 [!code-vb[VbVbalrStrings#64](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#64)]  
  
 <span data-ttu-id="686c6-111">分配给 `String` 变量的任何文本都必须括在引号 ("") 内。</span><span class="sxs-lookup"><span data-stu-id="686c6-111">Any literal that is assigned to a `String` variable must be enclosed in quotation marks ("").</span></span> <span data-ttu-id="686c6-112">这意味着字符串中的引号不能使用引号进行表示。</span><span class="sxs-lookup"><span data-stu-id="686c6-112">This means that a quotation mark within a string cannot be represented by a quotation mark.</span></span> <span data-ttu-id="686c6-113">例如，下面的代码会导致编译器错误：</span><span class="sxs-lookup"><span data-stu-id="686c6-113">For example, the following code causes a compiler error:</span></span>  
  
 [!code-vb[VbVbalrStrings#65](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#65)]  
  
 <span data-ttu-id="686c6-114">此代码会导致错误，因为编译器会在第二个引号之后终止字符串，字符串的其余部分会解释为代码。</span><span class="sxs-lookup"><span data-stu-id="686c6-114">This code causes an error because the compiler terminates the string after the second quotation mark, and the remainder of the string is interpreted as code.</span></span> <span data-ttu-id="686c6-115">若要解决此问题，Visual Basic 将字符串文本中的两个引号解释为字符串中的一个引号。</span><span class="sxs-lookup"><span data-stu-id="686c6-115">To solve this problem, Visual Basic interprets two quotation marks in a string literal as one quotation mark in the string.</span></span> <span data-ttu-id="686c6-116">下面的示例演示在字符串中包含引号的正确方法：</span><span class="sxs-lookup"><span data-stu-id="686c6-116">The following example demonstrates the correct way to include a quotation mark in a string:</span></span>  
  
 [!code-vb[VbVbalrStrings#66](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#66)]  
  
 <span data-ttu-id="686c6-117">在上面的示例中，字词 `Look` 前面的两个引号会成为字符串中的一个引号。</span><span class="sxs-lookup"><span data-stu-id="686c6-117">In the preceding example, the two quotation marks preceding the word `Look` become one quotation mark in the string.</span></span> <span data-ttu-id="686c6-118">行尾的三个引号表示字符串中的一个引号和字符串终止符。</span><span class="sxs-lookup"><span data-stu-id="686c6-118">The three quotation marks at the end of the line represent one quotation mark in the string and the string termination character.</span></span>  
  
 <span data-ttu-id="686c6-119">字符串可以包含多行：</span><span class="sxs-lookup"><span data-stu-id="686c6-119">String literals can contain multiple lines:</span></span>  
  
```vb  
Dim x = "hello  
world"  
```  
  
 <span data-ttu-id="686c6-120">生成的字符串包含在字符串中使用的换行符序列（vbcr、vbcrlf 等）。</span><span class="sxs-lookup"><span data-stu-id="686c6-120">The resulting string contains newline sequences that you used in your string literal (vbcr, vbcrlf, etc.).</span></span>  <span data-ttu-id="686c6-121">不再需要使用旧的解决方法：</span><span class="sxs-lookup"><span data-stu-id="686c6-121">You no longer need to use the old workaround:</span></span>  
  
```vb  
Dim x = <xml><![CDATA[Hello  
World]]></xml>.Value  
```  
  
## <a name="characters-in-strings"></a><span data-ttu-id="686c6-122">字符串中的字符</span><span class="sxs-lookup"><span data-stu-id="686c6-122">Characters in Strings</span></span>  

 <span data-ttu-id="686c6-123">可以将字符串视为一系列 `Char` 值，`String` 类型具有内置函数，可用于对字符串执行很多操作（类似于数组允许的操作）。</span><span class="sxs-lookup"><span data-stu-id="686c6-123">A string can be thought of as a series of `Char` values, and the `String` type has built-in functions that allow you to perform many manipulations on a string that resemble the manipulations allowed by arrays.</span></span> <span data-ttu-id="686c6-124">与 .NET Framework 中的所有数组一样，这些是从零开始的数组。</span><span class="sxs-lookup"><span data-stu-id="686c6-124">Like all array in .NET Framework, these are zero-based arrays.</span></span> <span data-ttu-id="686c6-125">还可以通过 `Chars` 属性引用字符串中的特定字符，该属性提供了一种方法，用于通过字符在字符串中出现的位置来访问它。</span><span class="sxs-lookup"><span data-stu-id="686c6-125">You may refer to a specific character in a string through the `Chars` property, which provides a way to access a character by the position in which it appears in the string.</span></span> <span data-ttu-id="686c6-126">例如：</span><span class="sxs-lookup"><span data-stu-id="686c6-126">For example:</span></span>  
  
 [!code-vb[VbVbalrStrings#67](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#67)]  
  
 <span data-ttu-id="686c6-127">在上面的示例中，字符串的 `Chars` 属性返回字符串中的第四个字符（即 `D`），并将它分配给 `myChar`。</span><span class="sxs-lookup"><span data-stu-id="686c6-127">In the above example, the `Chars` property of the string returns the fourth character in the string, which is `D`, and assigns it to `myChar`.</span></span> <span data-ttu-id="686c6-128">还可以通过 `Length` 属性获取特定字符串的长度。</span><span class="sxs-lookup"><span data-stu-id="686c6-128">You can also get the length of a particular string through the `Length` property.</span></span> <span data-ttu-id="686c6-129">如果需要对字符串执行多个数组类型的操作，则可以使用字符串的 `ToCharArray` 函数将它转换为 `Char` 实例的数组。</span><span class="sxs-lookup"><span data-stu-id="686c6-129">If you need to perform multiple array-type manipulations on a string, you can convert it to an array of `Char` instances using the `ToCharArray` function of the string.</span></span> <span data-ttu-id="686c6-130">例如：</span><span class="sxs-lookup"><span data-stu-id="686c6-130">For example:</span></span>  
  
 [!code-vb[VbVbalrStrings#68](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#68)]  
  
 <span data-ttu-id="686c6-131">变量 `myArray` 现在包含 `Char` 值的数组，其中每个值都表示 `myString` 中的一个字符。</span><span class="sxs-lookup"><span data-stu-id="686c6-131">The variable `myArray` now contains an array of `Char` values, each representing a character from `myString`.</span></span>  
  
## <a name="the-immutability-of-strings"></a><span data-ttu-id="686c6-132">字符串的不可变性</span><span class="sxs-lookup"><span data-stu-id="686c6-132">The Immutability of Strings</span></span>  

 <span data-ttu-id="686c6-133">字符串是 *不可变* 的，这意味着在创建后，不能更改其值。</span><span class="sxs-lookup"><span data-stu-id="686c6-133">A string is *immutable*, which means its value cannot be changed once it has been created.</span></span> <span data-ttu-id="686c6-134">但是，这不会阻止你将多个值分配给字符串变量。</span><span class="sxs-lookup"><span data-stu-id="686c6-134">However, this does not prevent you from assigning more than one value to a string variable.</span></span> <span data-ttu-id="686c6-135">请看下面的示例：</span><span class="sxs-lookup"><span data-stu-id="686c6-135">Consider the following example:</span></span>  
  
 [!code-vb[VbVbalrStrings#69](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStrings/VB/Class2.vb#69)]  
  
 <span data-ttu-id="686c6-136">这里会创建一个字符串变量（向它提供值），然后更改其值。</span><span class="sxs-lookup"><span data-stu-id="686c6-136">Here, a string variable is created, given a value, and then its value is changed.</span></span>  
  
 <span data-ttu-id="686c6-137">更具体地说，在第一行中，会创建类型 `String` 的实例，并提供值 `This string is immutable`。</span><span class="sxs-lookup"><span data-stu-id="686c6-137">More specifically, in the first line, an instance of type `String` is created and given the value `This string is immutable`.</span></span> <span data-ttu-id="686c6-138">在示例的第二个行中，会创建一个新实例并向它提供值 `Or is it?`，字符串变量会放弃它对第一个实例的引用，并存储对新实例的引用。</span><span class="sxs-lookup"><span data-stu-id="686c6-138">In the second line of the example, a new instance is created and given the value `Or is it?`, and the string variable discards its reference to the first instance and stores a reference to the new instance.</span></span>  
  
 <span data-ttu-id="686c6-139">与其他内部数据类型不同，`String` 是引用类型。</span><span class="sxs-lookup"><span data-stu-id="686c6-139">Unlike other intrinsic data types, `String` is a reference type.</span></span> <span data-ttu-id="686c6-140">当引用类型的变量作为参数传递给函数或子例程时，会传递对数据存储位置的内存地址的引用（而不是字符串的实际值）。</span><span class="sxs-lookup"><span data-stu-id="686c6-140">When a variable of reference type is passed as an argument to a function or subroutine, a reference to the memory address where the data is stored is passed instead of the actual value of the string.</span></span> <span data-ttu-id="686c6-141">因此在上面的示例中，变量的名称保持不变，但它会指向 `String` 类的另一个新实例（该实例会保存新值）。</span><span class="sxs-lookup"><span data-stu-id="686c6-141">So in the previous example, the name of the variable remains the same, but it points to a new and different instance of the `String` class, which holds the new value.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="686c6-142">请参阅</span><span class="sxs-lookup"><span data-stu-id="686c6-142">See also</span></span>

- [<span data-ttu-id="686c6-143">字符串介绍 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="686c6-143">Introduction to Strings in Visual Basic</span></span>](introduction-to-strings.md)
- [<span data-ttu-id="686c6-144">String 数据类型</span><span class="sxs-lookup"><span data-stu-id="686c6-144">String Data Type</span></span>](../../../language-reference/data-types/string-data-type.md)
- [<span data-ttu-id="686c6-145">Char 数据类型</span><span class="sxs-lookup"><span data-stu-id="686c6-145">Char Data Type</span></span>](../../../language-reference/data-types/char-data-type.md)
- [<span data-ttu-id="686c6-146">基本字符串操作</span><span class="sxs-lookup"><span data-stu-id="686c6-146">Basic String Operations</span></span>](../../../../standard/base-types/basic-string-operations.md)
