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
# <a name="arrays-c-programming-guide"></a>数组（C# 编程指南）

可以将同一类型的多个变量存储在一个数组数据结构中。 通过指定数组的元素类型来声明数组。 如果希望数组存储任意类型的元素，可将其类型指定为 `object`。 在 C# 的统一类型系统中，所有类型（预定义类型、用户定义类型、引用类型和值类型）都是直接或间接从 <xref:System.Object> 继承的。

```csharp
type[] arrayName;
```

## <a name="example"></a>示例

下面的示例创建一维数组、多维数组和交错数组：

[!code-csharp[csProgGuideArrays#1](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideArrays/CS/Arrays.cs#1)]

## <a name="array-overview"></a>数组概述

数组具有以下属性：

- 数组可以是[一维](single-dimensional-arrays.md)、[多维](multidimensional-arrays.md)或[交错](jagged-arrays.md)的。
- 创建数组实例时，将建立纬度数量和每个纬度的长度。 这些值在实例的生存期内无法更改。
- 数值数组元素的默认值设置为零，而引用元素设置为 null。
- 交错数组是数组的数组，因此其元素为引用类型且被初始化为 `null`。
- 数组从零开始编制索引：包含 `n` 元素的数组从 `0` 索引到 `n-1`。
- 数组元素可以是任何类型，其中包括数组类型。
- 数组类型是从抽象的基类型 <xref:System.Array> 派生的[引用类型](../../language-reference/keywords/reference-types.md)。 由于此类型实现 <xref:System.Collections.IEnumerable> 和 <xref:System.Collections.Generic.IEnumerable%601>，因此可以在 C# 中的所有数组上使用 [foreach](../../language-reference/keywords/foreach-in.md) 迭代。

### <a name="arrays-as-objects"></a>作为对象的数组

在 C# 中，数组实际上是对象，而不只是如在 C 和 C++ 中的连续内存的可寻址区域。 <xref:System.Array> 是所有数组类型的抽象基类型。 可以使用 <xref:System.Array> 具有的属性和其他类成员。 例如，使用 <xref:System.Array.Length%2A> 属性来获取数组的长度。 以下代码可将 `numbers` 数组的长度 `5` 分配给名为 `lengthOfNumbers` 的变量：

[!code-csharp[csProgGuideArrays#3](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideArrays/CS/Arrays.cs#3)]

<xref:System.Array> 类可提供多种其他有用的方法和属性，用于对数组进行排序、搜索和复制。 以下示例使用 <xref:System.Array.Rank%2A> 属性显示数组的维数。

[!code-csharp[csProgGuideArrays#2](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideArrays/CS/Arrays.cs#2)]

## <a name="see-also"></a>另请参阅

- [如何使用一维数组](single-dimensional-arrays.md)
- [如何使用多维数组](multidimensional-arrays.md)
- [如何使用交错数组](jagged-arrays.md)
- [对数组使用 foreach](using-foreach-with-arrays.md)
- [将数组作为参数传递](passing-arrays-as-arguments.md)
- [隐式类型的数组](implicitly-typed-arrays.md)
- [C# 编程指南](../index.md)
- [集合](../concepts/collections.md)

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]
