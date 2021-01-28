---
title: 数组 - C# 编程指南
description: 用 C# 将同一类型的多个变量存储在数组数据结构中。 通过指定类型或指定要存储任何类型的对象来声明数组。
ms.date: 01/22/2021
helpviewer_keywords:
- arrays [C#]
- C# language, arrays
ms.assetid: bb79bdde-e570-4c30-adb0-1dd5759ae041
ms.openlocfilehash: 203d8b86da4e74d8c5397132a0ba68618eedf348
ms.sourcegitcommit: 4d5e25a46aa7cd0d29b4b9227b92987354d444c4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/26/2021
ms.locfileid: "98794770"
---
# <a name="arrays-c-programming-guide"></a><span data-ttu-id="6d7be-104">数组（C# 编程指南）</span><span class="sxs-lookup"><span data-stu-id="6d7be-104">Arrays (C# Programming Guide)</span></span>

<span data-ttu-id="6d7be-105">可以将同一类型的多个变量存储在一个数组数据结构中。</span><span class="sxs-lookup"><span data-stu-id="6d7be-105">You can store multiple variables of the same type in an array data structure.</span></span> <span data-ttu-id="6d7be-106">通过指定数组的元素类型来声明数组。</span><span class="sxs-lookup"><span data-stu-id="6d7be-106">You declare an array by specifying the type of its elements.</span></span> <span data-ttu-id="6d7be-107">如果希望数组存储任意类型的元素，可将其类型指定为 `object`。</span><span class="sxs-lookup"><span data-stu-id="6d7be-107">If you want the array to store elements of any type, you can specify `object` as its type.</span></span> <span data-ttu-id="6d7be-108">在 C# 的统一类型系统中，所有类型（预定义类型、用户定义类型、引用类型和值类型）都是直接或间接从 <xref:System.Object> 继承的。</span><span class="sxs-lookup"><span data-stu-id="6d7be-108">In the unified type system of C#, all types, predefined and user-defined, reference types and value types, inherit directly or indirectly from <xref:System.Object>.</span></span>

```csharp
type[] arrayName;
```

## <a name="example"></a><span data-ttu-id="6d7be-109">示例</span><span class="sxs-lookup"><span data-stu-id="6d7be-109">Example</span></span>

<span data-ttu-id="6d7be-110">下面的示例创建一维数组、多维数组和交错数组：</span><span class="sxs-lookup"><span data-stu-id="6d7be-110">The following example creates single-dimensional, multidimensional, and jagged arrays:</span></span>

[!code-csharp[csProgGuideArrays#1](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideArrays/CS/Arrays.cs#1)]

## <a name="array-overview"></a><span data-ttu-id="6d7be-111">数组概述</span><span class="sxs-lookup"><span data-stu-id="6d7be-111">Array overview</span></span>

<span data-ttu-id="6d7be-112">数组具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="6d7be-112">An array has the following properties:</span></span>

- <span data-ttu-id="6d7be-113">数组可以是[一维](single-dimensional-arrays.md)、[多维](multidimensional-arrays.md)或[交错](jagged-arrays.md)的。</span><span class="sxs-lookup"><span data-stu-id="6d7be-113">An array can be [single-dimensional](single-dimensional-arrays.md), [multidimensional](multidimensional-arrays.md) or [jagged](jagged-arrays.md).</span></span>
- <span data-ttu-id="6d7be-114">创建数组实例时，将建立纬度数量和每个纬度的长度。</span><span class="sxs-lookup"><span data-stu-id="6d7be-114">The number of dimensions and the length of each dimension are established when the array instance is created.</span></span> <span data-ttu-id="6d7be-115">这些值在实例的生存期内无法更改。</span><span class="sxs-lookup"><span data-stu-id="6d7be-115">These values can't be changed during the lifetime of the instance.</span></span>
- <span data-ttu-id="6d7be-116">数值数组元素的默认值设置为零，而引用元素设置为 null。</span><span class="sxs-lookup"><span data-stu-id="6d7be-116">The default values of numeric array elements are set to zero, and reference elements are set to null.</span></span>
- <span data-ttu-id="6d7be-117">交错数组是数组的数组，因此其元素为引用类型且被初始化为 `null`。</span><span class="sxs-lookup"><span data-stu-id="6d7be-117">A jagged array is an array of arrays, and therefore its elements are reference types and are initialized to `null`.</span></span>
- <span data-ttu-id="6d7be-118">数组从零开始编制索引：包含 `n` 元素的数组从 `0` 索引到 `n-1`。</span><span class="sxs-lookup"><span data-stu-id="6d7be-118">Arrays are zero indexed: an array with `n` elements is indexed from `0` to `n-1`.</span></span>
- <span data-ttu-id="6d7be-119">数组元素可以是任何类型，其中包括数组类型。</span><span class="sxs-lookup"><span data-stu-id="6d7be-119">Array elements can be of any type, including an array type.</span></span>
- <span data-ttu-id="6d7be-120">数组类型是从抽象的基类型 <xref:System.Array> 派生的[引用类型](../../language-reference/keywords/reference-types.md)。</span><span class="sxs-lookup"><span data-stu-id="6d7be-120">Array types are [reference types](../../language-reference/keywords/reference-types.md) derived from the abstract base type <xref:System.Array>.</span></span> <span data-ttu-id="6d7be-121">由于此类型实现 <xref:System.Collections.IEnumerable> 和 <xref:System.Collections.Generic.IEnumerable%601>，因此可以在 C# 中的所有数组上使用 [foreach](../../language-reference/keywords/foreach-in.md) 迭代。</span><span class="sxs-lookup"><span data-stu-id="6d7be-121">Since this type implements <xref:System.Collections.IEnumerable> and <xref:System.Collections.Generic.IEnumerable%601>, you can use [foreach](../../language-reference/keywords/foreach-in.md) iteration on all arrays in C#.</span></span>

### <a name="arrays-as-objects"></a><span data-ttu-id="6d7be-122">作为对象的数组</span><span class="sxs-lookup"><span data-stu-id="6d7be-122">Arrays as Objects</span></span>

<span data-ttu-id="6d7be-123">在 C# 中，数组实际上是对象，而不只是如在 C 和 C++ 中的连续内存的可寻址区域。</span><span class="sxs-lookup"><span data-stu-id="6d7be-123">In C#, arrays are actually objects, and not just addressable regions of contiguous memory as in C and C++.</span></span> <span data-ttu-id="6d7be-124"><xref:System.Array> 是所有数组类型的抽象基类型。</span><span class="sxs-lookup"><span data-stu-id="6d7be-124"><xref:System.Array> is the abstract base type of all array types.</span></span> <span data-ttu-id="6d7be-125">可以使用 <xref:System.Array> 具有的属性和其他类成员。</span><span class="sxs-lookup"><span data-stu-id="6d7be-125">You can use the properties and other class members that <xref:System.Array> has.</span></span> <span data-ttu-id="6d7be-126">例如，使用 <xref:System.Array.Length%2A> 属性来获取数组的长度。</span><span class="sxs-lookup"><span data-stu-id="6d7be-126">An example of this is using the <xref:System.Array.Length%2A> property to get the length of an array.</span></span> <span data-ttu-id="6d7be-127">以下代码可将 `numbers` 数组的长度 `5` 分配给名为 `lengthOfNumbers` 的变量：</span><span class="sxs-lookup"><span data-stu-id="6d7be-127">The following code assigns the length of the `numbers` array, which is `5`, to a variable called `lengthOfNumbers`:</span></span>

[!code-csharp[csProgGuideArrays#3](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideArrays/CS/Arrays.cs#3)]

<span data-ttu-id="6d7be-128"><xref:System.Array> 类可提供多种其他有用的方法和属性，用于对数组进行排序、搜索和复制。</span><span class="sxs-lookup"><span data-stu-id="6d7be-128">The <xref:System.Array> class provides many other useful methods and properties for sorting, searching, and copying arrays.</span></span> <span data-ttu-id="6d7be-129">以下示例使用 <xref:System.Array.Rank%2A> 属性显示数组的维数。</span><span class="sxs-lookup"><span data-stu-id="6d7be-129">The following example uses the <xref:System.Array.Rank%2A> property to display the number of dimensions of an array.</span></span>

[!code-csharp[csProgGuideArrays#2](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideArrays/CS/Arrays.cs#2)]

## <a name="see-also"></a><span data-ttu-id="6d7be-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6d7be-130">See also</span></span>

- [<span data-ttu-id="6d7be-131">如何使用一维数组</span><span class="sxs-lookup"><span data-stu-id="6d7be-131">How to use single-dimensional arrays</span></span>](single-dimensional-arrays.md)
- [<span data-ttu-id="6d7be-132">如何使用多维数组</span><span class="sxs-lookup"><span data-stu-id="6d7be-132">How to use multi-dimensional arrays</span></span>](multidimensional-arrays.md)
- [<span data-ttu-id="6d7be-133">如何使用交错数组</span><span class="sxs-lookup"><span data-stu-id="6d7be-133">How to use jagged arrays</span></span>](jagged-arrays.md)
- [<span data-ttu-id="6d7be-134">对数组使用 foreach</span><span class="sxs-lookup"><span data-stu-id="6d7be-134">Using foreach with arrays</span></span>](using-foreach-with-arrays.md)
- [<span data-ttu-id="6d7be-135">将数组作为参数传递</span><span class="sxs-lookup"><span data-stu-id="6d7be-135">Passing arrays as arguments</span></span>](passing-arrays-as-arguments.md)
- [<span data-ttu-id="6d7be-136">隐式类型的数组</span><span class="sxs-lookup"><span data-stu-id="6d7be-136">Implicitly typed arrays</span></span>](implicitly-typed-arrays.md)
- [<span data-ttu-id="6d7be-137">C# 编程指南</span><span class="sxs-lookup"><span data-stu-id="6d7be-137">C# Programming Guide</span></span>](../index.md)
- [<span data-ttu-id="6d7be-138">集合</span><span class="sxs-lookup"><span data-stu-id="6d7be-138">Collections</span></span>](../concepts/collections.md)

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]
