---
description: '了解详细信息：创建自定义属性 (Visual Basic) '
title: 创建自定义特性
ms.date: 07/20/2015
ms.assetid: 5c9ef584-6c7c-496b-92a9-6e42f8d9ca28
ms.openlocfilehash: e989a4ce219609aafcec90d12f9d460681e98be9
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100437769"
---
# <a name="creating-custom-attributes-visual-basic"></a><span data-ttu-id="e06be-103">创建自定义特性 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e06be-103">Creating Custom Attributes (Visual Basic)</span></span>

<span data-ttu-id="e06be-104">可通过定义特性类创建自己的自定义特性，特性类是直接或间接派生自 <xref:System.Attribute> 的类，可快速轻松地识别元数据中的特性定义。</span><span class="sxs-lookup"><span data-stu-id="e06be-104">You can create your own custom attributes by defining an attribute class, a class that derives directly or indirectly from <xref:System.Attribute>, which makes identifying attribute definitions in metadata fast and easy.</span></span> <span data-ttu-id="e06be-105">假设希望使用编写类型的程序员的姓名来标记该类型。</span><span class="sxs-lookup"><span data-stu-id="e06be-105">Suppose you want to tag types with the name of the programmer who wrote the type.</span></span> <span data-ttu-id="e06be-106">可能需要定义一个自定义 `Author` 特性类：</span><span class="sxs-lookup"><span data-stu-id="e06be-106">You might define a custom `Author` attribute class:</span></span>

```vb
<System.AttributeUsage(System.AttributeTargets.Class Or
                       System.AttributeTargets.Struct)>
Public Class Author
    Inherits System.Attribute
    Private name As String
    Public version As Double
    Sub New(ByVal authorName As String)
        name = authorName
        version = 1.0
    End Sub
End Class
```

<span data-ttu-id="e06be-107">类名是该特性的名称，即 `Author`。</span><span class="sxs-lookup"><span data-stu-id="e06be-107">The class name is the attribute's name, `Author`.</span></span> <span data-ttu-id="e06be-108">由于该类派生自 `System.Attribute`，因此它是一个自定义特性类。</span><span class="sxs-lookup"><span data-stu-id="e06be-108">It is derived from `System.Attribute`, so it is a custom attribute class.</span></span> <span data-ttu-id="e06be-109">构造函数的参数是自定义特性的位置参数。</span><span class="sxs-lookup"><span data-stu-id="e06be-109">The constructor's parameters are the custom attribute's positional parameters.</span></span> <span data-ttu-id="e06be-110">在此示例中，`name` 是位置参数。</span><span class="sxs-lookup"><span data-stu-id="e06be-110">In this example, `name` is a positional parameter.</span></span> <span data-ttu-id="e06be-111">所有公共读写字段或属性都是命名参数。</span><span class="sxs-lookup"><span data-stu-id="e06be-111">Any public read-write fields or properties are named parameters.</span></span> <span data-ttu-id="e06be-112">在本例中，`version` 是唯一的命名参数。</span><span class="sxs-lookup"><span data-stu-id="e06be-112">In this case, `version` is the only named parameter.</span></span> <span data-ttu-id="e06be-113">请注意，使用 `AttributeUsage` 特性可使 `Author` 特性仅对类和 `Structure` 声明有效。</span><span class="sxs-lookup"><span data-stu-id="e06be-113">Note the use of the `AttributeUsage` attribute to make the `Author` attribute valid only on class and `Structure` declarations.</span></span>

<span data-ttu-id="e06be-114">可按如下方式使用这一新特性：</span><span class="sxs-lookup"><span data-stu-id="e06be-114">You could use this new attribute as follows:</span></span>

```vb
<Author("P. Ackerman", Version:=1.1)>
Class SampleClass
    ' P. Ackerman's code goes here...
End Class
```

<span data-ttu-id="e06be-115">`AttributeUsage` 有一个命名参数 `AllowMultiple`，通过此命名参数可一次或多次使用自定义特性。</span><span class="sxs-lookup"><span data-stu-id="e06be-115">`AttributeUsage` has a named parameter, `AllowMultiple`, with which you can make a custom attribute single-use or multiuse.</span></span> <span data-ttu-id="e06be-116">下面的代码示例创建了一个多用特性。</span><span class="sxs-lookup"><span data-stu-id="e06be-116">In the following code example, a multiuse attribute is created.</span></span>

```vb
' multiuse attribute
<System.AttributeUsage(System.AttributeTargets.Class Or
                       System.AttributeTargets.Struct,
                       AllowMultiple:=True)>
Public Class Author
    Inherits System.Attribute
```

<span data-ttu-id="e06be-117">在下面的代码示例中，某个类应用了同一类型的多个特性。</span><span class="sxs-lookup"><span data-stu-id="e06be-117">In the following code example, multiple attributes of the same type are applied to a class.</span></span>

```vb
<Author("P. Ackerman", Version:=1.1),
Author("R. Koch", Version:=1.2)>
Class SampleClass
    ' P. Ackerman's code goes here...
    ' R. Koch's code goes here...
End Class
```

> [!NOTE]
> <span data-ttu-id="e06be-118">如果特性类包含属性，则该属性必须为读写属性。</span><span class="sxs-lookup"><span data-stu-id="e06be-118">If your attribute class contains a property, that property must be read-write.</span></span>

## <a name="see-also"></a><span data-ttu-id="e06be-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="e06be-119">See also</span></span>

- <xref:System.Reflection>
- [<span data-ttu-id="e06be-120">Visual Basic 编程指南</span><span class="sxs-lookup"><span data-stu-id="e06be-120">Visual Basic Programming Guide</span></span>](../../index.md)
- [<span data-ttu-id="e06be-121">编写自定义特性</span><span class="sxs-lookup"><span data-stu-id="e06be-121">Writing Custom Attributes</span></span>](../../../../standard/attributes/writing-custom-attributes.md)
- [<span data-ttu-id="e06be-122">反射 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e06be-122">Reflection (Visual Basic)</span></span>](../reflection.md)
- [<span data-ttu-id="e06be-123">特性 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e06be-123">Attributes (Visual Basic)</span></span>](../../../language-reference/attributes.md)
- [<span data-ttu-id="e06be-124">使用反射访问特性 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e06be-124">Accessing Attributes by Using Reflection (Visual Basic)</span></span>](accessing-attributes-by-using-reflection.md)
- [<span data-ttu-id="e06be-125">AttributeUsage (Visual Basic) </span><span class="sxs-lookup"><span data-stu-id="e06be-125">AttributeUsage (Visual Basic)</span></span>](attributeusage.md)
