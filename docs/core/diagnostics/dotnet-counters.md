---
title: dotnet-counters 诊断工具 - .NET CLI
description: 了解如何安装和使用 dotnet-counter CLI 工具进行临时运行状况监视和初级性能调查。
ms.date: 11/17/2020
ms.openlocfilehash: 89695c77e7913d41f030890be7cc00947e42fa3a
ms.sourcegitcommit: e395fabeeea5c705d243d246fa64446839ac85b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/03/2021
ms.locfileid: "97856050"
---
# <a name="investigate-performance-counters-dotnet-counters"></a><span data-ttu-id="ee070-103">调查性能计数器 (dotnet-counters)</span><span class="sxs-lookup"><span data-stu-id="ee070-103">Investigate performance counters (dotnet-counters)</span></span>

<span data-ttu-id="ee070-104"> 本文适用于： ✔️ .NET Core 3.0 SDK 及更高版本</span><span class="sxs-lookup"><span data-stu-id="ee070-104">**This article applies to:** ✔️ .NET Core 3.0 SDK and later versions</span></span>

## <a name="install"></a><span data-ttu-id="ee070-105">安装</span><span class="sxs-lookup"><span data-stu-id="ee070-105">Install</span></span>

<span data-ttu-id="ee070-106">可采用两种方法来下载和安装 `dotnet-counters`：</span><span class="sxs-lookup"><span data-stu-id="ee070-106">There are two ways to download and install `dotnet-counters`:</span></span>

- <span data-ttu-id="ee070-107">**dotnet 全局工具：**</span><span class="sxs-lookup"><span data-stu-id="ee070-107">**dotnet global tool:**</span></span>

  <span data-ttu-id="ee070-108">若要安装最新版 `dotnet-counters` [NuGet 包](https://www.nuget.org/packages/dotnet-counters)，请使用 [dotnet tool install](../tools/dotnet-tool-install.md) 命令：</span><span class="sxs-lookup"><span data-stu-id="ee070-108">To install the latest release version of the `dotnet-counters` [NuGet package](https://www.nuget.org/packages/dotnet-counters), use the [dotnet tool install](../tools/dotnet-tool-install.md) command:</span></span>

  ```dotnetcli
  dotnet tool install --global dotnet-counters
  ```

- <span data-ttu-id="ee070-109">**直接下载：**</span><span class="sxs-lookup"><span data-stu-id="ee070-109">**Direct download:**</span></span>

  <span data-ttu-id="ee070-110">下载与平台相匹配的工具可执行文件：</span><span class="sxs-lookup"><span data-stu-id="ee070-110">Download the tool executable that matches your platform:</span></span>

  | <span data-ttu-id="ee070-111">(OS)</span><span class="sxs-lookup"><span data-stu-id="ee070-111">OS</span></span>  | <span data-ttu-id="ee070-112">平台</span><span class="sxs-lookup"><span data-stu-id="ee070-112">Platform</span></span> |
  | --- | -------- |
  | <span data-ttu-id="ee070-113">Windows</span><span class="sxs-lookup"><span data-stu-id="ee070-113">Windows</span></span> | <span data-ttu-id="ee070-114">[x86](https://aka.ms/dotnet-counters/win-x86) \| [x64](https://aka.ms/dotnet-counters/win-x64) \| [arm](https://aka.ms/dotnet-counters/win-arm) \| [arm-x64](https://aka.ms/dotnet-counters/win-arm64)</span><span class="sxs-lookup"><span data-stu-id="ee070-114">[x86](https://aka.ms/dotnet-counters/win-x86) \| [x64](https://aka.ms/dotnet-counters/win-x64) \| [arm](https://aka.ms/dotnet-counters/win-arm) \| [arm-x64](https://aka.ms/dotnet-counters/win-arm64)</span></span> |
  | <span data-ttu-id="ee070-115">macOS</span><span class="sxs-lookup"><span data-stu-id="ee070-115">macOS</span></span>   | [<span data-ttu-id="ee070-116">x64</span><span class="sxs-lookup"><span data-stu-id="ee070-116">x64</span></span>](https://aka.ms/dotnet-counters/osx-x64) |
  | <span data-ttu-id="ee070-117">Linux</span><span class="sxs-lookup"><span data-stu-id="ee070-117">Linux</span></span>   | <span data-ttu-id="ee070-118">[x64](https://aka.ms/dotnet-counters/linux-x64) \| [arm](https://aka.ms/dotnet-counters/linux-arm) \| [arm64](https://aka.ms/dotnet-counters/linux-arm64) \| [musl-x64](https://aka.ms/dotnet-counters/linux-musl-x64) \| [musl-arm64](https://aka.ms/dotnet-counters/linux-musl-arm64)</span><span class="sxs-lookup"><span data-stu-id="ee070-118">[x64](https://aka.ms/dotnet-counters/linux-x64) \| [arm](https://aka.ms/dotnet-counters/linux-arm) \| [arm64](https://aka.ms/dotnet-counters/linux-arm64) \| [musl-x64](https://aka.ms/dotnet-counters/linux-musl-x64) \| [musl-arm64](https://aka.ms/dotnet-counters/linux-musl-arm64)</span></span> |

## <a name="synopsis"></a><span data-ttu-id="ee070-119">摘要</span><span class="sxs-lookup"><span data-stu-id="ee070-119">Synopsis</span></span>

```console
dotnet-counters [-h|--help] [--version] <command>
```

## <a name="description"></a><span data-ttu-id="ee070-120">描述</span><span class="sxs-lookup"><span data-stu-id="ee070-120">Description</span></span>

<span data-ttu-id="ee070-121">`dotnet-counters` 是一个性能监视工具，用于临时运行状况监视和初级性能调查。</span><span class="sxs-lookup"><span data-stu-id="ee070-121">`dotnet-counters` is a performance monitoring tool for ad-hoc health monitoring and first-level performance investigation.</span></span> <span data-ttu-id="ee070-122">它可以观察通过 <xref:System.Diagnostics.Tracing.EventCounter> API 发布的性能计数器值。</span><span class="sxs-lookup"><span data-stu-id="ee070-122">It can observe performance counter values that are published via the <xref:System.Diagnostics.Tracing.EventCounter> API.</span></span> <span data-ttu-id="ee070-123">例如，可以快速监视 CPU 使用情况或 .NET Core 应用程序中引发的异常率，以了解在使用 `PerfView` 或 `dotnet-trace` 深入调查更严重的性能问题之前是否有任何可疑操作。</span><span class="sxs-lookup"><span data-stu-id="ee070-123">For example, you can quickly monitor things like the CPU usage or the rate of exceptions being thrown in your .NET Core application to see if there's anything suspicious before diving into more serious performance investigation using `PerfView` or `dotnet-trace`.</span></span>

## <a name="options"></a><span data-ttu-id="ee070-124">选项</span><span class="sxs-lookup"><span data-stu-id="ee070-124">Options</span></span>

- **`--version`**

  <span data-ttu-id="ee070-125">显示 dotnet-counters 实用工具的版本。</span><span class="sxs-lookup"><span data-stu-id="ee070-125">Displays the version of the dotnet-counters utility.</span></span>

- **`-h|--help`**

  <span data-ttu-id="ee070-126">显示命令行帮助。</span><span class="sxs-lookup"><span data-stu-id="ee070-126">Shows command-line help.</span></span>

## <a name="commands"></a><span data-ttu-id="ee070-127">命令</span><span class="sxs-lookup"><span data-stu-id="ee070-127">Commands</span></span>

| <span data-ttu-id="ee070-128">命令</span><span class="sxs-lookup"><span data-stu-id="ee070-128">Command</span></span>                                             |
|-----------------------------------------------------|
| [<span data-ttu-id="ee070-129">dotnet-counters collect</span><span class="sxs-lookup"><span data-stu-id="ee070-129">dotnet-counters collect</span></span>](#dotnet-counters-collect) |
| [<span data-ttu-id="ee070-130">dotnet-counters list</span><span class="sxs-lookup"><span data-stu-id="ee070-130">dotnet-counters list</span></span>](#dotnet-counters-list)       |
| [<span data-ttu-id="ee070-131">dotnet-counters monitor</span><span class="sxs-lookup"><span data-stu-id="ee070-131">dotnet-counters monitor</span></span>](#dotnet-counters-monitor) |
| [<span data-ttu-id="ee070-132">dotnet-counters ps</span><span class="sxs-lookup"><span data-stu-id="ee070-132">dotnet-counters ps</span></span>](#dotnet-counters-ps)           |

## <a name="dotnet-counters-collect"></a><span data-ttu-id="ee070-133">dotnet-counters collect</span><span class="sxs-lookup"><span data-stu-id="ee070-133">dotnet-counters collect</span></span>

<span data-ttu-id="ee070-134">定期收集所选计数器的值，并将它们导出为指定的文件格式以进行后续处理。</span><span class="sxs-lookup"><span data-stu-id="ee070-134">Periodically collect selected counter values and export them into a specified file format for post-processing.</span></span>

### <a name="synopsis"></a><span data-ttu-id="ee070-135">摘要</span><span class="sxs-lookup"><span data-stu-id="ee070-135">Synopsis</span></span>

```console
dotnet-counters collect [-h|--help] [-p|--process-id] [-n|--name] [--diagnostic-port] [--refresh-interval] [--counters <COUNTERS>] [--format] [-o|--output] [-- <command>]
```

### <a name="options"></a><span data-ttu-id="ee070-136">选项</span><span class="sxs-lookup"><span data-stu-id="ee070-136">Options</span></span>

- **`-p|--process-id <PID>`**

  <span data-ttu-id="ee070-137">要从中收集计数器数据的进程的 ID。</span><span class="sxs-lookup"><span data-stu-id="ee070-137">The ID of the process to be collect counter data from.</span></span>

- **`-n|--name <name>`**

  <span data-ttu-id="ee070-138">要从中收集计数器数据的进程的名称。</span><span class="sxs-lookup"><span data-stu-id="ee070-138">The name of the process to be collect counter data from.</span></span>

- **`--diagnostic-port`**

  <span data-ttu-id="ee070-139">要创建的诊断端口的名称。</span><span class="sxs-lookup"><span data-stu-id="ee070-139">The name of the diagnostic port to create.</span></span> <span data-ttu-id="ee070-140">请参阅[使用诊断端口](#using-diagnostic-port)，了解如何使用此选项从应用启动时开始监视计数器。</span><span class="sxs-lookup"><span data-stu-id="ee070-140">See [using diagnostic port](#using-diagnostic-port) for how to use this option to start monitoring counters from app startup.</span></span>

- **`--refresh-interval <SECONDS>`**

  <span data-ttu-id="ee070-141">更新显示的计数器之间延迟的秒数</span><span class="sxs-lookup"><span data-stu-id="ee070-141">The number of seconds to delay between updating the displayed counters</span></span>

- **`--counters <COUNTERS>`**

  <span data-ttu-id="ee070-142">计数器的逗号分隔列表。</span><span class="sxs-lookup"><span data-stu-id="ee070-142">A comma-separated list of counters.</span></span> <span data-ttu-id="ee070-143">计数器可以指定为 `provider_name[:counter_name]`。</span><span class="sxs-lookup"><span data-stu-id="ee070-143">Counters can be specified `provider_name[:counter_name]`.</span></span> <span data-ttu-id="ee070-144">如果使用 `provider_name` 时没有限定的计数器列表，则显示来自提供程序的所有计数器。</span><span class="sxs-lookup"><span data-stu-id="ee070-144">If the `provider_name` is used without a qualifying list of counters, then all counters from the provider are shown.</span></span> <span data-ttu-id="ee070-145">若要发现提供程序和计数器名称，请使用 [dotnet-counters list](#dotnet-counters-list) 命令。</span><span class="sxs-lookup"><span data-stu-id="ee070-145">To discover provider and counter names, use the [dotnet-counters list](#dotnet-counters-list) command.</span></span>

- **`--format <csv|json>`**

  <span data-ttu-id="ee070-146">要导出的格式。</span><span class="sxs-lookup"><span data-stu-id="ee070-146">The format to be exported.</span></span> <span data-ttu-id="ee070-147">当前可用的格式：csv 和 json。</span><span class="sxs-lookup"><span data-stu-id="ee070-147">Currently available: csv, json.</span></span>

- **`-o|--output <output>`**

  <span data-ttu-id="ee070-148">输出文件的名称。</span><span class="sxs-lookup"><span data-stu-id="ee070-148">The name of the output file.</span></span>

- <span data-ttu-id="ee070-149">`-- <command>`（仅适用于运行 .NET 5.0 或更高版本的目标应用程序）</span><span class="sxs-lookup"><span data-stu-id="ee070-149">**`-- <command>` (for target applications running .NET 5.0 or later only)**</span></span>

  <span data-ttu-id="ee070-150">在集合配置参数之后，用户可以追加 `--`，后跟一个命令，以启动至少具有 5.0 运行时的 .NET 应用程序。</span><span class="sxs-lookup"><span data-stu-id="ee070-150">After the collection configuration parameters, the user can append `--` followed by a command to start a .NET application with at least a 5.0 runtime.</span></span> <span data-ttu-id="ee070-151">`dotnet-counters` 将启动一个进程，并收集请求的指标。</span><span class="sxs-lookup"><span data-stu-id="ee070-151">`dotnet-counters` will launch a process with the provided command and collect the requested metrics.</span></span> <span data-ttu-id="ee070-152">这通常用于收集应用程序的启动路径的指标，并可用于诊断或监视在主入口点前后发生的问题。</span><span class="sxs-lookup"><span data-stu-id="ee070-152">This is often useful to collect metrics for the application's startup path and can be used to diagnose or monitor issues that happen early before or shortly after the main entrypoint.</span></span>

  > [!NOTE]
  > <span data-ttu-id="ee070-153">使用此选项监视第一个 .NET 5.0 进程，该进程与该工具通信，这意味着如果命令启动多个 .NET 应用程序，它将仅收集第一个应用。</span><span class="sxs-lookup"><span data-stu-id="ee070-153">Using this option monitors the first .NET 5.0 process that communicates back to the tool, which means if your command launches multiple .NET applications, it will only collect the first app.</span></span> <span data-ttu-id="ee070-154">因此，建议在自包含应用程序上使用此选项，或使用 `dotnet exec <app.dll>` 选项。</span><span class="sxs-lookup"><span data-stu-id="ee070-154">Therefore, it is recommended you use this option on self-contained applications, or using the `dotnet exec <app.dll>` option.</span></span>

  > [!NOTE]
  > <span data-ttu-id="ee070-155">通过 dotnet-counters 启动 .NET 可执行文件将重定向其输入/输出，你将无法与其 stdin/stdout 进行交互。</span><span class="sxs-lookup"><span data-stu-id="ee070-155">Launching a .NET executable via dotnet-counters will make its input/output to be redirected and you won't be able to interact with its stdin/stdout.</span></span> <span data-ttu-id="ee070-156">通过 CTRL+C 或 SIGTERM 退出工具将安全地结束该工具和子进程。</span><span class="sxs-lookup"><span data-stu-id="ee070-156">Exiting the tool via CTRL+C or SIGTERM will safely end both the tool and the child process.</span></span> <span data-ttu-id="ee070-157">如果子进程在工具之前退出，工具也将退出，应可安全查看跟踪。</span><span class="sxs-lookup"><span data-stu-id="ee070-157">If the child process exits before the tool, the tool will exit as well and the trace should be safely viewable.</span></span> <span data-ttu-id="ee070-158">如果需要使用 stdin/stdout，可以使用 `--diagnostic-port` 选项。</span><span class="sxs-lookup"><span data-stu-id="ee070-158">If you need to use stdin/stdout, you can use the `--diagnostic-port` option.</span></span> <span data-ttu-id="ee070-159">有关详细信息，请参阅[使用诊断端口](#using-diagnostic-port)。</span><span class="sxs-lookup"><span data-stu-id="ee070-159">See [Using diagnostic port](#using-diagnostic-port) for more information.</span></span>

### <a name="examples"></a><span data-ttu-id="ee070-160">示例</span><span class="sxs-lookup"><span data-stu-id="ee070-160">Examples</span></span>

- <span data-ttu-id="ee070-161">以 3 秒的刷新间隔时间收集所有计数器的值，并生成 csv 输出文件：</span><span class="sxs-lookup"><span data-stu-id="ee070-161">Collect all counters at a refresh interval of 3 seconds and generate a csv as output:</span></span>

  ```console
  > dotnet-counters collect --process-id 1902 --refresh-interval 3 --format csv

  counter_list is unspecified. Monitoring all counters by default.
  Starting a counter session. Press Q to quit.
  ```

- <span data-ttu-id="ee070-162">将 `dotnet mvc.dll` 作为子进程启动，开始从启动中收集运行时计算器和 ASP.NET Core Hosting 计算器，并将其另存为 JSON 输出：</span><span class="sxs-lookup"><span data-stu-id="ee070-162">Start `dotnet mvc.dll` as a child process and start collecting runtime counters and ASP.NET Core Hosting counters from startup and save it as a JSON output:</span></span>

  ```console
  > dotnet-counters collect --format json --counters System.Runtime,Microsoft.AspNetCore.Hosting -- dotnet mvc.dll
  Starting a counter session. Press Q to quit.
  File saved to counter.json
  ```

## <a name="dotnet-counters-list"></a><span data-ttu-id="ee070-163">dotnet-counters list</span><span class="sxs-lookup"><span data-stu-id="ee070-163">dotnet-counters list</span></span>

<span data-ttu-id="ee070-164">显示按提供程序分组的计数器名称和说明的列表。</span><span class="sxs-lookup"><span data-stu-id="ee070-164">Displays a list of counter names and descriptions, grouped by provider.</span></span>

### <a name="synopsis"></a><span data-ttu-id="ee070-165">摘要</span><span class="sxs-lookup"><span data-stu-id="ee070-165">Synopsis</span></span>

```console
dotnet-counters list [-h|--help]
```

### <a name="example"></a><span data-ttu-id="ee070-166">示例</span><span class="sxs-lookup"><span data-stu-id="ee070-166">Example</span></span>

```console
> dotnet-counters list
Showing well-known counters only. Specific processes may support additional counters.

System.Runtime
    cpu-usage                                    Amount of time the process has utilized the CPU (ms)
    working-set                                  Amount of working set used by the process (MB)
    gc-heap-size                                 Total heap size reported by the GC (MB)
    gen-0-gc-count                               Number of Gen 0 GCs per interval
    gen-1-gc-count                               Number of Gen 1 GCs per interval
    gen-2-gc-count                               Number of Gen 2 GCs per interval
    time-in-gc                                   % time in GC since the last GC
    gen-0-size                                   Gen 0 Heap Size
    gen-1-size                                   Gen 1 Heap Size
    gen-2-size                                   Gen 2 Heap Size
    loh-size                                     LOH Heap Size
    alloc-rate                                   Allocation Rate
    assembly-count                               Number of Assemblies Loaded
    exception-count                              Number of Exceptions per interval
    threadpool-thread-count                      Number of ThreadPool Threads
    monitor-lock-contention-count                Monitor Lock Contention Count
    threadpool-queue-length                      ThreadPool Work Items Queue Length
    threadpool-completed-items-count             ThreadPool Completed Work Items Count
    active-timer-count                           Active Timers Count

Microsoft.AspNetCore.Hosting
    requests-per-second                  Request rate
    total-requests                       Total number of requests
    current-requests                     Current number of requests
    failed-requests                      Failed number of requests
```

> [!NOTE]
> <span data-ttu-id="ee070-167">当有已标记的进程支持 `Microsoft.AspNetCore.Hosting` 计数器时（例如当 ASP.NET Core 应用程序在主机上运行时），将显示这些计数器。</span><span class="sxs-lookup"><span data-stu-id="ee070-167">The `Microsoft.AspNetCore.Hosting` counters are displayed when there are processes identified that support these counters, for example; when an ASP.NET Core application is running on the host machine.</span></span>

## <a name="dotnet-counters-monitor"></a><span data-ttu-id="ee070-168">dotnet-counters monitor</span><span class="sxs-lookup"><span data-stu-id="ee070-168">dotnet-counters monitor</span></span>

<span data-ttu-id="ee070-169">显示所选计数器的定期刷新值。</span><span class="sxs-lookup"><span data-stu-id="ee070-169">Displays periodically refreshing values of selected counters.</span></span>

### <a name="synopsis"></a><span data-ttu-id="ee070-170">摘要</span><span class="sxs-lookup"><span data-stu-id="ee070-170">Synopsis</span></span>

```console
dotnet-counters monitor [-h|--help] [-p|--process-id] [-n|--name] [--diagnostic-port] [--refresh-interval] [--counters] [-- <command>]
```

### <a name="options"></a><span data-ttu-id="ee070-171">选项</span><span class="sxs-lookup"><span data-stu-id="ee070-171">Options</span></span>

- **`-p|--process-id <PID>`**

  <span data-ttu-id="ee070-172">要监视的进程的 ID。</span><span class="sxs-lookup"><span data-stu-id="ee070-172">The ID of the process to be monitored.</span></span>

- **`-n|--name <name>`**

  <span data-ttu-id="ee070-173">要监视的进程的名称。</span><span class="sxs-lookup"><span data-stu-id="ee070-173">The name of the process to be monitored.</span></span>

- **`--diagnostic-port`**

  <span data-ttu-id="ee070-174">要创建的诊断端口的名称。</span><span class="sxs-lookup"><span data-stu-id="ee070-174">The name of the diagnostic port to create.</span></span> <span data-ttu-id="ee070-175">请参阅[使用诊断端口](#using-diagnostic-port)，了解如何使用此选项从应用启动时开始监视计数器。</span><span class="sxs-lookup"><span data-stu-id="ee070-175">See [using diagnostic port](#using-diagnostic-port) for how to use this option to start monitoring counters from app startup.</span></span>

- **`--refresh-interval <SECONDS>`**

  <span data-ttu-id="ee070-176">更新显示的计数器之间延迟的秒数</span><span class="sxs-lookup"><span data-stu-id="ee070-176">The number of seconds to delay between updating the displayed counters</span></span>

- **`--counters <COUNTERS>`**

  <span data-ttu-id="ee070-177">计数器的逗号分隔列表。</span><span class="sxs-lookup"><span data-stu-id="ee070-177">A comma-separated list of counters.</span></span> <span data-ttu-id="ee070-178">计数器可以指定为 `provider_name[:counter_name]`。</span><span class="sxs-lookup"><span data-stu-id="ee070-178">Counters can be specified `provider_name[:counter_name]`.</span></span> <span data-ttu-id="ee070-179">如果使用 `provider_name` 时没有限定的计数器列表，则显示来自提供程序的所有计数器。</span><span class="sxs-lookup"><span data-stu-id="ee070-179">If the `provider_name` is used without a qualifying list of counters, then all counters from the provider are shown.</span></span> <span data-ttu-id="ee070-180">若要发现提供程序和计数器名称，请使用 [dotnet-counters list](#dotnet-counters-list) 命令。</span><span class="sxs-lookup"><span data-stu-id="ee070-180">To discover provider and counter names, use the [dotnet-counters list](#dotnet-counters-list) command.</span></span>

 <span data-ttu-id="ee070-181">`-- <command>`（仅适用于运行 .NET 5.0 或更高版本的目标应用程序）</span><span class="sxs-lookup"><span data-stu-id="ee070-181">**`-- <command>` (for target applications running .NET 5.0 or later only)**</span></span>

  <span data-ttu-id="ee070-182">在集合配置参数之后，用户可以追加 `--`，后跟一个命令，以启动至少具有 5.0 运行时的 .NET 应用程序。</span><span class="sxs-lookup"><span data-stu-id="ee070-182">After the collection configuration parameters, the user can append `--` followed by a command to start a .NET application with at least a 5.0 runtime.</span></span> <span data-ttu-id="ee070-183">`dotnet-counters` 将启动一个进程，并监视请求的指标。</span><span class="sxs-lookup"><span data-stu-id="ee070-183">`dotnet-counters` will launch a process with the provided command and monitor the requested metrics.</span></span> <span data-ttu-id="ee070-184">这通常用于收集应用程序的启动路径的指标，并可用于诊断或监视在主入口点前后发生的问题。</span><span class="sxs-lookup"><span data-stu-id="ee070-184">This is often useful to collect metrics for the application's startup path and can be used to diagnose or monitor issues that happen early before or shortly after the main entrypoint.</span></span>

  > [!NOTE]
  > <span data-ttu-id="ee070-185">使用此选项监视第一个 .NET 5.0 进程，该进程与该工具通信，这意味着如果命令启动多个 .NET 应用程序，它将仅收集第一个应用。</span><span class="sxs-lookup"><span data-stu-id="ee070-185">Using this option monitors the first .NET 5.0 process that communicates back to the tool, which means if your command launches multiple .NET applications, it will only collect the first app.</span></span> <span data-ttu-id="ee070-186">因此，建议在自包含应用程序上使用此选项，或使用 `dotnet exec <app.dll>` 选项。</span><span class="sxs-lookup"><span data-stu-id="ee070-186">Therefore, it is recommended you use this option on self-contained applications, or using the `dotnet exec <app.dll>` option.</span></span>

  > [!NOTE]
  > <span data-ttu-id="ee070-187">通过 dotnet-counters 启动 .NET 可执行文件将重定向其输入/输出，你将无法与其 stdin/stdout 进行交互。</span><span class="sxs-lookup"><span data-stu-id="ee070-187">Launching a .NET executable via dotnet-counters will make its input/output to be redirected and you won't be able to interact with its stdin/stdout.</span></span> <span data-ttu-id="ee070-188">通过 CTRL+C 或 SIGTERM 退出工具将安全地结束该工具和子进程。</span><span class="sxs-lookup"><span data-stu-id="ee070-188">Exiting the tool via CTRL+C or SIGTERM will safely end both the tool and the child process.</span></span> <span data-ttu-id="ee070-189">如果子进程在工具之前退出，工具也将退出，应可安全查看跟踪。</span><span class="sxs-lookup"><span data-stu-id="ee070-189">If the child process exits before the tool, the tool will exit as well and the trace should be safely viewable.</span></span> <span data-ttu-id="ee070-190">如果需要使用 stdin/stdout，可以使用 `--diagnostic-port` 选项。</span><span class="sxs-lookup"><span data-stu-id="ee070-190">If you need to use stdin/stdout, you can use the `--diagnostic-port` option.</span></span> <span data-ttu-id="ee070-191">有关详细信息，请参阅[使用诊断端口](#using-diagnostic-port)。</span><span class="sxs-lookup"><span data-stu-id="ee070-191">See [Using diagnostic port](#using-diagnostic-port) for more information.</span></span>

### <a name="examples"></a><span data-ttu-id="ee070-192">示例</span><span class="sxs-lookup"><span data-stu-id="ee070-192">Examples</span></span>

- <span data-ttu-id="ee070-193">以 3 秒的刷新间隔监视 `System.Runtime` 中的所有计数器：</span><span class="sxs-lookup"><span data-stu-id="ee070-193">Monitor all counters from `System.Runtime` at a refresh interval of 3 seconds:</span></span>

  ```console
  > dotnet-counters monitor --process-id 1902  --refresh-interval 3 --counters System.Runtime
  Press p to pause, r to resume, q to quit.
      Status: Running

  [System.Runtime]
      % Time in GC since last GC (%)                                 0
      Allocation Rate (B / 1 sec)                                5,376
      CPU Usage (%)                                                  0
      Exception Count (Count / 1 sec)                                0
      GC Fragmentation (%)                                          48.467
      GC Heap Size (MB)                                              0
      Gen 0 GC Count (Count / 1 sec)                                 1
      Gen 0 Size (B)                                                24
      Gen 1 GC Count (Count / 1 sec)                                 1
      Gen 1 Size (B)                                                24
      Gen 2 GC Count (Count / 1 sec)                                 1
      Gen 2 Size (B)                                           272,000
      IL Bytes Jitted (B)                                       19,449
      LOH Size (B)                                              19,640
      Monitor Lock Contention Count (Count / 1 sec)                  0
      Number of Active Timers                                        0
      Number of Assemblies Loaded                                    7
      Number of Methods Jitted                                     166
      POH (Pinned Object Heap) Size (B)                             24
      ThreadPool Completed Work Item Count (Count / 1 sec)           0
      ThreadPool Queue Length                                        0
      ThreadPool Thread Count                                        2
      Working Set (MB)                                              19
  ```

- <span data-ttu-id="ee070-194">仅监视 `System.Runtime` 中的 CPU 使用情况和 GC 堆大小：</span><span class="sxs-lookup"><span data-stu-id="ee070-194">Monitor just CPU usage and GC heap size from `System.Runtime`:</span></span>

  ```console
  > dotnet-counters monitor --process-id 1902 --counters System.Runtime[cpu-usage,gc-heap-size]

  Press p to pause, r to resume, q to quit.
    Status: Running

  [System.Runtime]
      CPU Usage (%)                                 24
      GC Heap Size (MB)                            811
  ```

- <span data-ttu-id="ee070-195">监视用户定义的 `EventSource` 中的 `EventCounter` 值。</span><span class="sxs-lookup"><span data-stu-id="ee070-195">Monitor `EventCounter` values from user-defined `EventSource`.</span></span> <span data-ttu-id="ee070-196">有关详细信息，请参阅[教程：使用 .NET Core 中的 EventCounters 衡量性能](event-counter-perf.md)。</span><span class="sxs-lookup"><span data-stu-id="ee070-196">For more information, see [Tutorial: Measure performance using EventCounters in .NET Core](event-counter-perf.md).</span></span>

  ```console
  > dotnet-counters monitor --process-id 1902 --counters Samples-EventCounterDemos-Minimal

  Press p to pause, r to resume, q to quit.
      request                                      100
  ```

- <span data-ttu-id="ee070-197">查看 `dotnet-counters` 中可用的所有已知计数器：</span><span class="sxs-lookup"><span data-stu-id="ee070-197">View all well-known counters that are available in `dotnet-counters`:</span></span>

  ```console
  > dotnet-counters list

  Showing well-known counters for .NET (Core) version 3.1 only. Specific processes may support additional counters.
  System.Runtime              
      cpu-usage                          The percent of process' CPU usage relative to all of the system CPU resources [0-100]
      working-set                        Amount of working set used by the process (MB)
      gc-heap-size                       Total heap size reported by the GC (MB)
      gen-0-gc-count                     Number of Gen 0 GCs between update intervals
      gen-1-gc-count                     Number of Gen 1 GCs between update intervals
      gen-2-gc-count                     Number of Gen 2 GCs between update intervals
      time-in-gc                         % time in GC since the last GC
      gen-0-size                         Gen 0 Heap Size
      gen-1-size                         Gen 1 Heap Size
      gen-2-size                         Gen 2 Heap Size
      loh-size                           LOH Size
      alloc-rate                         Number of bytes allocated in the managed heap between update intervals
      assembly-count                     Number of Assemblies Loaded
      exception-count                    Number of Exceptions / sec
      threadpool-thread-count            Number of ThreadPool Threads
      monitor-lock-contention-count      Number of times there were contention when trying to take the monitor lock between update intervals
      threadpool-queue-length            ThreadPool Work Items Queue Length
      threadpool-completed-items-count   ThreadPool Completed Work Items Count
      active-timer-count                 Number of timers that are currently active

  Microsoft.AspNetCore.Hosting
      requests-per-second                Number of requests between update intervals
      total-requests                     Total number of requests
      current-requests                   Current number of requests
      failed-requests                    Failed number of requests
  ```

- <span data-ttu-id="ee070-198">查看 `dotnet-counters` 中可用于 .NET 5 应用的所有已知计数器：</span><span class="sxs-lookup"><span data-stu-id="ee070-198">View all well-known counters that are available in `dotnet-counters` for .NET 5 apps:</span></span>

  ```console
  > dotnet-counters list --runtime-version 5.0

  Showing well-known counters for .NET (Core) version 5.0 only. Specific processes may support additional counters.
  System.Runtime                     
      cpu-usage                          The percent of process' CPU usage relative to all of the system CPU resources [0-100]
      working-set                        Amount of working set used by the process (MB)
      gc-heap-size                       Total heap size reported by the GC (MB)
      gen-0-gc-count                     Number of Gen 0 GCs between update intervals
      gen-1-gc-count                     Number of Gen 1 GCs between update intervals
      gen-2-gc-count                     Number of Gen 2 GCs between update intervals
      time-in-gc                         % time in GC since the last GC
      gen-0-size                         Gen 0 Heap Size
      gen-1-size                         Gen 1 Heap Size
      gen-2-size                         Gen 2 Heap Size
      loh-size                           LOH Size
      poh-size                           POH (Pinned Object Heap) Size
      alloc-rate                         Number of bytes allocated in the managed heap between update intervals
      gc-fragmentation                   GC Heap Fragmentation
      assembly-count                     Number of Assemblies Loaded
      exception-count                    Number of Exceptions / sec
      threadpool-thread-count            Number of ThreadPool Threads
      monitor-lock-contention-count      Number of times there were contention when trying to take the monitor lock between update intervals
      threadpool-queue-length            ThreadPool Work Items Queue Length
      threadpool-completed-items-count   ThreadPool Completed Work Items Count
      active-timer-count                 Number of timers that are currently active
      il-bytes-jitted                    Total IL bytes jitted
      methods-jitted-count               Number of methods jitted

  Microsoft.AspNetCore.Hosting       
      requests-per-second   Number of requests between update intervals
      total-requests        Total number of requests
      current-requests      Current number of requests
      failed-requests       Failed number of requests

  Microsoft-AspNetCore-Server-Kestrel
      connections-per-second      Number of connections between update intervals
      total-connections           Total Connections
      tls-handshakes-per-second   Number of TLS Handshakes made between update intervals
      total-tls-handshakes        Total number of TLS handshakes made
      current-tls-handshakes      Number of currently active TLS handshakes
      failed-tls-handshakes       Total number of failed TLS handshakes
      current-connections         Number of current connections
      connection-queue-length     Length of Kestrel Connection Queue
      request-queue-length        Length total HTTP request queue

  System.Net.Http                    
      requests-started        Total Requests Started
      requests-started-rate   Number of Requests Started between update intervals
      requests-aborted        Total Requests Aborted
      requests-aborted-rate   Number of Requests Aborted between update intervals
      current-requests        Current Requests
  ```

- <span data-ttu-id="ee070-199">启动 `my-aspnet-server.exe` 并从其启动监视加载的程序集的数量（仅限 .NET 5.0 或更高版本）：</span><span class="sxs-lookup"><span data-stu-id="ee070-199">Launch `my-aspnet-server.exe` and monitor the # of assemblies loaded from its startup (.NET 5.0 or later only):</span></span>

  > [!IMPORTANT]
  > <span data-ttu-id="ee070-200">这仅适用于运行 .NET 5.0 或更高版本的应用。</span><span class="sxs-lookup"><span data-stu-id="ee070-200">This works for apps running .NET 5.0 or later only.</span></span>

  ```console
  > dotnet-counters monitor --counters System.Runtime[assembly-count] -- my-aspnet-server.exe

  Press p to pause, r to resume, q to quit.
    Status: Running

  [System.Runtime]
      Number of Assemblies Loaded                   24
  ```
  
- <span data-ttu-id="ee070-201">启动 `my-aspnet-server.exe`，以 `arg1` 及 `arg2` 作为命令行参数，并从其启动监视其工作集和 GC 堆大小（仅限 .NET 5.0 或更高版本）：</span><span class="sxs-lookup"><span data-stu-id="ee070-201">Launch `my-aspnet-server.exe` with `arg1` and `arg2` as command-line arguments and monitor its working set and GC heap size from its startup (.NET 5.0 or later only):</span></span>

  > [!IMPORTANT]
  > <span data-ttu-id="ee070-202">这仅适用于运行 .NET 5.0 或更高版本的应用。</span><span class="sxs-lookup"><span data-stu-id="ee070-202">This works for apps running .NET 5.0 or later only.</span></span>

  ```console
  > dotnet-counters monitor --counters System.Runtime[working-set,gc-heap-size] -- my-aspnet-server.exe arg1 arg2
  ```

  ```console
  Press p to pause, r to resume, q to quit.
    Status: Running

  [System.Runtime]
      GC Heap Size (MB)                                 39
      Working Set (MB)                                  59
  ```

## <a name="dotnet-counters-ps"></a><span data-ttu-id="ee070-203">dotnet-counters ps</span><span class="sxs-lookup"><span data-stu-id="ee070-203">dotnet-counters ps</span></span>

<span data-ttu-id="ee070-204">显示可监视的 dotnet 进程的列表。</span><span class="sxs-lookup"><span data-stu-id="ee070-204">Display a list of dotnet processes that can be monitored.</span></span>

### <a name="synopsis"></a><span data-ttu-id="ee070-205">摘要</span><span class="sxs-lookup"><span data-stu-id="ee070-205">Synopsis</span></span>

```console
dotnet-counters ps [-h|--help]
```

### <a name="example"></a><span data-ttu-id="ee070-206">示例</span><span class="sxs-lookup"><span data-stu-id="ee070-206">Example</span></span>

```console
> dotnet-counters ps
  
  15683 WebApi     /home/user/repos/WebApi/WebApi
  16324 dotnet     /usr/local/share/dotnet/dotnet
```

## <a name="using-diagnostic-port"></a><span data-ttu-id="ee070-207">使用诊断端口</span><span class="sxs-lookup"><span data-stu-id="ee070-207">Using diagnostic port</span></span>

  > [!IMPORTANT]
  > <span data-ttu-id="ee070-208">这仅适用于运行 .NET 5.0 或更高版本的应用。</span><span class="sxs-lookup"><span data-stu-id="ee070-208">This works for apps running .NET 5.0 or later only.</span></span>

<span data-ttu-id="ee070-209">诊断端口是 .NET 5 中新增的运行时功能，你可以通过它从应用启动时开始监视或收集计数器。</span><span class="sxs-lookup"><span data-stu-id="ee070-209">Diagnostic port is a new runtime feature that was added in .NET 5 that allows you to start monitoring or collecting counters from app startup.</span></span> <span data-ttu-id="ee070-210">若要使用 `dotnet-counters` 执行此操作，可以使用以上示例中所述的 `dotnet-counters <collect|monitor> -- <command>`，也可以使用 `--diagnostic-port` 选项。</span><span class="sxs-lookup"><span data-stu-id="ee070-210">To do this using `dotnet-counters`, you can either use `dotnet-counters <collect|monitor> -- <command>` as described in the examples above, or use the `--diagnostic-port` option.</span></span>

<span data-ttu-id="ee070-211">使用 `dotnet-counters <collect|monitor> -- <command>` 以子进程的形式启动应用程序，是从启动时开始对其进行快速监视的最简单方法。</span><span class="sxs-lookup"><span data-stu-id="ee070-211">Using `dotnet-counters <collect|monitor> -- <command>` to launch the application as a child process is the simplest way to quickly monitor it from its startup.</span></span>

<span data-ttu-id="ee070-212">但是，如果想要更好地控制所监视应用的生存期（例如，仅在前 10 分钟内监视应用并继续执行），或者如果需要使用 CLI 与应用进行交互，则使用 `--diagnostic-port` 选项可以同时控制要监视的目标应用和 `dotnet-counters`。</span><span class="sxs-lookup"><span data-stu-id="ee070-212">However, when you want to gain a finer control over the lifetime of the app being monitored (for example, monitor the app for the first 10 minutes only and continue executing) or if you need to interact with the app using the CLI, using `--diagnostic-port` option allows you to control both the target app being monitored and `dotnet-counters`.</span></span>

1. <span data-ttu-id="ee070-213">以下命令使 dotnet-counters 创建一个名为 `myport.sock` 的诊断套接字并等待连接。</span><span class="sxs-lookup"><span data-stu-id="ee070-213">The command below makes dotnet-counters create a diagnostics socket named `myport.sock` and wait for a connection.</span></span>

    > ```dotnet-cli
    > dotnet-counters collect --diagnostic-port myport.sock
    > ```

    <span data-ttu-id="ee070-214">输出：</span><span class="sxs-lookup"><span data-stu-id="ee070-214">Output:</span></span>

    > ```bash
    > Waiting for connection on myport.sock
    > Start an application with the following environment variable: DOTNET_DiagnosticPorts=/home/user/myport.sock
    > ```

2. <span data-ttu-id="ee070-215">在单独的控制台中，通过将环境变量 `DOTNET_DiagnosticPorts` 设置为 `dotnet-counters` 输出中的值，启动目标应用程序。</span><span class="sxs-lookup"><span data-stu-id="ee070-215">In a separate console, launch the target application with the environment variable `DOTNET_DiagnosticPorts` set to the value in the `dotnet-counters` output.</span></span>

    > ```bash
    > export DOTNET_DiagnosticPorts=/home/user/myport.sock
    > ./my-dotnet-app arg1 arg2
    > ```

    <span data-ttu-id="ee070-216">这应该会使 `dotnet-counters` 开始在 `my-dotnet-app` 上收集计数器：</span><span class="sxs-lookup"><span data-stu-id="ee070-216">This should then enable `dotnet-counters` to start collecting counters on `my-dotnet-app`:</span></span>

    > ```bash
    > Waiting for connection on myport.sock
    > Start an application with the following environment variable: DOTNET_DiagnosticPorts=myport.sock
    > Starting a counter session. Press Q to quit.
    > ```

    > [!IMPORTANT]
    > <span data-ttu-id="ee070-217">通过 `dotnet run` 启动应用可能会产生问题，因为 dotnet CLI 可能会生成许多子进程，这些子程序不是应用，并且可以在应用之前连接到 `dotnet-counters`，从而导致应用在运行时挂起。</span><span class="sxs-lookup"><span data-stu-id="ee070-217">Launching your app with `dotnet run` can be problematic because the dotnet CLI may spawn many child processes that are not your app and they can connect to `dotnet-counters` before your app, leaving your app to be suspended at runtime.</span></span> <span data-ttu-id="ee070-218">建议直接使用应用的独立版本或使用 `dotnet exec` 来启动应用程序。</span><span class="sxs-lookup"><span data-stu-id="ee070-218">It is recommended you directly use a self-contained version of the app or use `dotnet exec` to launch the application.</span></span>
