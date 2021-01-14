---
title: 诊断工具概述 - .NET Core
description: 概述用于 .NET Core 应用程序的工具和技术。
ms.date: 07/16/2020
ms.topic: overview
ms.openlocfilehash: ee79057e45700e17fdd37cc36288b790d64d7a09
ms.sourcegitcommit: a4cecb7389f02c27e412b743f9189bd2a6dea4d6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/14/2021
ms.locfileid: "98188473"
---
# <a name="what-diagnostic-tools-are-available-in-net-core"></a><span data-ttu-id="f8989-103">.NET Core 中提供哪些诊断工具？</span><span class="sxs-lookup"><span data-stu-id="f8989-103">What diagnostic tools are available in .NET Core?</span></span>

<span data-ttu-id="f8989-104">软件并非始终按预计方式运行，但 .NET Core 具有可帮助用户快速有效地诊断这些问题的工具和 API。</span><span class="sxs-lookup"><span data-stu-id="f8989-104">Software doesn't always behave as you would expect, but .NET Core has tools and APIs that will help you diagnose these issues quickly and effectively.</span></span>

<span data-ttu-id="f8989-105">本文可帮助用户查找各种所需的工具。</span><span class="sxs-lookup"><span data-stu-id="f8989-105">This article helps you find the various tools you need.</span></span>

## <a name="managed-debuggers"></a><span data-ttu-id="f8989-106">托管调试器</span><span class="sxs-lookup"><span data-stu-id="f8989-106">Managed debuggers</span></span>

<span data-ttu-id="f8989-107">借助[托管调试器](managed-debuggers.md)，用户可以与程序进行交互。</span><span class="sxs-lookup"><span data-stu-id="f8989-107">[Managed debuggers](managed-debuggers.md) allow you to interact with your program.</span></span> <span data-ttu-id="f8989-108">暂停、增量执行、检查和恢复操作可让用户深入了解代码的行为。</span><span class="sxs-lookup"><span data-stu-id="f8989-108">Pausing, incrementally executing, examining,  and resuming gives you insight into the behavior of your code.</span></span> <span data-ttu-id="f8989-109">调试器是诊断易于重现的功能问题的首选。</span><span class="sxs-lookup"><span data-stu-id="f8989-109">A debugger is the first choice for diagnosing functional problems that can be easily reproduced.</span></span>

## <a name="logging-and-tracing"></a><span data-ttu-id="f8989-110">日志记录和跟踪</span><span class="sxs-lookup"><span data-stu-id="f8989-110">Logging and tracing</span></span>

<span data-ttu-id="f8989-111">[日志记录和跟踪](logging-tracing.md)是相关技术。</span><span class="sxs-lookup"><span data-stu-id="f8989-111">[Logging and tracing](logging-tracing.md) are related techniques.</span></span> <span data-ttu-id="f8989-112">它们指的是用于创建日志文件的检测代码。</span><span class="sxs-lookup"><span data-stu-id="f8989-112">They refer to instrumenting code to create log files.</span></span> <span data-ttu-id="f8989-113">这些文件记录了程序操作的详细信息。</span><span class="sxs-lookup"><span data-stu-id="f8989-113">The files record the details of what a program does.</span></span> <span data-ttu-id="f8989-114">这些细节可用于诊断最复杂的问题。</span><span class="sxs-lookup"><span data-stu-id="f8989-114">These details can be used to diagnose the most complex problems.</span></span> <span data-ttu-id="f8989-115">当与时间戳结合使用时，这些技术在性能调查中也非常有用。</span><span class="sxs-lookup"><span data-stu-id="f8989-115">When combined with time stamps, these techniques are also valuable in performance investigations.</span></span>

## <a name="metrics"></a><span data-ttu-id="f8989-116">指标</span><span class="sxs-lookup"><span data-stu-id="f8989-116">Metrics</span></span>

<span data-ttu-id="f8989-117">[EventCounters](event-counters.md) 使你可编写指标来识别和监视性能问题。</span><span class="sxs-lookup"><span data-stu-id="f8989-117">[EventCounters](event-counters.md) allows you to write metrics to identify and monitor performance issues.</span></span> <span data-ttu-id="f8989-118">与跟踪相比，指标产生的性能开销较低，这使指标更适合 always-on 性能监视。</span><span class="sxs-lookup"><span data-stu-id="f8989-118">Metrics incur lower performance overhead compared to tracing, making it more suitable for an always-on performance monitoring.</span></span> <span data-ttu-id="f8989-119">.NET 运行时和库发布了多个[已知 EventCounters](available-counters.md)，你也可以对其进行监视。</span><span class="sxs-lookup"><span data-stu-id="f8989-119">The .NET runtime and libraries publish several [well-known EventCounters](available-counters.md) that you can monitor as well.</span></span>

## <a name="unit-testing"></a><span data-ttu-id="f8989-120">单元测试</span><span class="sxs-lookup"><span data-stu-id="f8989-120">Unit testing</span></span>

<span data-ttu-id="f8989-121">[单元测试](../testing/index.md)是持续集成和部署高质量软件的关键组件。</span><span class="sxs-lookup"><span data-stu-id="f8989-121">[Unit testing](../testing/index.md) is a key component of continuous integration and deployment of high-quality software.</span></span> <span data-ttu-id="f8989-122">单元测试的目的在于，在用户操作导致系统出现问题时提前向其发出警告。</span><span class="sxs-lookup"><span data-stu-id="f8989-122">Unit tests are designed to give you an early warning when you break something.</span></span>

## <a name="dumps"></a><span data-ttu-id="f8989-123">转储</span><span class="sxs-lookup"><span data-stu-id="f8989-123">Dumps</span></span>

<span data-ttu-id="f8989-124">[转储](./dumps.md)是一个文件，其中包含创建时进程的快照。</span><span class="sxs-lookup"><span data-stu-id="f8989-124">A [dump](./dumps.md) is a file that contains a snapshot of the process at the time of creation.</span></span> <span data-ttu-id="f8989-125">它们可用于检查应用程序的状态，以便进行调试。</span><span class="sxs-lookup"><span data-stu-id="f8989-125">These can be useful for examining the state of your application for debugging purposes.</span></span>

## <a name="symbols"></a><span data-ttu-id="f8989-126">符号</span><span class="sxs-lookup"><span data-stu-id="f8989-126">Symbols</span></span>

<span data-ttu-id="f8989-127">符号是调试和其他诊断工具的基本需求。</span><span class="sxs-lookup"><span data-stu-id="f8989-127">Symbols are a fundamental requirement for debugging and other diagnostic tools.</span></span> <span data-ttu-id="f8989-128">符号文件的内容在语言、编译器和平台之间各有不同。</span><span class="sxs-lookup"><span data-stu-id="f8989-128">The contents of symbol files vary between languages, compilers, and platforms.</span></span> <span data-ttu-id="f8989-129">以非常概要的角度来看，符号是源代码和编译器生成的二进制文件之间的映射。</span><span class="sxs-lookup"><span data-stu-id="f8989-129">At a very high level symbols are a mapping between the source code and the binary produced by the compiler.</span></span> <span data-ttu-id="f8989-130">这些映射用于在 [Visual Studio](/visualstudio/debugger/what-is-debugging) 和 [Visual Studio Code](https://code.visualstudio.com/Docs/editor/debugging) 等诊断工具中提供行号信息和局部变量名称之类的内容。</span><span class="sxs-lookup"><span data-stu-id="f8989-130">These mappings are used to provide things like line number information and names of your local variables in diagnostics tools such as [Visual Studio](/visualstudio/debugger/what-is-debugging) and [Visual Studio Code](https://code.visualstudio.com/Docs/editor/debugging).</span></span>  <span data-ttu-id="f8989-131">以下链接包含适用于 Windows 的[符号](/windows/win32/dxtecharts/debugging-with-symbols)的详细说明，但许多概念也适用于其他平台。</span><span class="sxs-lookup"><span data-stu-id="f8989-131">The following link contains a detailed explanation of [symbols](/windows/win32/dxtecharts/debugging-with-symbols) for Windows, although many of the concepts apply to other platforms as well.</span></span> <span data-ttu-id="f8989-132">[.NET 可移植符号](https://github.com/dotnet/core/blob/master/Documentation/diagnostics/portable_pdb.md)具有类似于 Windows PDB 的“PDB”文件扩展名，但并不与 Windows PDB 格式兼容。</span><span class="sxs-lookup"><span data-stu-id="f8989-132">[.NET portable symbols](https://github.com/dotnet/core/blob/master/Documentation/diagnostics/portable_pdb.md) have a "PDB" file extension similar to Windows PDB, though are not compatible with the Windows PDB format.</span></span>

## <a name="collect-diagnostics-in-containers"></a><span data-ttu-id="f8989-133">收集容器中的诊断</span><span class="sxs-lookup"><span data-stu-id="f8989-133">Collect diagnostics in containers</span></span>

<span data-ttu-id="f8989-134">也可使用非容器化 Linux 环境中使用的相同诊断工具[收集容器中的诊断](diagnostics-in-containers.md)。</span><span class="sxs-lookup"><span data-stu-id="f8989-134">The same diagnostics tools that are used in non-containerized Linux environments can also be used to [collect diagnostics in containers](diagnostics-in-containers.md).</span></span> <span data-ttu-id="f8989-135">只需进行几次使用更改就可使这些工具在 Docker 容器中运行。</span><span class="sxs-lookup"><span data-stu-id="f8989-135">There are just a few usage changes needed to make sure the tools work in a Docker container.</span></span>

## <a name="net-core-diagnostic-global-tools"></a><span data-ttu-id="f8989-136">.NET Core 诊断全局工具</span><span class="sxs-lookup"><span data-stu-id="f8989-136">.NET Core diagnostic global tools</span></span>

### <a name="dotnet-counters"></a><span data-ttu-id="f8989-137">dotnet-counters</span><span class="sxs-lookup"><span data-stu-id="f8989-137">dotnet-counters</span></span>

<span data-ttu-id="f8989-138">[dotnet-counters](dotnet-counters.md) 是一个性能监视工具，用于初级运行状况监视和性能调查。</span><span class="sxs-lookup"><span data-stu-id="f8989-138">[dotnet-counters](dotnet-counters.md) is a performance monitoring tool for first-level health monitoring and performance investigation.</span></span> <span data-ttu-id="f8989-139">它通过 <xref:System.Diagnostics.Tracing.EventCounter> API 观察已发布的性能计数器值。</span><span class="sxs-lookup"><span data-stu-id="f8989-139">It observes performance counter values published via the <xref:System.Diagnostics.Tracing.EventCounter> API.</span></span> <span data-ttu-id="f8989-140">例如，可以快速监视 CPU 使用情况或 .NET Core 应用程序中的异常率等指标。</span><span class="sxs-lookup"><span data-stu-id="f8989-140">For example, you can quickly monitor things like the CPU usage or the rate of exceptions being thrown in your .NET Core application.</span></span>

### <a name="dotnet-dump"></a><span data-ttu-id="f8989-141">dotnet-dump</span><span class="sxs-lookup"><span data-stu-id="f8989-141">dotnet-dump</span></span>

<span data-ttu-id="f8989-142">通过 [dotnet-dump](dotnet-dump.md) 工具，可在不使用本机调试器的情况下收集和分析 Windows 和 Linux 核心转储。</span><span class="sxs-lookup"><span data-stu-id="f8989-142">The [dotnet-dump](dotnet-dump.md) tool is a way to collect and analyze Windows and Linux core dumps without a native debugger.</span></span>

### <a name="dotnet-gcdump"></a><span data-ttu-id="f8989-143">dotnet-gcdump</span><span class="sxs-lookup"><span data-stu-id="f8989-143">dotnet-gcdump</span></span>

<span data-ttu-id="f8989-144">[dotnet-gcdump](dotnet-gcdump.md) 工具可用于为活动 .NET 进程收集 GC（垃圾回收器）转储。</span><span class="sxs-lookup"><span data-stu-id="f8989-144">The [dotnet-gcdump](dotnet-gcdump.md) tool is a way to collect GC (Garbage Collector) dumps of live .NET processes.</span></span>

### <a name="dotnet-trace"></a><span data-ttu-id="f8989-145">dotnet-trace</span><span class="sxs-lookup"><span data-stu-id="f8989-145">dotnet-trace</span></span>

<span data-ttu-id="f8989-146">分析数据通过 .NET Core 中的 `EventPipe` 公开。</span><span class="sxs-lookup"><span data-stu-id="f8989-146">.NET Core includes what is called the `EventPipe` through which diagnostics data is exposed.</span></span> <span data-ttu-id="f8989-147">通过 [dotnet-trace](dotnet-trace.md) 工具，可以使用来自应用的有意思的分析数据，这些数据可帮助你分析应用运行缓慢的根本原因。</span><span class="sxs-lookup"><span data-stu-id="f8989-147">The [dotnet-trace](dotnet-trace.md) tool allows you to consume interesting profiling data from your app that can help in scenarios where you need to root cause apps running slow.</span></span>

### <a name="dotnet-symbol"></a><span data-ttu-id="f8989-148">dotnet-symbol</span><span class="sxs-lookup"><span data-stu-id="f8989-148">dotnet-symbol</span></span>

<span data-ttu-id="f8989-149">[dotnet-symbol](dotnet-symbol.md) 用于下载打开核心转储或小型转储所需的文件（符号、DAC/DBI、主机文件等）。</span><span class="sxs-lookup"><span data-stu-id="f8989-149">[dotnet-symbol](dotnet-symbol.md) downloads files (symbols, DAC/DBI, host files, etc.) needed to open a core dump or minidump.</span></span> <span data-ttu-id="f8989-150">如果需要使用符号和模块来调试在其他计算机上捕获的转储文件，请使用此工具。</span><span class="sxs-lookup"><span data-stu-id="f8989-150">Use this tool if you need symbols and modules to debug a dump file captured on a different machine.</span></span>

### <a name="dotnet-sos"></a><span data-ttu-id="f8989-151">dotnet-sos</span><span class="sxs-lookup"><span data-stu-id="f8989-151">dotnet-sos</span></span>

<span data-ttu-id="f8989-152">[dotnet-sos](dotnet-sos.md) 在 Linux 和 macOS（如果使用的是 [Windbg/cdb](/windows-hardware/drivers/debugger/debugger-download-tools)，则在 Windows 上）安装 [SOS调试扩展](sos-debugging-extension.md)。</span><span class="sxs-lookup"><span data-stu-id="f8989-152">[dotnet-sos](dotnet-sos.md) installs the [SOS debugging extension](sos-debugging-extension.md) on Linux and macOS (and on Windows if you're using [Windbg/cdb](/windows-hardware/drivers/debugger/debugger-download-tools)).</span></span>

### <a name="perfcollect"></a><span data-ttu-id="f8989-153">PerfCollect</span><span class="sxs-lookup"><span data-stu-id="f8989-153">PerfCollect</span></span>

<span data-ttu-id="f8989-154">[PerfCollect](trace-perfcollect-lttng.md) 是一个 bash 脚本，可用于收集包含 `perf` 和 `LTTng` 的跟踪，以便更深入地分析在 Linux 分发版上运行的 .NET 应用的性能。</span><span class="sxs-lookup"><span data-stu-id="f8989-154">[PerfCollect](trace-perfcollect-lttng.md) is a bash script you can use to collect traces with `perf` and `LTTng` for a more in-depth performance analysis of .NET apps running on Linux distributions.</span></span>

## <a name="net-core-diagnostics-tutorials"></a><span data-ttu-id="f8989-155">.NET Core 诊断教程</span><span class="sxs-lookup"><span data-stu-id="f8989-155">.NET Core diagnostics tutorials</span></span>

### <a name="debug-a-memory-leak"></a><span data-ttu-id="f8989-156">调试内存泄露</span><span class="sxs-lookup"><span data-stu-id="f8989-156">Debug a memory leak</span></span>

<span data-ttu-id="f8989-157">[教程：调试内存泄漏](debug-memory-leak.md)演示了如何查找内存泄漏。</span><span class="sxs-lookup"><span data-stu-id="f8989-157">[Tutorial: Debug a memory leak](debug-memory-leak.md) walks through finding a memory leak.</span></span> <span data-ttu-id="f8989-158">[dotnet-counters](dotnet-counters.md) 工具用于确认泄露，[dotnet-dump](dotnet-dump.md) 工具用于诊断泄露。</span><span class="sxs-lookup"><span data-stu-id="f8989-158">The [dotnet-counters](dotnet-counters.md) tool is used to confirm the leak and the [dotnet-dump](dotnet-dump.md) tool is used to diagnose the leak.</span></span>

### <a name="debug-high-cpu-usage"></a><span data-ttu-id="f8989-159">调试高 CPU 使用率</span><span class="sxs-lookup"><span data-stu-id="f8989-159">Debug high CPU usage</span></span>

<span data-ttu-id="f8989-160">[教程：调试高 CPU 使用率](debug-highcpu.md)逐步介绍了如何调查高 CPU 使用率。</span><span class="sxs-lookup"><span data-stu-id="f8989-160">[Tutorial: Debug high CPU usage](debug-highcpu.md) walks you through investigating high CPU usage.</span></span> <span data-ttu-id="f8989-161">它使用 [dotnet-counters](dotnet-counters.md) 工具来确认高 CPU 使用率。</span><span class="sxs-lookup"><span data-stu-id="f8989-161">It uses the [dotnet-counters](dotnet-counters.md) tool to confirm the high CPU usage.</span></span> <span data-ttu-id="f8989-162">然后，它逐步介绍了如何使用[性能分析实用工具 (`dotnet-trace`) 跟踪](dotnet-trace.md)或 Linux `perf` 来收集和查看 CPU 使用率配置文件。</span><span class="sxs-lookup"><span data-stu-id="f8989-162">It then walks you through using [Trace for performance analysis utility (`dotnet-trace`)](dotnet-trace.md) or Linux `perf` to collect and view CPU usage profile.</span></span>

### <a name="debug-deadlock"></a><span data-ttu-id="f8989-163">调试死锁</span><span class="sxs-lookup"><span data-stu-id="f8989-163">Debug deadlock</span></span>

<span data-ttu-id="f8989-164">[教程：调试死锁](debug-deadlock.md)介绍了如何使用 [dotnet-dump](dotnet-dump.md) 工具来调查线程和锁。</span><span class="sxs-lookup"><span data-stu-id="f8989-164">[Tutorial: Debug deadlock](debug-deadlock.md) shows you how to use the [dotnet-dump](dotnet-dump.md) tool to investigate threads and locks.</span></span>

### <a name="debug-a-stackoverflow"></a><span data-ttu-id="f8989-165">调试 StackOverflow</span><span class="sxs-lookup"><span data-stu-id="f8989-165">Debug a StackOverflow</span></span>

<span data-ttu-id="f8989-166">[教程：调试 StackOverflow](debug-stackoverflow.md) 演示了如何在 Linux 上调试 <xref:System.StackOverflowException>。</span><span class="sxs-lookup"><span data-stu-id="f8989-166">[Tutorial: Debug a StackOverflow](debug-stackoverflow.md) demonstrates how to debug a <xref:System.StackOverflowException> on Linux.</span></span>

### <a name="debug-linux-dumps"></a><span data-ttu-id="f8989-167">调试 Linux 转储</span><span class="sxs-lookup"><span data-stu-id="f8989-167">Debug Linux dumps</span></span>

<span data-ttu-id="f8989-168">[调试 Linux 转储](debug-linux-dumps.md)说明了如何收集和分析 Linux 上的转储。</span><span class="sxs-lookup"><span data-stu-id="f8989-168">[Debug Linux dumps](debug-linux-dumps.md) explains how to collect and analyze dumps on Linux.</span></span>

### <a name="measure-performance-using-eventcounters"></a><span data-ttu-id="f8989-169">使用 EventCounters 衡量性能</span><span class="sxs-lookup"><span data-stu-id="f8989-169">Measure performance using EventCounters</span></span>

<span data-ttu-id="f8989-170">[教程：使用 .NET 中的 EventCounters 度量性能](event-counter-perf.md)演示了如何使用 <xref:System.Diagnostics.Tracing.EventCounter> API 来衡量 .NET 应用的性能。</span><span class="sxs-lookup"><span data-stu-id="f8989-170">[Tutorial: Measure performance using EventCounters in .NET](event-counter-perf.md) shows you how to use the <xref:System.Diagnostics.Tracing.EventCounter> API to measure performance in your .NET app.</span></span>
