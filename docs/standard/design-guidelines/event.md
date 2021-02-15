---
description: 详细了解：事件设计
title: 事件设计
ms.date: 10/22/2008
helpviewer_keywords:
- pre-events
- events [.NET Framework], design guidelines
- member design guidelines, events
- event handlers [.NET Framework], event design guidelines
- post-events
- signatures, event handling
ms.assetid: 67b3c6e2-6a8f-480d-a78f-ebeeaca1b95a
ms.openlocfilehash: d64bfb13792aa9d646560de844acddd9b7e188c0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99642196"
---
# <a name="event-design"></a><span data-ttu-id="382e1-103">事件设计</span><span class="sxs-lookup"><span data-stu-id="382e1-103">Event Design</span></span>

<span data-ttu-id="382e1-104">事件是最常用的回叫形式（“回叫”就是允许框架调入用户代码的构造）。</span><span class="sxs-lookup"><span data-stu-id="382e1-104">Events are the most commonly used form of callbacks (constructs that allow the framework to call into user code).</span></span> <span data-ttu-id="382e1-105">其他回叫机制包括采用委托的成员、虚拟成员和基于接口的插件。可用性调查中的数据显示，大多数开发人员更喜欢使用事件，而不是使用其他回叫机制。</span><span class="sxs-lookup"><span data-stu-id="382e1-105">Other callback mechanisms include members taking delegates, virtual members, and interface-based plug-ins. Data from usability studies indicate that the majority of developers are more comfortable using events than they are using the other callback mechanisms.</span></span> <span data-ttu-id="382e1-106">事件与 Visual Studio 和多种语言完美集成。</span><span class="sxs-lookup"><span data-stu-id="382e1-106">Events are nicely integrated with Visual Studio and many languages.</span></span>

 <span data-ttu-id="382e1-107">值得注意的是存在两组事件：在系统状态更改前引发的事件（称为前期事件），以及在状态更改后引发的事件（称为后期事件）。</span><span class="sxs-lookup"><span data-stu-id="382e1-107">It is important to note that there are two groups of events: events raised before a state of the system changes, called pre-events, and events raised after a state changes, called post-events.</span></span> <span data-ttu-id="382e1-108">前期事件的一个例子是 `Form.Closing`，它是在窗体关闭前引发的。</span><span class="sxs-lookup"><span data-stu-id="382e1-108">An example of a pre-event would be `Form.Closing`, which is raised before a form is closed.</span></span> <span data-ttu-id="382e1-109">后期事件的一个例子是 `Form.Closed`，它是在窗体关闭后引发的。</span><span class="sxs-lookup"><span data-stu-id="382e1-109">An example of a post-event would be `Form.Closed`, which is raised after a form is closed.</span></span>

 <span data-ttu-id="382e1-110">✔️ 请对事件使用“raise”（引发）这个词，而不是使用“fire”（激发）或“trigger”（触发）。</span><span class="sxs-lookup"><span data-stu-id="382e1-110">✔️ DO use the term "raise" for events rather than "fire" or "trigger."</span></span>

 <span data-ttu-id="382e1-111">✔️ 请使用 <xref:System.EventHandler%601?displayProperty=nameWithType>，而不是手动创建新的委托来用作事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="382e1-111">✔️ DO use <xref:System.EventHandler%601?displayProperty=nameWithType> instead of manually creating new delegates to be used as event handlers.</span></span>

 <span data-ttu-id="382e1-112">✔️ 请考虑将 <xref:System.EventArgs> 的子类用作事件参数，除非你完全确信事件将永不需要将任何数据传递到事件处理方法（在此情况下，你可直接使用 `EventArgs` 类型）。</span><span class="sxs-lookup"><span data-stu-id="382e1-112">✔️ CONSIDER using a subclass of <xref:System.EventArgs> as the event argument, unless you are absolutely sure the event will never need to carry any data to the event handling method, in which case you can use the `EventArgs` type directly.</span></span>

 <span data-ttu-id="382e1-113">如果你直接使用 `EventArgs` 来传递 API，则你永远无法在不破坏兼容性的情况下添加任何要与事件一起传递的数据。</span><span class="sxs-lookup"><span data-stu-id="382e1-113">If you ship an API using `EventArgs` directly, you will never be able to add any data to be carried with the event without breaking compatibility.</span></span> <span data-ttu-id="382e1-114">如果你使用子类，则即使最开始完全为空，你也将能够在需要时向子类添加属性。</span><span class="sxs-lookup"><span data-stu-id="382e1-114">If you use a subclass, even if initially completely empty, you will be able to add properties to the subclass when needed.</span></span>

 <span data-ttu-id="382e1-115">✔️ 请使用受保护的虚拟方法来引发每个事件。</span><span class="sxs-lookup"><span data-stu-id="382e1-115">✔️ DO use a protected virtual method to raise each event.</span></span> <span data-ttu-id="382e1-116">这仅适用于非密封类上的非静态事件，不可用于结构、密封类和静态事件。</span><span class="sxs-lookup"><span data-stu-id="382e1-116">This is only applicable to nonstatic events on unsealed classes, not to structs, sealed classes, or static events.</span></span>

 <span data-ttu-id="382e1-117">此方法旨在使派生类能够处理使用替代项的事件。</span><span class="sxs-lookup"><span data-stu-id="382e1-117">The purpose of the method is to provide a way for a derived class to handle the event using an override.</span></span> <span data-ttu-id="382e1-118">对于处理派生类中的基类事件，替代操作更加灵活、更加快速，也更自然。</span><span class="sxs-lookup"><span data-stu-id="382e1-118">Overriding is a more flexible, faster, and more natural way to handle base class events in derived classes.</span></span> <span data-ttu-id="382e1-119">按照约定，方法的名称应以“On”开头，后跟事件的名称。</span><span class="sxs-lookup"><span data-stu-id="382e1-119">By convention, the name of the method should start with "On" and be followed with the name of the event.</span></span>

 <span data-ttu-id="382e1-120">派生类可选择不在其替代中调用方法的基础实现。</span><span class="sxs-lookup"><span data-stu-id="382e1-120">The derived class can choose not to call the base implementation of the method in its override.</span></span> <span data-ttu-id="382e1-121">为此，请不要在为使基类正常工作而所需的方法中包含任何处理。</span><span class="sxs-lookup"><span data-stu-id="382e1-121">Be prepared for this by not including any processing in the method that is required for the base class to work correctly.</span></span>

 <span data-ttu-id="382e1-122">✔️ 请将一个参数传递给会引发事件的受保护的方法。</span><span class="sxs-lookup"><span data-stu-id="382e1-122">✔️ DO take one parameter to the protected method that raises an event.</span></span>

 <span data-ttu-id="382e1-123">该参数应被命名为 `e`，且其类型应为事件参数类。</span><span class="sxs-lookup"><span data-stu-id="382e1-123">The parameter should be named `e` and should be typed as the event argument class.</span></span>

 <span data-ttu-id="382e1-124">❌ 在引发非静态事件时，请勿将 NULL 作为发送方传递。</span><span class="sxs-lookup"><span data-stu-id="382e1-124">❌ DO NOT pass null as the sender when raising a nonstatic event.</span></span>

 <span data-ttu-id="382e1-125">✔️ 在引发静态事件时，请将 NULL 作为发送方传递。</span><span class="sxs-lookup"><span data-stu-id="382e1-125">✔️ DO pass null as the sender when raising a static event.</span></span>

 <span data-ttu-id="382e1-126">❌ 在引发事件时，请勿将 NULL 作为事件数据参数传递。</span><span class="sxs-lookup"><span data-stu-id="382e1-126">❌ DO NOT pass null as the event data parameter when raising an event.</span></span>

 <span data-ttu-id="382e1-127">如果不想向事件处理方法传递任何数据，则应传递 `EventArgs.Empty`。</span><span class="sxs-lookup"><span data-stu-id="382e1-127">You should pass `EventArgs.Empty` if you don’t want to pass any data to the event handling method.</span></span> <span data-ttu-id="382e1-128">开发人员希望此参数不是 NULL。</span><span class="sxs-lookup"><span data-stu-id="382e1-128">Developers expect this parameter not to be null.</span></span>

 <span data-ttu-id="382e1-129">✔️ 请考虑引发最终用户可取消的事件。</span><span class="sxs-lookup"><span data-stu-id="382e1-129">✔️ CONSIDER raising events that the end user can cancel.</span></span> <span data-ttu-id="382e1-130">这仅适用于前期事件。</span><span class="sxs-lookup"><span data-stu-id="382e1-130">This only applies to pre-events.</span></span>

 <span data-ttu-id="382e1-131">使用 <xref:System.ComponentModel.CancelEventArgs?displayProperty=nameWithType> 或其子类作为事件参数，以允许最终用户取消事件。</span><span class="sxs-lookup"><span data-stu-id="382e1-131">Use <xref:System.ComponentModel.CancelEventArgs?displayProperty=nameWithType> or its subclass as the event argument to allow the end user to cancel events.</span></span>

### <a name="custom-event-handler-design"></a><span data-ttu-id="382e1-132">自定义事件处理程序设计</span><span class="sxs-lookup"><span data-stu-id="382e1-132">Custom Event Handler Design</span></span>

 <span data-ttu-id="382e1-133">在有些情况下无法使用 `EventHandler<T>`，例如当框架需要与不支持泛型的较早版本的 CLR 一起使用时。</span><span class="sxs-lookup"><span data-stu-id="382e1-133">There are cases in which `EventHandler<T>` cannot be used, such as when the framework needs to work with earlier versions of the CLR, which did not support Generics.</span></span> <span data-ttu-id="382e1-134">在这种情况下，你可能需要设计和开发自定义事件处理程序委托。</span><span class="sxs-lookup"><span data-stu-id="382e1-134">In such cases, you might need to design and develop a custom event handler delegate.</span></span>

 <span data-ttu-id="382e1-135">✔️ 请对事件处理程序使用返回类型 void。</span><span class="sxs-lookup"><span data-stu-id="382e1-135">✔️ DO use a return type of void for event handlers.</span></span>

 <span data-ttu-id="382e1-136">事件处理程序可调用多个事件处理方法，可能是对多个对象调用。</span><span class="sxs-lookup"><span data-stu-id="382e1-136">An event handler can invoke multiple event handling methods, possibly on multiple objects.</span></span> <span data-ttu-id="382e1-137">如果事件处理方法可返回值，则每个事件调用都有多个返回值。</span><span class="sxs-lookup"><span data-stu-id="382e1-137">If event handling methods were allowed to return a value, there would be multiple return values for each event invocation.</span></span>

 <span data-ttu-id="382e1-138">✔️ 请使用 `object` 作为事件处理程序的第一个参数的类型，并将其称为 `sender`。</span><span class="sxs-lookup"><span data-stu-id="382e1-138">✔️ DO use `object` as the type of the first parameter of the event handler, and call it `sender`.</span></span>

 <span data-ttu-id="382e1-139">✔️ 请使用 <xref:System.EventArgs?displayProperty=nameWithType> 或其子类作为事件处理程序的第二个参数的类型，并将其称为 `e`。</span><span class="sxs-lookup"><span data-stu-id="382e1-139">✔️ DO use <xref:System.EventArgs?displayProperty=nameWithType> or its subclass as the type of the second parameter of the event handler, and call it `e`.</span></span>

 <span data-ttu-id="382e1-140">❌ 事件处理程序上请勿带有两个以上的参数。</span><span class="sxs-lookup"><span data-stu-id="382e1-140">❌ DO NOT have more than two parameters on event handlers.</span></span>

 <span data-ttu-id="382e1-141">*Portions © 2005, 2009 Microsoft Corporation 版权所有。保留所有权利。*</span><span class="sxs-lookup"><span data-stu-id="382e1-141">*Portions © 2005, 2009 Microsoft Corporation. All rights reserved.*</span></span>

 <span data-ttu-id="382e1-142">*在 Pearson Education, Inc. 授权下，由 Addison-Wesley Professional 作为 Microsoft Windows 开发系列的一部分再版自 [Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619)（Framework 设计准则：可重用 .NET 库的约定、惯例和模式第 2 版），由 Krzysztof Cwalina 和 Brad Abrams 发布于 2008 年 10 月 22 日。*</span><span class="sxs-lookup"><span data-stu-id="382e1-142">*Reprinted by permission of Pearson Education, Inc. from [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) by Krzysztof Cwalina and Brad Abrams, published Oct 22, 2008 by Addison-Wesley Professional as part of the Microsoft Windows Development Series.*</span></span>

## <a name="see-also"></a><span data-ttu-id="382e1-143">请参阅</span><span class="sxs-lookup"><span data-stu-id="382e1-143">See also</span></span>

- [<span data-ttu-id="382e1-144">成员设计准则</span><span class="sxs-lookup"><span data-stu-id="382e1-144">Member Design Guidelines</span></span>](member.md)
- [<span data-ttu-id="382e1-145">框架设计指南</span><span class="sxs-lookup"><span data-stu-id="382e1-145">Framework Design Guidelines</span></span>](index.md)
