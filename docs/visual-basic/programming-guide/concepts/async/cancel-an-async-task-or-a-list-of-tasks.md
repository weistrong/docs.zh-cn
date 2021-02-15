---
description: '了解详细信息：取消异步任务或任务列表 (Visual Basic) '
title: 取消一个异步任务或一组任务
ms.date: 07/20/2015
ms.assetid: a9ee1b71-5bec-4736-a1e9-448042dd7215
ms.openlocfilehash: d61db65db62c62e93abf0a5036533dd2967fe917
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100467077"
---
# <a name="cancel-an-async-task-or-a-list-of-tasks-visual-basic"></a><span data-ttu-id="7ffd6-103">取消一个异步任务或一组任务 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="7ffd6-103">Cancel an Async Task or a List of Tasks (Visual Basic)</span></span>

<span data-ttu-id="7ffd6-104">如果不想等待异步应用程序完成，可以设置一个按钮用来取消它。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-104">You can set up a button that you can use to cancel an async application if you don't want to wait for it to finish.</span></span> <span data-ttu-id="7ffd6-105">通过遵循本主题中的示例，可以为下载一个或一组网站内容的应用程序添加一个取消按钮。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-105">By following the examples in this topic, you can add a cancellation button to an application that downloads the contents of one website or a list of websites.</span></span>

<span data-ttu-id="7ffd6-106">这些示例使用 UI 来 [微调异步应用程序 (Visual Basic) ](fine-tuning-your-async-application.md) 描述。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-106">The examples use the UI that [Fine-Tuning Your Async Application (Visual Basic)](fine-tuning-your-async-application.md) describes.</span></span>

> [!NOTE]
> <span data-ttu-id="7ffd6-107">若要运行该示例，计算机上必须安装有 Visual Studio 2012 或更高版本和 .NET Framework 4.5 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-107">To run the examples, you must have Visual Studio 2012 or newer and the .NET Framework 4.5 or newer installed on your computer.</span></span>

## <a name="cancel-a-task"></a><a name="BKMK_CancelaTask"></a> <span data-ttu-id="7ffd6-108">取消任务</span><span class="sxs-lookup"><span data-stu-id="7ffd6-108">Cancel a Task</span></span>

<span data-ttu-id="7ffd6-109">第一个示例将“取消”按钮与单个下载任务关联。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-109">The first example associates the **Cancel** button with a single download task.</span></span> <span data-ttu-id="7ffd6-110">如果在应用程序下载内容时选择按钮，下载将取消。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-110">If you choose the button while the application is downloading content, the download is canceled.</span></span>

### <a name="downloading-the-example"></a><span data-ttu-id="7ffd6-111">下载示例</span><span class="sxs-lookup"><span data-stu-id="7ffd6-111">Downloading the Example</span></span>

<span data-ttu-id="7ffd6-112">若要下载完整的 Windows Presentation Foundation (WPF) 项目，请参阅 [Async Sample:Fine Tuning Your Application](https://code.msdn.microsoft.com/Async-Fine-Tuning-Your-a676abea)（异步示例：微调应用程序）。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-112">You can download the complete Windows Presentation Foundation (WPF) project from [Async Sample: Fine Tuning Your Application](https://code.msdn.microsoft.com/Async-Fine-Tuning-Your-a676abea) and then follow these steps.</span></span>

1. <span data-ttu-id="7ffd6-113">解压缩下载的文件，然后启动 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-113">Decompress the file that you downloaded, and then start Visual Studio.</span></span>

2. <span data-ttu-id="7ffd6-114">在菜单栏上，依次选择 **“文件”** 、 **“打开”** 和 **“项目/解决方案”** 。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-114">On the menu bar, choose **File**, **Open**, **Project/Solution**.</span></span>

3. <span data-ttu-id="7ffd6-115">在“打开项目”对话框中，打开保存已解压的示例代码的文件夹，然后打开 AsyncFineTuningVB 的解决方案 (.sln) 文件。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-115">In the **Open Project** dialog box, open the folder that holds the sample code that you decompressed, and then open the solution (.sln) file for AsyncFineTuningVB.</span></span>

4. <span data-ttu-id="7ffd6-116">在“解决方案资源管理器”中，打开 “CancelATask” 项目的快捷菜单，然后选择“设为启动项目”。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-116">In **Solution Explorer**, open the shortcut menu for the **CancelATask** project, and then choose **Set as StartUp Project**.</span></span>

5. <span data-ttu-id="7ffd6-117">选择 F5 键运行该项目。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-117">Choose the F5 key to run the project.</span></span>

     <span data-ttu-id="7ffd6-118">选择 Ctrl+F5 键运行该项目，而不进行调试。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-118">Choose the Ctrl+F5 keys to run the project without debugging it.</span></span>

 <span data-ttu-id="7ffd6-119">如果不想下载项目，可在本主题末尾处查看 Mainwindow.xaml 文件的内容。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-119">If you don't want to download the project, you can review the MainWindow.xaml.vb files at the end of this topic.</span></span>

### <a name="building-the-example"></a><span data-ttu-id="7ffd6-120">生成示例</span><span class="sxs-lookup"><span data-stu-id="7ffd6-120">Building the Example</span></span>

<span data-ttu-id="7ffd6-121">下列更改将“取消”按钮添加到下载网站的应用程序中。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-121">The following changes add a **Cancel** button to an application that downloads a website.</span></span> <span data-ttu-id="7ffd6-122">如果不想下载或生成示例，则可在本主题末尾的“完整示例”部分查看最终产品。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-122">If you don't want to download or build the example, you can review the final product in the "Complete Examples" section at the end of this topic.</span></span> <span data-ttu-id="7ffd6-123">星号标记了代码中的更改。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-123">Asterisks mark the changes in the code.</span></span>

<span data-ttu-id="7ffd6-124">要自行生成示例，请按“下载示例”部分的说明逐步操作，选择“StarterCode”而不是“CancelATask”作为“启动项目”。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-124">To build the example yourself, step by step, follow the instructions in the "Downloading the Example" section, but choose **StarterCode** as the **StartUp Project** instead of **CancelATask**.</span></span>

<span data-ttu-id="7ffd6-125">然后，将以下更改添加到该项目的 Mainwindow.xaml 文件中。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-125">Then add the following changes to the MainWindow.xaml.vb file of that project.</span></span>

1. <span data-ttu-id="7ffd6-126">声明一个 `CancellationTokenSource` 变量 `cts`，它作用于所有访问它的方法。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-126">Declare a `CancellationTokenSource` variable, `cts`, that’s in scope for all methods that access it.</span></span>

    ```vb
    Class MainWindow

        ' ***Declare a System.Threading.CancellationTokenSource.
        Dim cts As CancellationTokenSource
    ```

2. <span data-ttu-id="7ffd6-127">为“取消”按钮添加以下事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-127">Add the following event handler for the **Cancel** button.</span></span> <span data-ttu-id="7ffd6-128">用户请求取消时，事件处理程序使用 <xref:System.Threading.CancellationTokenSource.Cancel%2A?displayProperty=nameWithType> 方法通知 `cts`。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-128">The event handler uses the <xref:System.Threading.CancellationTokenSource.Cancel%2A?displayProperty=nameWithType> method to notify `cts` when the user requests cancellation.</span></span>

    ```vb
    ' ***Add an event handler for the Cancel button.
    Private Sub cancelButton_Click(sender As Object, e As RoutedEventArgs)

        If cts IsNot Nothing Then
            cts.Cancel()
        End If
    End Sub
    ```

3. <span data-ttu-id="7ffd6-129">为“启动”按钮 `startButton_Click` 在事件处理程序中进行下列更改。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-129">Make the following changes in the event handler for the **Start** button, `startButton_Click`.</span></span>

    - <span data-ttu-id="7ffd6-130">实例化 `CancellationTokenSource`、`cts`。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-130">Instantiate the `CancellationTokenSource`, `cts`.</span></span>

      ```vb
      ' ***Instantiate the CancellationTokenSource.
      cts = New CancellationTokenSource()
      ```

    - <span data-ttu-id="7ffd6-131">在 `AccessTheWebAsync` 调用中（该操作下载指定网站的内容），将 `cts` 的 <xref:System.Threading.CancellationTokenSource.Token%2A?displayProperty=nameWithType> 属性作为参数发送。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-131">In the call to `AccessTheWebAsync`, which downloads the contents of a specified website, send the <xref:System.Threading.CancellationTokenSource.Token%2A?displayProperty=nameWithType> property of `cts` as an argument.</span></span> <span data-ttu-id="7ffd6-132">如果请求取消，则 `Token` 属性传播消息。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-132">The `Token` property propagates the message if cancellation is requested.</span></span> <span data-ttu-id="7ffd6-133">如果用户选择取消下载操作，请添加显示消息的 catch 块。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-133">Add a catch block that displays a message if the user chooses to cancel the download operation.</span></span> <span data-ttu-id="7ffd6-134">下列代码显示这些更改。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-134">The following code shows the changes.</span></span>

      ```vb
      Try
          ' ***Send a token to carry the message if cancellation is requested.
          Dim contentLength As Integer = Await AccessTheWebAsync(cts.Token)

          resultsTextBox.Text &=
              vbCrLf & $"Length of the downloaded string: {contentLength}." & vbCrLf

          ' *** If cancellation is requested, an OperationCanceledException results.
      Catch ex As OperationCanceledException
          resultsTextBox.Text &= vbCrLf & "Download canceled." & vbCrLf

      Catch ex As Exception
          resultsTextBox.Text &= vbCrLf & "Download failed." & vbCrLf
      End Try
      ```

4. <span data-ttu-id="7ffd6-135">在 `AccessTheWebAsync` 中，使用 <xref:System.Net.Http.HttpClient> 类型中 `GetAsync` 方法的 <xref:System.Net.Http.HttpClient.GetAsync%28System.String%2CSystem.Threading.CancellationToken%29?displayProperty=nameWithType> 重载来下载网站内容。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-135">In `AccessTheWebAsync`, use the  <xref:System.Net.Http.HttpClient.GetAsync%28System.String%2CSystem.Threading.CancellationToken%29?displayProperty=nameWithType> overload of the `GetAsync` method in the <xref:System.Net.Http.HttpClient> type to download the contents of a website.</span></span> <span data-ttu-id="7ffd6-136">将 `ct`（`AccessTheWebAsync` 的 <xref:System.Threading.CancellationToken> 参数）作为第二个参数传递。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-136">Pass `ct`, the <xref:System.Threading.CancellationToken> parameter of `AccessTheWebAsync`, as the second argument.</span></span> <span data-ttu-id="7ffd6-137">如果用户选择“取消”按钮，则令牌携带消息。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-137">The token carries the message if the user chooses the **Cancel** button.</span></span>

    <span data-ttu-id="7ffd6-138">下列代码显示 `AccessTheWebAsync` 中的更改。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-138">The following code shows the changes in `AccessTheWebAsync`.</span></span>

    ```vb
    ' ***Provide a parameter for the CancellationToken.
    Async Function AccessTheWebAsync(ct As CancellationToken) As Task(Of Integer)

        Dim client As HttpClient = New HttpClient()

        resultsTextBox.Text &= vbCrLf & "Ready to download." & vbCrLf

        ' You might need to slow things down to have a chance to cancel.
        Await Task.Delay(250)

        ' GetAsync returns a Task(Of HttpResponseMessage).
        ' ***The ct argument carries the message if the Cancel button is chosen.
        Dim response As HttpResponseMessage = Await client.GetAsync("https://msdn.microsoft.com/library/dd470362.aspx", ct)

        ' Retrieve the website contents from the HttpResponseMessage.
        Dim urlContents As Byte() = Await response.Content.ReadAsByteArrayAsync()

        ' The result of the method is the length of the downloaded website.
        Return urlContents.Length
    End Function
    ```

5. <span data-ttu-id="7ffd6-139">如果不取消该程序，它将生成以下输出：</span><span class="sxs-lookup"><span data-stu-id="7ffd6-139">If you don’t cancel the program, it produces the following output:</span></span>

    ```console
    Ready to download.
    Length of the downloaded string: 158125.
    ```

    <span data-ttu-id="7ffd6-140">如果在程序完成下载内容之前选择 " **取消** " 按钮，则程序会生成以下输出：</span><span class="sxs-lookup"><span data-stu-id="7ffd6-140">If you choose the **Cancel** button before the program finishes downloading the content, the program produces the following output:</span></span>

    ```console
    Ready to download.
    Download canceled.
    ```

## <a name="cancel-a-list-of-tasks"></a><a name="BKMK_CancelaListofTasks"></a> <span data-ttu-id="7ffd6-141">取消任务列表</span><span class="sxs-lookup"><span data-stu-id="7ffd6-141">Cancel a List of Tasks</span></span>

<span data-ttu-id="7ffd6-142">通过将相同的 `CancellationTokenSource` 示例与每个任务关联，可以扩展先前的示例，从而取消多个任务。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-142">You can extend the previous example to cancel many tasks by associating the same `CancellationTokenSource` instance with each task.</span></span> <span data-ttu-id="7ffd6-143">如果选择“取消”按钮，则将取消所有尚未完成的任务。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-143">If you choose the **Cancel** button, you cancel all tasks that aren’t yet complete.</span></span>

### <a name="downloading-the-example"></a><span data-ttu-id="7ffd6-144">下载示例</span><span class="sxs-lookup"><span data-stu-id="7ffd6-144">Downloading the Example</span></span>

<span data-ttu-id="7ffd6-145">若要下载完整的 Windows Presentation Foundation (WPF) 项目，请参阅 [Async Sample:Fine Tuning Your Application](https://code.msdn.microsoft.com/Async-Fine-Tuning-Your-a676abea)（异步示例：微调应用程序）。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-145">You can download the complete Windows Presentation Foundation (WPF) project from [Async Sample: Fine Tuning Your Application](https://code.msdn.microsoft.com/Async-Fine-Tuning-Your-a676abea) and then follow these steps.</span></span>

1. <span data-ttu-id="7ffd6-146">解压缩下载的文件，然后启动 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-146">Decompress the file that you downloaded, and then start Visual Studio.</span></span>

2. <span data-ttu-id="7ffd6-147">在菜单栏上，依次选择 **“文件”** 、 **“打开”** 和 **“项目/解决方案”** 。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-147">On the menu bar, choose **File**, **Open**, **Project/Solution**.</span></span>

3. <span data-ttu-id="7ffd6-148">在“打开项目”对话框中，打开保存已解压的示例代码的文件夹，然后打开 AsyncFineTuningVB 的解决方案 (.sln) 文件。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-148">In the **Open Project** dialog box, open the folder that holds the sample code that you decompressed, and then open the solution (.sln) file for AsyncFineTuningVB.</span></span>

4. <span data-ttu-id="7ffd6-149">在“解决方案资源管理器”中，打开 “CancelAListOfTasks” 项目的快捷菜单，然后选择“设为启动项目”。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-149">In **Solution Explorer**, open the shortcut menu for the **CancelAListOfTasks** project, and then choose **Set as StartUp Project**.</span></span>

5. <span data-ttu-id="7ffd6-150">选择 F5 键运行该项目。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-150">Choose the F5 key to run the project.</span></span>

     <span data-ttu-id="7ffd6-151">选择 Ctrl+F5 键运行该项目，而不进行调试。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-151">Choose the Ctrl+F5 keys to run the project without debugging it.</span></span>

 <span data-ttu-id="7ffd6-152">如果不想下载项目，可在本主题末尾处查看 Mainwindow.xaml 文件的内容。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-152">If you don't want to download the project, you can review the MainWindow.xaml.vb files at the end of this topic.</span></span>

### <a name="building-the-example"></a><span data-ttu-id="7ffd6-153">生成示例</span><span class="sxs-lookup"><span data-stu-id="7ffd6-153">Building the Example</span></span>

<span data-ttu-id="7ffd6-154">要自行扩展示例，请按“下载示例”部分的说明逐步操作，但要选择“CancelATask”作为“启动项目”。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-154">To extend the example yourself, step by step, follow the instructions in the "Downloading the Example" section, but choose **CancelATask** as the **StartUp Project**.</span></span> <span data-ttu-id="7ffd6-155">向该项目添加下列更改。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-155">Add the following changes to that project.</span></span> <span data-ttu-id="7ffd6-156">星号标记了程序中的更改。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-156">Asterisks mark the changes in the program.</span></span>

1. <span data-ttu-id="7ffd6-157">添加一个方法，用于创建 Web 地址的列表。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-157">Add a method to create a list of web addresses.</span></span>

    ```vb
    ' ***Add a method that creates a list of web addresses.
    Private Function SetUpURLList() As List(Of String)

        Dim urls = New List(Of String) From
            {
                "https://msdn.microsoft.com",
                "https://msdn.microsoft.com/library/hh290138.aspx",
                "https://msdn.microsoft.com/library/hh290140.aspx",
                "https://msdn.microsoft.com/library/dd470362.aspx",
                "https://msdn.microsoft.com/library/aa578028.aspx",
                "https://msdn.microsoft.com/library/ms404677.aspx",
                "https://msdn.microsoft.com/library/ff730837.aspx"
            }
        Return urls
    End Function
    ```

2. <span data-ttu-id="7ffd6-158">在 `AccessTheWebAsync` 中调用方法。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-158">Call the method in `AccessTheWebAsync`.</span></span>

    ```vb
    ' ***Call SetUpURLList to make a list of web addresses.
    Dim urlList As List(Of String) = SetUpURLList()
    ```

3. <span data-ttu-id="7ffd6-159">在 `AccessTheWebAsync` 中添加下列循环，用于处理列表中的每个 Web 地址。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-159">Add the following loop in `AccessTheWebAsync` to process each web address in the list.</span></span>

    ```vb
    ' ***Add a loop to process the list of web addresses.
    For Each url In urlList
        ' GetAsync returns a Task(Of HttpResponseMessage).
        ' Argument ct carries the message if the Cancel button is chosen.
        ' ***Note that the Cancel button can cancel all remaining downloads.
        Dim response As HttpResponseMessage = Await client.GetAsync(url, ct)

        ' Retrieve the website contents from the HttpResponseMessage.
        Dim urlContents As Byte() = Await response.Content.ReadAsByteArrayAsync()

        resultsTextBox.Text &=
            vbCrLf & $"Length of the downloaded string: {urlContents.Length}." & vbCrLf
    Next
    ```

4. <span data-ttu-id="7ffd6-160">由于 `AccessTheWebAsync` 显示了长度，因此该方法无需返回任何内容。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-160">Because `AccessTheWebAsync` displays the lengths, the method doesn't need to return anything.</span></span> <span data-ttu-id="7ffd6-161">删除返回语句，并将方法的返回类型更改为 <xref:System.Threading.Tasks.Task>，而不是 <xref:System.Threading.Tasks.Task%601>。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-161">Remove the return statement, and change the return type of the method to <xref:System.Threading.Tasks.Task> instead of <xref:System.Threading.Tasks.Task%601>.</span></span>

    ```vb
    Async Function AccessTheWebAsync(ct As CancellationToken) As Task
    ```

    <span data-ttu-id="7ffd6-162">使用语句而非表达式从 `startButton_Click` 调用方法。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-162">Call the method from `startButton_Click` by using a statement instead of an expression.</span></span>

    ```vb
    Await AccessTheWebAsync(cts.Token)
    ```

5. <span data-ttu-id="7ffd6-163">如果不取消该程序，它将生成以下输出：</span><span class="sxs-lookup"><span data-stu-id="7ffd6-163">If you don’t cancel the program, it produces the following output:</span></span>

    ```console
    Length of the downloaded string: 35939.

    Length of the downloaded string: 237682.

    Length of the downloaded string: 128607.

    Length of the downloaded string: 158124.

    Length of the downloaded string: 204890.

    Length of the downloaded string: 175488.

    Length of the downloaded string: 145790.

    Downloads complete.
    ```

    <span data-ttu-id="7ffd6-164">如果在下载完成之前选择“取消”按钮，则输出将包含取消前已完成下载的长度。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-164">If you choose the **Cancel** button before the downloads are complete, the output contains the lengths of the downloads that completed before the cancellation.</span></span>

    ```console
    Length of the downloaded string: 35939.

    Length of the downloaded string: 237682.

    Length of the downloaded string: 128607.

    Downloads canceled.
    ```

## <a name="complete-examples"></a><a name="BKMK_CompleteExamples"></a> <span data-ttu-id="7ffd6-165">完整示例</span><span class="sxs-lookup"><span data-stu-id="7ffd6-165">Complete Examples</span></span>

<span data-ttu-id="7ffd6-166">以下各部分包含每个前面示例的代码。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-166">The following sections contain the code for each of the previous examples.</span></span> <span data-ttu-id="7ffd6-167">请注意，必须为 <xref:System.Net.Http> 添加引用。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-167">Notice that you must add a reference for <xref:System.Net.Http>.</span></span>

<span data-ttu-id="7ffd6-168">可以从[异步示例：Fine Tuning Your Application](https://code.msdn.microsoft.com/Async-Fine-Tuning-Your-a676abea)（异步示例：微调应用程序）下载这些项目。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-168">You can download the projects from [Async Sample: Fine Tuning Your Application](https://code.msdn.microsoft.com/Async-Fine-Tuning-Your-a676abea).</span></span>

### <a name="cancel-a-task-example"></a><span data-ttu-id="7ffd6-169">取消任务示例</span><span class="sxs-lookup"><span data-stu-id="7ffd6-169">Cancel a Task Example</span></span>

<span data-ttu-id="7ffd6-170">下面的代码是取消单个任务的示例的完整 Mainwindow.xaml 文件。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-170">The following code is the complete MainWindow.xaml.vb file for the example that cancels a single task.</span></span>

```vb
' Add an Imports directive and a reference for System.Net.Http.
Imports System.Net.Http

' Add the following Imports directive for System.Threading.
Imports System.Threading

Class MainWindow

    ' ***Declare a System.Threading.CancellationTokenSource.
    Dim cts As CancellationTokenSource

    Private Async Sub startButton_Click(sender As Object, e As RoutedEventArgs)
        ' ***Instantiate the CancellationTokenSource.
        cts = New CancellationTokenSource()

        resultsTextBox.Clear()

        Try
            ' ***Send a token to carry the message if cancellation is requested.
            Dim contentLength As Integer = Await AccessTheWebAsync(cts.Token)

            resultsTextBox.Text &=
                vbCrLf & $"Length of the downloaded string: {contentLength}." & vbCrLf

            ' *** If cancellation is requested, an OperationCanceledException results.
        Catch ex As OperationCanceledException
            resultsTextBox.Text &= vbCrLf & "Download canceled." & vbCrLf

        Catch ex As Exception
            resultsTextBox.Text &= vbCrLf & "Download failed." & vbCrLf
        End Try

        ' ***Set the CancellationTokenSource to Nothing when the download is complete.
        cts = Nothing
    End Sub

    ' ***Add an event handler for the Cancel button.
    Private Sub cancelButton_Click(sender As Object, e As RoutedEventArgs)

        If cts IsNot Nothing Then
            cts.Cancel()
        End If
    End Sub

    ' ***Provide a parameter for the CancellationToken.
    Async Function AccessTheWebAsync(ct As CancellationToken) As Task(Of Integer)

        Dim client As HttpClient = New HttpClient()

        resultsTextBox.Text &=
            vbCrLf & "Ready to download." & vbCrLf

        ' You might need to slow things down to have a chance to cancel.
        Await Task.Delay(250)

        ' GetAsync returns a Task(Of HttpResponseMessage).
        ' ***The ct argument carries the message if the Cancel button is chosen.
        Dim response As HttpResponseMessage = Await client.GetAsync("https://msdn.microsoft.com/library/dd470362.aspx", ct)

        ' Retrieve the website contents from the HttpResponseMessage.
        Dim urlContents As Byte() = Await response.Content.ReadAsByteArrayAsync()

        ' The result of the method is the length of the downloaded website.
        Return urlContents.Length
    End Function
End Class

' Output for a successful download:

' Ready to download.

' Length of the downloaded string: 158125.

' Or, if you cancel:

' Ready to download.

' Download canceled.
```

### <a name="cancel-a-list-of-tasks-example"></a><span data-ttu-id="7ffd6-171">取消任务列表示例</span><span class="sxs-lookup"><span data-stu-id="7ffd6-171">Cancel a List of Tasks Example</span></span>

<span data-ttu-id="7ffd6-172">下面的代码是取消任务列表的示例的完整 Mainwindow.xaml 文件。</span><span class="sxs-lookup"><span data-stu-id="7ffd6-172">The following code is the complete MainWindow.xaml.vb file for the example that cancels a list of tasks.</span></span>

```vb
' Add an Imports directive and a reference for System.Net.Http.
Imports System.Net.Http

' Add the following Imports directive for System.Threading.
Imports System.Threading

Class MainWindow

    ' Declare a System.Threading.CancellationTokenSource.
    Dim cts As CancellationTokenSource

    Private Async Sub startButton_Click(sender As Object, e As RoutedEventArgs)

        ' Instantiate the CancellationTokenSource.
        cts = New CancellationTokenSource()

        resultsTextBox.Clear()

        Try
            ' ***AccessTheWebAsync returns a Task, not a Task(Of Integer).
            Await AccessTheWebAsync(cts.Token)
            '  ***Small change in the display lines.
            resultsTextBox.Text &= vbCrLf & "Downloads complete."

        Catch ex As OperationCanceledException
            resultsTextBox.Text &= vbCrLf & "Downloads canceled." & vbCrLf

        Catch ex As Exception
            resultsTextBox.Text &= vbCrLf & "Downloads failed." & vbCrLf
        End Try

        ' Set the CancellationTokenSource to Nothing when the download is complete.
        cts = Nothing
    End Sub

    ' Add an event handler for the Cancel button.
    Private Sub cancelButton_Click(sender As Object, e As RoutedEventArgs)

        If cts IsNot Nothing Then
            cts.Cancel()
        End If
    End Sub

    ' Provide a parameter for the CancellationToken.
    ' ***Change the return type to Task because the method has no return statement.
    Async Function AccessTheWebAsync(ct As CancellationToken) As Task

        Dim client As HttpClient = New HttpClient()

        ' ***Call SetUpURLList to make a list of web addresses.
        Dim urlList As List(Of String) = SetUpURLList()

        ' ***Add a loop to process the list of web addresses.
        For Each url In urlList
            ' GetAsync returns a Task(Of HttpResponseMessage).
            ' Argument ct carries the message if the Cancel button is chosen.
            ' ***Note that the Cancel button can cancel all remaining downloads.
            Dim response As HttpResponseMessage = Await client.GetAsync(url, ct)

            ' Retrieve the website contents from the HttpResponseMessage.
            Dim urlContents As Byte() = Await response.Content.ReadAsByteArrayAsync()

            resultsTextBox.Text &=
                vbCrLf & $"Length of the downloaded string: {urlContents.Length}." & vbCrLf
        Next
    End Function

    ' ***Add a method that creates a list of web addresses.
    Private Function SetUpURLList() As List(Of String)

        Dim urls = New List(Of String) From
            {
                "https://msdn.microsoft.com",
                "https://msdn.microsoft.com/library/hh290138.aspx",
                "https://msdn.microsoft.com/library/hh290140.aspx",
                "https://msdn.microsoft.com/library/dd470362.aspx",
                "https://msdn.microsoft.com/library/aa578028.aspx",
                "https://msdn.microsoft.com/library/ms404677.aspx",
                "https://msdn.microsoft.com/library/ff730837.aspx"
            }
        Return urls
    End Function

End Class

' Output if you do not choose to cancel:

' Length of the downloaded string: 35939.

' Length of the downloaded string: 237682.

' Length of the downloaded string: 128607.

' Length of the downloaded string: 158124.

' Length of the downloaded string: 204890.

' Length of the downloaded string: 175488.

' Length of the downloaded string: 145790.

' Downloads complete.

'  Sample output if you choose to cancel:

' Length of the downloaded string: 35939.

' Length of the downloaded string: 237682.

' Length of the downloaded string: 128607.

' Downloads canceled.
```

## <a name="see-also"></a><span data-ttu-id="7ffd6-173">请参阅</span><span class="sxs-lookup"><span data-stu-id="7ffd6-173">See also</span></span>

- <xref:System.Threading.CancellationTokenSource>
- <xref:System.Threading.CancellationToken>
- [<span data-ttu-id="7ffd6-174">使用 Async 和 Await 的异步编程 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="7ffd6-174">Asynchronous Programming with Async and Await (Visual Basic)</span></span>](index.md)
- [<span data-ttu-id="7ffd6-175">微调异步应用程序 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="7ffd6-175">Fine-Tuning Your Async Application (Visual Basic)</span></span>](fine-tuning-your-async-application.md)
- [<span data-ttu-id="7ffd6-176">异步示例：微调应用程序</span><span class="sxs-lookup"><span data-stu-id="7ffd6-176">Async Sample: Fine Tuning Your Application</span></span>](https://code.msdn.microsoft.com/Async-Fine-Tuning-Your-a676abea)
