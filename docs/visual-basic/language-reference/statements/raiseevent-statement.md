---
description: 了解详细信息： RaiseEvent 语句
title: RaiseEvent 语句
ms.date: 07/20/2015
f1_keywords:
- vb.RaiseEventMethod
- vb.RaiseEvent
- RaiseEvent
helpviewer_keywords:
- raising events [Visual Basic], RaiseEvent statement
- RaiseEvent statement [Visual Basic]
- event handlers, connecting events to
ms.assetid: f82e380a-1e6b-4047-bea8-c853f4d2c742
ms.openlocfilehash: 9549eb64ef32147ed49ae8f805d01db8610b336e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99741336"
---
# <a name="raiseevent-statement"></a><span data-ttu-id="ed462-103">RaiseEvent 语句</span><span class="sxs-lookup"><span data-stu-id="ed462-103">RaiseEvent Statement</span></span>

<span data-ttu-id="ed462-104">触发在类、窗体或文档中的模块级别声明的事件。</span><span class="sxs-lookup"><span data-stu-id="ed462-104">Triggers an event declared at module level within a class, form, or document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ed462-105">语法</span><span class="sxs-lookup"><span data-stu-id="ed462-105">Syntax</span></span>  
  
```vb  
RaiseEvent eventname[( argumentlist )]  
```  
  
## <a name="parts"></a><span data-ttu-id="ed462-106">组成部分</span><span class="sxs-lookup"><span data-stu-id="ed462-106">Parts</span></span>  

 `eventname`  
 <span data-ttu-id="ed462-107">必需。</span><span class="sxs-lookup"><span data-stu-id="ed462-107">Required.</span></span> <span data-ttu-id="ed462-108">要触发的事件的名称。</span><span class="sxs-lookup"><span data-stu-id="ed462-108">Name of the event to trigger.</span></span>  
  
 `argumentlist`  
 <span data-ttu-id="ed462-109">可选。</span><span class="sxs-lookup"><span data-stu-id="ed462-109">Optional.</span></span> <span data-ttu-id="ed462-110">以逗号分隔的变量、数组或表达式的列表。</span><span class="sxs-lookup"><span data-stu-id="ed462-110">Comma-delimited list of variables, arrays, or expressions.</span></span> <span data-ttu-id="ed462-111">`argumentlist`参数必须括在括号中。</span><span class="sxs-lookup"><span data-stu-id="ed462-111">The `argumentlist` argument must be enclosed by parentheses.</span></span> <span data-ttu-id="ed462-112">如果没有参数，则必须省略括号。</span><span class="sxs-lookup"><span data-stu-id="ed462-112">If there are no arguments, the parentheses must be omitted.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ed462-113">备注</span><span class="sxs-lookup"><span data-stu-id="ed462-113">Remarks</span></span>  

 <span data-ttu-id="ed462-114">所需的 `eventname` 是在模块中声明的事件的名称。</span><span class="sxs-lookup"><span data-stu-id="ed462-114">The required `eventname` is the name of an event declared within the module.</span></span> <span data-ttu-id="ed462-115">它遵循 Visual Basic 变量命名约定。</span><span class="sxs-lookup"><span data-stu-id="ed462-115">It follows Visual Basic variable naming conventions.</span></span>  
  
 <span data-ttu-id="ed462-116">如果未在引发事件的模块内声明事件，则会发生错误。</span><span class="sxs-lookup"><span data-stu-id="ed462-116">If the event has not been declared within the module in which it is raised, an error occurs.</span></span> <span data-ttu-id="ed462-117">下面的代码段演示了事件声明和引发事件的过程。</span><span class="sxs-lookup"><span data-stu-id="ed462-117">The following code fragment illustrates an event declaration and a procedure in which the event is raised.</span></span>  
  
 [!code-vb[VbVbalrEvents#37](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrEvents/VB/Class1.vb#37)]  
  
 <span data-ttu-id="ed462-118">不能使用 `RaiseEvent` 来引发未在模块中显式声明的事件。</span><span class="sxs-lookup"><span data-stu-id="ed462-118">You cannot use `RaiseEvent` to raise events that are not explicitly declared in the module.</span></span> <span data-ttu-id="ed462-119">例如，所有窗体都 <xref:System.Windows.Forms.Control.Click> 从继承事件 <xref:System.Windows.Forms.Form?displayProperty=nameWithType> ，无法 `RaiseEvent` 在派生窗体中使用来引发该事件。</span><span class="sxs-lookup"><span data-stu-id="ed462-119">For example, all forms inherit a <xref:System.Windows.Forms.Control.Click> event from <xref:System.Windows.Forms.Form?displayProperty=nameWithType>, it cannot be raised using `RaiseEvent` in a derived form.</span></span> <span data-ttu-id="ed462-120">如果在 `Click` 窗体模块中声明事件，它将隐藏窗体的 <xref:System.Windows.Forms.Control.Click> 事件。</span><span class="sxs-lookup"><span data-stu-id="ed462-120">If you declare a `Click` event in the form module, it shadows the form's own <xref:System.Windows.Forms.Control.Click> event.</span></span> <span data-ttu-id="ed462-121">你仍可以通过调用方法来调用窗体的 <xref:System.Windows.Forms.Control.Click> 事件 <xref:System.Windows.Forms.Control.OnClick%2A> 。</span><span class="sxs-lookup"><span data-stu-id="ed462-121">You can still invoke the form's <xref:System.Windows.Forms.Control.Click> event by calling the <xref:System.Windows.Forms.Control.OnClick%2A> method.</span></span>  
  
 <span data-ttu-id="ed462-122">默认情况下，在 Visual Basic 中定义的事件将按照建立连接的顺序引发其事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="ed462-122">By default, an event defined in Visual Basic raises its event handlers in the order that the connections are established.</span></span> <span data-ttu-id="ed462-123">由于事件可以有 `ByRef` 参数，因此，延迟连接的进程可能会收到先前的事件处理程序已更改的参数。</span><span class="sxs-lookup"><span data-stu-id="ed462-123">Because events can have `ByRef` parameters, a process that connects late may receive parameters that have been changed by an earlier event handler.</span></span> <span data-ttu-id="ed462-124">在事件处理程序执行后，控制将返回到引发事件的子例程。</span><span class="sxs-lookup"><span data-stu-id="ed462-124">After the event handlers execute, control is returned to the subroutine that raised the event.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="ed462-125">非共享事件不应在声明它们的类的构造函数中引发。</span><span class="sxs-lookup"><span data-stu-id="ed462-125">Non-shared events should not be raised within the constructor of the class in which they are declared.</span></span> <span data-ttu-id="ed462-126">尽管此类事件不会导致运行时错误，但是它们可能无法被关联的事件处理程序捕获。</span><span class="sxs-lookup"><span data-stu-id="ed462-126">Although such events do not cause run-time errors, they may fail to be caught by associated event handlers.</span></span> <span data-ttu-id="ed462-127">`Shared`如果需要从构造函数引发事件，请使用修饰符创建共享事件。</span><span class="sxs-lookup"><span data-stu-id="ed462-127">Use the `Shared` modifier to create a shared event if you need to raise an event from a constructor.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="ed462-128">可以通过定义自定义事件来更改事件的默认行为。</span><span class="sxs-lookup"><span data-stu-id="ed462-128">You can change the default behavior of events by defining a custom event.</span></span> <span data-ttu-id="ed462-129">对于自定义事件，该 `RaiseEvent` 语句将调用事件的 `RaiseEvent` 访问器。</span><span class="sxs-lookup"><span data-stu-id="ed462-129">For custom events, the `RaiseEvent` statement invokes the event's `RaiseEvent` accessor.</span></span> <span data-ttu-id="ed462-130">有关自定义事件的详细信息，请参阅 [Event 语句](event-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="ed462-130">For more information on custom events, see [Event Statement](event-statement.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="ed462-131">示例</span><span class="sxs-lookup"><span data-stu-id="ed462-131">Example</span></span>  

 <span data-ttu-id="ed462-132">下面的示例使用事件从 10 秒到 0 秒进行倒计时。</span><span class="sxs-lookup"><span data-stu-id="ed462-132">The following example uses events to count down seconds from 10 to 0.</span></span> <span data-ttu-id="ed462-133">此代码演示了一些与事件相关的方法、属性和语句，包括 `RaiseEvent` 语句。</span><span class="sxs-lookup"><span data-stu-id="ed462-133">The code illustrates several of the event-related methods, properties, and statements, including the `RaiseEvent` statement.</span></span>  
  
 <span data-ttu-id="ed462-134">引发事件的类是事件源，处理事件的方法是事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="ed462-134">The class that raises an event is the event source, and the methods that process the event are the event handlers.</span></span> <span data-ttu-id="ed462-135">事件源对于它生成的事件可以具有多个处理程序。</span><span class="sxs-lookup"><span data-stu-id="ed462-135">An event source can have multiple handlers for the events it generates.</span></span> <span data-ttu-id="ed462-136">类引发事件时，会在选择用于为对象的该实例处理事件的每个类上引发该事件。</span><span class="sxs-lookup"><span data-stu-id="ed462-136">When the class raises the event, that event is raised on every class that has elected to handle events for that instance of the object.</span></span>  
  
 <span data-ttu-id="ed462-137">该示例还使用一个窗体 (`Form1`)，其中包含一个按钮 (`Button1`) 和一个文本框 (`TextBox1`)。</span><span class="sxs-lookup"><span data-stu-id="ed462-137">The example also uses a form (`Form1`) with a button (`Button1`) and a text box (`TextBox1`).</span></span> <span data-ttu-id="ed462-138">单击该按钮时，第一个文本框显示从 10 秒到 0 秒的倒计时。</span><span class="sxs-lookup"><span data-stu-id="ed462-138">When you click the button, the first text box displays a countdown from 10 to 0 seconds.</span></span> <span data-ttu-id="ed462-139">经过了全部时间（10 秒）之后，第一个文本框会显示“Done”。</span><span class="sxs-lookup"><span data-stu-id="ed462-139">When the full time (10 seconds) has elapsed, the first text box displays "Done".</span></span>  
  
 <span data-ttu-id="ed462-140">`Form1` 的代码指定窗体的初始和最终状态。</span><span class="sxs-lookup"><span data-stu-id="ed462-140">The code for `Form1` specifies the initial and terminal states of the form.</span></span> <span data-ttu-id="ed462-141">它还包含引发事件时执行的代码。</span><span class="sxs-lookup"><span data-stu-id="ed462-141">It also contains the code executed when events are raised.</span></span>  
  
 <span data-ttu-id="ed462-142">若要使用此示例，请打开一个新的 Windows 应用程序项目，添加一个名为的按钮， `Button1` 并将一个名 `TextBox1` 为的文本框添加到名为的主窗体 `Form1` 。</span><span class="sxs-lookup"><span data-stu-id="ed462-142">To use this example, open a new Windows Application project, add a button named `Button1` and a text box named `TextBox1` to the main form, named `Form1`.</span></span> <span data-ttu-id="ed462-143">然后，右键单击该窗体，然后单击 " **查看代码** " 以打开代码编辑器。</span><span class="sxs-lookup"><span data-stu-id="ed462-143">Then right-click the form and click **View Code** to open the Code Editor.</span></span>  
  
 <span data-ttu-id="ed462-144">将 `WithEvents` 变量添加到类的声明部分 `Form1` 。</span><span class="sxs-lookup"><span data-stu-id="ed462-144">Add a `WithEvents` variable to the declarations section of the `Form1` class.</span></span>  
  
 [!code-vb[VbVbalrEvents#14](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrEvents/VB/Class1.vb#14)]  
  
## <a name="example"></a><span data-ttu-id="ed462-145">示例</span><span class="sxs-lookup"><span data-stu-id="ed462-145">Example</span></span>  

 <span data-ttu-id="ed462-146">将下面的代码添加到 `Form1` 的代码：</span><span class="sxs-lookup"><span data-stu-id="ed462-146">Add the following code to the code for `Form1`.</span></span> <span data-ttu-id="ed462-147">替换任何可能存在的重复过程，如 `Form_Load` 或 `Button_Click` 。</span><span class="sxs-lookup"><span data-stu-id="ed462-147">Replace any duplicate procedures that may exist, such as `Form_Load`, or `Button_Click`.</span></span>  
  
 [!code-vb[VbVbalrEvents#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrEvents/VB/Class1.vb#15)]  
  
 <span data-ttu-id="ed462-148">按 F5 运行前面的示例，并单击标签为 " **启动**" 的按钮。</span><span class="sxs-lookup"><span data-stu-id="ed462-148">Press F5 to run the preceding example, and click the button labeled **Start**.</span></span> <span data-ttu-id="ed462-149">第一个文本框中开始倒计时秒数。</span><span class="sxs-lookup"><span data-stu-id="ed462-149">The first text box starts to count down the seconds.</span></span> <span data-ttu-id="ed462-150">经过了全部时间（10 秒）之后，第一个文本框会显示“Done”。</span><span class="sxs-lookup"><span data-stu-id="ed462-150">When the full time (10 seconds) has elapsed, the first text box displays "Done".</span></span>  
  
> [!NOTE]
> <span data-ttu-id="ed462-151">`My.Application.DoEvents`方法不以与窗体相同的方式处理事件。</span><span class="sxs-lookup"><span data-stu-id="ed462-151">The `My.Application.DoEvents` method does not process events in exactly the same way as the form does.</span></span> <span data-ttu-id="ed462-152">若要允许窗体直接处理事件，可以使用多线程处理。</span><span class="sxs-lookup"><span data-stu-id="ed462-152">To allow the form to handle the events directly, you can use multithreading.</span></span> <span data-ttu-id="ed462-153">有关详细信息，请参阅 [托管线程处理](../../../standard/threading/index.md)。</span><span class="sxs-lookup"><span data-stu-id="ed462-153">For more information, see [Managed Threading](../../../standard/threading/index.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ed462-154">请参阅</span><span class="sxs-lookup"><span data-stu-id="ed462-154">See also</span></span>

- [<span data-ttu-id="ed462-155">事件</span><span class="sxs-lookup"><span data-stu-id="ed462-155">Events</span></span>](../../programming-guide/language-features/events/index.md)
- [<span data-ttu-id="ed462-156">Event 语句</span><span class="sxs-lookup"><span data-stu-id="ed462-156">Event Statement</span></span>](event-statement.md)
- [<span data-ttu-id="ed462-157">AddHandler 语句</span><span class="sxs-lookup"><span data-stu-id="ed462-157">AddHandler Statement</span></span>](addhandler-statement.md)
- [<span data-ttu-id="ed462-158">RemoveHandler 语句</span><span class="sxs-lookup"><span data-stu-id="ed462-158">RemoveHandler Statement</span></span>](removehandler-statement.md)
- [<span data-ttu-id="ed462-159">句柄数</span><span class="sxs-lookup"><span data-stu-id="ed462-159">Handles</span></span>](handles-clause.md)
