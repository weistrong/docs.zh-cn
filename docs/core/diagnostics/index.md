---
title: 诊断工具概述 - .NET Core
description: 概述用于 .NET Core 应用程序的工具和技术。
ms.date: 07/16/2020
ms.topic: overview
ms.openlocfilehash: 9836ea11e7f17d6ed6e04bcba8bc0ed851bb368f
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102105279"
---
# <a name="what-diagnostic-tools-are-available-in-net-core"></a><span data-ttu-id="a142f-103">.NET Core 中提供哪些诊断工具？</span><span class="sxs-lookup"><span data-stu-id="a142f-103">What diagnostic tools are available in .NET Core?</span></span>

<span data-ttu-id="a142f-104">软件并非始终按预计方式运行，但 .NET Core 具有可帮助用户快速有效地诊断这些问题的工具和 API。</span><span class="sxs-lookup"><span data-stu-id="a142f-104">Software doesn't always behave as you would expect, but .NET Core has tools and APIs that will help you diagnose these issues quickly and effectively.</span></span>

<span data-ttu-id="a142f-105">本文可帮助用户查找各种所需的工具。</span><span class="sxs-lookup"><span data-stu-id="a142f-105">This article helps you find the various tools you need.</span></span>

## <a name="managed-debuggers"></a><span data-ttu-id="a142f-106">托管调试器</span><span class="sxs-lookup"><span data-stu-id="a142f-106">Managed debuggers</span></span>

<span data-ttu-id="a142f-107">借助[托管调试器](managed-debuggers.md)，用户可以与程序进行交互。</span><span class="sxs-lookup"><span data-stu-id="a142f-107">[Managed debuggers](managed-debuggers.md) allow you to interact with your program.</span></span> <span data-ttu-id="a142f-108">暂停、增量执行、检查和恢复操作可让用户深入了解代码的行为。</span><span class="sxs-lookup"><span data-stu-id="a142f-108">Pausing, incrementally executing, examining,  and resuming gives you insight into the behavior of your code.</span></span> <span data-ttu-id="a142f-109">调试器是诊断易于重现的功能问题的首选。</span><span class="sxs-lookup"><span data-stu-id="a142f-109">A debugger is the first choice for diagnosing functional problems that can be easily reproduced.</span></span>

## <a name="logging-and-tracing"></a><span data-ttu-id="a142f-110">日志记录和跟踪</span><span class="sxs-lookup"><span data-stu-id="a142f-110">Logging and tracing</span></span>

<span data-ttu-id="a142f-111">[日志记录和跟踪](logging-tracing.md)是相关技术。</span><span class="sxs-lookup"><span data-stu-id="a142f-111">[Logging and tracing](logging-tracing.md) are related techniques.</span></span> <span data-ttu-id="a142f-112">它们指的是用于创建日志文件的检测代码。</span><span class="sxs-lookup"><span data-stu-id="a142f-112">They refer to instrumenting code to create log files.</span></span> <span data-ttu-id="a142f-113">这些文件记录了程序操作的详细信息。</span><span class="sxs-lookup"><span data-stu-id="a142f-113">The files record the details of what a program does.</span></span> <span data-ttu-id="a142f-114">这些细节可用于诊断最复杂的问题。</span><span class="sxs-lookup"><span data-stu-id="a142f-114">These details can be used to diagnose the most complex problems.</span></span> <span data-ttu-id="a142f-115">当与时间戳结合使用时，这些技术在性能调查中也非常有用。</span><span class="sxs-lookup"><span data-stu-id="a142f-115">When combined with time stamps, these techniques are also valuable in performance investigations.</span></span>

## <a name="metrics"></a><span data-ttu-id="a142f-116">指标</span><span class="sxs-lookup"><span data-stu-id="a142f-116">Metrics</span></span>

<span data-ttu-id="a142f-117">[EventCounters](event-counters.md) 使你可编写指标来识别和监视性能问题。</span><span class="sxs-lookup"><span data-stu-id="a142f-117">[EventCounters](event-counters.md) allows you to write metrics to identify and monitor performance issues.</span></span> <span data-ttu-id="a142f-118">与跟踪相比，指标产生的性能开销较低，这使指标更适合 always-on 性能监视。</span><span class="sxs-lookup"><span data-stu-id="a142f-118">Metrics incur lower performance overhead compared to tracing, making it more suitable for an always-on performance monitoring.</span></span> <span data-ttu-id="a142f-119">.NET 运行时和库发布了多个[已知 EventCounters](available-counters.md)，你也可以对其进行监视。</span><span class="sxs-lookup"><span data-stu-id="a142f-119">The .NET runtime and libraries publish several [well-known EventCounters](available-counters.md) that you can monitor as well.</span></span>

## <a name="unit-testing"></a><span data-ttu-id="a142f-120">单元测试</span><span class="sxs-lookup"><span data-stu-id="a142f-120">Unit testing</span></span>

<span data-ttu-id="a142f-121">[单元测试](../testing/index.md)是持续集成和部署高质量软件的关键组件。</span><span class="sxs-lookup"><span data-stu-id="a142f-121">[Unit testing](../testing/index.md) is a key component of continuous integration and deployment of high-quality software.</span></span> <span data-ttu-id="a142f-122">单元测试的目的在于，在用户操作导致系统出现问题时提前向其发出警告。</span><span class="sxs-lookup"><span data-stu-id="a142f-122">Unit tests are designed to give you an early warning when you break something.</span></span>

## <a name="dumps"></a><span data-ttu-id="a142f-123">转储</span><span class="sxs-lookup"><span data-stu-id="a142f-123">Dumps</span></span>

<span data-ttu-id="a142f-124">[转储](./dumps.md)是一个文件，其中包含创建时进程的快照。</span><span class="sxs-lookup"><span data-stu-id="a142f-124">A [dump](./dumps.md) is a file that contains a snapshot of the process at the time of creation.</span></span> <span data-ttu-id="a142f-125">它们可用于检查应用程序的状态，以便进行调试。</span><span class="sxs-lookup"><span data-stu-id="a142f-125">These can be useful for examining the state of your application for debugging purposes.</span></span>

## <a name="symbols"></a><span data-ttu-id="a142f-126">符号</span><span class="sxs-lookup"><span data-stu-id="a142f-126">Symbols</span></span>

<span data-ttu-id="a142f-127">[符号](./symbols.md)是源代码和编译器生成的二进制代码之间的映射。</span><span class="sxs-lookup"><span data-stu-id="a142f-127">[Symbols](./symbols.md) are a mapping between the source code and the binary produced by the compiler.</span></span> <span data-ttu-id="a142f-128">这些通常被 .NET 调试器用来解析源行号、局部变量名称以及其他类型的诊断信息。</span><span class="sxs-lookup"><span data-stu-id="a142f-128">These are commonly used by .NET debuggers to resolve source line numbers, local variable names, and other types of diagnostic information.</span></span>

## <a name="collect-diagnostics-in-containers"></a><span data-ttu-id="a142f-129">收集容器中的诊断</span><span class="sxs-lookup"><span data-stu-id="a142f-129">Collect diagnostics in containers</span></span>

<span data-ttu-id="a142f-130">也可使用非容器化 Linux 环境中使用的相同诊断工具[收集容器中的诊断](diagnostics-in-containers.md)。</span><span class="sxs-lookup"><span data-stu-id="a142f-130">The same diagnostics tools that are used in non-containerized Linux environments can also be used to [collect diagnostics in containers](diagnostics-in-containers.md).</span></span> <span data-ttu-id="a142f-131">只需进行几次使用更改就可使这些工具在 Docker 容器中运行。</span><span class="sxs-lookup"><span data-stu-id="a142f-131">There are just a few usage changes needed to make sure the tools work in a Docker container.</span></span>

## <a name="net-core-diagnostic-global-tools"></a><span data-ttu-id="a142f-132">.NET Core 诊断全局工具</span><span class="sxs-lookup"><span data-stu-id="a142f-132">.NET Core diagnostic global tools</span></span>

### <a name="dotnet-counters"></a><span data-ttu-id="a142f-133">dotnet-counters</span><span class="sxs-lookup"><span data-stu-id="a142f-133">dotnet-counters</span></span>

<span data-ttu-id="a142f-134">[dotnet-counters](dotnet-counters.md) 是一个性能监视工具，用于初级运行状况监视和性能调查。</span><span class="sxs-lookup"><span data-stu-id="a142f-134">[dotnet-counters](dotnet-counters.md) is a performance monitoring tool for first-level health monitoring and performance investigation.</span></span> <span data-ttu-id="a142f-135">它通过 <xref:System.Diagnostics.Tracing.EventCounter> API 观察已发布的性能计数器值。</span><span class="sxs-lookup"><span data-stu-id="a142f-135">It observes performance counter values published via the <xref:System.Diagnostics.Tracing.EventCounter> API.</span></span> <span data-ttu-id="a142f-136">例如，可以快速监视 CPU 使用情况或 .NET Core 应用程序中的异常率等指标。</span><span class="sxs-lookup"><span data-stu-id="a142f-136">For example, you can quickly monitor things like the CPU usage or the rate of exceptions being thrown in your .NET Core application.</span></span>

### <a name="dotnet-dump"></a><span data-ttu-id="a142f-137">dotnet-dump</span><span class="sxs-lookup"><span data-stu-id="a142f-137">dotnet-dump</span></span>

<span data-ttu-id="a142f-138">通过 [dotnet-dump](dotnet-dump.md) 工具，可在不使用本机调试器的情况下收集和分析 Windows 和 Linux 核心转储。</span><span class="sxs-lookup"><span data-stu-id="a142f-138">The [dotnet-dump](dotnet-dump.md) tool is a way to collect and analyze Windows and Linux core dumps without a native debugger.</span></span>

### <a name="dotnet-gcdump"></a><span data-ttu-id="a142f-139">dotnet-gcdump</span><span class="sxs-lookup"><span data-stu-id="a142f-139">dotnet-gcdump</span></span>

<span data-ttu-id="a142f-140">[dotnet-gcdump](dotnet-gcdump.md) 工具可用于为活动 .NET 进程收集 GC（垃圾回收器）转储。</span><span class="sxs-lookup"><span data-stu-id="a142f-140">The [dotnet-gcdump](dotnet-gcdump.md) tool is a way to collect GC (Garbage Collector) dumps of live .NET processes.</span></span>

### <a name="dotnet-trace"></a><span data-ttu-id="a142f-141">dotnet-trace</span><span class="sxs-lookup"><span data-stu-id="a142f-141">dotnet-trace</span></span>

<span data-ttu-id="a142f-142">分析数据通过 .NET Core 中的 `EventPipe` 公开。</span><span class="sxs-lookup"><span data-stu-id="a142f-142">.NET Core includes what is called the `EventPipe` through which diagnostics data is exposed.</span></span> <span data-ttu-id="a142f-143">通过 [dotnet-trace](dotnet-trace.md) 工具，可以使用来自应用的有意思的分析数据，这些数据可帮助你分析应用运行缓慢的根本原因。</span><span class="sxs-lookup"><span data-stu-id="a142f-143">The [dotnet-trace](dotnet-trace.md) tool allows you to consume interesting profiling data from your app that can help in scenarios where you need to root cause apps running slow.</span></span>

### <a name="dotnet-symbol"></a><span data-ttu-id="a142f-144">dotnet-symbol</span><span class="sxs-lookup"><span data-stu-id="a142f-144">dotnet-symbol</span></span>

<span data-ttu-id="a142f-145">[dotnet-symbol](dotnet-symbol.md) 用于下载打开核心转储或小型转储所需的文件（符号、DAC/DBI、主机文件等）。</span><span class="sxs-lookup"><span data-stu-id="a142f-145">[dotnet-symbol](dotnet-symbol.md) downloads files (symbols, DAC/DBI, host files, etc.) needed to open a core dump or minidump.</span></span> <span data-ttu-id="a142f-146">如果需要使用符号和模块来调试在其他计算机上捕获的转储文件，请使用此工具。</span><span class="sxs-lookup"><span data-stu-id="a142f-146">Use this tool if you need symbols and modules to debug a dump file captured on a different machine.</span></span>

### <a name="dotnet-sos"></a><span data-ttu-id="a142f-147">dotnet-sos</span><span class="sxs-lookup"><span data-stu-id="a142f-147">dotnet-sos</span></span>

<span data-ttu-id="a142f-148">[dotnet-sos](dotnet-sos.md) 在 Linux 和 macOS（如果使用的是 [Windbg/cdb](/windows-hardware/drivers/debugger/debugger-download-tools)，则在 Windows 上）安装 [SOS调试扩展](sos-debugging-extension.md)。</span><span class="sxs-lookup"><span data-stu-id="a142f-148">[dotnet-sos](dotnet-sos.md) installs the [SOS debugging extension](sos-debugging-extension.md) on Linux and macOS (and on Windows if you're using [Windbg/cdb](/windows-hardware/drivers/debugger/debugger-download-tools)).</span></span>

### <a name="perfcollect"></a><span data-ttu-id="a142f-149">PerfCollect</span><span class="sxs-lookup"><span data-stu-id="a142f-149">PerfCollect</span></span>

<span data-ttu-id="a142f-150">[PerfCollect](trace-perfcollect-lttng.md) 是一个 bash 脚本，可用于收集包含 `perf` 和 `LTTng` 的跟踪，以便更深入地分析在 Linux 分发版上运行的 .NET 应用的性能。</span><span class="sxs-lookup"><span data-stu-id="a142f-150">[PerfCollect](trace-perfcollect-lttng.md) is a bash script you can use to collect traces with `perf` and `LTTng` for a more in-depth performance analysis of .NET apps running on Linux distributions.</span></span>

## <a name="net-core-diagnostics-tutorials"></a><span data-ttu-id="a142f-151">.NET Core 诊断教程</span><span class="sxs-lookup"><span data-stu-id="a142f-151">.NET Core diagnostics tutorials</span></span>

### <a name="debug-a-memory-leak"></a><span data-ttu-id="a142f-152">调试内存泄露</span><span class="sxs-lookup"><span data-stu-id="a142f-152">Debug a memory leak</span></span>

<span data-ttu-id="a142f-153">[教程：调试内存泄漏](debug-memory-leak.md)演示了如何查找内存泄漏。</span><span class="sxs-lookup"><span data-stu-id="a142f-153">[Tutorial: Debug a memory leak](debug-memory-leak.md) walks through finding a memory leak.</span></span> <span data-ttu-id="a142f-154">[dotnet-counters](dotnet-counters.md) 工具用于确认泄露，[dotnet-dump](dotnet-dump.md) 工具用于诊断泄露。</span><span class="sxs-lookup"><span data-stu-id="a142f-154">The [dotnet-counters](dotnet-counters.md) tool is used to confirm the leak and the [dotnet-dump](dotnet-dump.md) tool is used to diagnose the leak.</span></span>

### <a name="debug-high-cpu-usage"></a><span data-ttu-id="a142f-155">调试高 CPU 使用率</span><span class="sxs-lookup"><span data-stu-id="a142f-155">Debug high CPU usage</span></span>

<span data-ttu-id="a142f-156">[教程：调试高 CPU 使用率](debug-highcpu.md)逐步介绍了如何调查高 CPU 使用率。</span><span class="sxs-lookup"><span data-stu-id="a142f-156">[Tutorial: Debug high CPU usage](debug-highcpu.md) walks you through investigating high CPU usage.</span></span> <span data-ttu-id="a142f-157">它使用 [dotnet-counters](dotnet-counters.md) 工具来确认高 CPU 使用率。</span><span class="sxs-lookup"><span data-stu-id="a142f-157">It uses the [dotnet-counters](dotnet-counters.md) tool to confirm the high CPU usage.</span></span> <span data-ttu-id="a142f-158">然后，它逐步介绍了如何使用[性能分析实用工具 (`dotnet-trace`) 跟踪](dotnet-trace.md)或 Linux `perf` 来收集和查看 CPU 使用率配置文件。</span><span class="sxs-lookup"><span data-stu-id="a142f-158">It then walks you through using [Trace for performance analysis utility (`dotnet-trace`)](dotnet-trace.md) or Linux `perf` to collect and view CPU usage profile.</span></span>

### <a name="debug-deadlock"></a><span data-ttu-id="a142f-159">调试死锁</span><span class="sxs-lookup"><span data-stu-id="a142f-159">Debug deadlock</span></span>

<span data-ttu-id="a142f-160">[教程：调试死锁](debug-deadlock.md)介绍了如何使用 [dotnet-dump](dotnet-dump.md) 工具来调查线程和锁。</span><span class="sxs-lookup"><span data-stu-id="a142f-160">[Tutorial: Debug deadlock](debug-deadlock.md) shows you how to use the [dotnet-dump](dotnet-dump.md) tool to investigate threads and locks.</span></span>

### <a name="debug-a-stackoverflow"></a><span data-ttu-id="a142f-161">调试 StackOverflow</span><span class="sxs-lookup"><span data-stu-id="a142f-161">Debug a StackOverflow</span></span>

<span data-ttu-id="a142f-162">[教程：调试 StackOverflow](debug-stackoverflow.md) 演示了如何在 Linux 上调试 <xref:System.StackOverflowException>。</span><span class="sxs-lookup"><span data-stu-id="a142f-162">[Tutorial: Debug a StackOverflow](debug-stackoverflow.md) demonstrates how to debug a <xref:System.StackOverflowException> on Linux.</span></span>

### <a name="debug-linux-dumps"></a><span data-ttu-id="a142f-163">调试 Linux 转储</span><span class="sxs-lookup"><span data-stu-id="a142f-163">Debug Linux dumps</span></span>

<span data-ttu-id="a142f-164">[调试 Linux 转储](debug-linux-dumps.md)说明了如何收集和分析 Linux 上的转储。</span><span class="sxs-lookup"><span data-stu-id="a142f-164">[Debug Linux dumps](debug-linux-dumps.md) explains how to collect and analyze dumps on Linux.</span></span>

### <a name="measure-performance-using-eventcounters"></a><span data-ttu-id="a142f-165">使用 EventCounters 衡量性能</span><span class="sxs-lookup"><span data-stu-id="a142f-165">Measure performance using EventCounters</span></span>

<span data-ttu-id="a142f-166">[教程：使用 .NET 中的 EventCounters 度量性能](event-counter-perf.md)演示了如何使用 <xref:System.Diagnostics.Tracing.EventCounter> API 来衡量 .NET 应用的性能。</span><span class="sxs-lookup"><span data-stu-id="a142f-166">[Tutorial: Measure performance using EventCounters in .NET](event-counter-perf.md) shows you how to use the <xref:System.Diagnostics.Tracing.EventCounter> API to measure performance in your .NET app.</span></span>
