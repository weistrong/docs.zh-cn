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
# <a name="how-to-sort-an-array-in-visual-basic"></a><span data-ttu-id="e5afe-103">如何：在 Visual Basic 中对数组进行排序</span><span class="sxs-lookup"><span data-stu-id="e5afe-103">How to: sort an array in Visual Basic</span></span>

<span data-ttu-id="e5afe-104">本文演示如何对 Visual Basic 中的字符串数组进行排序。</span><span class="sxs-lookup"><span data-stu-id="e5afe-104">This article shows an example of how to sort an array of strings in Visual Basic.</span></span>

## <a name="example"></a><span data-ttu-id="e5afe-105">示例</span><span class="sxs-lookup"><span data-stu-id="e5afe-105">Example</span></span>

<span data-ttu-id="e5afe-106">此示例声明一个 `String` 名为的对象的数组 `zooAnimals` ，填充该数组，然后按字母顺序对其进行排序：</span><span class="sxs-lookup"><span data-stu-id="e5afe-106">This example declares an array of `String` objects named `zooAnimals`, populates it, and then sorts it alphabetically:</span></span>
  
```vb
Private Sub SortAnimals()
    Dim zooAnimals(2) As String
    zooAnimals(0) = "lion"
    zooAnimals(1) = "turtle"
    zooAnimals(2) = "ostrich"
    Array.Sort(zooAnimals)
End Sub
```

## <a name="robust-programming"></a><span data-ttu-id="e5afe-107">可靠编程</span><span class="sxs-lookup"><span data-stu-id="e5afe-107">Robust programming</span></span>

<span data-ttu-id="e5afe-108">以下情况可能会导致异常：</span><span class="sxs-lookup"><span data-stu-id="e5afe-108">The following conditions may cause an exception:</span></span>

- <span data-ttu-id="e5afe-109">数组 (<xref:System.ArgumentNullException> 类) 为空。</span><span class="sxs-lookup"><span data-stu-id="e5afe-109">Array is empty (<xref:System.ArgumentNullException> class).</span></span>
- <span data-ttu-id="e5afe-110">数组是多维 (<xref:System.RankException> 类) 。</span><span class="sxs-lookup"><span data-stu-id="e5afe-110">Array is multidimensional (<xref:System.RankException> class).</span></span>
- <span data-ttu-id="e5afe-111">数组中的一个或多个元素未实现 <xref:System.IComparable> 接口 (<xref:System.InvalidOperationException> 类) 。</span><span class="sxs-lookup"><span data-stu-id="e5afe-111">One or more elements of the array don't implement the <xref:System.IComparable> interface (<xref:System.InvalidOperationException> class).</span></span>

## <a name="see-also"></a><span data-ttu-id="e5afe-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="e5afe-112">See also</span></span>

- <xref:System.Array.Sort%2A?displayProperty=nameWithType>
- [<span data-ttu-id="e5afe-113">数组</span><span class="sxs-lookup"><span data-stu-id="e5afe-113">Arrays</span></span>](index.md)
- [<span data-ttu-id="e5afe-114">数组疑难解答</span><span class="sxs-lookup"><span data-stu-id="e5afe-114">Troubleshooting Arrays</span></span>](troubleshooting-arrays.md)
- [<span data-ttu-id="e5afe-115">集合</span><span class="sxs-lookup"><span data-stu-id="e5afe-115">Collections</span></span>](../../concepts/collections.md)
- [<span data-ttu-id="e5afe-116">For Each...Next 语句</span><span class="sxs-lookup"><span data-stu-id="e5afe-116">For Each...Next Statement</span></span>](../../../language-reference/statements/for-each-next-statement.md)
