---
description: 了解详细信息：如何：在 Visual Basic 中对数组进行排序
title: 如何：对数组进行排序
ms.date: 07/20/2015
f1_keywords:
- Array.Sort
helpviewer_keywords:
- arrays [Visual Basic], sorting
- examples [Visual Basic], arrays
ms.assetid: 9289aeaa-9626-4698-94a7-1d1fd3702b87
ms.openlocfilehash: ea030b63dbbb5f5ea1d6160757afe2e9b58f7c21
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100462758"
---
# <a name="how-to-sort-an-array-in-visual-basic"></a>如何：在 Visual Basic 中对数组进行排序

本文演示如何对 Visual Basic 中的字符串数组进行排序。

## <a name="example"></a>示例

此示例声明一个 `String` 名为的对象的数组 `zooAnimals` ，填充该数组，然后按字母顺序对其进行排序：
  
```vb
Private Sub SortAnimals()
    Dim zooAnimals(2) As String
    zooAnimals(0) = "lion"
    zooAnimals(1) = "turtle"
    zooAnimals(2) = "ostrich"
    Array.Sort(zooAnimals)
End Sub
```

## <a name="robust-programming"></a>可靠编程

以下情况可能会导致异常：

- 数组 (<xref:System.ArgumentNullException> 类) 为空。
- 数组是多维 (<xref:System.RankException> 类) 。
- 数组中的一个或多个元素未实现 <xref:System.IComparable> 接口 (<xref:System.InvalidOperationException> 类) 。

## <a name="see-also"></a>请参阅

- <xref:System.Array.Sort%2A?displayProperty=nameWithType>
- [数组](index.md)
- [数组疑难解答](troubleshooting-arrays.md)
- [集合](../../concepts/collections.md)
- [For Each...Next 语句](../../../language-reference/statements/for-each-next-statement.md)
