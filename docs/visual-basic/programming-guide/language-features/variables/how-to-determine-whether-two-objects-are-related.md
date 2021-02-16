---
description: '了解有关详细信息，请参阅如何：确定两个对象是否与 (Visual Basic 相关) '
title: 如何：确定两个对象是否相关
ms.date: 07/20/2015
helpviewer_keywords:
- inheritance [Visual Basic], Visual Basic objects
- objects [Visual Basic], inheritance
- object variables [Visual Basic], determining relation
ms.assetid: da002e3f-6616-4bad-a229-f842d06652bb
ms.openlocfilehash: 79a6dae83cc780a3aed64fd40fb284e7479ffacc
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100481903"
---
# <a name="how-to-determine-whether-two-objects-are-related-visual-basic"></a><span data-ttu-id="1f1a4-103">如何：确定两个对象是否相关 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="1f1a4-103">How to: Determine Whether Two Objects Are Related (Visual Basic)</span></span>

<span data-ttu-id="1f1a4-104">您可以比较两个对象，以确定从中创建它们的类之间的关系（如果有）。</span><span class="sxs-lookup"><span data-stu-id="1f1a4-104">You can compare two objects to determine the relationship, if any, between the classes from which they are created.</span></span> <span data-ttu-id="1f1a4-105"><xref:System.Type.IsInstanceOfType%2A> <xref:System.Type?displayProperty=nameWithType> `True` 如果指定的类从当前类继承，或者当前类型是指定的类所支持的接口，则类的方法将返回。</span><span class="sxs-lookup"><span data-stu-id="1f1a4-105">The <xref:System.Type.IsInstanceOfType%2A> method of the <xref:System.Type?displayProperty=nameWithType> class returns `True` if the specified class inherits from the current class, or if the current type is an interface supported by the specified class.</span></span>

### <a name="to-determine-if-one-object-inherits-from-another-objects-class-or-interface"></a><span data-ttu-id="1f1a4-106">确定一个对象是否继承自另一个对象的类或接口</span><span class="sxs-lookup"><span data-stu-id="1f1a4-106">To determine if one object inherits from another object's class or interface</span></span>

1. <span data-ttu-id="1f1a4-107">在您认为可能是基类型的对象上调用 <xref:System.Object.GetType%2A> 方法。</span><span class="sxs-lookup"><span data-stu-id="1f1a4-107">On the object you think might be of the base type, invoke the <xref:System.Object.GetType%2A> method.</span></span>

2. <span data-ttu-id="1f1a4-108">在 <xref:System.Type?displayProperty=nameWithType> 返回的对象上 <xref:System.Object.GetType%2A> 调用 <xref:System.Type.IsInstanceOfType%2A> 方法。</span><span class="sxs-lookup"><span data-stu-id="1f1a4-108">On the <xref:System.Type?displayProperty=nameWithType> object returned by <xref:System.Object.GetType%2A>, invoke the <xref:System.Type.IsInstanceOfType%2A> method.</span></span>

3. <span data-ttu-id="1f1a4-109">在的参数列表中 <xref:System.Type.IsInstanceOfType%2A> ，指定你认为可能是派生类型的对象。</span><span class="sxs-lookup"><span data-stu-id="1f1a4-109">In the argument list for <xref:System.Type.IsInstanceOfType%2A>, specify the object you think might be of the derived type.</span></span>

    <span data-ttu-id="1f1a4-110"><xref:System.Type.IsInstanceOfType%2A>`True`如果其参数类型继承自对象类型，则返回 <xref:System.Type?displayProperty=nameWithType> 。</span><span class="sxs-lookup"><span data-stu-id="1f1a4-110"><xref:System.Type.IsInstanceOfType%2A> returns `True` if its argument type inherits from the <xref:System.Type?displayProperty=nameWithType> object type.</span></span>

## <a name="example"></a><span data-ttu-id="1f1a4-111">示例</span><span class="sxs-lookup"><span data-stu-id="1f1a4-111">Example</span></span>

 <span data-ttu-id="1f1a4-112">下面的示例确定一个对象是否表示一个派生自另一个对象的类的类。</span><span class="sxs-lookup"><span data-stu-id="1f1a4-112">The following example determines whether one object represents a class derived from another object's class.</span></span>

```vb
Public Class baseClass
End Class
Public Class derivedClass : Inherits baseClass
End Class
Public Class testTheseClasses
    Public Sub seeIfRelated()
        Dim baseObj As Object = New baseClass()
        Dim derivedObj As Object = New derivedClass()
        Dim related As Boolean
        related = baseObj.GetType().IsInstanceOfType(derivedObj)
        MsgBox(CStr(related))
    End Sub
End Class
```

<span data-ttu-id="1f1a4-113">请注意调用中的两个对象变量的意外位置 <xref:System.Type.IsInstanceOfType%2A> 。</span><span class="sxs-lookup"><span data-stu-id="1f1a4-113">Note the unexpected placement of the two object variables in the call to <xref:System.Type.IsInstanceOfType%2A>.</span></span> <span data-ttu-id="1f1a4-114">假定的基类型用于生成 <xref:System.Type?displayProperty=nameWithType> 类，假设派生类型作为参数传递给 <xref:System.Type.IsInstanceOfType%2A> 方法。</span><span class="sxs-lookup"><span data-stu-id="1f1a4-114">The supposed base type is used to generate the <xref:System.Type?displayProperty=nameWithType> class, and the supposed derived type is passed as an argument to the <xref:System.Type.IsInstanceOfType%2A> method.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f1a4-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="1f1a4-115">See also</span></span>

- <xref:System.Object.GetType%2A>
- <xref:System.Type?displayProperty=nameWithType>
- <xref:System.Type.IsInstanceOfType%2A>
- [<span data-ttu-id="1f1a4-116">Object Data Type</span><span class="sxs-lookup"><span data-stu-id="1f1a4-116">Object Data Type</span></span>](../../../language-reference/data-types/object-data-type.md)
- [<span data-ttu-id="1f1a4-117">对象变量</span><span class="sxs-lookup"><span data-stu-id="1f1a4-117">Object Variables</span></span>](object-variables.md)
- [<span data-ttu-id="1f1a4-118">对象变量值</span><span class="sxs-lookup"><span data-stu-id="1f1a4-118">Object Variable Values</span></span>](object-variable-values.md)
- [<span data-ttu-id="1f1a4-119">如何：确定两个对象是否相同</span><span class="sxs-lookup"><span data-stu-id="1f1a4-119">How to: Determine Whether Two Objects Are Identical</span></span>](how-to-determine-whether-two-objects-are-identical.md)
