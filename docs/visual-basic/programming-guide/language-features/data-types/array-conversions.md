---
description: '了解详细信息：数组转换 (Visual Basic) '
title: 数组转换
ms.date: 07/20/2015
helpviewer_keywords:
- arrays [Visual Basic], converting type
- type conversion [Visual Basic], arrays
- conversions [Visual Basic], type
- arrays [Visual Basic], data types
- conversions [Visual Basic], data type
- object arrays [Visual Basic], converting type
- data type conversion [Visual Basic], array conversions
- conversions [Visual Basic], array types
- object arrays
ms.assetid: fceff7d2-a1b7-44c7-b9aa-8bd831d8a444
ms.openlocfilehash: 1600042e1d41cbc2bd52468544db0e806e776d9c
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100466401"
---
# <a name="array-conversions-visual-basic"></a><span data-ttu-id="5a3b6-103">数组转换 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="5a3b6-103">Array Conversions (Visual Basic)</span></span>

<span data-ttu-id="5a3b6-104">如果满足以下条件，则可以将数组类型转换为不同的数组类型：</span><span class="sxs-lookup"><span data-stu-id="5a3b6-104">You can convert an array type to a different array type provided you meet the following conditions:</span></span>  
  
- <span data-ttu-id="5a3b6-105">**秩相等。**</span><span class="sxs-lookup"><span data-stu-id="5a3b6-105">**Equal Rank.**</span></span> <span data-ttu-id="5a3b6-106">两个数组的秩必须相同，也就是说，它们必须具有相同的维数。</span><span class="sxs-lookup"><span data-stu-id="5a3b6-106">The ranks of the two arrays must be the same, that is, they must have the same number of dimensions.</span></span> <span data-ttu-id="5a3b6-107">但是，各个维度的长度不必相同。</span><span class="sxs-lookup"><span data-stu-id="5a3b6-107">However, the lengths of the respective dimensions do not need to be the same.</span></span>  
  
- <span data-ttu-id="5a3b6-108">**元素数据类型。**</span><span class="sxs-lookup"><span data-stu-id="5a3b6-108">**Element Data Type.**</span></span> <span data-ttu-id="5a3b6-109">这两个数组的元素的数据类型必须是引用类型。</span><span class="sxs-lookup"><span data-stu-id="5a3b6-109">The data types of the elements of both arrays must be reference types.</span></span> <span data-ttu-id="5a3b6-110">`Integer` `Long` `Object` 由于至少涉及一种值类型，因此不能将数组转换为数组，甚至不能转换为数组。</span><span class="sxs-lookup"><span data-stu-id="5a3b6-110">You cannot convert an `Integer` array to a `Long` array, or even to an `Object` array, because at least one value type is involved.</span></span> <span data-ttu-id="5a3b6-111">有关详细信息，请参阅 [值类型和引用类型](value-types-and-reference-types.md)。</span><span class="sxs-lookup"><span data-stu-id="5a3b6-111">For more information, see [Value Types and Reference Types](value-types-and-reference-types.md).</span></span>  
  
- <span data-ttu-id="5a3b6-112">**Convertibility.**</span><span class="sxs-lookup"><span data-stu-id="5a3b6-112">**Convertibility.**</span></span> <span data-ttu-id="5a3b6-113">可以在两个数组的元素类型之间进行扩大或收缩转换。</span><span class="sxs-lookup"><span data-stu-id="5a3b6-113">A conversion, either widening or narrowing, must be possible between the element types of the two arrays.</span></span> <span data-ttu-id="5a3b6-114">未能满足此要求的一个示例是在 `String` 数组和从派生的类的数组之间尝试转换 <xref:System.Attribute?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="5a3b6-114">An example that fails this requirement is an attempted conversion between a `String` array and an array of a class derived from <xref:System.Attribute?displayProperty=nameWithType>.</span></span> <span data-ttu-id="5a3b6-115">这两种类型共有，它们之间不存在任何类型的转换。</span><span class="sxs-lookup"><span data-stu-id="5a3b6-115">These two types have nothing in common, and no conversion of any kind exists between them.</span></span>  
  
 <span data-ttu-id="5a3b6-116">将一个数组类型转换为另一个数组类型是扩大或收缩，这取决于各个元素的转换是扩大还是收缩。</span><span class="sxs-lookup"><span data-stu-id="5a3b6-116">A conversion of one array type to another is widening or narrowing depending on whether the conversion of the respective elements is widening or narrowing.</span></span> <span data-ttu-id="5a3b6-117">有关详细信息，请参阅 [Widening and Narrowing Conversions](widening-and-narrowing-conversions.md)。</span><span class="sxs-lookup"><span data-stu-id="5a3b6-117">For more information, see [Widening and Narrowing Conversions](widening-and-narrowing-conversions.md).</span></span>  
  
## <a name="conversion-to-an-object-array"></a><span data-ttu-id="5a3b6-118">转换为对象数组</span><span class="sxs-lookup"><span data-stu-id="5a3b6-118">Conversion to an Object Array</span></span>  

 <span data-ttu-id="5a3b6-119">在 `Object` 不初始化数组的情况下声明数组时，其元素类型将 `Object` 保持未初始化状态。</span><span class="sxs-lookup"><span data-stu-id="5a3b6-119">When you declare an `Object` array without initializing it, its element type is `Object` as long as it remains uninitialized.</span></span> <span data-ttu-id="5a3b6-120">将其设置为特定类的数组时，它将采用该类的类型。</span><span class="sxs-lookup"><span data-stu-id="5a3b6-120">When you set it to an array of a specific class, it takes on the type of that class.</span></span> <span data-ttu-id="5a3b6-121">但是，它的基础类型仍为 `Object` ，你随后可以将其设置为不相关的类的另一个数组。</span><span class="sxs-lookup"><span data-stu-id="5a3b6-121">However, its underlying type is still `Object`, and you can subsequently set it to another array of an unrelated class.</span></span> <span data-ttu-id="5a3b6-122">由于所有类均派生自 `Object` ，因此可以将数组的元素类型从任何类更改为任何其他类。</span><span class="sxs-lookup"><span data-stu-id="5a3b6-122">Since all classes derive from `Object`, you can change the array's element type from any class to any other class.</span></span>  
  
 <span data-ttu-id="5a3b6-123">在下面的示例中，类型与之间不存在转换 `student` `String` ，但均派生自 `Object` ，因此所有分配都有效。</span><span class="sxs-lookup"><span data-stu-id="5a3b6-123">In the following example, no conversion exists between types `student` and `String`, but both derive from `Object`, so all assignments are valid.</span></span>  
  
```vb  
' Assume student has already been defined as a class.  
Dim testArray() As Object  
' testArray is still an Object array at this point.  
Dim names() As String = New String(3) {"Name0", "Name1", "Name2", "Name3"}  
testArray = New student(3) {}  
' testArray is now of type student().  
testArray = names  
' testArray is now a String array.  
```  
  
### <a name="underlying-type-of-an-array"></a><span data-ttu-id="5a3b6-124">数组的基础类型</span><span class="sxs-lookup"><span data-stu-id="5a3b6-124">Underlying Type of an Array</span></span>  

 <span data-ttu-id="5a3b6-125">如果最初使用特定类声明数组，则其基础元素类型为该类。</span><span class="sxs-lookup"><span data-stu-id="5a3b6-125">If you originally declare an array with a specific class, its underlying element type is that class.</span></span> <span data-ttu-id="5a3b6-126">如果随后将其设置为另一个类的数组，则这两个类之间必须存在转换。</span><span class="sxs-lookup"><span data-stu-id="5a3b6-126">If you subsequently set it to an array of another class, there must be a conversion between the two classes.</span></span>  
  
 <span data-ttu-id="5a3b6-127">在下面的示例中， `students` 是一个 `student` 数组。</span><span class="sxs-lookup"><span data-stu-id="5a3b6-127">In the following example, `students` is a `student` array.</span></span> <span data-ttu-id="5a3b6-128">由于与之间不存在 `String` 转换 `student` ，因此最后一个语句会失败。</span><span class="sxs-lookup"><span data-stu-id="5a3b6-128">Since no conversion exists between `String` and `student`, the last statement fails.</span></span>  
  
```vb  
Dim students() As student  
Dim names() As String = New String(3) {"Name0", "Name1", "Name2", "Name3"}  
students = New Student(3) {}  
' The following statement fails at compile time.  
students = names  
```  
  
## <a name="see-also"></a><span data-ttu-id="5a3b6-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="5a3b6-129">See also</span></span>

- [<span data-ttu-id="5a3b6-130">数据类型</span><span class="sxs-lookup"><span data-stu-id="5a3b6-130">Data Types</span></span>](index.md)
- [<span data-ttu-id="5a3b6-131">Visual Basic 中的类型转换</span><span class="sxs-lookup"><span data-stu-id="5a3b6-131">Type Conversions in Visual Basic</span></span>](type-conversions.md)
- [<span data-ttu-id="5a3b6-132">隐式转换和显式转换</span><span class="sxs-lookup"><span data-stu-id="5a3b6-132">Implicit and Explicit Conversions</span></span>](implicit-and-explicit-conversions.md)
- [<span data-ttu-id="5a3b6-133">字符串和其他类型之间的转换</span><span class="sxs-lookup"><span data-stu-id="5a3b6-133">Conversions Between Strings and Other Types</span></span>](conversions-between-strings-and-other-types.md)
- [<span data-ttu-id="5a3b6-134">如何：在 Visual Basic 中将一个对象转换为其他类型</span><span class="sxs-lookup"><span data-stu-id="5a3b6-134">How to: Convert an Object to Another Type in Visual Basic</span></span>](how-to-convert-an-object-to-another-type.md)
- [<span data-ttu-id="5a3b6-135">数据类型</span><span class="sxs-lookup"><span data-stu-id="5a3b6-135">Data Types</span></span>](../../../language-reference/data-types/index.md)
- [<span data-ttu-id="5a3b6-136">Type Conversion Functions</span><span class="sxs-lookup"><span data-stu-id="5a3b6-136">Type Conversion Functions</span></span>](../../../language-reference/functions/type-conversion-functions.md)
- [<span data-ttu-id="5a3b6-137">数组</span><span class="sxs-lookup"><span data-stu-id="5a3b6-137">Arrays</span></span>](../arrays/index.md)
