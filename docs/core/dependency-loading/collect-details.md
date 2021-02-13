---
title: 收集详细的程序集加载信息 - .NET Core
description: 介绍了如何在 .NET Core 中收集程序集加载信息
author: elinor-fung
ms.author: elfung
ms.date: 11/17/2020
ms.openlocfilehash: b121982995b440ade6d72190f44f9b9d237c8af6
ms.sourcegitcommit: f2ab02d9a780819ca2e5310bbcf5cfe5b7993041
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2021
ms.locfileid: "99506468"
---
# <a name="collect-detailed-assembly-loading-information"></a><span data-ttu-id="510e4-103">收集详细的程序集加载信息</span><span class="sxs-lookup"><span data-stu-id="510e4-103">Collect detailed assembly loading information</span></span>

<span data-ttu-id="510e4-104">自 .NET 5.0 起，运行时可以通过 `EventPipe` 发出事件，其中包含关于[托管程序集加载](loading-managed.md)的详细信息，以帮助诊断程序集加载问题。</span><span class="sxs-lookup"><span data-stu-id="510e4-104">Starting with .NET 5.0, the runtime can emit events through `EventPipe` with detailed information about [managed assembly loading](loading-managed.md) to aid in diagnosing assembly loading issues.</span></span> <span data-ttu-id="510e4-105">这些[事件](../../fundamentals/diagnostics/runtime-loader-binder-events.md)是由 `Microsoft-Windows-DotNETRuntime` 提供程序在 `AssemblyLoader` 关键字 (`0x4`) 下发出的。</span><span class="sxs-lookup"><span data-stu-id="510e4-105">These [events](../../fundamentals/diagnostics/runtime-loader-binder-events.md) are emitted by the `Microsoft-Windows-DotNETRuntime` provider under the `AssemblyLoader` keyword (`0x4`).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="510e4-106">先决条件</span><span class="sxs-lookup"><span data-stu-id="510e4-106">Prerequisites</span></span>

- <span data-ttu-id="510e4-107">[.NET 5.0 SDK](https://dotnet.microsoft.com/download) 或更高版本</span><span class="sxs-lookup"><span data-stu-id="510e4-107">[.NET 5.0 SDK](https://dotnet.microsoft.com/download) or later versions</span></span>
- <span data-ttu-id="510e4-108">[dotnet-trace](../diagnostics/dotnet-trace.md) 工具。</span><span class="sxs-lookup"><span data-stu-id="510e4-108">[dotnet-trace](../diagnostics/dotnet-trace.md) tool.</span></span>

## <a name="collect-a-trace-with-assembly-loading-events"></a><span data-ttu-id="510e4-109">收集包含程序集加载事件的跟踪</span><span class="sxs-lookup"><span data-stu-id="510e4-109">Collect a trace with assembly loading events</span></span>

<span data-ttu-id="510e4-110">若要在运行时中启用程序集加载事件并收集它们的跟踪，请使用 `dotnet-trace` 和以下命令：</span><span class="sxs-lookup"><span data-stu-id="510e4-110">To enable assembly loading events in the runtime and collect a trace of them, use `dotnet-trace` with the following command:</span></span>

```console
dotnet-trace collect --providers Microsoft-Windows-DotNETRuntime:4 --process-id <pid>
```

<span data-ttu-id="510e4-111">这将收集指定 `<pid>` 的跟踪，从而在 `Microsoft-Windows-DotNETRuntime` 提供程序中启用 `AssemblyLoader` 事件。</span><span class="sxs-lookup"><span data-stu-id="510e4-111">This will collect a trace of the specified `<pid>`, enabling the `AssemblyLoader` events in the `Microsoft-Windows-DotNETRuntime` provider.</span></span> <span data-ttu-id="510e4-112">结果是 `.nettrace` 文件。</span><span class="sxs-lookup"><span data-stu-id="510e4-112">The result is a `.nettrace` file.</span></span>

## <a name="view-a-trace"></a><span data-ttu-id="510e4-113">查看跟踪</span><span class="sxs-lookup"><span data-stu-id="510e4-113">View a trace</span></span>

<span data-ttu-id="510e4-114">可以使用 [PerfView](https://github.com/microsoft/perfview)中的“事件”视图在 Windows 上查看所收集的跟踪文件。</span><span class="sxs-lookup"><span data-stu-id="510e4-114">The collected trace file can be viewed on Windows using the Events view in [PerfView](https://github.com/microsoft/perfview).</span></span> <span data-ttu-id="510e4-115">所有程序集加载事件都将以 `Microsoft-Windows-DotNETRuntime/AssemblyLoader` 为前缀。</span><span class="sxs-lookup"><span data-stu-id="510e4-115">All the assembly loading events will be prefixed with `Microsoft-Windows-DotNETRuntime/AssemblyLoader`.</span></span>

## <a name="example-on-windows"></a><span data-ttu-id="510e4-116">示例（在 Windows 上）</span><span class="sxs-lookup"><span data-stu-id="510e4-116">Example (on Windows)</span></span>

<span data-ttu-id="510e4-117">本例使用[程序集加载扩展点示例](https://github.com/dotnet/samples/tree/master/core/extensions/AssemblyLoading)。</span><span class="sxs-lookup"><span data-stu-id="510e4-117">This example uses the [assembly loading extension points sample](https://github.com/dotnet/samples/tree/master/core/extensions/AssemblyLoading).</span></span> <span data-ttu-id="510e4-118">应用程序尝试加载程序集 `MyLibrary`（应用程序未引用的程序集），因此需要在程序集加载扩展点中进行处理才能成功加载。</span><span class="sxs-lookup"><span data-stu-id="510e4-118">The application attempts to load an assembly `MyLibrary` - an assembly that is not referenced by the application and thus requires handling in an assembly loading extension point to be successfully loaded.</span></span>

### <a name="collect-the-trace"></a><span data-ttu-id="510e4-119">收集跟踪</span><span class="sxs-lookup"><span data-stu-id="510e4-119">Collect the trace</span></span>

01. <span data-ttu-id="510e4-120">导航到包含下载的示例的目录。</span><span class="sxs-lookup"><span data-stu-id="510e4-120">Navigate to the directory with the downloaded sample.</span></span> <span data-ttu-id="510e4-121">通过以下方式生成应用程序：</span><span class="sxs-lookup"><span data-stu-id="510e4-121">Build the application with:</span></span>

    ```console
    dotnet build
    ```

01. <span data-ttu-id="510e4-122">使用指明应用程序应暂停的参数来启动应用程序，并等待按键。</span><span class="sxs-lookup"><span data-stu-id="510e4-122">Launch the application with arguments indicating that it should pause, waiting for a key press.</span></span> <span data-ttu-id="510e4-123">恢复后，它将尝试在默认 `AssemblyLoadContext` 中加载程序集，不需要进行成功加载所需的处理。</span><span class="sxs-lookup"><span data-stu-id="510e4-123">On resuming, it will attempt to load the assembly in the default `AssemblyLoadContext` - without the handling necessary for a successful load.</span></span> <span data-ttu-id="510e4-124">导航到输出目录并运行：</span><span class="sxs-lookup"><span data-stu-id="510e4-124">Navigate to the output directory and run:</span></span>

    ```console
    AssemblyLoading.exe /d default
    ```

01. <span data-ttu-id="510e4-125">找到应用程序的进程 ID。</span><span class="sxs-lookup"><span data-stu-id="510e4-125">Find the application's process ID.</span></span>

    ```console
    dotnet-trace ps
    ```

    <span data-ttu-id="510e4-126">输出将列出可用进程。</span><span class="sxs-lookup"><span data-stu-id="510e4-126">The output will list the available processes.</span></span> <span data-ttu-id="510e4-127">例如： 。</span><span class="sxs-lookup"><span data-stu-id="510e4-127">For example:</span></span>

    ```console
    35832 AssemblyLoading C:\src\AssemblyLoading\bin\Debug\net5.0\AssemblyLoading.exe
    ```

01. <span data-ttu-id="510e4-128">将 `dotnet-trace` 附加到正在运行的应用程序。</span><span class="sxs-lookup"><span data-stu-id="510e4-128">Attach `dotnet-trace` to the running application.</span></span>

    ```console
    dotnet-trace collect --providers Microsoft-Windows-DotNETRuntime:4 --process-id 35832
    ```

01. <span data-ttu-id="510e4-129">在运行应用程序的窗口中，按任意键让程序继续运行。</span><span class="sxs-lookup"><span data-stu-id="510e4-129">In the window running the application, press any key to let the program continue.</span></span> <span data-ttu-id="510e4-130">一旦应用程序退出，跟踪将自动停止。</span><span class="sxs-lookup"><span data-stu-id="510e4-130">Tracing will automatically stop once the application exits.</span></span>

### <a name="view-the-trace"></a><span data-ttu-id="510e4-131">查看跟踪</span><span class="sxs-lookup"><span data-stu-id="510e4-131">View the trace</span></span>

<span data-ttu-id="510e4-132">在 [PerfView](https://github.com/microsoft/perfview) 中打开所收集的跟踪，然后打开“事件”视图。</span><span class="sxs-lookup"><span data-stu-id="510e4-132">Open the collected trace in [PerfView](https://github.com/microsoft/perfview) and open the Events view.</span></span> <span data-ttu-id="510e4-133">将“事件”列表筛选为 `Microsoft-Windows-DotNETRuntime/AssemblyLoader` 事件。</span><span class="sxs-lookup"><span data-stu-id="510e4-133">Filter the events list to `Microsoft-Windows-DotNETRuntime/AssemblyLoader` events.</span></span>

:::image type="content" source="media/collect-details/assembly-loader-filter.png" alt-text="PerfView 程序集加载程序筛选器图像":::

<span data-ttu-id="510e4-135">将显示在跟踪启动后应用程序中发生的所有程序集加载。</span><span class="sxs-lookup"><span data-stu-id="510e4-135">All assembly loads that occurred in the application after tracing started will be shown.</span></span> <span data-ttu-id="510e4-136">若要检查此示例中关注的程序集 (`MyLibrary`) 的加载操作，可以执行更多筛选。</span><span class="sxs-lookup"><span data-stu-id="510e4-136">To inspect the load operation for the assembly of interest for this example - `MyLibrary`, we can do some more filtering.</span></span>

### <a name="assembly-loads"></a><span data-ttu-id="510e4-137">程序集加载</span><span class="sxs-lookup"><span data-stu-id="510e4-137">Assembly loads</span></span>

<span data-ttu-id="510e4-138">使用左侧的“事件”列表，将视图筛选为 `Microsoft-Windows-DotNETRuntime/AssemblyLoader` 下的 [`Start`](../../fundamentals/diagnostics/runtime-loader-binder-events.md#assemblyloadstart-event) 和 [`Stop`](../../fundamentals/diagnostics/runtime-loader-binder-events.md#assemblyloadstop-event) 事件。</span><span class="sxs-lookup"><span data-stu-id="510e4-138">Filter the view to the [`Start`](../../fundamentals/diagnostics/runtime-loader-binder-events.md#assemblyloadstart-event) and [`Stop`](../../fundamentals/diagnostics/runtime-loader-binder-events.md#assemblyloadstop-event) events under `Microsoft-Windows-DotNETRuntime/AssemblyLoader` using the event list on the left.</span></span> <span data-ttu-id="510e4-139">将列 `AssemblyName`、`ActivityID` 和 `Success` 添加到视图中。</span><span class="sxs-lookup"><span data-stu-id="510e4-139">Add the columns `AssemblyName`, `ActivityID`, and `Success` to the view.</span></span> <span data-ttu-id="510e4-140">筛选为包含 `MyLibrary` 的事件。</span><span class="sxs-lookup"><span data-stu-id="510e4-140">Filter to events containing `MyLibrary`.</span></span>

:::image type="content" source="media/collect-details/start-stop.png" alt-text="PerfView Start 和 Stop 事件图像":::

| <span data-ttu-id="510e4-142">事件名称</span><span class="sxs-lookup"><span data-stu-id="510e4-142">Event Name</span></span>             | <span data-ttu-id="510e4-143">AssemblyName</span><span class="sxs-lookup"><span data-stu-id="510e4-143">AssemblyName</span></span>                                      | <span data-ttu-id="510e4-144">ActivityID</span><span class="sxs-lookup"><span data-stu-id="510e4-144">ActivityID</span></span> | <span data-ttu-id="510e4-145">Success</span><span class="sxs-lookup"><span data-stu-id="510e4-145">Success</span></span> |
| ---------------------- | ------------------------------------------------- | ---------- | ------- |
| `AssemblyLoader/Start` | `MyLibrary, Culture=neutral, PublicKeyToken=null` | <span data-ttu-id="510e4-146">//1/2/</span><span class="sxs-lookup"><span data-stu-id="510e4-146">//1/2/</span></span>     |         |
| `AssemblyLoader/Stop`  | `MyLibrary, Culture=neutral, PublicKeyToken=null` | <span data-ttu-id="510e4-147">//1/2/</span><span class="sxs-lookup"><span data-stu-id="510e4-147">//1/2/</span></span>     | <span data-ttu-id="510e4-148">False</span><span class="sxs-lookup"><span data-stu-id="510e4-148">False</span></span>   |

<span data-ttu-id="510e4-149">你应该会在 `Stop` 事件上看到一个带有 `Success=False` 的 `Start`/`Stop` 对，表明加载操作失败。</span><span class="sxs-lookup"><span data-stu-id="510e4-149">You should see one `Start`/`Stop` pair with `Success=False` on the `Stop` event, indicating the load operation failed.</span></span> <span data-ttu-id="510e4-150">请注意，这两个事件有相同的活动 ID。</span><span class="sxs-lookup"><span data-stu-id="510e4-150">Note that the two events have the same activity ID.</span></span> <span data-ttu-id="510e4-151">活动 ID 可用于将其他所有程序集加载程序事件筛选为仅与此加载操作相对应的事件。</span><span class="sxs-lookup"><span data-stu-id="510e4-151">The activity ID can be used to filter all the other assembly loader events to just the ones corresponding to this load operation.</span></span>

### <a name="breakdown-of-attempt-to-load"></a><span data-ttu-id="510e4-152">加载尝试明细</span><span class="sxs-lookup"><span data-stu-id="510e4-152">Breakdown of attempt to load</span></span>

<span data-ttu-id="510e4-153">有关加载操作的更详细明细，请使用左侧的“事件”列表，将视图筛选为 `Microsoft-Windows-DotNETRuntime/AssemblyLoader` 下的 [`ResolutionAttempted` 事件](../../fundamentals/diagnostics/runtime-loader-binder-events.md#resolutionattempted-event)。</span><span class="sxs-lookup"><span data-stu-id="510e4-153">For a more detailed breakdown of the load operation, filter the view to the [`ResolutionAttempted` events](../../fundamentals/diagnostics/runtime-loader-binder-events.md#resolutionattempted-event) under `Microsoft-Windows-DotNETRuntime/AssemblyLoader` using the event list on the left.</span></span> <span data-ttu-id="510e4-154">将列 `AssemblyName`、`Stage` 和 `Result` 添加到视图中。</span><span class="sxs-lookup"><span data-stu-id="510e4-154">Add the columns `AssemblyName`, `Stage`, and `Result` to the view.</span></span> <span data-ttu-id="510e4-155">筛选为包含 `Start`/`Stop` 对中的活动 ID 的事件。</span><span class="sxs-lookup"><span data-stu-id="510e4-155">Filter to events with the activity ID from the `Start`/`Stop` pair.</span></span>

:::image type="content" source="media/collect-details/resolution-attempted.png" alt-text="PerfView ResolutionAttempted 事件图像":::

| <span data-ttu-id="510e4-157">事件名称</span><span class="sxs-lookup"><span data-stu-id="510e4-157">Event Name</span></span>                           | <span data-ttu-id="510e4-158">AssemblyName</span><span class="sxs-lookup"><span data-stu-id="510e4-158">AssemblyName</span></span>                                      | <span data-ttu-id="510e4-159">阶段</span><span class="sxs-lookup"><span data-stu-id="510e4-159">Stage</span></span>                               | <span data-ttu-id="510e4-160">结果</span><span class="sxs-lookup"><span data-stu-id="510e4-160">Result</span></span>             |
| ------------------------------------ | ------------------------------------------------- | ----------------------------------- | ------------------ |
| `AssemblyLoader/ResolutionAttempted` | `MyLibrary, Culture=neutral, PublicKeyToken=null` | `FindInLoadContext`                 | `AssemblyNotFound` |
| `AssemblyLoader/ResolutionAttempted` | `MyLibrary, Culture=neutral, PublicKeyToken=null` | `ApplicationAssemblies`             | `AssemblyNotFound` |
| `AssemblyLoader/ResolutionAttempted` | `MyLibrary, Culture=neutral, PublicKeyToken=null` | `AssemblyLoadContextResolvingEvent` | `AssemblyNotFound` |
| `AssemblyLoader/ResolutionAttempted` | `MyLibrary, Culture=neutral, PublicKeyToken=null` | `AppDomainAssemblyResolveEvent`     | `AssemblyNotFound` |

<span data-ttu-id="510e4-161">上面的事件表明，程序集加载程序试图通过以下方式解析程序集：在当前加载上下文中查找、运行托管应用程序程序集的默认探测逻辑、调用 <xref:System.Runtime.Loader.AssemblyLoadContext.Resolving?displayProperty=nameWithType> 事件的处理程序，以及调用 <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType> 的处理程序。</span><span class="sxs-lookup"><span data-stu-id="510e4-161">The events above indicate that the assembly loader attempted to resolve the assembly by looking in the current load context, running the default probing logic for managed application assemblies, invoking handlers for the <xref:System.Runtime.Loader.AssemblyLoadContext.Resolving?displayProperty=nameWithType> event, and invoking handlers for the <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType>.</span></span> <span data-ttu-id="510e4-162">对于所有这些步骤，都没有找到程序集。</span><span class="sxs-lookup"><span data-stu-id="510e4-162">For all of these steps, the assembly was not found.</span></span>

### <a name="extension-points"></a><span data-ttu-id="510e4-163">扩展点</span><span class="sxs-lookup"><span data-stu-id="510e4-163">Extension points</span></span>

<span data-ttu-id="510e4-164">若要查看调用了哪些扩展点，请使用左侧的“事件”列表，将视图筛选为 `Microsoft-Windows-DotNETRuntime/AssemblyLoader` 下的 [`AssemblyLoadContextResolvingHandlerInvoked`](../../fundamentals/diagnostics/runtime-loader-binder-events.md#assemblyloadcontextresolvinghandlerinvoked-event) 和 [`AppDomainAssemblyResolveHandlerInvoked`](../../fundamentals/diagnostics/runtime-loader-binder-events.md#appdomainassemblyresolvehandlerinvoked-event)。</span><span class="sxs-lookup"><span data-stu-id="510e4-164">To see which extension points were invoked, filter the view to the [`AssemblyLoadContextResolvingHandlerInvoked`](../../fundamentals/diagnostics/runtime-loader-binder-events.md#assemblyloadcontextresolvinghandlerinvoked-event) and [`AppDomainAssemblyResolveHandlerInvoked`](../../fundamentals/diagnostics/runtime-loader-binder-events.md#appdomainassemblyresolvehandlerinvoked-event) under `Microsoft-Windows-DotNETRuntime/AssemblyLoader` using the event list on the left.</span></span> <span data-ttu-id="510e4-165">将列 `AssemblyName` 和 `HandlerName` 添加到视图中。</span><span class="sxs-lookup"><span data-stu-id="510e4-165">Add the columns `AssemblyName` and `HandlerName` to the view.</span></span> <span data-ttu-id="510e4-166">筛选为包含 `Start`/`Stop` 对中的活动 ID 的事件。</span><span class="sxs-lookup"><span data-stu-id="510e4-166">Filter to events with the activity ID from the `Start`/`Stop` pair.</span></span>

:::image type="content" source="media/collect-details/extension-point.png" alt-text="PerfView 扩展点事件图像":::

| <span data-ttu-id="510e4-168">事件名称</span><span class="sxs-lookup"><span data-stu-id="510e4-168">Event Name</span></span>                                                  | <span data-ttu-id="510e4-169">AssemblyName</span><span class="sxs-lookup"><span data-stu-id="510e4-169">AssemblyName</span></span>                                      | <span data-ttu-id="510e4-170">HandlerName</span><span class="sxs-lookup"><span data-stu-id="510e4-170">HandlerName</span></span>                      |
| ----------------------------------------------------------- | ------------------------------------------------- | -------------------------------- |
| `AssemblyLoader/AssemblyLoadContextResolvingHandlerInvoked` | `MyLibrary, Culture=neutral, PublicKeyToken=null` | `OnAssemblyLoadContextResolving` |
| `AssemblyLoader/AppDomainAssemblyResolveHandlerInvoked`     | `MyLibrary, Culture=neutral, PublicKeyToken=null` | `OnAppDomainAssemblyResolve`     |

<span data-ttu-id="510e4-171">上面的事件表明，为 <xref:System.Runtime.Loader.AssemblyLoadContext.Resolving?displayProperty=nameWithType> 事件调用了名为 `OnAssemblyLoadContextResolving` 的处理程序，为 <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType> 事件调用了名为 `OnAppDomainAssemblyResolve` 的处理程序。</span><span class="sxs-lookup"><span data-stu-id="510e4-171">The events above indicate that a handler named `OnAssemblyLoadContextResolving` was invoked for the <xref:System.Runtime.Loader.AssemblyLoadContext.Resolving?displayProperty=nameWithType> event and a handler named `OnAppDomainAssemblyResolve` was invoked for the <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType> event.</span></span>

### <a name="collect-another-trace"></a><span data-ttu-id="510e4-172">收集另一个跟踪</span><span class="sxs-lookup"><span data-stu-id="510e4-172">Collect another trace</span></span>

<span data-ttu-id="510e4-173">使用参数运行应用程序，以便 <xref:System.Runtime.Loader.AssemblyLoadContext.Resolving?displayProperty=nameWithType> 事件的处理程序将加载 `MyLibrary` 程序集。</span><span class="sxs-lookup"><span data-stu-id="510e4-173">Run the application with arguments such that its handler for the <xref:System.Runtime.Loader.AssemblyLoadContext.Resolving?displayProperty=nameWithType> event will load the `MyLibrary` assembly.</span></span>

```console
AssemblyLoading /d default alc-resolving
```

<span data-ttu-id="510e4-174">收集并使用[上面的步骤](#collect-the-trace)打开另一个 `.nettrace` 文件。</span><span class="sxs-lookup"><span data-stu-id="510e4-174">Collect and open another `.nettrace` file using the [steps from above](#collect-the-trace).</span></span>

<span data-ttu-id="510e4-175">再次筛选为 `MyLibrary` 的 `Start` 和 `Stop` 事件。</span><span class="sxs-lookup"><span data-stu-id="510e4-175">Filter to the `Start` and `Stop` events for `MyLibrary` again.</span></span> <span data-ttu-id="510e4-176">你应该会看到 `Start`/`Stop` 对，以及另一个 `Start`/`Stop` 介于二者之间。</span><span class="sxs-lookup"><span data-stu-id="510e4-176">You should see a `Start`/`Stop` pair with another `Start`/`Stop` between them.</span></span> <span data-ttu-id="510e4-177">内部加载操作表示 <xref:System.Runtime.Loader.AssemblyLoadContext.Resolving?displayProperty=nameWithType> 的处理程序在调用 <xref:System.Runtime.Loader.AssemblyLoadContext.LoadFromAssemblyPath%2A?displayProperty=nameWithType> 时触发的加载。</span><span class="sxs-lookup"><span data-stu-id="510e4-177">The inner load operation represents the load triggered by the handler for <xref:System.Runtime.Loader.AssemblyLoadContext.Resolving?displayProperty=nameWithType> when it called <xref:System.Runtime.Loader.AssemblyLoadContext.LoadFromAssemblyPath%2A?displayProperty=nameWithType>.</span></span> <span data-ttu-id="510e4-178">这一次，你应该会在 `Stop` 事件上看到 `Success=True`，表明加载操作成功。</span><span class="sxs-lookup"><span data-stu-id="510e4-178">This time, you should see `Success=True` on the `Stop` event, indicating the load operation succeeded.</span></span> <span data-ttu-id="510e4-179">`ResultAssemblyPath` 字段显示生成的程序集的路径。</span><span class="sxs-lookup"><span data-stu-id="510e4-179">The `ResultAssemblyPath` field shows the path of the resulting assembly.</span></span>

:::image type="content" source="media/collect-details/start-stop-success.png" alt-text="PerfView 成功 Start 和 Stop 事件图像":::

| <span data-ttu-id="510e4-181">事件名称</span><span class="sxs-lookup"><span data-stu-id="510e4-181">Event Name</span></span>             | <span data-ttu-id="510e4-182">AssemblyName</span><span class="sxs-lookup"><span data-stu-id="510e4-182">AssemblyName</span></span>                                                       | <span data-ttu-id="510e4-183">ActivityID</span><span class="sxs-lookup"><span data-stu-id="510e4-183">ActivityID</span></span> | <span data-ttu-id="510e4-184">Success</span><span class="sxs-lookup"><span data-stu-id="510e4-184">Success</span></span> | <span data-ttu-id="510e4-185">ResultAssemblyPath</span><span class="sxs-lookup"><span data-stu-id="510e4-185">ResultAssemblyPath</span></span>                                      |
| ---------------------- | ------------------------------------------------------------------ |------------|---------| ------------------------------------------------------- |
| `AssemblyLoader/Start` |                  `MyLibrary, Culture=neutral, PublicKeyToken=null` | <span data-ttu-id="510e4-186">//1/2/</span><span class="sxs-lookup"><span data-stu-id="510e4-186">//1/2/</span></span>     |         |                                                         |
| `AssemblyLoader/Start` | `MyLibrary, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null` | <span data-ttu-id="510e4-187">//1/2/1/</span><span class="sxs-lookup"><span data-stu-id="510e4-187">//1/2/1/</span></span>   |         |                                                         |
| `AssemblyLoader/Stop`  | `MyLibrary, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null` | <span data-ttu-id="510e4-188">//1/2/1/</span><span class="sxs-lookup"><span data-stu-id="510e4-188">//1/2/1/</span></span>   | <span data-ttu-id="510e4-189">True</span><span class="sxs-lookup"><span data-stu-id="510e4-189">True</span></span>    | <span data-ttu-id="510e4-190">C:\src\AssemblyLoading\bin\Debug\net5.0\MyLibrary.dll</span><span class="sxs-lookup"><span data-stu-id="510e4-190">*C:\src\AssemblyLoading\bin\Debug\net5.0\MyLibrary.dll*</span></span> |
| `AssemblyLoader/Stop`  |                  `MyLibrary, Culture=neutral, PublicKeyToken=null` | <span data-ttu-id="510e4-191">//1/2/</span><span class="sxs-lookup"><span data-stu-id="510e4-191">//1/2/</span></span>     | <span data-ttu-id="510e4-192">True</span><span class="sxs-lookup"><span data-stu-id="510e4-192">True</span></span>    | <span data-ttu-id="510e4-193">C:\src\AssemblyLoading\bin\Debug\net5.0\MyLibrary.dll</span><span class="sxs-lookup"><span data-stu-id="510e4-193">*C:\src\AssemblyLoading\bin\Debug\net5.0\MyLibrary.dll*</span></span> |

<span data-ttu-id="510e4-194">然后，我们可以查看带有外部负载的活动 ID 的 `ResolutionAttempted` 事件，以确定成功解析程序集的步骤。</span><span class="sxs-lookup"><span data-stu-id="510e4-194">We can then look at the `ResolutionAttempted` events with the activity ID from the outer load to determine the step at which the assembly was successfully resolved.</span></span> <span data-ttu-id="510e4-195">这一次，事件会显示 `AssemblyLoadContextResolvingEvent` 阶段已成功完成。</span><span class="sxs-lookup"><span data-stu-id="510e4-195">This time, the events will show that the `AssemblyLoadContextResolvingEvent` stage was successful.</span></span> <span data-ttu-id="510e4-196">`ResultAssemblyPath` 字段显示生成的程序集的路径。</span><span class="sxs-lookup"><span data-stu-id="510e4-196">The `ResultAssemblyPath` field shows the path of the resulting assembly.</span></span>

:::image type="content" source="media/collect-details/resolution-attempted-success.png" alt-text="PerfView 成功 ResolutionAttempted 事件图像":::

| <span data-ttu-id="510e4-198">事件名称</span><span class="sxs-lookup"><span data-stu-id="510e4-198">Event Name</span></span>                           | <span data-ttu-id="510e4-199">AssemblyName</span><span class="sxs-lookup"><span data-stu-id="510e4-199">AssemblyName</span></span>                                      | <span data-ttu-id="510e4-200">阶段</span><span class="sxs-lookup"><span data-stu-id="510e4-200">Stage</span></span>                               | <span data-ttu-id="510e4-201">结果</span><span class="sxs-lookup"><span data-stu-id="510e4-201">Result</span></span>             | <span data-ttu-id="510e4-202">ResultAssemblyPath</span><span class="sxs-lookup"><span data-stu-id="510e4-202">ResultAssemblyPath</span></span> |
| ------------------------------------ | ------------------------------------------------- | ----------------------------------- | ------------------ | ------------------ |
| `AssemblyLoader/ResolutionAttempted` | `MyLibrary, Culture=neutral, PublicKeyToken=null` | `FindInLoadContext`                 | `AssemblyNotFound` |                    |
| `AssemblyLoader/ResolutionAttempted` | `MyLibrary, Culture=neutral, PublicKeyToken=null` | `ApplicationAssemblies`             | `AssemblyNotFound` |                    |
| `AssemblyLoader/ResolutionAttempted` | `MyLibrary, Culture=neutral, PublicKeyToken=null` | `AssemblyLoadContextResolvingEvent` | `Success`          | <span data-ttu-id="510e4-203">C:\src\AssemblyLoading\bin\Debug\net5.0\MyLibrary.dll</span><span class="sxs-lookup"><span data-stu-id="510e4-203">*C:\src\AssemblyLoading\bin\Debug\net5.0\MyLibrary.dll*</span></span> |

<span data-ttu-id="510e4-204">查看 `AssemblyLoadContextResolvingHandlerInvoked` 事件将看到调用了名为 `OnAssemblyLoadContextResolving` 的处理程序。</span><span class="sxs-lookup"><span data-stu-id="510e4-204">Looking at `AssemblyLoadContextResolvingHandlerInvoked` events will show that the handler named `OnAssemblyLoadContextResolving` was invoked.</span></span> <span data-ttu-id="510e4-205">`ResultAssemblyPath` 字段显示由处理程序返回的程序集的路径。</span><span class="sxs-lookup"><span data-stu-id="510e4-205">The `ResultAssemblyPath` field shows the path of the assembly returned by the handler.</span></span>

:::image type="content" source="media/collect-details/extension-point-success.png" alt-text="PerfView 成功扩展点事件图像":::

| <span data-ttu-id="510e4-207">事件名称</span><span class="sxs-lookup"><span data-stu-id="510e4-207">Event Name</span></span>                                                  | <span data-ttu-id="510e4-208">AssemblyName</span><span class="sxs-lookup"><span data-stu-id="510e4-208">AssemblyName</span></span>                                      | <span data-ttu-id="510e4-209">HandlerName</span><span class="sxs-lookup"><span data-stu-id="510e4-209">HandlerName</span></span>                      | <span data-ttu-id="510e4-210">ResultAssemblyPath</span><span class="sxs-lookup"><span data-stu-id="510e4-210">ResultAssemblyPath</span></span> |
| ----------------------------------------------------------- | ------------------------------------------------- | -------------------------------- | ------------------ |
| `AssemblyLoader/AssemblyLoadContextResolvingHandlerInvoked` | `MyLibrary, Culture=neutral, PublicKeyToken=null` | `OnAssemblyLoadContextResolving` | <span data-ttu-id="510e4-211">C:\src\AssemblyLoading\bin\Debug\net5.0\MyLibrary.dll</span><span class="sxs-lookup"><span data-stu-id="510e4-211">*C:\src\AssemblyLoading\bin\Debug\net5.0\MyLibrary.dll*</span></span> |

<span data-ttu-id="510e4-212">请注意，不再存在带有 `AppDomainAssemblyResolveEvent` 阶段的 `ResolutionAttempted` 事件或任何 `AppDomainAssemblyResolveHandlerInvoked` 事件，因为程序集在到达引发 <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType> 事件的加载算法步骤之前已成功加载。</span><span class="sxs-lookup"><span data-stu-id="510e4-212">Note that there is no longer a `ResolutionAttempted` event with the `AppDomainAssemblyResolveEvent` stage or any `AppDomainAssemblyResolveHandlerInvoked` events, as the assembly was successfully loaded before reaching the step of the loading algorithm that raises the <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType> event.</span></span>

## <a name="see-also"></a><span data-ttu-id="510e4-213">另请参阅</span><span class="sxs-lookup"><span data-stu-id="510e4-213">See also</span></span>

- [<span data-ttu-id="510e4-214">程序集加载程序事件</span><span class="sxs-lookup"><span data-stu-id="510e4-214">Assembly loader events</span></span>](../../fundamentals/diagnostics/runtime-loader-binder-events.md)
- [<span data-ttu-id="510e4-215">dotnet-trace</span><span class="sxs-lookup"><span data-stu-id="510e4-215">dotnet-trace</span></span>](../diagnostics/dotnet-trace.md)
- [<span data-ttu-id="510e4-216">PerfView</span><span class="sxs-lookup"><span data-stu-id="510e4-216">PerfView</span></span>](https://github.com/microsoft/perfview)
