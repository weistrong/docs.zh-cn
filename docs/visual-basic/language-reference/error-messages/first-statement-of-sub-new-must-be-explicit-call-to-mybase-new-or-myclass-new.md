---
description: 了解详细信息： BC30920：此 "Sub New" 的第一条语句必须是对 "MyBase. New" 或 "MyClass" 的显式调用，因为 <constructorname> "" 的基类 "" 中的 "" <baseclassname> <derivedclassname> 被标记为已过时： "<errormessage>
title: 此“Sub New”的第一条语句必须是对“MyBase.New”或“MyClass.New”的显式调用，因为“<constructorname>”的基类“<baseclassname>”中的“<derivedclassname>”被标记为已过时：“<errormessage>”
ms.date: 07/20/2015
f1_keywords:
- vbc30920
- bc30920
helpviewer_keywords:
- BC30920
ms.assetid: e47dc755-4294-4368-b813-2177b7677957
ms.openlocfilehash: 777543b7f29fb17dd5eb6a6196035ef0f18bb907
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99796231"
---
# <a name="bc30920-first-statement-of-this-sub-new-must-be-an-explicit-call-to-mybasenew-or-myclassnew-because-the-constructorname-in-the-base-class-baseclassname-of-derivedclassname-is-marked-obsolete-errormessage"></a><span data-ttu-id="8cf4d-103">BC30920：此 "Sub New" 的第一条语句必须是对 "MyBase. New" 或 "MyClass" 的显式调用，因为 \<constructorname> "" 的基类 "" 中的 "" \<baseclassname> \<derivedclassname> 被标记为已过时： " \<errormessage> "</span><span class="sxs-lookup"><span data-stu-id="8cf4d-103">BC30920: First statement of this 'Sub New' must be an explicit call to 'MyBase.New' or 'MyClass.New' because the '\<constructorname>' in the base class '\<baseclassname>' of '\<derivedclassname>' is marked obsolete: '\<errormessage>'</span></span>

<span data-ttu-id="8cf4d-104">类构造函数不显式调用基类构造函数，并且隐式基类构造函数标有 <xref:System.ObsoleteAttribute> 特性和将其视为错误的指令。</span><span class="sxs-lookup"><span data-stu-id="8cf4d-104">A class constructor does not explicitly call a base class constructor, and the implicit base class constructor is marked with the <xref:System.ObsoleteAttribute> attribute and the directive to treat it as an error.</span></span>

 <span data-ttu-id="8cf4d-105">当派生类构造函数不调用基类构造函数时，Visual Basic 会尝试生成对无参数基类构造函数的隐式调用。</span><span class="sxs-lookup"><span data-stu-id="8cf4d-105">When a derived class constructor does not call a base class constructor, Visual Basic attempts to generate an implicit call to a parameterless base class constructor.</span></span> <span data-ttu-id="8cf4d-106">如果基类中没有无需参数即可调用的可访问的构造函数，则 Visual Basic 无法生成隐式调用。</span><span class="sxs-lookup"><span data-stu-id="8cf4d-106">If there is no accessible constructor in the base class that can be called without arguments, Visual Basic cannot generate an implicit call.</span></span> <span data-ttu-id="8cf4d-107">在这种情况下，所需的构造函数标记有 <xref:System.ObsoleteAttribute> 特性，因此 Visual Basic 不能调用它。</span><span class="sxs-lookup"><span data-stu-id="8cf4d-107">In this case, the required constructor is marked with the <xref:System.ObsoleteAttribute> attribute, so Visual Basic cannot call it.</span></span>

 <span data-ttu-id="8cf4d-108">可以通过将 <xref:System.ObsoleteAttribute> 应用于任意编程元素，将其标记为不再使用。</span><span class="sxs-lookup"><span data-stu-id="8cf4d-108">You can mark any programming element as being no longer in use by applying <xref:System.ObsoleteAttribute> to it.</span></span> <span data-ttu-id="8cf4d-109">如果执行此操作，则可以将特性的 <xref:System.ObsoleteAttribute.IsError%2A> 属性设置为 `True` 或 `False`。</span><span class="sxs-lookup"><span data-stu-id="8cf4d-109">If you do this, you can set the attribute's <xref:System.ObsoleteAttribute.IsError%2A> property to either `True` or `False`.</span></span> <span data-ttu-id="8cf4d-110">如果设置为 `True`，则编译器将尝试使用该元素的操作视为错误。</span><span class="sxs-lookup"><span data-stu-id="8cf4d-110">If you set it to `True`, the compiler treats an attempt to use the element as an error.</span></span> <span data-ttu-id="8cf4d-111">如果设置为 `False`，或将其默认为 `False`，则编译器会在有操作尝试使用该元素时发出警告。</span><span class="sxs-lookup"><span data-stu-id="8cf4d-111">If you set it to `False`, or let it default to `False`, the compiler issues a warning if there is an attempt to use the element.</span></span>

 <span data-ttu-id="8cf4d-112">**错误 ID：** BC30920</span><span class="sxs-lookup"><span data-stu-id="8cf4d-112">**Error ID:** BC30920</span></span>

## <a name="to-correct-this-error"></a><span data-ttu-id="8cf4d-113">更正此错误</span><span class="sxs-lookup"><span data-stu-id="8cf4d-113">To correct this error</span></span>

1. <span data-ttu-id="8cf4d-114">检查引用的错误信息并采取相应的操作。</span><span class="sxs-lookup"><span data-stu-id="8cf4d-114">Examine the quoted error message and take appropriate action.</span></span>

2. <span data-ttu-id="8cf4d-115">将对 `MyBase.New()` 或 `MyClass.New()` 的调用包括为派生类中 `Sub New` 的第一个语句。</span><span class="sxs-lookup"><span data-stu-id="8cf4d-115">Include a call to `MyBase.New()` or `MyClass.New()` as the first statement of the `Sub New` in the derived class.</span></span>

## <a name="see-also"></a><span data-ttu-id="8cf4d-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="8cf4d-116">See also</span></span>

- [<span data-ttu-id="8cf4d-117">属性概述</span><span class="sxs-lookup"><span data-stu-id="8cf4d-117">Attributes overview</span></span>](../../programming-guide/concepts/attributes/index.md)
