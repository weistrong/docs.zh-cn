---
description: '了解详细信息：演练：使用 Async 和 Await 访问 Web (Visual Basic) '
title: 演练：使用 Async 和 Await 访问 Web
ms.date: 07/20/2015
ms.assetid: 84fd047f-fab8-4d89-8ced-104fb7310a91
ms.openlocfilehash: 08488d4909e4fbc40cc11213eb293c2693fdec71
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100474156"
---
# <a name="walkthrough-accessing-the-web-by-using-async-and-await-visual-basic"></a><span data-ttu-id="2ba80-103">演练：使用 Async 和 Await 访问 Web (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="2ba80-103">Walkthrough: Accessing the Web by Using Async and Await (Visual Basic)</span></span>

<span data-ttu-id="2ba80-104">使用 async/await 功能可以更轻松直观地编写异步程序。</span><span class="sxs-lookup"><span data-stu-id="2ba80-104">You can write asynchronous programs more easily and intuitively by using async/await features.</span></span> <span data-ttu-id="2ba80-105">你可以编写类似于同步代码的异步代码，并让编译器处理异步代码通常需要的疑难回调函数和延续。</span><span class="sxs-lookup"><span data-stu-id="2ba80-105">You can write asynchronous code that looks like synchronous code and let the compiler handle the difficult callback functions and continuations that asynchronous code usually entails.</span></span>

<span data-ttu-id="2ba80-106">有关异步功能的详细信息，请参阅 [异步编程 With async 和 Await (Visual Basic) ](index.md)。</span><span class="sxs-lookup"><span data-stu-id="2ba80-106">For more information about the Async feature, see [Asynchronous Programming with Async and Await (Visual Basic)](index.md).</span></span>

<span data-ttu-id="2ba80-107">本演练从对网站列表中的字节数进行求和的同步 Windows Presentation Foundation (WPF) 应用程序入手，</span><span class="sxs-lookup"><span data-stu-id="2ba80-107">This walkthrough starts with a synchronous Windows Presentation Foundation (WPF) application that sums the number of bytes in a list of websites.</span></span> <span data-ttu-id="2ba80-108">然后使用新功能将该应用程序转换为异步解决方案。</span><span class="sxs-lookup"><span data-stu-id="2ba80-108">The walkthrough then converts the application to an asynchronous solution by using the new features.</span></span>

<span data-ttu-id="2ba80-109">如果不想自行生成应用程序，可以从[开发人员代码示例](https://code.msdn.microsoft.com/Async-Sample-Accessing-the-9c10497f)下载“Async 示例：访问 Web 演练（C# 和 Visual Basic）”。</span><span class="sxs-lookup"><span data-stu-id="2ba80-109">If you don't want to build the applications yourself, you can download "Async Sample: Accessing the Web Walkthrough (C# and Visual Basic)" from [Developer Code Samples](https://code.msdn.microsoft.com/Async-Sample-Accessing-the-9c10497f).</span></span>

<span data-ttu-id="2ba80-110">在本演练中，你将完成下列任务：</span><span class="sxs-lookup"><span data-stu-id="2ba80-110">In this walkthrough, you complete the following tasks:</span></span>

> [!div class="checklist"]
>
> - [<span data-ttu-id="2ba80-111">创建 WPF 应用程序</span><span class="sxs-lookup"><span data-stu-id="2ba80-111">Create a WPF application</span></span>](#create-a-wpf-application)
> - [<span data-ttu-id="2ba80-112">设计简单的 WPF MainWindow</span><span class="sxs-lookup"><span data-stu-id="2ba80-112">Design a simple WPF MainWindow</span></span>](#design-a-simple-wpf-mainwindow)
> - [<span data-ttu-id="2ba80-113">添加引用</span><span class="sxs-lookup"><span data-stu-id="2ba80-113">Add a reference</span></span>](#add-a-reference)
> - [<span data-ttu-id="2ba80-114">添加必要的 Imports 语句</span><span class="sxs-lookup"><span data-stu-id="2ba80-114">Add necessary Imports statements</span></span>](#add-necessary-imports-statements)
> - [<span data-ttu-id="2ba80-115">创建同步应用程序</span><span class="sxs-lookup"><span data-stu-id="2ba80-115">Create a synchronous application</span></span>](#create-a-synchronous-application)
> - [<span data-ttu-id="2ba80-116">测试同步解决方案</span><span class="sxs-lookup"><span data-stu-id="2ba80-116">Test the synchronous solution</span></span>](#test-the-synchronous-solution)
> - [<span data-ttu-id="2ba80-117">将 GetURLContents 转换为异步方法</span><span class="sxs-lookup"><span data-stu-id="2ba80-117">Convert GetURLContents to an asynchronous method</span></span>](#convert-geturlcontents-to-an-asynchronous-method)
> - [<span data-ttu-id="2ba80-118">将 SumPageSizes 转换为异步方法</span><span class="sxs-lookup"><span data-stu-id="2ba80-118">Convert SumPageSizes to an asynchronous method</span></span>](#convert-sumpagesizes-to-an-asynchronous-method)
> - [<span data-ttu-id="2ba80-119">将 startButton_Click 转换为异步方法</span><span class="sxs-lookup"><span data-stu-id="2ba80-119">Convert startButton_Click to an asynchronous method</span></span>](#convert-startbutton_click-to-an-asynchronous-method)
> - [<span data-ttu-id="2ba80-120">测试异步解决方案</span><span class="sxs-lookup"><span data-stu-id="2ba80-120">Test the asynchronous solution</span></span>](#test-the-asynchronous-solution)
> - [<span data-ttu-id="2ba80-121">将 GetURLContentsAsync 方法替换为 .NET Framework 方法</span><span class="sxs-lookup"><span data-stu-id="2ba80-121">Replace the GetURLContentsAsync method with a .NET Framework method</span></span>](#replace-the-geturlcontentsasync-method-with-a-net-framework-method)

<span data-ttu-id="2ba80-122">有关完整的异步示例，请参阅 " [示例](#example) " 部分。</span><span class="sxs-lookup"><span data-stu-id="2ba80-122">See the [Example](#example) section for the complete asynchronous example.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2ba80-123">先决条件</span><span class="sxs-lookup"><span data-stu-id="2ba80-123">Prerequisites</span></span>

<span data-ttu-id="2ba80-124">计算机上必须安装 Visual Studio 2012 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="2ba80-124">Visual Studio 2012 or later must be installed on your computer.</span></span> <span data-ttu-id="2ba80-125">有关详细信息，请参阅 Visual Studio [下载](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019) 页。</span><span class="sxs-lookup"><span data-stu-id="2ba80-125">For more information, see the Visual Studio [Downloads](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019) page.</span></span>

## <a name="create-a-wpf-application"></a><span data-ttu-id="2ba80-126">创建 WPF 应用程序</span><span class="sxs-lookup"><span data-stu-id="2ba80-126">Create a WPF application</span></span>

1. <span data-ttu-id="2ba80-127">启动 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="2ba80-127">Start Visual Studio.</span></span>

2. <span data-ttu-id="2ba80-128">在菜单栏上，依次选择“文件” 、“新建” 、“项目” 。</span><span class="sxs-lookup"><span data-stu-id="2ba80-128">On the menu bar, choose **File**, **New**, **Project**.</span></span>

    <span data-ttu-id="2ba80-129">**“新建项目”** 对话框随即打开。</span><span class="sxs-lookup"><span data-stu-id="2ba80-129">The **New Project** dialog box opens.</span></span>

3. <span data-ttu-id="2ba80-130">在 " **已安装的模板** " 窗格中选择 "Visual Basic"，然后从项目类型列表中选择 " **WPF 应用程序** "。</span><span class="sxs-lookup"><span data-stu-id="2ba80-130">In the **Installed Templates** pane, choose Visual Basic, and then choose **WPF Application** from the list of project types.</span></span>

4. <span data-ttu-id="2ba80-131">在“名称”文本框中，输入 `AsyncExampleWPF`，然后选择“确定”按钮。</span><span class="sxs-lookup"><span data-stu-id="2ba80-131">In the **Name** text box, enter `AsyncExampleWPF`, and then choose the **OK** button.</span></span>

    <span data-ttu-id="2ba80-132">新项目将出现在“解决方案资源管理器”中。</span><span class="sxs-lookup"><span data-stu-id="2ba80-132">The new project appears in **Solution Explorer**.</span></span>

## <a name="design-a-simple-wpf-mainwindow"></a><span data-ttu-id="2ba80-133">设计简单的 WPF MainWindow</span><span class="sxs-lookup"><span data-stu-id="2ba80-133">Design a simple WPF MainWindow</span></span>

1. <span data-ttu-id="2ba80-134">在 Visual Studio 代码编辑器中，选择 **“MainWindow.xaml”** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="2ba80-134">In the Visual Studio Code Editor, choose the **MainWindow.xaml** tab.</span></span>

2. <span data-ttu-id="2ba80-135">如果 " **工具箱** " 窗口不可见，请打开 " **视图** " 菜单，然后选择 **"工具箱**"。</span><span class="sxs-lookup"><span data-stu-id="2ba80-135">If the **Toolbox** window isn’t visible, open the **View** menu, and then choose **Toolbox**.</span></span>

3. <span data-ttu-id="2ba80-136">向“MainWindow”窗口添加一个“Button”控件和一个“TextBox”控件。</span><span class="sxs-lookup"><span data-stu-id="2ba80-136">Add a **Button** control and a **TextBox** control to the **MainWindow** window.</span></span>

4. <span data-ttu-id="2ba80-137">突出显示“TextBox”控件，在“属性”窗口中，设置下列值：</span><span class="sxs-lookup"><span data-stu-id="2ba80-137">Highlight the **TextBox** control and, in the **Properties** window, set the following values:</span></span>

    - <span data-ttu-id="2ba80-138">将“名称”属性设置为 `resultsTextBox`。</span><span class="sxs-lookup"><span data-stu-id="2ba80-138">Set the **Name** property to `resultsTextBox`.</span></span>

    - <span data-ttu-id="2ba80-139">将“高度”属性设置为 250。</span><span class="sxs-lookup"><span data-stu-id="2ba80-139">Set the **Height** property to 250.</span></span>

    - <span data-ttu-id="2ba80-140">将“宽度”属性设置为 500。</span><span class="sxs-lookup"><span data-stu-id="2ba80-140">Set the **Width** property to 500.</span></span>

    - <span data-ttu-id="2ba80-141">在“文本”选项卡中，指定等宽字体，例如 Lucida Console 或 Global Monospace。</span><span class="sxs-lookup"><span data-stu-id="2ba80-141">On the **Text** tab, specify a monospaced font, such as Lucida Console or Global Monospace.</span></span>

5. <span data-ttu-id="2ba80-142">突出显示“Button”控件，在“属性”窗口中，设置下列值：</span><span class="sxs-lookup"><span data-stu-id="2ba80-142">Highlight the **Button** control and, in the **Properties** window, set the following values:</span></span>

    - <span data-ttu-id="2ba80-143">将“名称”属性设置为 `startButton`。</span><span class="sxs-lookup"><span data-stu-id="2ba80-143">Set the **Name** property to `startButton`.</span></span>

    - <span data-ttu-id="2ba80-144">将“内容”属性的值从“Button”更改为“Start”。</span><span class="sxs-lookup"><span data-stu-id="2ba80-144">Change the value of the **Content** property from **Button** to **Start**.</span></span>

6. <span data-ttu-id="2ba80-145">确定文本框和按钮的位置，以便它们都在“MainWindow”窗口中显示。</span><span class="sxs-lookup"><span data-stu-id="2ba80-145">Position the text box and the button so that both appear in the **MainWindow** window.</span></span>

    <span data-ttu-id="2ba80-146">有关 WPF XAML 设计器的详细信息，请参阅[使用 XAML 设计器创建 UI](/visualstudio/xaml-tools/creating-a-ui-by-using-xaml-designer-in-visual-studio)。</span><span class="sxs-lookup"><span data-stu-id="2ba80-146">For more information about the WPF XAML Designer, see [Creating a UI by using XAML Designer](/visualstudio/xaml-tools/creating-a-ui-by-using-xaml-designer-in-visual-studio).</span></span>

## <a name="add-a-reference"></a><span data-ttu-id="2ba80-147">添加引用</span><span class="sxs-lookup"><span data-stu-id="2ba80-147">Add a reference</span></span>

1. <span data-ttu-id="2ba80-148">在“解决方案资源管理器”中，突出显示项目的名称。</span><span class="sxs-lookup"><span data-stu-id="2ba80-148">In **Solution Explorer**, highlight your project's name.</span></span>

2. <span data-ttu-id="2ba80-149">在菜单栏上，依次选择“项目”、“添加引用”。</span><span class="sxs-lookup"><span data-stu-id="2ba80-149">On the menu bar, choose **Project**, **Add Reference**.</span></span>

    <span data-ttu-id="2ba80-150">此时将显示“引用管理器”对话框。</span><span class="sxs-lookup"><span data-stu-id="2ba80-150">The **Reference Manager** dialog box appears.</span></span>

3. <span data-ttu-id="2ba80-151">在对话框顶部，验证项目是否以 .NET Framework 4.5 或更高版本为目标。</span><span class="sxs-lookup"><span data-stu-id="2ba80-151">At the top of the dialog box, verify that your project is targeting the .NET Framework 4.5 or higher.</span></span>

4. <span data-ttu-id="2ba80-152">在“程序集”区域，选择“Framework”（如果尚未选择它）。</span><span class="sxs-lookup"><span data-stu-id="2ba80-152">In the **Assemblies** area, choose **Framework** if it isn’t already chosen.</span></span>

5. <span data-ttu-id="2ba80-153">在名称列表中，选中“System.Net.Http”复选框。</span><span class="sxs-lookup"><span data-stu-id="2ba80-153">In the list of names, select the **System.Net.Http** check box.</span></span>

6. <span data-ttu-id="2ba80-154">选择“确定”按钮关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="2ba80-154">Choose the **OK** button to close the dialog box.</span></span>

## <a name="add-necessary-imports-statements"></a><span data-ttu-id="2ba80-155">添加必要的 Imports 语句</span><span class="sxs-lookup"><span data-stu-id="2ba80-155">Add necessary Imports statements</span></span>

1. <span data-ttu-id="2ba80-156">在 **解决方案资源管理器** 中，打开 mainwindow.xaml 的快捷菜单，然后选择 " **查看代码**"。</span><span class="sxs-lookup"><span data-stu-id="2ba80-156">In **Solution Explorer**, open the shortcut menu for MainWindow.xaml.vb, and then choose **View Code**.</span></span>

2. <span data-ttu-id="2ba80-157">将以下语句添加到 `Imports` 代码文件的顶部（如果它们尚不存在）。</span><span class="sxs-lookup"><span data-stu-id="2ba80-157">Add the following `Imports` statements at the top of the code file if they’re not already present.</span></span>

    ```vb
    Imports System.Net.Http
    Imports System.Net
    Imports System.IO
    ```

## <a name="create-a-synchronous-application"></a><span data-ttu-id="2ba80-158">创建同步应用程序</span><span class="sxs-lookup"><span data-stu-id="2ba80-158">Create a synchronous application</span></span>

1. <span data-ttu-id="2ba80-159">在设计窗口 Mainwindow.xaml 中，双击 " **开始** " 按钮以 `startButton_Click` 在 mainwindow.xaml 中创建事件处理程序。</span><span class="sxs-lookup"><span data-stu-id="2ba80-159">In the design window, MainWindow.xaml, double-click the **Start** button to create the `startButton_Click` event handler in MainWindow.xaml.vb.</span></span>

2. <span data-ttu-id="2ba80-160">在 Mainwindow.xaml 中，将以下代码复制到的正文中 `startButton_Click` ：</span><span class="sxs-lookup"><span data-stu-id="2ba80-160">In MainWindow.xaml.vb, copy the following code into the body of `startButton_Click`:</span></span>

    ```vb
    resultsTextBox.Clear()
    SumPageSizes()
    resultsTextBox.Text &= vbCrLf & "Control returned to startButton_Click."
    ```

    <span data-ttu-id="2ba80-161">代码调用驱动应用程序 `SumPageSizes` 的方法，并在控件返回到 `startButton_Click` 时显示一条消息。</span><span class="sxs-lookup"><span data-stu-id="2ba80-161">The code calls the method that drives the application, `SumPageSizes`, and displays a message when control returns to `startButton_Click`.</span></span>

3. <span data-ttu-id="2ba80-162">该同步解决方案的代码包含以下四个方法：</span><span class="sxs-lookup"><span data-stu-id="2ba80-162">The code for the synchronous solution contains the following four methods:</span></span>

    - <span data-ttu-id="2ba80-163">`SumPageSizes`，从 `SetUpURLList` 获取网页 URL 列表并随后调用 `GetURLContents` 和 `DisplayResults` 以处理每个 URL。</span><span class="sxs-lookup"><span data-stu-id="2ba80-163">`SumPageSizes`, which gets a list of webpage URLs from `SetUpURLList` and then calls `GetURLContents` and `DisplayResults` to process each URL.</span></span>

    - <span data-ttu-id="2ba80-164">`SetUpURLList`，生成并返回 Web 地址列表。</span><span class="sxs-lookup"><span data-stu-id="2ba80-164">`SetUpURLList`, which makes and returns a list of web addresses.</span></span>

    - <span data-ttu-id="2ba80-165">`GetURLContents`，下载每个网站的内容并将内容作为字节数组返回。</span><span class="sxs-lookup"><span data-stu-id="2ba80-165">`GetURLContents`, which downloads the contents of each website and returns the contents as a byte array.</span></span>

    - <span data-ttu-id="2ba80-166">`DisplayResults`，显示每个 URL 的字节数组中的字节数。</span><span class="sxs-lookup"><span data-stu-id="2ba80-166">`DisplayResults`, which displays  the number of bytes in the byte array for each URL.</span></span>

    <span data-ttu-id="2ba80-167">复制以下四个方法，然后将它们粘贴到 `startButton_Click` mainwindow.xaml 中的事件处理程序下：</span><span class="sxs-lookup"><span data-stu-id="2ba80-167">Copy the following four methods, and then paste them under the `startButton_Click` event handler in MainWindow.xaml.vb:</span></span>

    ```vb
    Private Sub SumPageSizes()

        ' Make a list of web addresses.
        Dim urlList As List(Of String) = SetUpURLList()

        Dim total = 0
        For Each url In urlList
            ' GetURLContents returns the contents of url as a byte array.
            Dim urlContents As Byte() = GetURLContents(url)

            DisplayResults(url, urlContents)

            ' Update the total.
            total += urlContents.Length
        Next

        ' Display the total count for all of the web addresses.
        resultsTextBox.Text &= String.Format(vbCrLf & vbCrLf & "Total bytes returned:  {0}" & vbCrLf, total)
    End Sub

    Private Function SetUpURLList() As List(Of String)

        Dim urls = New List(Of String) From
            {
                "https://msdn.microsoft.com/library/windows/apps/br211380.aspx",
                "https://msdn.microsoft.com",
                "https://msdn.microsoft.com/library/hh290136.aspx",
                "https://msdn.microsoft.com/library/ee256749.aspx",
                "https://msdn.microsoft.com/library/hh290138.aspx",
                "https://msdn.microsoft.com/library/hh290140.aspx",
                "https://msdn.microsoft.com/library/dd470362.aspx",
                "https://msdn.microsoft.com/library/aa578028.aspx",
                "https://msdn.microsoft.com/library/ms404677.aspx",
                "https://msdn.microsoft.com/library/ff730837.aspx"
            }
        Return urls
    End Function

    Private Function GetURLContents(url As String) As Byte()

        ' The downloaded resource ends up in the variable named content.
        Dim content = New MemoryStream()

        ' Initialize an HttpWebRequest for the current URL.
        Dim webReq = CType(WebRequest.Create(url), HttpWebRequest)

        ' Send the request to the Internet resource and wait for
        ' the response.
        ' Note: you can't use HttpWebRequest.GetResponse in a Windows Store app.
        Using response As WebResponse = webReq.GetResponse()
            ' Get the data stream that is associated with the specified URL.
            Using responseStream As Stream = response.GetResponseStream()
                ' Read the bytes in responseStream and copy them to content.
                responseStream.CopyTo(content)
            End Using
        End Using

        ' Return the result as a byte array.
        Return content.ToArray()
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

## <a name="test-the-synchronous-solution"></a><span data-ttu-id="2ba80-168">测试同步解决方案</span><span class="sxs-lookup"><span data-stu-id="2ba80-168">Test the synchronous solution</span></span>

1. <span data-ttu-id="2ba80-169">按 F5 键以运行程序，然后选择 **“启动”** 按钮。</span><span class="sxs-lookup"><span data-stu-id="2ba80-169">Choose the F5 key to run the program, and then choose the **Start** button.</span></span>

    <span data-ttu-id="2ba80-170">此时应显示类似于以下列表的输出：</span><span class="sxs-lookup"><span data-stu-id="2ba80-170">Output that resembles the following list should appear:</span></span>

    ```console
    msdn.microsoft.com/library/windows/apps/br211380.aspx        383832
    msdn.microsoft.com                                            33964
    msdn.microsoft.com/library/hh290136.aspx               225793
    msdn.microsoft.com/library/ee256749.aspx               143577
    msdn.microsoft.com/library/hh290138.aspx               237372
    msdn.microsoft.com/library/hh290140.aspx               128279
    msdn.microsoft.com/library/dd470362.aspx               157649
    msdn.microsoft.com/library/aa578028.aspx               204457
    msdn.microsoft.com/library/ms404677.aspx               176405
    msdn.microsoft.com/library/ff730837.aspx               143474

    Total bytes returned:  1834802

    Control returned to startButton_Click.
    ```

    <span data-ttu-id="2ba80-171">请注意，显示计数需要几秒钟时间。</span><span class="sxs-lookup"><span data-stu-id="2ba80-171">Notice that it takes a few seconds to display the counts.</span></span> <span data-ttu-id="2ba80-172">与此同时，在等待请求的资源下载时，UI 线程处于被阻止状态。</span><span class="sxs-lookup"><span data-stu-id="2ba80-172">During that time, the UI thread is blocked while it waits for requested resources to download.</span></span> <span data-ttu-id="2ba80-173">因此，选择“启动”按钮后，将无法移动、最大化、最小化显示窗口，甚至也无法关闭显示窗口。</span><span class="sxs-lookup"><span data-stu-id="2ba80-173">As a result, you can't move, maximize, minimize, or even close the display window after you choose the  **Start** button.</span></span> <span data-ttu-id="2ba80-174">在字节计数开始显示之前，这些操作都会失败。</span><span class="sxs-lookup"><span data-stu-id="2ba80-174">These efforts fail until the byte counts start to appear.</span></span> <span data-ttu-id="2ba80-175">如果网站没有响应，将不会指示哪个网站失败。</span><span class="sxs-lookup"><span data-stu-id="2ba80-175">If a website isn’t responding, you have no indication of which site failed.</span></span> <span data-ttu-id="2ba80-176">甚至停止等待和关闭程序也会很困难。</span><span class="sxs-lookup"><span data-stu-id="2ba80-176">It is difficult even to stop waiting and close the program.</span></span>

## <a name="convert-geturlcontents-to-an-asynchronous-method"></a><span data-ttu-id="2ba80-177">将 GetURLContents 转换为异步方法</span><span class="sxs-lookup"><span data-stu-id="2ba80-177">Convert GetURLContents to an asynchronous method</span></span>

1. <span data-ttu-id="2ba80-178">若要将同步解决方案转换为异步解决方案，最好开始使用， `GetURLContents` 因为调用 <xref:System.Net.HttpWebRequest.GetResponse%2A?displayProperty=nameWithType> 方法和 <xref:System.IO.Stream.CopyTo%2A?displayProperty=nameWithType> 方法是应用程序访问 web 的位置。</span><span class="sxs-lookup"><span data-stu-id="2ba80-178">To convert the synchronous solution to an asynchronous solution, the best place to start is in `GetURLContents` because the calls to the <xref:System.Net.HttpWebRequest.GetResponse%2A?displayProperty=nameWithType> method and to the <xref:System.IO.Stream.CopyTo%2A?displayProperty=nameWithType> method are where the application accesses the web.</span></span> <span data-ttu-id="2ba80-179">.NET Framework 提供两种方法的异步版本，这让转换变得轻松。</span><span class="sxs-lookup"><span data-stu-id="2ba80-179">The .NET Framework makes the conversion easy by supplying asynchronous versions of both methods.</span></span>

    <span data-ttu-id="2ba80-180">有关 `GetURLContents` 中使用的方法的详细信息，请参阅 <xref:System.Net.WebRequest>。</span><span class="sxs-lookup"><span data-stu-id="2ba80-180">For more information about the methods that are used in `GetURLContents`, see <xref:System.Net.WebRequest>.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2ba80-181">在你按照本演练中的步骤进行操作的过程中，将出现多个编译器错误。</span><span class="sxs-lookup"><span data-stu-id="2ba80-181">As you follow the steps in this walkthrough, several compiler errors appear.</span></span> <span data-ttu-id="2ba80-182">你可以忽略这些错误并继续演练。</span><span class="sxs-lookup"><span data-stu-id="2ba80-182">You can ignore them and continue with the walkthrough.</span></span>

    <span data-ttu-id="2ba80-183">将在 `GetURLContents` 的第三行中调用的方法从 `GetResponse` 更改为基于任务的异步 <xref:System.Net.WebRequest.GetResponseAsync%2A> 方法。</span><span class="sxs-lookup"><span data-stu-id="2ba80-183">Change the method that's called in the third line of `GetURLContents` from `GetResponse` to the asynchronous, task-based <xref:System.Net.WebRequest.GetResponseAsync%2A> method.</span></span>

    ```vb
    Using response As WebResponse = webReq.GetResponseAsync()
    ```

2. <span data-ttu-id="2ba80-184">`GetResponseAsync` 返回 <xref:System.Threading.Tasks.Task%601>。</span><span class="sxs-lookup"><span data-stu-id="2ba80-184">`GetResponseAsync` returns a <xref:System.Threading.Tasks.Task%601>.</span></span> <span data-ttu-id="2ba80-185">在这种情况下，任务返回变量 `TResult` 具有类型 <xref:System.Net.WebResponse>。</span><span class="sxs-lookup"><span data-stu-id="2ba80-185">In this case, the *task return variable*, `TResult`, has type <xref:System.Net.WebResponse>.</span></span> <span data-ttu-id="2ba80-186">该任务是在请求的任务已下载且任务已完成运行后，生成实际 `WebResponse` 对象的承诺。</span><span class="sxs-lookup"><span data-stu-id="2ba80-186">The task is a promise to produce an actual `WebResponse` object after the requested data has been downloaded and the task has run to completion.</span></span>

    <span data-ttu-id="2ba80-187">若要 `WebResponse` 从任务检索值，请将 [Await](../../../language-reference/operators/await-operator.md) 运算符应用到对的调用 `GetResponseAsync` ，如以下代码所示。</span><span class="sxs-lookup"><span data-stu-id="2ba80-187">To retrieve the `WebResponse` value from the task, apply an [Await](../../../language-reference/operators/await-operator.md) operator to the call to `GetResponseAsync`, as the following code shows.</span></span>

    ```vb
    Using response As WebResponse = Await webReq.GetResponseAsync()
    ```

    <span data-ttu-id="2ba80-188">`Await` 运算符将当前方法 `GetURLContents` 的执行挂起，直到完成等待的任务为止。</span><span class="sxs-lookup"><span data-stu-id="2ba80-188">The `Await` operator suspends the execution of the current method, `GetURLContents`, until the awaited task is complete.</span></span> <span data-ttu-id="2ba80-189">同时，控制权返回给当前方法的调用方。</span><span class="sxs-lookup"><span data-stu-id="2ba80-189">In the meantime, control returns to the caller of the current method.</span></span> <span data-ttu-id="2ba80-190">在此示例中，当前方法是 `GetURLContents`，调用方是 `SumPageSizes`。</span><span class="sxs-lookup"><span data-stu-id="2ba80-190">In this example, the current method is `GetURLContents`, and the caller is `SumPageSizes`.</span></span> <span data-ttu-id="2ba80-191">任务完成时，承诺的 `WebResponse` 对象作为等待的任务的值生成，并分配给变量 `response`。</span><span class="sxs-lookup"><span data-stu-id="2ba80-191">When the task is finished, the promised `WebResponse` object is produced as the value of the awaited task and assigned to the variable `response`.</span></span>

    <span data-ttu-id="2ba80-192">上一条语句可以分为以下两条语句，以阐明所发生的情况。</span><span class="sxs-lookup"><span data-stu-id="2ba80-192">The previous statement can be separated into the following two statements to clarify what happens.</span></span>

    ```vb
    Dim responseTask As Task(Of WebResponse) = webReq.GetResponseAsync()
    Using response As WebResponse = Await responseTask
    ```

    <span data-ttu-id="2ba80-193">对 `webReq.GetResponseAsync` 的调用返回 `Task(Of WebResponse)` 或 `Task<WebResponse>`。</span><span class="sxs-lookup"><span data-stu-id="2ba80-193">The call to `webReq.GetResponseAsync` returns a `Task(Of WebResponse)` or `Task<WebResponse>`.</span></span> <span data-ttu-id="2ba80-194">然后，将 `Await` 运算符应用于任务以检索 `WebResponse` 值。</span><span class="sxs-lookup"><span data-stu-id="2ba80-194">Then an `Await` operator is applied to the task to retrieve the `WebResponse` value.</span></span>

    <span data-ttu-id="2ba80-195">如果你的异步方法需要完成不依赖于任务的完成的工作，则在调用异步方法之后及应用 await 运算符之前的这段时间，该方法可以在这两个语句之间继续完成该工作。</span><span class="sxs-lookup"><span data-stu-id="2ba80-195">If your async method has work to do that doesn’t depend on the completion of the task, the method can continue with that work between these two statements, after the call to the async method and before the await operator is applied.</span></span> <span data-ttu-id="2ba80-196">有关示例，请参阅 [如何：使用 Async 和 Await 并行发出多个 Web 请求 (Visual Basic) ](how-to-make-multiple-web-requests-in-parallel-by-using-async-and-await.md) 和 [如何：使用 system.threading.tasks.task.whenall (Visual Basic) 扩展 Async 演练 ](how-to-extend-the-async-walkthrough-by-using-task-whenall.md)。</span><span class="sxs-lookup"><span data-stu-id="2ba80-196">For examples, see [How to: Make Multiple Web Requests in Parallel by Using Async and Await (Visual Basic)](how-to-make-multiple-web-requests-in-parallel-by-using-async-and-await.md) and [How to: Extend the Async Walkthrough by Using Task.WhenAll (Visual Basic)](how-to-extend-the-async-walkthrough-by-using-task-whenall.md).</span></span>

3. <span data-ttu-id="2ba80-197">因为在上一步中添加了 `Await` 运算符，所以会发生编译器错误。</span><span class="sxs-lookup"><span data-stu-id="2ba80-197">Because you added the `Await` operator in the previous step, a compiler error occurs.</span></span> <span data-ttu-id="2ba80-198">运算符只能在使用 [Async](../../../language-reference/modifiers/async.md) 修饰符标记的方法中使用。</span><span class="sxs-lookup"><span data-stu-id="2ba80-198">The operator can be used only in methods that are marked with the [Async](../../../language-reference/modifiers/async.md) modifier.</span></span> <span data-ttu-id="2ba80-199">当你重复转换步骤以使用对 `CopyToAsync` 的调用替换对 `CopyTo` 的调用时，请忽略该错误。</span><span class="sxs-lookup"><span data-stu-id="2ba80-199">Ignore the error while you repeat the conversion steps to replace the call to `CopyTo` with a call to `CopyToAsync`.</span></span>

    - <span data-ttu-id="2ba80-200">更改被调用到 <xref:System.IO.Stream.CopyToAsync%2A> 的方法的名称。</span><span class="sxs-lookup"><span data-stu-id="2ba80-200">Change the name of the method that’s called to <xref:System.IO.Stream.CopyToAsync%2A>.</span></span>

    - <span data-ttu-id="2ba80-201">`CopyTo` 或 `CopyToAsync` 方法复制字节到其参数 `content`，并且不返回有意义的值。</span><span class="sxs-lookup"><span data-stu-id="2ba80-201">The `CopyTo` or `CopyToAsync` method copies bytes to its argument, `content`, and doesn’t return a meaningful value.</span></span> <span data-ttu-id="2ba80-202">在同步版本中，对 `CopyTo` 的调用是不返回值的简单语句。</span><span class="sxs-lookup"><span data-stu-id="2ba80-202">In the synchronous version, the call to `CopyTo` is a simple statement that doesn't return a value.</span></span> <span data-ttu-id="2ba80-203">异步版本 `CopyToAsync` 返回 <xref:System.Threading.Tasks.Task>。</span><span class="sxs-lookup"><span data-stu-id="2ba80-203">The asynchronous version, `CopyToAsync`, returns a <xref:System.Threading.Tasks.Task>.</span></span> <span data-ttu-id="2ba80-204">任务函数类似“Task(void)”，并让该方法能够等待。</span><span class="sxs-lookup"><span data-stu-id="2ba80-204">The task functions like "Task(void)" and enables the method to be awaited.</span></span> <span data-ttu-id="2ba80-205">应用 `Await` 或 `await` 到对 `CopyToAsync` 的调用，如下列代码所示。</span><span class="sxs-lookup"><span data-stu-id="2ba80-205">Apply `Await` or `await` to the call to `CopyToAsync`, as the following code shows.</span></span>

        ```vb
        Await responseStream.CopyToAsync(content)
        ```

         <span data-ttu-id="2ba80-206">上一条语句缩写以下两行代码。</span><span class="sxs-lookup"><span data-stu-id="2ba80-206">The previous statement abbreviates the following two lines of code.</span></span>

        ```vb
        ' CopyToAsync returns a Task, not a Task<T>.
        Dim copyTask As Task = responseStream.CopyToAsync(content)

        ' When copyTask is completed, content contains a copy of
        ' responseStream.
        Await copyTask
        ```

4. <span data-ttu-id="2ba80-207">`GetURLContents` 中仍需要完成的操作是调整方法签名。</span><span class="sxs-lookup"><span data-stu-id="2ba80-207">All that remains to be done in `GetURLContents` is to adjust the method signature.</span></span> <span data-ttu-id="2ba80-208">`Await`只能在使用[Async](../../../language-reference/modifiers/async.md)修饰符标记的方法中使用运算符。</span><span class="sxs-lookup"><span data-stu-id="2ba80-208">You can use the `Await` operator only in methods that are marked with the [Async](../../../language-reference/modifiers/async.md) modifier.</span></span> <span data-ttu-id="2ba80-209">添加修饰符以将方法标记为 *异步方法*，如下列代码所示。</span><span class="sxs-lookup"><span data-stu-id="2ba80-209">Add the modifier to mark the method as an *async method*, as the following code shows.</span></span>

    ```vb
    Private Async Function GetURLContents(url As String) As Byte()
    ```

5. <span data-ttu-id="2ba80-210">异步方法的返回类型只能为 <xref:System.Threading.Tasks.Task> 、 <xref:System.Threading.Tasks.Task%601> 。</span><span class="sxs-lookup"><span data-stu-id="2ba80-210">The return type of an async method can only be <xref:System.Threading.Tasks.Task>, <xref:System.Threading.Tasks.Task%601>.</span></span> <span data-ttu-id="2ba80-211">在 Visual Basic 中，方法必须为返回 `Task` 或 `Task(Of T)` 的 `Function`，或方法必须为 `Sub`。</span><span class="sxs-lookup"><span data-stu-id="2ba80-211">In Visual Basic, the method must be a `Function` that returns a `Task` or a `Task(Of T)`, or the method must be a `Sub`.</span></span> <span data-ttu-id="2ba80-212">通常， `Sub` 方法仅在异步事件处理程序中使用，其中 `Sub` 需要。</span><span class="sxs-lookup"><span data-stu-id="2ba80-212">Typically, a `Sub` method  is used only in an async event handler, where `Sub` is required.</span></span> <span data-ttu-id="2ba80-213">在其他情况下， `Task(T)` 如果完成的方法具有返回 T 类型的值的 [Return](../../../language-reference/statements/return-statement.md) 语句，则使用; `Task` 如果完成的方法不返回有意义的值，则使用。</span><span class="sxs-lookup"><span data-stu-id="2ba80-213">In other cases, you use `Task(T)` if the completed method has a [Return](../../../language-reference/statements/return-statement.md) statement that returns a value of type T, and you use `Task` if the completed method doesn’t return a meaningful value.</span></span>

    <span data-ttu-id="2ba80-214">有关详细信息，请参阅 [异步返回类型 (Visual Basic) ](async-return-types.md)。</span><span class="sxs-lookup"><span data-stu-id="2ba80-214">For more information, see [Async Return Types (Visual Basic)](async-return-types.md).</span></span>

    <span data-ttu-id="2ba80-215">方法 `GetURLContents` 具有 return 语句，且该语句返回字节数组。</span><span class="sxs-lookup"><span data-stu-id="2ba80-215">Method `GetURLContents` has a return statement, and the statement returns a byte array.</span></span> <span data-ttu-id="2ba80-216">因此，异步版本的返回类型为 Task(T)，其中 T 为字节数组。</span><span class="sxs-lookup"><span data-stu-id="2ba80-216">Therefore, the return type of the async version is Task(T), where T is a byte array.</span></span> <span data-ttu-id="2ba80-217">在方法签名中进行下列更改：</span><span class="sxs-lookup"><span data-stu-id="2ba80-217">Make the following changes in the method signature:</span></span>

    - <span data-ttu-id="2ba80-218">将返回类型更改为 `Task(Of Byte())`。</span><span class="sxs-lookup"><span data-stu-id="2ba80-218">Change the return type to `Task(Of Byte())`.</span></span>

    - <span data-ttu-id="2ba80-219">按照约定，异步方法的名称以“Async”结尾，因此，请重命名方法 `GetURLContentsAsync`。</span><span class="sxs-lookup"><span data-stu-id="2ba80-219">By convention, asynchronous methods have names that end in "Async," so rename the method `GetURLContentsAsync`.</span></span>

    <span data-ttu-id="2ba80-220">下列代码显示这些更改。</span><span class="sxs-lookup"><span data-stu-id="2ba80-220">The following code shows these changes.</span></span>

    ```vb
    Private Async Function GetURLContentsAsync(url As String) As Task(Of Byte())
    ```

    <span data-ttu-id="2ba80-221">进行这几处更改后，`GetURLContents` 到异步方法的转换完成。</span><span class="sxs-lookup"><span data-stu-id="2ba80-221">With those few changes, the conversion of `GetURLContents` to an asynchronous method is complete.</span></span>

## <a name="convert-sumpagesizes-to-an-asynchronous-method"></a><span data-ttu-id="2ba80-222">将 SumPageSizes 转换为异步方法</span><span class="sxs-lookup"><span data-stu-id="2ba80-222">Convert SumPageSizes to an asynchronous method</span></span>

1. <span data-ttu-id="2ba80-223">为 `SumPageSizes` 重复之前过程中的步骤。</span><span class="sxs-lookup"><span data-stu-id="2ba80-223">Repeat the steps from the previous procedure for `SumPageSizes`.</span></span> <span data-ttu-id="2ba80-224">首先，将对 `GetURLContents` 的调用更改为异步调用。</span><span class="sxs-lookup"><span data-stu-id="2ba80-224">First, change the call to `GetURLContents` to an asynchronous call.</span></span>

    - <span data-ttu-id="2ba80-225">将调用的方法的名称从 `GetURLContents` 更改为 `GetURLContentsAsync`（如果尚未执行此操作）。</span><span class="sxs-lookup"><span data-stu-id="2ba80-225">Change the name of the method that’s called from `GetURLContents` to `GetURLContentsAsync`, if you haven't already done so.</span></span>

    - <span data-ttu-id="2ba80-226">将 `Await` 应用到 `GetURLContentsAsync` 返回的任务，以便获取字节数组值。</span><span class="sxs-lookup"><span data-stu-id="2ba80-226">Apply `Await` to the task that `GetURLContentsAsync` returns to obtain the byte array value.</span></span>

    <span data-ttu-id="2ba80-227">下列代码显示这些更改。</span><span class="sxs-lookup"><span data-stu-id="2ba80-227">The following code shows these changes.</span></span>

    ```vb
    Dim urlContents As Byte() = Await GetURLContentsAsync(url)
    ```

    <span data-ttu-id="2ba80-228">上一个分配缩写以下两行代码。</span><span class="sxs-lookup"><span data-stu-id="2ba80-228">The previous assignment abbreviates the following two lines of code.</span></span>

    ```vb
    ' GetURLContentsAsync returns a task. At completion, the task
    ' produces a byte array.
    Dim getContentsTask As Task(Of Byte()) = GetURLContentsAsync(url)
    Dim urlContents As Byte() = Await getContentsTask
    ```

2. <span data-ttu-id="2ba80-229">在方法签名中进行下列更改：</span><span class="sxs-lookup"><span data-stu-id="2ba80-229">Make the following changes in the method's signature:</span></span>

    - <span data-ttu-id="2ba80-230">使用 `Async` 修饰符标记方法。</span><span class="sxs-lookup"><span data-stu-id="2ba80-230">Mark the method with the `Async` modifier.</span></span>

    - <span data-ttu-id="2ba80-231">将“Async”添加到方法名称。</span><span class="sxs-lookup"><span data-stu-id="2ba80-231">Add "Async" to the method name.</span></span>

    - <span data-ttu-id="2ba80-232">由于不返回 T 的值，因此这一次没有任务返回变量 T，因为 `SumPageSizesAsync` 不返回 T 的值。 (方法不包含任何 `Return` 语句。 ) 不过，该方法必须返回， `Task` 才能进行可等待。</span><span class="sxs-lookup"><span data-stu-id="2ba80-232">There is no task return variable, T, this time because `SumPageSizesAsync` doesn’t return a value for T. (The method has no `Return` statement.) However, the method must return a `Task` to be awaitable.</span></span> <span data-ttu-id="2ba80-233">因此，将方法类型从更改 `Sub` 为 `Function` 。</span><span class="sxs-lookup"><span data-stu-id="2ba80-233">Therefore, change the method type from `Sub` to `Function`.</span></span> <span data-ttu-id="2ba80-234">函数的返回类型为 `Task`。</span><span class="sxs-lookup"><span data-stu-id="2ba80-234">The return type of the function is `Task`.</span></span>

    <span data-ttu-id="2ba80-235">下列代码显示这些更改。</span><span class="sxs-lookup"><span data-stu-id="2ba80-235">The following code shows these changes.</span></span>

    ```vb
    Private Async Function SumPageSizesAsync() As Task
    ```

    <span data-ttu-id="2ba80-236">从 `SumPageSizes` 到 `SumPageSizesAsync` 的转换完成。</span><span class="sxs-lookup"><span data-stu-id="2ba80-236">The conversion of `SumPageSizes` to `SumPageSizesAsync` is complete.</span></span>

## <a name="convert-startbutton_click-to-an-asynchronous-method"></a><span data-ttu-id="2ba80-237">将 startButton_Click 转换为异步方法</span><span class="sxs-lookup"><span data-stu-id="2ba80-237">Convert startButton_Click to an asynchronous method</span></span>

1. <span data-ttu-id="2ba80-238">在事件处理程序中，将调用的方法的名称从 `SumPageSizes` 更改为 `SumPageSizesAsync`（如果尚未执行此操作）。</span><span class="sxs-lookup"><span data-stu-id="2ba80-238">In the event handler, change the name of the called method from `SumPageSizes` to `SumPageSizesAsync`, if you haven’t already done so.</span></span>

2. <span data-ttu-id="2ba80-239">由于 `SumPageSizesAsync` 是异步方法，请更改事件处理程序中的代码以等待结果。</span><span class="sxs-lookup"><span data-stu-id="2ba80-239">Because `SumPageSizesAsync` is an async method, change the code in the event handler to await the result.</span></span>

    <span data-ttu-id="2ba80-240">对 `SumPageSizesAsync` 的调用反射对 `GetURLContentsAsync` 中的 `CopyToAsync` 的调用。</span><span class="sxs-lookup"><span data-stu-id="2ba80-240">The call to `SumPageSizesAsync` mirrors the call to `CopyToAsync` in `GetURLContentsAsync`.</span></span> <span data-ttu-id="2ba80-241">调用返回的是 `Task`，而不是 `Task(T)`。</span><span class="sxs-lookup"><span data-stu-id="2ba80-241">The call returns a `Task`, not a `Task(T)`.</span></span>

    <span data-ttu-id="2ba80-242">与之前的过程一样，你可以使用一条语句或两条语句转换调用。</span><span class="sxs-lookup"><span data-stu-id="2ba80-242">As in previous procedures, you can convert the call by using one statement or two statements.</span></span> <span data-ttu-id="2ba80-243">下列代码显示这些更改。</span><span class="sxs-lookup"><span data-stu-id="2ba80-243">The following code shows these changes.</span></span>

    ```vb
    ' One-step async call.
    Await SumPageSizesAsync()

    ' Two-step async call.
    Dim sumTask As Task = SumPageSizesAsync()
    Await sumTask
    ```

3. <span data-ttu-id="2ba80-244">要防止意外重新进入操作，请在 `startButton_Click` 顶部添加下列语句，以禁用“启动”按钮。</span><span class="sxs-lookup"><span data-stu-id="2ba80-244">To prevent accidentally reentering the operation, add the following statement at the top of `startButton_Click` to disable the **Start** button.</span></span>

    ```vb
    ' Disable the button until the operation is complete.
    startButton.IsEnabled = False
    ```

    <span data-ttu-id="2ba80-245">可以重新启用事件处理程序末尾的按钮。</span><span class="sxs-lookup"><span data-stu-id="2ba80-245">You can reenable the button at the end of the event handler.</span></span>

    ```vb
    ' Reenable the button in case you want to run the operation again.
    startButton.IsEnabled = True
    ```

    <span data-ttu-id="2ba80-246">有关重新进入的详细信息，请参阅 [处理异步应用中的重新进入 (Visual Basic) ](handling-reentrancy-in-async-apps.md)。</span><span class="sxs-lookup"><span data-stu-id="2ba80-246">For more information about reentrancy, see [Handling Reentrancy in Async Apps (Visual Basic)](handling-reentrancy-in-async-apps.md).</span></span>

4. <span data-ttu-id="2ba80-247">最后，将 `Async` 修饰符添加到声明，以便事件处理程序可以等待 `SumPagSizesAsync`。</span><span class="sxs-lookup"><span data-stu-id="2ba80-247">Finally, add the `Async` modifier to the declaration so that the event handler can await `SumPagSizesAsync`.</span></span>

    ```vb
    Async Sub startButton_Click(sender As Object, e As RoutedEventArgs) Handles startButton.Click
    ```

    <span data-ttu-id="2ba80-248">通常情况下，事件处理程序的名称不会更改。</span><span class="sxs-lookup"><span data-stu-id="2ba80-248">Typically, the names of event handlers aren’t changed.</span></span> <span data-ttu-id="2ba80-249">返回类型没有更改为， `Task` 因为事件处理程序必须是 `Sub` Visual Basic 中的过程。</span><span class="sxs-lookup"><span data-stu-id="2ba80-249">The return type isn’t changed to `Task` because event handlers must be `Sub` procedures in Visual Basic.</span></span>

    <span data-ttu-id="2ba80-250">项目从同步处理到异步处理的转换完成。</span><span class="sxs-lookup"><span data-stu-id="2ba80-250">The conversion of the project from synchronous to asynchronous processing is complete.</span></span>

## <a name="test-the-asynchronous-solution"></a><span data-ttu-id="2ba80-251">测试异步解决方案</span><span class="sxs-lookup"><span data-stu-id="2ba80-251">Test the asynchronous solution</span></span>

1. <span data-ttu-id="2ba80-252">按 F5 键以运行程序，然后选择 **“启动”** 按钮。</span><span class="sxs-lookup"><span data-stu-id="2ba80-252">Choose the F5 key to run the program, and then choose the **Start** button.</span></span>

2. <span data-ttu-id="2ba80-253">此时应显示类似于同步解决方案的输出的输出。</span><span class="sxs-lookup"><span data-stu-id="2ba80-253">Output that resembles the output of the synchronous solution should appear.</span></span> <span data-ttu-id="2ba80-254">但是，请注意下列差异。</span><span class="sxs-lookup"><span data-stu-id="2ba80-254">However, notice the following differences.</span></span>

    - <span data-ttu-id="2ba80-255">处理完成后，所有结果不会同时出现。</span><span class="sxs-lookup"><span data-stu-id="2ba80-255">The results don’t all occur at the same time, after the processing is complete.</span></span> <span data-ttu-id="2ba80-256">例如，两个程序都在 `startButton_Click` 中包含一行可以清除文本框的代码。</span><span class="sxs-lookup"><span data-stu-id="2ba80-256">For example, both programs contain a line in `startButton_Click` that clears the text box.</span></span> <span data-ttu-id="2ba80-257">目的在于，在一组结果显示后，第二次选择“启动”按钮时，可以清除运行之间的文本框。</span><span class="sxs-lookup"><span data-stu-id="2ba80-257">The intent is to clear the text box between runs if you choose the **Start** button for a second time, after one set of results has appeared.</span></span> <span data-ttu-id="2ba80-258">在同步版本中，下载完成且 UI 线程可以自由完成其他工作时，文本框在计数第二次显示之前即被清除。</span><span class="sxs-lookup"><span data-stu-id="2ba80-258">In the synchronous version, the text box is cleared just before the counts appear for the second time, when the downloads are completed and the UI thread is free to do other work.</span></span> <span data-ttu-id="2ba80-259">在异步版本中，选择“启动”按钮后立即清除文本框。</span><span class="sxs-lookup"><span data-stu-id="2ba80-259">In the asynchronous version, the text box clears immediately after you choose the **Start** button.</span></span>

    - <span data-ttu-id="2ba80-260">最重要的是，UI 线程在下载过程中未被阻止。</span><span class="sxs-lookup"><span data-stu-id="2ba80-260">Most importantly, the UI thread isn’t blocked during the downloads.</span></span> <span data-ttu-id="2ba80-261">在 Web 资源下载、计数和显示期间，可以移动窗口或调整窗口大小。</span><span class="sxs-lookup"><span data-stu-id="2ba80-261">You can move or resize the window while the web resources are being downloaded, counted, and displayed.</span></span> <span data-ttu-id="2ba80-262">如果其中一个网站速度缓慢或没有响应，则可以通过选择“关闭”按钮取消操作（右上角红色字段中的 x）。</span><span class="sxs-lookup"><span data-stu-id="2ba80-262">If one of the websites is slow or not responding, you can cancel the operation by choosing the **Close** button (the x in the red field in the upper-right corner).</span></span>

## <a name="replace-the-geturlcontentsasync-method-with-a-net-framework-method"></a><span data-ttu-id="2ba80-263">将 GetURLContentsAsync 方法替换为 .NET Framework 方法</span><span class="sxs-lookup"><span data-stu-id="2ba80-263">Replace the GetURLContentsAsync method with a .NET Framework method</span></span>

1. <span data-ttu-id="2ba80-264">.NET Framework 提供了许多可以使用的异步方法。</span><span class="sxs-lookup"><span data-stu-id="2ba80-264">The .NET Framework provides many async methods that you can use.</span></span> <span data-ttu-id="2ba80-265">其中一种 <xref:System.Net.Http.HttpClient.GetByteArrayAsync%28System.String%29?displayProperty=nameWithType> 方法是方法，它可以执行本演练所需的操作。</span><span class="sxs-lookup"><span data-stu-id="2ba80-265">One of them, the <xref:System.Net.Http.HttpClient.GetByteArrayAsync%28System.String%29?displayProperty=nameWithType> method, does just what you need for this walkthrough.</span></span> <span data-ttu-id="2ba80-266">你可以使用它来替代你在早前过程中创建的 `GetURLContentsAsync` 方法。</span><span class="sxs-lookup"><span data-stu-id="2ba80-266">You can use it instead of the `GetURLContentsAsync` method that you created in an earlier procedure.</span></span>

    <span data-ttu-id="2ba80-267">第一步是 <xref:System.Net.Http.HttpClient> 在方法中创建对象 `SumPageSizesAsync` 。</span><span class="sxs-lookup"><span data-stu-id="2ba80-267">The first step is to create an <xref:System.Net.Http.HttpClient> object in the `SumPageSizesAsync` method.</span></span> <span data-ttu-id="2ba80-268">在方法的开头添加下列声明。</span><span class="sxs-lookup"><span data-stu-id="2ba80-268">Add the following declaration at the start of the method.</span></span>

    ```vb
    ' Declare an HttpClient object and increase the buffer size. The
    ' default buffer size is 65,536.
    Dim client As HttpClient =
        New HttpClient() With {.MaxResponseContentBufferSize = 1000000}
    ```

2. <span data-ttu-id="2ba80-269">在 `SumPageSizesAsync,` 中，使用对 `HttpClient` 方法的调用替换对 `GetURLContentsAsync` 方法的调用。</span><span class="sxs-lookup"><span data-stu-id="2ba80-269">In `SumPageSizesAsync,` replace the call to your `GetURLContentsAsync` method with a call to the `HttpClient` method.</span></span>

    ```vb
    Dim urlContents As Byte() = Await client.GetByteArrayAsync(url)
    ```

3. <span data-ttu-id="2ba80-270">删除或注释禁用你编写的 `GetURLContentsAsync` 方法。</span><span class="sxs-lookup"><span data-stu-id="2ba80-270">Remove or comment out the `GetURLContentsAsync` method that you wrote.</span></span>

4. <span data-ttu-id="2ba80-271">按 F5 键以运行程序，然后选择 **“启动”** 按钮。</span><span class="sxs-lookup"><span data-stu-id="2ba80-271">Choose the F5 key to run the program, and then choose the **Start** button.</span></span>

    <span data-ttu-id="2ba80-272">此版本的项目的行为应与“测试异步解决方案”过程描述的行为匹配，且你的工作量应该更少。</span><span class="sxs-lookup"><span data-stu-id="2ba80-272">The behavior of this version of the project should match the behavior that the "To test the asynchronous solution" procedure describes but with even less effort from you.</span></span>

## <a name="example"></a><span data-ttu-id="2ba80-273">示例</span><span class="sxs-lookup"><span data-stu-id="2ba80-273">Example</span></span>

<span data-ttu-id="2ba80-274">下面是使用异步方法转换后的异步解决方案的完整示例 `GetURLContentsAsync` 。</span><span class="sxs-lookup"><span data-stu-id="2ba80-274">The following is the full example of the converted asynchronous solution that uses the asynchronous `GetURLContentsAsync` method.</span></span> <span data-ttu-id="2ba80-275">请注意，它与原始同步解决方案十分类似。</span><span class="sxs-lookup"><span data-stu-id="2ba80-275">Notice that it strongly resembles the original, synchronous solution.</span></span>

```vb
' Add the following Imports statements, and add a reference for System.Net.Http.
Imports System.Net.Http
Imports System.Net
Imports System.IO

Class MainWindow

    Async Sub startButton_Click(sender As Object, e As RoutedEventArgs) Handles startButton.Click

        ' Disable the button until the operation is complete.
        startButton.IsEnabled = False

        resultsTextBox.Clear()

        '' One-step async call.
        Await SumPageSizesAsync()

        ' Two-step async call.
        'Dim sumTask As Task = SumPageSizesAsync()
        'Await sumTask

        resultsTextBox.Text &= vbCrLf & "Control returned to button1_Click."

        ' Reenable the button in case you want to run the operation again.
        startButton.IsEnabled = True
    End Sub

    Private Async Function SumPageSizesAsync() As Task

        ' Make a list of web addresses.
        Dim urlList As List(Of String) = SetUpURLList()

        Dim total = 0
        For Each url In urlList
            Dim urlContents As Byte() = Await GetURLContentsAsync(url)

            ' The previous line abbreviates the following two assignment statements.

            '//<snippet21>
            ' GetURLContentsAsync returns a task. At completion, the task
            ' produces a byte array.
            'Dim getContentsTask As Task(Of Byte()) = GetURLContentsAsync(url)
            'Dim urlContents As Byte() = Await getContentsTask

            DisplayResults(url, urlContents)

            ' Update the total.
            total += urlContents.Length
        Next

        ' Display the total count for all of the websites.
        resultsTextBox.Text &= String.Format(vbCrLf & vbCrLf &
                                             "Total bytes returned:  {0}" & vbCrLf, total)
    End Function

    Private Function SetUpURLList() As List(Of String)

        Dim urls = New List(Of String) From
            {
                "https://msdn.microsoft.com/library/windows/apps/br211380.aspx",
                "https://msdn.microsoft.com",
                "https://msdn.microsoft.com/library/hh290136.aspx",
                "https://msdn.microsoft.com/library/ee256749.aspx",
                "https://msdn.microsoft.com/library/hh290138.aspx",
                "https://msdn.microsoft.com/library/hh290140.aspx",
                "https://msdn.microsoft.com/library/dd470362.aspx",
                "https://msdn.microsoft.com/library/aa578028.aspx",
                "https://msdn.microsoft.com/library/ms404677.aspx",
                "https://msdn.microsoft.com/library/ff730837.aspx"
            }
        Return urls
    End Function

    Private Async Function GetURLContentsAsync(url As String) As Task(Of Byte())

        ' The downloaded resource ends up in the variable named content.
        Dim content = New MemoryStream()

        ' Initialize an HttpWebRequest for the current URL.
        Dim webReq = CType(WebRequest.Create(url), HttpWebRequest)

        ' Send the request to the Internet resource and wait for
        ' the response.
        Using response As WebResponse = Await webReq.GetResponseAsync()

            ' The previous statement abbreviates the following two statements.

            'Dim responseTask As Task(Of WebResponse) = webReq.GetResponseAsync()
            'Using response As WebResponse = Await responseTask

            ' Get the data stream that is associated with the specified URL.
            Using responseStream As Stream = response.GetResponseStream()
                ' Read the bytes in responseStream and copy them to content.
                Await responseStream.CopyToAsync(content)

                ' The previous statement abbreviates the following two statements.

                ' CopyToAsync returns a Task, not a Task<T>.
                'Dim copyTask As Task = responseStream.CopyToAsync(content)

                ' When copyTask is completed, content contains a copy of
                ' responseStream.
                'Await copyTask
            End Using
        End Using

        ' Return the result as a byte array.
        Return content.ToArray()
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

<span data-ttu-id="2ba80-276">下列代码包含使用 `HttpClient` 方法 `GetByteArrayAsync` 的解决方案的完整示例。</span><span class="sxs-lookup"><span data-stu-id="2ba80-276">The following code contains the full example of the solution that uses the `HttpClient` method, `GetByteArrayAsync`.</span></span>

```vb
' Add the following Imports statements, and add a reference for System.Net.Http.
Imports System.Net.Http
Imports System.Net
Imports System.IO

Class MainWindow

    Async Sub startButton_Click(sender As Object, e As RoutedEventArgs) Handles startButton.Click

        resultsTextBox.Clear()

        ' Disable the button until the operation is complete.
        startButton.IsEnabled = False

        ' One-step async call.
        Await SumPageSizesAsync()

        ' Two-step async call.
        'Dim sumTask As Task = SumPageSizesAsync()
        'Await sumTask

        resultsTextBox.Text &= vbCrLf & "Control returned to button1_Click."

        ' Reenable the button in case you want to run the operation again.
        startButton.IsEnabled = True
    End Sub

    Private Async Function SumPageSizesAsync() As Task

        ' Declare an HttpClient object and increase the buffer size. The
        ' default buffer size is 65,536.
        Dim client As HttpClient =
            New HttpClient() With {.MaxResponseContentBufferSize = 1000000}

        ' Make a list of web addresses.
        Dim urlList As List(Of String) = SetUpURLList()

        Dim total = 0
        For Each url In urlList
            ' GetByteArrayAsync returns a task. At completion, the task
            ' produces a byte array.
            Dim urlContents As Byte() = Await client.GetByteArrayAsync(url)

            ' The following two lines can replace the previous assignment statement.
            'Dim getContentsTask As Task(Of Byte()) = client.GetByteArrayAsync(url)
            'Dim urlContents As Byte() = Await getContentsTask

            DisplayResults(url, urlContents)

            ' Update the total.
            total += urlContents.Length
        Next

        ' Display the total count for all of the websites.
        resultsTextBox.Text &= String.Format(vbCrLf & vbCrLf &
                                             "Total bytes returned:  {0}" & vbCrLf, total)
    End Function

    Private Function SetUpURLList() As List(Of String)

        Dim urls = New List(Of String) From
            {
                "https://msdn.microsoft.com/library/windows/apps/br211380.aspx",
                "https://msdn.microsoft.com",
                "https://msdn.microsoft.com/library/hh290136.aspx",
                "https://msdn.microsoft.com/library/ee256749.aspx",
                "https://msdn.microsoft.com/library/hh290138.aspx",
                "https://msdn.microsoft.com/library/hh290140.aspx",
                "https://msdn.microsoft.com/library/dd470362.aspx",
                "https://msdn.microsoft.com/library/aa578028.aspx",
                "https://msdn.microsoft.com/library/ms404677.aspx",
                "https://msdn.microsoft.com/library/ff730837.aspx"
            }
        Return urls
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

## <a name="see-also"></a><span data-ttu-id="2ba80-277">请参阅</span><span class="sxs-lookup"><span data-stu-id="2ba80-277">See also</span></span>

- [<span data-ttu-id="2ba80-278">异步示例：访问 Web 演练（C# 和 Visual Basic）</span><span class="sxs-lookup"><span data-stu-id="2ba80-278">Async Sample: Accessing the Web Walkthrough (C# and Visual Basic)</span></span>](https://code.msdn.microsoft.com/Async-Sample-Accessing-the-9c10497f)
- [<span data-ttu-id="2ba80-279">Await 运算符</span><span class="sxs-lookup"><span data-stu-id="2ba80-279">Await Operator</span></span>](../../../language-reference/operators/await-operator.md)
- [<span data-ttu-id="2ba80-280">异步</span><span class="sxs-lookup"><span data-stu-id="2ba80-280">Async</span></span>](../../../language-reference/modifiers/async.md)
- [<span data-ttu-id="2ba80-281">使用 Async 和 Await 的异步编程 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="2ba80-281">Asynchronous Programming with Async and Await (Visual Basic)</span></span>](index.md)
- [<span data-ttu-id="2ba80-282">异步返回类型 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="2ba80-282">Async Return Types (Visual Basic)</span></span>](async-return-types.md)
- [<span data-ttu-id="2ba80-283">基于任务的异步编程 (TAP)</span><span class="sxs-lookup"><span data-stu-id="2ba80-283">Task-based Asynchronous Programming (TAP)</span></span>](https://www.microsoft.com/download/details.aspx?id=19957)
- [<span data-ttu-id="2ba80-284">如何：使用 Task.WhenAll 扩展异步演练 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="2ba80-284">How to: Extend the Async Walkthrough by Using Task.WhenAll (Visual Basic)</span></span>](how-to-extend-the-async-walkthrough-by-using-task-whenall.md)
- [<span data-ttu-id="2ba80-285">如何：使用 Async 和 Await 并行发出多个 Web 请求 (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="2ba80-285">How to: Make Multiple Web Requests in Parallel by Using Async and Await (Visual Basic)</span></span>](how-to-make-multiple-web-requests-in-parallel-by-using-async-and-await.md)
