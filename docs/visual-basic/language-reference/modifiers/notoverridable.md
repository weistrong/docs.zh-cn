---
description: '了解详细信息： NotOverridable (Visual Basic) '
title: NotOverridable
ms.date: 07/20/2015
f1_keywords:
- vb.NotOverridable
- NotOverridable
helpviewer_keywords:
- sealed methods [Visual Basic]
- NotOverridable keyword [Visual Basic]
- properties [Visual Basic], redefining
- elements [Visual Basic], sealed
- sealed [elements VB]
- procedures [Visual Basic], overriding
- procedures [Visual Basic], redefining
- overriding
- methods [Visual Basic], sealed
- properties [Visual Basic], overriding
ms.assetid: 66ec6984-f5f5-4857-b362-6a3907aaf9e0
ms.openlocfilehash: f0363024aacc1ed6ab9d8820cc965b5b71e557b6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99666090"
---
# <a name="notoverridable-visual-basic"></a><span data-ttu-id="cdc29-103">NotOverridable (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="cdc29-103">NotOverridable (Visual Basic)</span></span>

<span data-ttu-id="cdc29-104">指定不能在派生类中重写属性或过程。</span><span class="sxs-lookup"><span data-stu-id="cdc29-104">Specifies that a property or procedure cannot be overridden in a derived class.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cdc29-105">备注</span><span class="sxs-lookup"><span data-stu-id="cdc29-105">Remarks</span></span>  

 <span data-ttu-id="cdc29-106">`NotOverridable`修饰符可防止在派生类中重写属性或方法。</span><span class="sxs-lookup"><span data-stu-id="cdc29-106">The `NotOverridable` modifier prevents a property or method from being overridden in a derived class.</span></span>  <span data-ttu-id="cdc29-107">可 [重写](overridable.md) 的修饰符允许在派生类中重写类中的属性或方法。</span><span class="sxs-lookup"><span data-stu-id="cdc29-107">The [Overridable](overridable.md) modifier allows a property or method in a class to be overridden in a derived class.</span></span> <span data-ttu-id="cdc29-108">有关详细信息，请参阅[继承基础知识](../../programming-guide/language-features/objects-and-classes/inheritance-basics.md)。</span><span class="sxs-lookup"><span data-stu-id="cdc29-108">For more information, see [Inheritance Basics](../../programming-guide/language-features/objects-and-classes/inheritance-basics.md).</span></span>  
  
 <span data-ttu-id="cdc29-109">如果 `Overridable` `NotOverridable` 未指定或修饰符，则默认设置取决于属性或方法是重写基类属性还是替代方法。</span><span class="sxs-lookup"><span data-stu-id="cdc29-109">If the `Overridable` or `NotOverridable` modifier is not specified, the default setting depends on whether the property or method overrides a base class property or method.</span></span> <span data-ttu-id="cdc29-110">如果属性或方法重写基类属性或方法，则默认设置为 `Overridable` ; 否则为 `NotOverridable` 。</span><span class="sxs-lookup"><span data-stu-id="cdc29-110">If the property or method overrides a base class property or method, the default setting is `Overridable`; otherwise, it is `NotOverridable`.</span></span>  
  
 <span data-ttu-id="cdc29-111">不能重写的元素有时称为 *密封* 元素。</span><span class="sxs-lookup"><span data-stu-id="cdc29-111">An element that cannot be overridden is sometimes called a *sealed* element.</span></span>  
  
 <span data-ttu-id="cdc29-112">`NotOverridable`只能在属性或过程声明语句中使用。</span><span class="sxs-lookup"><span data-stu-id="cdc29-112">You can use `NotOverridable` only in a property or procedure declaration statement.</span></span> <span data-ttu-id="cdc29-113">只能 `NotOverridable` 在替代另一个属性或过程的属性或过程上指定，即，只能与一起使用 `Overrides` 。</span><span class="sxs-lookup"><span data-stu-id="cdc29-113">You can specify `NotOverridable` only on a property or procedure that overrides another property or procedure, that is, only in combination with `Overrides`.</span></span>  
  
## <a name="combined-modifiers"></a><span data-ttu-id="cdc29-114">组合修饰符</span><span class="sxs-lookup"><span data-stu-id="cdc29-114">Combined Modifiers</span></span>  

 <span data-ttu-id="cdc29-115">不能 `Overridable` `NotOverridable` 为方法指定或 `Private` 。</span><span class="sxs-lookup"><span data-stu-id="cdc29-115">You cannot specify `Overridable` or `NotOverridable` for a `Private` method.</span></span>  
  
 <span data-ttu-id="cdc29-116">不能 `NotOverridable` `MustOverride` `Overridable` `Shared` 在同一声明中同时指定、或。</span><span class="sxs-lookup"><span data-stu-id="cdc29-116">You cannot specify `NotOverridable` together with `MustOverride`, `Overridable`, or `Shared` in the same declaration.</span></span>  
  
## <a name="usage"></a><span data-ttu-id="cdc29-117">使用情况</span><span class="sxs-lookup"><span data-stu-id="cdc29-117">Usage</span></span>  

 <span data-ttu-id="cdc29-118">`NotOverridable` 修饰符可用于下面的上下文中：</span><span class="sxs-lookup"><span data-stu-id="cdc29-118">The `NotOverridable` modifier can be used in these contexts:</span></span>  
  
 [<span data-ttu-id="cdc29-119">Function 语句</span><span class="sxs-lookup"><span data-stu-id="cdc29-119">Function Statement</span></span>](../statements/function-statement.md)  
  
 [<span data-ttu-id="cdc29-120">Property Statement</span><span class="sxs-lookup"><span data-stu-id="cdc29-120">Property Statement</span></span>](../statements/property-statement.md)  
  
 [<span data-ttu-id="cdc29-121">Sub 语句</span><span class="sxs-lookup"><span data-stu-id="cdc29-121">Sub Statement</span></span>](../statements/sub-statement.md)  
  
## <a name="see-also"></a><span data-ttu-id="cdc29-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="cdc29-122">See also</span></span>

- [<span data-ttu-id="cdc29-123">修饰符</span><span class="sxs-lookup"><span data-stu-id="cdc29-123">Modifiers</span></span>](index.md)
- [<span data-ttu-id="cdc29-124">继承基础知识</span><span class="sxs-lookup"><span data-stu-id="cdc29-124">Inheritance Basics</span></span>](../../programming-guide/language-features/objects-and-classes/inheritance-basics.md)
- [<span data-ttu-id="cdc29-125">New</span><span class="sxs-lookup"><span data-stu-id="cdc29-125">MustOverride</span></span>](mustoverride.md)
- [<span data-ttu-id="cdc29-126">Overrides</span><span class="sxs-lookup"><span data-stu-id="cdc29-126">Overridable</span></span>](overridable.md)
- [<span data-ttu-id="cdc29-127">替代</span><span class="sxs-lookup"><span data-stu-id="cdc29-127">Overrides</span></span>](overrides.md)
- [<span data-ttu-id="cdc29-128">关键字</span><span class="sxs-lookup"><span data-stu-id="cdc29-128">Keywords</span></span>](../keywords/index.md)
- [<span data-ttu-id="cdc29-129">Visual Basic 中的隐藏</span><span class="sxs-lookup"><span data-stu-id="cdc29-129">Shadowing in Visual Basic</span></span>](../../programming-guide/language-features/declared-elements/shadowing.md)
