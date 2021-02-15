---
description: '了解详细信息：如何：使用 Async 和 Await (Visual Basic 并行发出多个 Web 请求) '
title: 如何：使用 Async 和 Await 并行发出多个 Web 请求
ms.date: 07/20/2015
ms.assetid: a894b99b-7cfd-4a38-adfb-20d24f986730
ms.openlocfilehash: e1137424911b77ba94a760a4b4b034e45ef83462
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100474338"
---
# <a name="how-to-make-multiple-web-requests-in-parallel-by-using-async-and-await-visual-basic"></a><span data-ttu-id="44dc8-103">如何：使用 Async 和 Await 并行发出多个 Web 请求 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="44dc8-103">How to: Make Multiple Web Requests in Parallel by Using Async and Await (Visual Basic)</span></span>

<span data-ttu-id="44dc8-104">在 async 方法中，任务在创建后即启动。</span><span class="sxs-lookup"><span data-stu-id="44dc8-104">In an async method, tasks are started when they’re created.</span></span> <span data-ttu-id="44dc8-105">[Await](../../../language-reference/operators/await-operator.md)运算符应用于方法中的点，在该方法中，处理无法继续，直到任务完成。</span><span class="sxs-lookup"><span data-stu-id="44dc8-105">The [Await](../../../language-reference/operators/await-operator.md) operator is applied to the task at the point in the method where processing can’t continue until the task finishes.</span></span> <span data-ttu-id="44dc8-106">通常任务被创建后即等待，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="44dc8-106">Often a task is awaited as soon as it’s created, as the following example shows.</span></span>

```vb
Dim result = Await someWebAccessMethodAsync(url)
```

<span data-ttu-id="44dc8-107">但是，如果程序有其他不依赖于任务的完成的工作要完成，则可以将创建任务和等待任务分开。</span><span class="sxs-lookup"><span data-stu-id="44dc8-107">However, you can separate creating the task from awaiting the task if your program has other work to accomplish that doesn’t depend on the completion of the task.</span></span>

```vb
' The following line creates and starts the task.
Dim myTask = someWebAccessMethodAsync(url)

' While the task is running, you can do other work that does not depend
' on the results of the task.
' . . . . .

' The application of Await suspends the rest of this method until the task is
' complete.
Dim result = Await myTask
```

<span data-ttu-id="44dc8-108">在启动任务和等待任务之间，可以启动其他任务。</span><span class="sxs-lookup"><span data-stu-id="44dc8-108">Between starting a task and awaiting it, you can start other tasks.</span></span> <span data-ttu-id="44dc8-109">其他任务以并行方式隐式运行，但不会创建其他线程。</span><span class="sxs-lookup"><span data-stu-id="44dc8-109">The additional tasks implicitly run in parallel, but no additional threads are created.</span></span>

<span data-ttu-id="44dc8-110">下面的程序启动三个异步 Web 下载任务，然后按照任务的调用顺序等待其完成。</span><span class="sxs-lookup"><span data-stu-id="44dc8-110">The following program starts three asynchronous web downloads and then awaits them in the order in which they’re called.</span></span> <span data-ttu-id="44dc8-111">请注意，运行此程序时，任务并不总是按照创建和等待它们的顺序完成。</span><span class="sxs-lookup"><span data-stu-id="44dc8-111">Notice, when you run the program, that the tasks don’t always finish in the order in which they’re created and awaited.</span></span> <span data-ttu-id="44dc8-112">任务在创建后开始运行，在此方法到达 await 表达式之前可能已完成一个或多个任务。</span><span class="sxs-lookup"><span data-stu-id="44dc8-112">They start to run when they’re created, and one or more of the tasks might finish before the method reaches the await expressions.</span></span>

> [!NOTE]
> <span data-ttu-id="44dc8-113">若要完成此项目，计算机上必须安装有 Visual Studio 2012 或更高版本和 .NET Framework 4.5 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="44dc8-113">To complete this project, you must have Visual Studio 2012 or higher and the .NET Framework 4.5 or higher installed on your computer.</span></span>

<span data-ttu-id="44dc8-114">对于同时启动多个任务的另一个示例，请参阅 [如何：使用 system.threading.tasks.task.whenall (Visual Basic) 扩展 Async 演练 ](how-to-extend-the-async-walkthrough-by-using-task-whenall.md)。</span><span class="sxs-lookup"><span data-stu-id="44dc8-114">For another example that starts multiple tasks at the same time, see [How to: Extend the Async Walkthrough by Using Task.WhenAll (Visual Basic)](how-to-extend-the-async-walkthrough-by-using-task-whenall.md).</span></span>

<span data-ttu-id="44dc8-115">可以从[开发人员代码示例](https://code.msdn.microsoft.com/Async-Make-Multiple-Web-49adb82e)下载此示例的代码。</span><span class="sxs-lookup"><span data-stu-id="44dc8-115">You can download the code for this example from [Developer Code Samples](https://code.msdn.microsoft.com/Async-Make-Multiple-Web-49adb82e).</span></span>

### <a name="to-set-up-the-project"></a><span data-ttu-id="44dc8-116">设置项目</span><span class="sxs-lookup"><span data-stu-id="44dc8-116">To set up the project</span></span>

1. <span data-ttu-id="44dc8-117">若要设置 WPF 应用程序，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="44dc8-117">To set up a WPF application, complete the following steps.</span></span> <span data-ttu-id="44dc8-118">可以在 [演练：使用 Async 和 Await 访问 Web (Visual Basic) ](walkthrough-accessing-the-web-by-using-async-and-await.md)中找到有关这些步骤的详细说明。</span><span class="sxs-lookup"><span data-stu-id="44dc8-118">You can find detailed instructions for these steps in [Walkthrough: Accessing the Web by Using Async and Await (Visual Basic)](walkthrough-accessing-the-web-by-using-async-and-await.md).</span></span>

    - <span data-ttu-id="44dc8-119">创建包含一个文本框和一个按钮的 WPF 应用程序。</span><span class="sxs-lookup"><span data-stu-id="44dc8-119">Create a WPF application that contains a text box and a button.</span></span> <span data-ttu-id="44dc8-120">将按钮命名为 `startButton`，将文本框命名为 `resultsTextBox`。</span><span class="sxs-lookup"><span data-stu-id="44dc8-120">Name the button `startButton`, and name the text box `resultsTextBox`.</span></span>

    - <span data-ttu-id="44dc8-121">对 <xref:System.Net.Http> 添加引用。</span><span class="sxs-lookup"><span data-stu-id="44dc8-121">Add a reference for <xref:System.Net.Http>.</span></span>

    - <span data-ttu-id="44dc8-122">在 Mainwindow.xaml 文件中， `Imports` 为添加语句 `System.Net.Http` 。</span><span class="sxs-lookup"><span data-stu-id="44dc8-122">In the MainWindow.xaml.vb file, add an `Imports` statement for `System.Net.Http`.</span></span>

### <a name="to-add-the-code"></a><span data-ttu-id="44dc8-123">添加代码</span><span class="sxs-lookup"><span data-stu-id="44dc8-123">To add the code</span></span>

1. <span data-ttu-id="44dc8-124">在 "设计" 窗口中，双击 "Mainwindow.xaml" 按钮以 `startButton_Click` 在 mainwindow.xaml 中创建事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="44dc8-124">In the design window, MainWindow.xaml, double-click the button to create the `startButton_Click` event handler in MainWindow.xaml.vb.</span></span>

2. <span data-ttu-id="44dc8-125">复制以下代码，并将其粘贴到 `startButton_Click` mainwindow.xaml 中的正文中。</span><span class="sxs-lookup"><span data-stu-id="44dc8-125">Copy the following code, and paste it into the body of `startButton_Click` in MainWindow.xaml.vb.</span></span>

    ```vb
    resultsTextBox.Clear()
    Await CreateMultipleTasksAsync()
    resultsTextBox.Text &= vbCrLf & "Control returned to button1_Click."
    ```

     <span data-ttu-id="44dc8-126">此代码调用异步方法 `CreateMultipleTasksAsync`，此方法驱动应用程序。</span><span class="sxs-lookup"><span data-stu-id="44dc8-126">The code calls an asynchronous method, `CreateMultipleTasksAsync`, which drives the application.</span></span>

3. <span data-ttu-id="44dc8-127">向项目中添加以下支持方法：</span><span class="sxs-lookup"><span data-stu-id="44dc8-127">Add the following support methods to the project:</span></span>

    - <span data-ttu-id="44dc8-128">`ProcessURLAsync` 使用 <xref:System.Net.Http.HttpClient> 方法将网站内容下载为字节数组。</span><span class="sxs-lookup"><span data-stu-id="44dc8-128">`ProcessURLAsync` uses an <xref:System.Net.Http.HttpClient> method to download the contents of a website as a byte array.</span></span> <span data-ttu-id="44dc8-129">支持方法 `ProcessURLAsync` 随后显示并返回数组的长度。</span><span class="sxs-lookup"><span data-stu-id="44dc8-129">The support method, `ProcessURLAsync` then displays and returns the length of the array.</span></span>

    - <span data-ttu-id="44dc8-130">`DisplayResults` 显示每个 URL 的字节数组中的字节数。</span><span class="sxs-lookup"><span data-stu-id="44dc8-130">`DisplayResults` displays the number of bytes in the byte array for each URL.</span></span> <span data-ttu-id="44dc8-131">当所有任务完成下载后显示。</span><span class="sxs-lookup"><span data-stu-id="44dc8-131">This display shows when each task has finished downloading.</span></span>

     <span data-ttu-id="44dc8-132">复制以下方法，并将其粘贴到 `startButton_Click` mainwindow.xaml 中的事件处理程序之后。</span><span class="sxs-lookup"><span data-stu-id="44dc8-132">Copy the following methods, and paste them after the `startButton_Click` event handler in MainWindow.xaml.vb.</span></span>

    ```vb
    Private Async Function ProcessURLAsync(url As String, client As HttpClient) As Task(Of Integer)

        Dim byteArray = Await client.GetByteArrayAsync(url)
        DisplayResults(url, byteArray)
        Return byteArray.Length
    End Function

    Private Sub DisplayResults(url As String, content As Byte())

        ' Display the length of each website. The string format
        ' is designed to be used with a monospaced font, such as
        ' Lucida Console or Global Monospace.
        Dim bytes = content.Length
        ' Strip off the "https://".
        Dim displayURL = url.Replace("https://", "")
        resultsTextBox.Text &= String.Format(vbCrLf & "{0,-58} {1,8}", displayURL, bytes)
    End Sub
    ```

4. <span data-ttu-id="44dc8-133">最后，定义方法 `CreateMultipleTasksAsync`，用于执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="44dc8-133">Finally, define method `CreateMultipleTasksAsync`, which performs the following steps.</span></span>

    - <span data-ttu-id="44dc8-134">该方法声明 `HttpClient` 对象，这需要你访问 `ProcessURLAsync` 中的 <xref:System.Net.Http.HttpClient.GetByteArrayAsync%2A> 方法。</span><span class="sxs-lookup"><span data-stu-id="44dc8-134">The method declares an `HttpClient` object,which you need  to access method <xref:System.Net.Http.HttpClient.GetByteArrayAsync%2A> in `ProcessURLAsync`.</span></span>

    - <span data-ttu-id="44dc8-135">此方法创建并启动三个类型为 <xref:System.Threading.Tasks.Task%601> 的任务，其中 `TResult` 是一个整数。</span><span class="sxs-lookup"><span data-stu-id="44dc8-135">The method creates and starts three tasks of type <xref:System.Threading.Tasks.Task%601>, where `TResult` is an integer.</span></span> <span data-ttu-id="44dc8-136">每个任务完成后，`DisplayResults` 显示任务的 URL 和下载内容的长度。</span><span class="sxs-lookup"><span data-stu-id="44dc8-136">As each task finishes, `DisplayResults` displays the task's URL and the length of the downloaded contents.</span></span> <span data-ttu-id="44dc8-137">由于任务是异步运行的，因此显示结果的顺序可能与声明任务的顺序不同。</span><span class="sxs-lookup"><span data-stu-id="44dc8-137">Because the tasks are running asynchronously, the order in which the results appear might differ from the order in which they were declared.</span></span>

    - <span data-ttu-id="44dc8-138">此方法等待每个任务完成。</span><span class="sxs-lookup"><span data-stu-id="44dc8-138">The method awaits the completion of each task.</span></span> <span data-ttu-id="44dc8-139">每个 `Await` 运算符暂停执行 `CreateMultipleTasksAsync`，直到所等待的任务完成。</span><span class="sxs-lookup"><span data-stu-id="44dc8-139">Each `Await` operator suspends execution of `CreateMultipleTasksAsync` until the awaited task is finished.</span></span> <span data-ttu-id="44dc8-140">此运算符还会从每个已完成的任务的 `ProcessURLAsync` 调用中检索返回值。</span><span class="sxs-lookup"><span data-stu-id="44dc8-140">The operator also retrieves the return value from the call to `ProcessURLAsync` from each completed task.</span></span>

    - <span data-ttu-id="44dc8-141">当任务已完成并已检索到整数值时，此方法对网站的长度求和，并显示结果。</span><span class="sxs-lookup"><span data-stu-id="44dc8-141">When the tasks have been completed and the integer values have been retrieved, the method sums the lengths of the websites and displays the result.</span></span>

     <span data-ttu-id="44dc8-142">复制下面的方法，并将其粘贴到你的解决方案。</span><span class="sxs-lookup"><span data-stu-id="44dc8-142">Copy the following method, and paste it into your solution.</span></span>

    ```vb
    Private Async Function CreateMultipleTasksAsync() As Task

        ' Declare an HttpClient object, and increase the buffer size. The
        ' default buffer size is 65,536.
        Dim client As HttpClient =
            New HttpClient() With {.MaxResponseContentBufferSize = 1000000}

        ' Create and start the tasks. As each task finishes, DisplayResults
        ' displays its length.
        Dim download1 As Task(Of Integer) =
            ProcessURLAsync("https://msdn.microsoft.com", client)
        Dim download2 As Task(Of Integer) =
            ProcessURLAsync("https://msdn.microsoft.com/library/hh156528(VS.110).aspx", client)
        Dim download3 As Task(Of Integer) =
            ProcessURLAsync("https://msdn.microsoft.com/library/67w7t67f.aspx", client)

        ' Await each task.
        Dim length1 As Integer = Await download1
        Dim length2 As Integer = Await download2
        Dim length3 As Integer = Await download3

        Dim total As Integer = length1 + length2 + length3

        ' Display the total count for all of the websites.
        resultsTextBox.Text &= String.Format(vbCrLf & vbCrLf &
                                             "Total bytes returned:  {0}" & vbCrLf, total)
    End Function
    ```

5. <span data-ttu-id="44dc8-143">按 F5 键以运行程序，然后选择 **“启动”** 按钮。</span><span class="sxs-lookup"><span data-stu-id="44dc8-143">Choose the F5 key to run the program, and then choose the **Start** button.</span></span>

     <span data-ttu-id="44dc8-144">多次运行此程序以确认三个任务并不总是以相同的顺序完成，并且完成的顺序不一定是创建和等待任务的顺序。</span><span class="sxs-lookup"><span data-stu-id="44dc8-144">Run the program several times to verify that the three tasks don’t always finish in the same order and that the order in which they finish isn't necessarily the order in which they’re created and awaited.</span></span>

## <a name="example"></a><span data-ttu-id="44dc8-145">示例</span><span class="sxs-lookup"><span data-stu-id="44dc8-145">Example</span></span>

<span data-ttu-id="44dc8-146">下面的代码包括完整的示例。</span><span class="sxs-lookup"><span data-stu-id="44dc8-146">The following code contains the full example.</span></span>

```vb
' Add the following Imports statements, and add a reference for System.Net.Http.
Imports System.Net.Http

Class MainWindow

    Async Sub startButton_Click(sender As Object, e As RoutedEventArgs) Handles startButton.Click
        resultsTextBox.Clear()
        Await CreateMultipleTasksAsync()
        resultsTextBox.Text &= vbCrLf & "Control returned to button1_Click."
    End Sub

    Private Async Function CreateMultipleTasksAsync() As Task

        ' Declare an HttpClient object, and increase the buffer size. The
        ' default buffer size is 65,536.
        Dim client As HttpClient =
            New HttpClient() With {.MaxResponseContentBufferSize = 1000000}

        ' Create and start the tasks. As each task finishes, DisplayResults
        ' displays its length.
        Dim download1 As Task(Of Integer) =
            ProcessURLAsync("https://msdn.microsoft.com", client)
        Dim download2 As Task(Of Integer) =
            ProcessURLAsync("https://msdn.microsoft.com/library/hh156528(VS.110).aspx", client)
        Dim download3 As Task(Of Integer) =
            ProcessURLAsync("https://msdn.microsoft.com/library/67w7t67f.aspx", client)

        ' Await each task.
        Dim length1 As Integer = Await download1
        Dim length2 As Integer = Await download2
        Dim length3 As Integer = Await download3

        Dim total As Integer = length1 + length2 + length3

        ' Display the total count for all of the websites.
        resultsTextBox.Text &= String.Format(vbCrLf & vbCrLf &
                                             "Total bytes returned:  {0}" & vbCrLf, total)
    End Function

    Private Async Function ProcessURLAsync(url As String, client As HttpClient) As Task(Of Integer)

        Dim byteArray = Await client.GetByteArrayAsync(url)
        DisplayResults(url, byteArray)
        Return byteArray.Length
    End Function

    Private Sub DisplayResults(url As String, content As Byte())

        ' Display the length of each website. The string format
        ' is designed to be used with a monospaced font, such as
        ' Lucida Console or Global Monospace.
        Dim bytes = content.Length
        ' Strip off the "https://".
        Dim displayURL = url.Replace("https://", "")
        resultsTextBox.Text &= String.Format(vbCrLf & "{0,-58} {1,8}", displayURL, bytes)
    End Sub
End Class
```

## <a name="see-also"></a><span data-ttu-id="44dc8-147">请参阅</span><span class="sxs-lookup"><span data-stu-id="44dc8-147">See also</span></span>

- [<span data-ttu-id="44dc8-148">演练：使用 Async 和 Await 访问 Web (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="44dc8-148">Walkthrough: Accessing the Web by Using Async and Await (Visual Basic)</span></span>](walkthrough-accessing-the-web-by-using-async-and-await.md)
- [<span data-ttu-id="44dc8-149">使用 Async 和 Await 的异步编程 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="44dc8-149">Asynchronous Programming with Async and Await (Visual Basic)</span></span>](index.md)
- [<span data-ttu-id="44dc8-150">如何：使用 Task.WhenAll 扩展异步演练 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="44dc8-150">How to: Extend the Async Walkthrough by Using Task.WhenAll (Visual Basic)</span></span>](how-to-extend-the-async-walkthrough-by-using-task-whenall.md)
