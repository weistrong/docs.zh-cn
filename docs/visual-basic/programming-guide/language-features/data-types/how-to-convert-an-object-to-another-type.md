---
description: 了解有关详细信息，请参阅如何：在 Visual Basic 中将对象转换为另一种类型
title: 如何：将一个对象转换为其他类型
ms.date: 07/20/2015
helpviewer_keywords:
- objects [Visual Basic], converting
ms.assetid: 60cb5fc7-7ba4-4ab5-9c24-480fa12ddcdc
ms.openlocfilehash: d6840cfd440483720f8ca9a0fa0140c3727a8688
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100484023"
---
# <a name="how-to-convert-an-object-to-another-type-in-visual-basic"></a><span data-ttu-id="2f661-103">如何：在 Visual Basic 中将一个对象转换为其他类型</span><span class="sxs-lookup"><span data-stu-id="2f661-103">How to: Convert an Object to Another Type in Visual Basic</span></span>

<span data-ttu-id="2f661-104">您可以 `Object` 使用转换关键字（如 [CType 函数](../../../language-reference/functions/ctype-function.md)）将变量转换为另一种数据类型。</span><span class="sxs-lookup"><span data-stu-id="2f661-104">You convert an `Object` variable to another data type by using a conversion keyword such as [CType Function](../../../language-reference/functions/ctype-function.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="2f661-105">示例</span><span class="sxs-lookup"><span data-stu-id="2f661-105">Example</span></span>  

 <span data-ttu-id="2f661-106">下面的示例将 `Object` 变量转换为 `Integer` 和 `String` 。</span><span class="sxs-lookup"><span data-stu-id="2f661-106">The following example converts an `Object` variable to an `Integer` and a `String`.</span></span>  
  
```vb  
Public Sub objectConversion(ByVal anObject As Object)  
    Dim anInteger As Integer  
    Dim aString As String  
    anInteger = CType(anObject, Integer)  
    aString = CType(anObject, String)  
End Sub  
```  
  
 <span data-ttu-id="2f661-107">如果知道变量的内容属于 `Object` 特定的数据类型，最好将该变量转换为该数据类型。</span><span class="sxs-lookup"><span data-stu-id="2f661-107">If you know that the contents of an `Object` variable are of a particular data type, it is better to convert the variable to that data type.</span></span> <span data-ttu-id="2f661-108">如果继续使用该 `Object` 变量，则将对值类型进行 *装箱* 和 *取消装箱* 操作 () 或 (引用类型) 的 *后期绑定* 。</span><span class="sxs-lookup"><span data-stu-id="2f661-108">If you continue to use the `Object` variable, you incur either *boxing* and *unboxing* (for a value type) or *late binding* (for a reference type).</span></span> <span data-ttu-id="2f661-109">这些操作都需要额外的执行时间，并使性能更慢。</span><span class="sxs-lookup"><span data-stu-id="2f661-109">These operations all take extra execution time and make your performance slower.</span></span>  
  
## <a name="compile-the-code"></a><span data-ttu-id="2f661-110">编译代码</span><span class="sxs-lookup"><span data-stu-id="2f661-110">Compile the code</span></span>  

 <span data-ttu-id="2f661-111">此示例需要：</span><span class="sxs-lookup"><span data-stu-id="2f661-111">This example requires:</span></span>  
  
- <span data-ttu-id="2f661-112">对 <xref:System?displayProperty=nameWithType> 命名空间的引用。</span><span class="sxs-lookup"><span data-stu-id="2f661-112">A reference to the <xref:System?displayProperty=nameWithType> namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2f661-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="2f661-113">See also</span></span>

- <xref:System.Object>
- [<span data-ttu-id="2f661-114">Visual Basic 中的类型转换</span><span class="sxs-lookup"><span data-stu-id="2f661-114">Type Conversions in Visual Basic</span></span>](type-conversions.md)
- [<span data-ttu-id="2f661-115">Widening and Narrowing Conversions</span><span class="sxs-lookup"><span data-stu-id="2f661-115">Widening and Narrowing Conversions</span></span>](widening-and-narrowing-conversions.md)
- [<span data-ttu-id="2f661-116">隐式转换和显式转换</span><span class="sxs-lookup"><span data-stu-id="2f661-116">Implicit and Explicit Conversions</span></span>](implicit-and-explicit-conversions.md)
- [<span data-ttu-id="2f661-117">字符串和其他类型之间的转换</span><span class="sxs-lookup"><span data-stu-id="2f661-117">Conversions Between Strings and Other Types</span></span>](conversions-between-strings-and-other-types.md)
- [<span data-ttu-id="2f661-118">数组转换</span><span class="sxs-lookup"><span data-stu-id="2f661-118">Array Conversions</span></span>](array-conversions.md)
- [<span data-ttu-id="2f661-119">结构</span><span class="sxs-lookup"><span data-stu-id="2f661-119">Structures</span></span>](structures.md)
- [<span data-ttu-id="2f661-120">数据类型</span><span class="sxs-lookup"><span data-stu-id="2f661-120">Data Types</span></span>](../../../language-reference/data-types/index.md)
- [<span data-ttu-id="2f661-121">Type Conversion Functions</span><span class="sxs-lookup"><span data-stu-id="2f661-121">Type Conversion Functions</span></span>](../../../language-reference/functions/type-conversion-functions.md)
