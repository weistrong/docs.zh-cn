---
title: 在一段时间后取消异步任务 (C#)
description: 了解如何计划取消未在一段时间内完成的任何关联任务。
ms.date: 02/03/2021
ms.topic: tutorial
ms.assetid: 194282c2-399f-46da-a7a6-96674e00b0b3
ms.openlocfilehash: 98c42a2df6153d668b99b6dec49ffe380293b205
ms.sourcegitcommit: 65af0f0ad316858882845391d60ef7e303b756e8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "99585372"
---
# <a name="cancel-async-tasks-after-a-period-of-time-c"></a><span data-ttu-id="c3cc6-103">在一段时间后取消异步任务 (C#)</span><span class="sxs-lookup"><span data-stu-id="c3cc6-103">Cancel async tasks after a period of time (C#)</span></span>

<span data-ttu-id="c3cc6-104">如果不希望等待操作结束，可使用 <xref:System.Threading.CancellationTokenSource.CancelAfter%2A?displayProperty=nameWithType> 方法在一段时间后取消异步操作。</span><span class="sxs-lookup"><span data-stu-id="c3cc6-104">You can cancel an asynchronous operation after a period of time by using the <xref:System.Threading.CancellationTokenSource.CancelAfter%2A?displayProperty=nameWithType> method if you don't want to wait for the operation to finish.</span></span> <span data-ttu-id="c3cc6-105">此方法会计划取消未在 `CancelAfter` 表达式指定的时间段内完成的任何关联任务。</span><span class="sxs-lookup"><span data-stu-id="c3cc6-105">This method schedules the cancellation of any associated tasks that aren't complete within the period of time that's designated by the `CancelAfter` expression.</span></span>

<span data-ttu-id="c3cc6-106">此示例添加到[取消任务列表 (C#)](cancel-an-async-task-or-a-list-of-tasks.md) 中开发的代码，以下载网站列表并显示每个网站的内容长度。</span><span class="sxs-lookup"><span data-stu-id="c3cc6-106">This example adds to the code that's developed in [Cancel a list of tasks (C#)](cancel-an-async-task-or-a-list-of-tasks.md) to download a list of websites and to display the length of the contents of each one.</span></span>

<span data-ttu-id="c3cc6-107">本教程涉及：</span><span class="sxs-lookup"><span data-stu-id="c3cc6-107">This tutorial covers:</span></span>

> [!div class="checklist"]
>
> - <span data-ttu-id="c3cc6-108">更新现有的 .NET 控制台应用程序</span><span class="sxs-lookup"><span data-stu-id="c3cc6-108">Updating an existing .NET console application</span></span>
> - <span data-ttu-id="c3cc6-109">计划取消</span><span class="sxs-lookup"><span data-stu-id="c3cc6-109">Scheduling a cancellation</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c3cc6-110">必备条件</span><span class="sxs-lookup"><span data-stu-id="c3cc6-110">Prerequisites</span></span>

<span data-ttu-id="c3cc6-111">本教程需要的内容如下：</span><span class="sxs-lookup"><span data-stu-id="c3cc6-111">This tutorial requires the following:</span></span>

- <span data-ttu-id="c3cc6-112">在[取消任务列表 (C#)](cancel-an-async-task-or-a-list-of-tasks.md) 教程中已创建应用程序</span><span class="sxs-lookup"><span data-stu-id="c3cc6-112">You're expected to have created an application in the [Cancel a list of tasks (C#)](cancel-an-async-task-or-a-list-of-tasks.md) tutorial</span></span>
- [<span data-ttu-id="c3cc6-113">.NET 5.0 或更高版本的 SDK</span><span class="sxs-lookup"><span data-stu-id="c3cc6-113">.NET 5.0 or later SDK</span></span>](https://dotnet.microsoft.com/download/dotnet/5.0)
- <span data-ttu-id="c3cc6-114">集成开发环境 (IDE)</span><span class="sxs-lookup"><span data-stu-id="c3cc6-114">Integrated development environment (IDE)</span></span>
  - [<span data-ttu-id="c3cc6-115">建议使用 Visual Studio、Visual Studio Code 或 Visual Studio for Mac</span><span class="sxs-lookup"><span data-stu-id="c3cc6-115">We recommend Visual Studio, Visual Studio Code, or Visual Studio for Mac</span></span>](https://visualstudio.microsoft.com)

## <a name="update-application-entry-point"></a><span data-ttu-id="c3cc6-116">更新应用程序入口点</span><span class="sxs-lookup"><span data-stu-id="c3cc6-116">Update application entry point</span></span>

<span data-ttu-id="c3cc6-117">将现有的 `Main` 方法替换为以下内容：</span><span class="sxs-lookup"><span data-stu-id="c3cc6-117">Replace the existing `Main` method with the following:</span></span>

```csharp
static async Task Main()
{
    Console.WriteLine("Application started.");

    try
    {
        s_cts.CancelAfter(3500);

        await SumPageSizesAsync();
    }
    catch (TaskCanceledException)
    {
        Console.WriteLine("\nTasks cancelled: timed out.\n");
    }
    finally
    {
        s_cts.Dispose();
    }

    Console.WriteLine("Application ending.");
}
```

<span data-ttu-id="c3cc6-118">更新后的 `Main` 方法将一些说明性消息写入控制台。</span><span class="sxs-lookup"><span data-stu-id="c3cc6-118">The updated `Main` method writes a few instructional messages to the console.</span></span> <span data-ttu-id="c3cc6-119">在 [try catch](../../../language-reference/keywords/try-catch.md) 内，对 <xref:System.Threading.CancellationTokenSource.CancelAfter(System.Int32)?displayProperty=nameWithType> 调用安排取消。</span><span class="sxs-lookup"><span data-stu-id="c3cc6-119">Within the [try catch](../../../language-reference/keywords/try-catch.md), a call to <xref:System.Threading.CancellationTokenSource.CancelAfter(System.Int32)?displayProperty=nameWithType> schedules a cancellation.</span></span> <span data-ttu-id="c3cc6-120">一段时间后将发出取消信号。</span><span class="sxs-lookup"><span data-stu-id="c3cc6-120">This will signal cancellation after a period of time.</span></span>

<span data-ttu-id="c3cc6-121">接下来，等待 `SumPageSizesAsync` 方法。</span><span class="sxs-lookup"><span data-stu-id="c3cc6-121">Next, the `SumPageSizesAsync` method is awaited.</span></span> <span data-ttu-id="c3cc6-122">如果处理所有 URL 的速度比计划取消的速度快，应用程序将结束。</span><span class="sxs-lookup"><span data-stu-id="c3cc6-122">If processing all of the URLs occurs faster than the scheduled cancellation, the application ends.</span></span> <span data-ttu-id="c3cc6-123">但如果在处理所有 URL 之前触发了计划取消，则会引发 <xref:System.Threading.Tasks.TaskCanceledException>。</span><span class="sxs-lookup"><span data-stu-id="c3cc6-123">However, if the scheduled cancellation is triggered before all of the URLs are processed, a <xref:System.Threading.Tasks.TaskCanceledException> is thrown.</span></span>

### <a name="example-application-output"></a><span data-ttu-id="c3cc6-124">示例应用程序输出</span><span class="sxs-lookup"><span data-stu-id="c3cc6-124">Example application output</span></span>

```console
Application started.

https://docs.microsoft.com                                       37,357
https://docs.microsoft.com/aspnet/core                           85,589
https://docs.microsoft.com/azure                                398,939
https://docs.microsoft.com/azure/devops                          73,663

Tasks cancelled: timed out.

Application ending.
```

## <a name="complete-example"></a><span data-ttu-id="c3cc6-125">完整示例</span><span class="sxs-lookup"><span data-stu-id="c3cc6-125">Complete example</span></span>

<span data-ttu-id="c3cc6-126">下列代码是示例的 Program.cs 文件的完整文本。</span><span class="sxs-lookup"><span data-stu-id="c3cc6-126">The following code is the complete text of the *Program.cs* file for the example.</span></span>

:::code language="csharp" source="snippets/cancel-tasks/cancel-task-after-period-of-time/Program.cs":::

## <a name="see-also"></a><span data-ttu-id="c3cc6-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c3cc6-127">See also</span></span>

- <xref:System.Threading.CancellationToken>
- <xref:System.Threading.CancellationTokenSource>
- [<span data-ttu-id="c3cc6-128">使用 Async 和 Await 的异步编程 (C#)</span><span class="sxs-lookup"><span data-stu-id="c3cc6-128">Asynchronous programming with async and await (C#)</span></span>](index.md)
- [<span data-ttu-id="c3cc6-129">取消任务列表 (C#)</span><span class="sxs-lookup"><span data-stu-id="c3cc6-129">Cancel a list of tasks (C#)</span></span>](cancel-an-async-task-or-a-list-of-tasks.md)
