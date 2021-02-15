---
description: 了解详细信息：如何在 Visual Basic 中调用事件处理程序
title: 如何调用事件处理程序
ms.date: 07/20/2015
helpviewer_keywords:
- Visual Basic code, procedures
- event handlers [Visual Basic], calling
- event handlers
- procedures [Visual Basic], event handlers
- procedures [Visual Basic], calling
no-loc:
- WithEvents
ms.assetid: 72e18ef8-144e-40df-a1f4-066a57271e28
ms.openlocfilehash: 7e65b36d392211be533bb4881658b1cdb8057d5d
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100476249"
---
# <a name="how-to-call-an-event-handler-in-visual-basic"></a><span data-ttu-id="013f0-103">如何在 Visual Basic 中调用事件处理程序</span><span class="sxs-lookup"><span data-stu-id="013f0-103">How to call an event handler in Visual Basic</span></span>

<span data-ttu-id="013f0-104">事件是指由某些程序组件识别的操作或 *事件* （例如鼠标单击或信用限制），可以为其编写代码来做出响应。</span><span class="sxs-lookup"><span data-stu-id="013f0-104">An *event* is an action or occurrence — such as a mouse click or a credit limit exceeded — that is recognized by some program component, and for which you can write code to respond.</span></span> <span data-ttu-id="013f0-105">*事件处理程序* 是为响应事件而编写的代码。</span><span class="sxs-lookup"><span data-stu-id="013f0-105">An *event handler* is the code you write to respond to an event.</span></span>

<span data-ttu-id="013f0-106">Visual Basic 中的事件处理程序是一个 `Sub` 过程。</span><span class="sxs-lookup"><span data-stu-id="013f0-106">An event handler in Visual Basic is a `Sub` procedure.</span></span> <span data-ttu-id="013f0-107">不过，通常不会像其他过程那样调用它 `Sub` 。</span><span class="sxs-lookup"><span data-stu-id="013f0-107">However, you do not normally call it the same way as other `Sub` procedures.</span></span> <span data-ttu-id="013f0-108">而是将该过程标识为事件的处理程序。</span><span class="sxs-lookup"><span data-stu-id="013f0-108">Instead, you identify the procedure as a handler for the event.</span></span> <span data-ttu-id="013f0-109">可以通过 [`Handles`](../../../language-reference/statements/handles-clause.md) 子句和 [`WithEvents`](../../../language-reference/modifiers/withevents.md) 变量或使用 [AddHandler 语句](../../../language-reference/statements/addhandler-statement.md)来执行此操作。</span><span class="sxs-lookup"><span data-stu-id="013f0-109">You can do this either with a [`Handles`](../../../language-reference/statements/handles-clause.md) clause and a [`WithEvents`](../../../language-reference/modifiers/withevents.md) variable, or with an [AddHandler Statement](../../../language-reference/statements/addhandler-statement.md).</span></span> <span data-ttu-id="013f0-110">使用 `Handles` 子句是在 Visual Basic 中声明事件处理程序的默认方式。</span><span class="sxs-lookup"><span data-stu-id="013f0-110">Using a `Handles` clause is the default way to declare an event handler in Visual Basic.</span></span> <span data-ttu-id="013f0-111">当你在集成开发环境中 (IDE) 编程时，这就是设计器编写事件处理程序的方式。</span><span class="sxs-lookup"><span data-stu-id="013f0-111">This is the way the event handlers are written by the designers when you program in the integrated development environment (IDE).</span></span> <span data-ttu-id="013f0-112">`AddHandler`语句适用于在运行时动态引发事件。</span><span class="sxs-lookup"><span data-stu-id="013f0-112">The `AddHandler` statement is suitable for raising events dynamically at run time.</span></span>

<span data-ttu-id="013f0-113">事件发生时，Visual Basic 会自动调用事件处理程序过程。</span><span class="sxs-lookup"><span data-stu-id="013f0-113">When the event occurs, Visual Basic automatically calls the event handler procedure.</span></span> <span data-ttu-id="013f0-114">有权访问事件的任何代码都可以通过执行 [RaiseEvent 语句](../../../language-reference/statements/raiseevent-statement.md)来导致事件发生。</span><span class="sxs-lookup"><span data-stu-id="013f0-114">Any code that has access to the event can cause it to occur by executing a [RaiseEvent Statement](../../../language-reference/statements/raiseevent-statement.md).</span></span>

<span data-ttu-id="013f0-115">可以将多个事件处理程序与同一事件关联。</span><span class="sxs-lookup"><span data-stu-id="013f0-115">You can associate more than one event handler with the same event.</span></span> <span data-ttu-id="013f0-116">在某些情况下，您可以取消关联事件的处理程序。</span><span class="sxs-lookup"><span data-stu-id="013f0-116">In some cases you can dissociate a handler from an event.</span></span> <span data-ttu-id="013f0-117">有关详细信息，请参阅[事件](../events/index.md)。</span><span class="sxs-lookup"><span data-stu-id="013f0-117">For more information, see [Events](../events/index.md).</span></span>

## <a name="call-an-event-handler-using-no-loc-texthandles-and-withevents"></a><span data-ttu-id="013f0-118">使用和调用事件处理程序 :::no-loc text="Handles":::WithEvents</span><span class="sxs-lookup"><span data-stu-id="013f0-118">Call an event handler using :::no-loc text="Handles"::: and WithEvents</span></span>

1. <span data-ttu-id="013f0-119">请确保事件是用 [事件语句](../../../language-reference/statements/event-statement.md)声明的。</span><span class="sxs-lookup"><span data-stu-id="013f0-119">Make sure the event is declared with an [Event Statement](../../../language-reference/statements/event-statement.md).</span></span>

2. <span data-ttu-id="013f0-120">使用关键字在模块或类级别声明对象变量 [`WithEvents`](../../../language-reference/modifiers/withevents.md) 。</span><span class="sxs-lookup"><span data-stu-id="013f0-120">Declare an object variable at module or class level, using the [`WithEvents`](../../../language-reference/modifiers/withevents.md) keyword.</span></span> <span data-ttu-id="013f0-121">`As`此变量的子句必须指定引发事件的类。</span><span class="sxs-lookup"><span data-stu-id="013f0-121">The `As` clause for this variable must specify the class that raises the event.</span></span>

3. <span data-ttu-id="013f0-122">在事件处理过程的声明中 `Sub` ，添加一个 [`Handles`](../../../language-reference/statements/handles-clause.md) 指定 `WithEvents` 变量和事件名称的子句。</span><span class="sxs-lookup"><span data-stu-id="013f0-122">In the declaration of the event-handling `Sub` procedure, add a [`Handles`](../../../language-reference/statements/handles-clause.md) clause that specifies the `WithEvents` variable and the event name.</span></span>

4. <span data-ttu-id="013f0-123">事件发生时，Visual Basic 自动调用 `Sub` 过程。</span><span class="sxs-lookup"><span data-stu-id="013f0-123">When the event occurs, Visual Basic automatically calls the `Sub` procedure.</span></span> <span data-ttu-id="013f0-124">你的代码可以使用 `RaiseEvent` 语句来使事件发生。</span><span class="sxs-lookup"><span data-stu-id="013f0-124">Your code can use a `RaiseEvent` statement to make the event occur.</span></span>

    <span data-ttu-id="013f0-125">下面的示例定义了一个事件和一个 `WithEvents` 引用引发事件的类的变量。</span><span class="sxs-lookup"><span data-stu-id="013f0-125">The following example defines an event and a `WithEvents` variable that refers to the class that raises the event.</span></span> <span data-ttu-id="013f0-126">事件处理 `Sub` 过程使用 `Handles` 子句来指定它处理的类和事件。</span><span class="sxs-lookup"><span data-stu-id="013f0-126">The event-handling `Sub` procedure uses a `Handles` clause to specify the class and event it handles.</span></span>

    :::code language="vb" source="snippets/how-to-call-an-event-handler/SpecialForm.vb" id="4":::

## <a name="call-an-event-handler-using-addhandler"></a><span data-ttu-id="013f0-127">使用 AddHandler 调用事件处理程序</span><span class="sxs-lookup"><span data-stu-id="013f0-127">Call an event handler using AddHandler</span></span>

1. <span data-ttu-id="013f0-128">请确保用语句声明了该事件 `Event` 。</span><span class="sxs-lookup"><span data-stu-id="013f0-128">Make sure the event is declared with an `Event` statement.</span></span>

2. <span data-ttu-id="013f0-129">执行 [AddHandler 语句](../../../language-reference/statements/addhandler-statement.md) 以使用事件动态连接事件处理 `Sub` 过程。</span><span class="sxs-lookup"><span data-stu-id="013f0-129">Execute an [AddHandler statement](../../../language-reference/statements/addhandler-statement.md) to dynamically connect the event-handling `Sub` procedure with the event.</span></span>

3. <span data-ttu-id="013f0-130">事件发生时，Visual Basic 自动调用 `Sub` 过程。</span><span class="sxs-lookup"><span data-stu-id="013f0-130">When the event occurs, Visual Basic automatically calls the `Sub` procedure.</span></span> <span data-ttu-id="013f0-131">你的代码可以使用 `RaiseEvent` 语句来使事件发生。</span><span class="sxs-lookup"><span data-stu-id="013f0-131">Your code can use a `RaiseEvent` statement to make the event occur.</span></span>

    <span data-ttu-id="013f0-132">下面的示例使用构造函数中的 [AddHandler 语句](../../../language-reference/statements/addhandler-statement.md) 将过程与的 `OnFormClosing` 事件处理程序相关联 <xref:System.Windows.Forms.Form.FormClosing> 。</span><span class="sxs-lookup"><span data-stu-id="013f0-132">The following example uses the [AddHandler statement](../../../language-reference/statements/addhandler-statement.md) in the constructor to associate the `OnFormClosing` procedure as an event handler for <xref:System.Windows.Forms.Form.FormClosing>.</span></span>

    :::code language="vb" source="snippets/how-to-call-an-event-handler/SpecialForm.vb" id="5":::

    <span data-ttu-id="013f0-133">可以通过执行 [RemoveHandler 语句](../../../language-reference/statements/removehandler-statement.md)，将事件处理程序与事件取消关联。</span><span class="sxs-lookup"><span data-stu-id="013f0-133">You can dissociate an event handler from an event by executing the [RemoveHandler statement](../../../language-reference/statements/removehandler-statement.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="013f0-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="013f0-134">See also</span></span>

- [<span data-ttu-id="013f0-135">过程</span><span class="sxs-lookup"><span data-stu-id="013f0-135">Procedures</span></span>](index.md)
- [<span data-ttu-id="013f0-136">Sub 过程</span><span class="sxs-lookup"><span data-stu-id="013f0-136">Sub Procedures</span></span>](sub-procedures.md)
- [<span data-ttu-id="013f0-137">Sub 语句</span><span class="sxs-lookup"><span data-stu-id="013f0-137">Sub Statement</span></span>](../../../language-reference/statements/sub-statement.md)
- [<span data-ttu-id="013f0-138">AddressOf 运算符</span><span class="sxs-lookup"><span data-stu-id="013f0-138">AddressOf Operator</span></span>](../../../language-reference/operators/addressof-operator.md)
- [<span data-ttu-id="013f0-139">如何：创建过程</span><span class="sxs-lookup"><span data-stu-id="013f0-139">How to: Create a Procedure</span></span>](how-to-create-a-procedure.md)
- [<span data-ttu-id="013f0-140">如何：调用不返回值的过程</span><span class="sxs-lookup"><span data-stu-id="013f0-140">How to: Call a Procedure that Does Not Return a Value</span></span>](how-to-call-a-procedure-that-does-not-return-a-value.md)
