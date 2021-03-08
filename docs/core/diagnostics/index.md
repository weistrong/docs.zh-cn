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
# <a name="what-diagnostic-tools-are-available-in-net-core"></a>.NET Core 中提供哪些诊断工具？

软件并非始终按预计方式运行，但 .NET Core 具有可帮助用户快速有效地诊断这些问题的工具和 API。

本文可帮助用户查找各种所需的工具。

## <a name="managed-debuggers"></a>托管调试器

借助[托管调试器](managed-debuggers.md)，用户可以与程序进行交互。 暂停、增量执行、检查和恢复操作可让用户深入了解代码的行为。 调试器是诊断易于重现的功能问题的首选。

## <a name="logging-and-tracing"></a>日志记录和跟踪

[日志记录和跟踪](logging-tracing.md)是相关技术。 它们指的是用于创建日志文件的检测代码。 这些文件记录了程序操作的详细信息。 这些细节可用于诊断最复杂的问题。 当与时间戳结合使用时，这些技术在性能调查中也非常有用。

## <a name="metrics"></a>指标

[EventCounters](event-counters.md) 使你可编写指标来识别和监视性能问题。 与跟踪相比，指标产生的性能开销较低，这使指标更适合 always-on 性能监视。 .NET 运行时和库发布了多个[已知 EventCounters](available-counters.md)，你也可以对其进行监视。

## <a name="unit-testing"></a>单元测试

[单元测试](../testing/index.md)是持续集成和部署高质量软件的关键组件。 单元测试的目的在于，在用户操作导致系统出现问题时提前向其发出警告。

## <a name="dumps"></a>转储

[转储](./dumps.md)是一个文件，其中包含创建时进程的快照。 它们可用于检查应用程序的状态，以便进行调试。

## <a name="symbols"></a>符号

[符号](./symbols.md)是源代码和编译器生成的二进制代码之间的映射。 这些通常被 .NET 调试器用来解析源行号、局部变量名称以及其他类型的诊断信息。

## <a name="collect-diagnostics-in-containers"></a>收集容器中的诊断

也可使用非容器化 Linux 环境中使用的相同诊断工具[收集容器中的诊断](diagnostics-in-containers.md)。 只需进行几次使用更改就可使这些工具在 Docker 容器中运行。

## <a name="net-core-diagnostic-global-tools"></a>.NET Core 诊断全局工具

### <a name="dotnet-counters"></a>dotnet-counters

[dotnet-counters](dotnet-counters.md) 是一个性能监视工具，用于初级运行状况监视和性能调查。 它通过 <xref:System.Diagnostics.Tracing.EventCounter> API 观察已发布的性能计数器值。 例如，可以快速监视 CPU 使用情况或 .NET Core 应用程序中的异常率等指标。

### <a name="dotnet-dump"></a>dotnet-dump

通过 [dotnet-dump](dotnet-dump.md) 工具，可在不使用本机调试器的情况下收集和分析 Windows 和 Linux 核心转储。

### <a name="dotnet-gcdump"></a>dotnet-gcdump

[dotnet-gcdump](dotnet-gcdump.md) 工具可用于为活动 .NET 进程收集 GC（垃圾回收器）转储。

### <a name="dotnet-trace"></a>dotnet-trace

分析数据通过 .NET Core 中的 `EventPipe` 公开。 通过 [dotnet-trace](dotnet-trace.md) 工具，可以使用来自应用的有意思的分析数据，这些数据可帮助你分析应用运行缓慢的根本原因。

### <a name="dotnet-symbol"></a>dotnet-symbol

[dotnet-symbol](dotnet-symbol.md) 用于下载打开核心转储或小型转储所需的文件（符号、DAC/DBI、主机文件等）。 如果需要使用符号和模块来调试在其他计算机上捕获的转储文件，请使用此工具。

### <a name="dotnet-sos"></a>dotnet-sos

[dotnet-sos](dotnet-sos.md) 在 Linux 和 macOS（如果使用的是 [Windbg/cdb](/windows-hardware/drivers/debugger/debugger-download-tools)，则在 Windows 上）安装 [SOS调试扩展](sos-debugging-extension.md)。

### <a name="perfcollect"></a>PerfCollect

[PerfCollect](trace-perfcollect-lttng.md) 是一个 bash 脚本，可用于收集包含 `perf` 和 `LTTng` 的跟踪，以便更深入地分析在 Linux 分发版上运行的 .NET 应用的性能。

## <a name="net-core-diagnostics-tutorials"></a>.NET Core 诊断教程

### <a name="debug-a-memory-leak"></a>调试内存泄露

[教程：调试内存泄漏](debug-memory-leak.md)演示了如何查找内存泄漏。 [dotnet-counters](dotnet-counters.md) 工具用于确认泄露，[dotnet-dump](dotnet-dump.md) 工具用于诊断泄露。

### <a name="debug-high-cpu-usage"></a>调试高 CPU 使用率

[教程：调试高 CPU 使用率](debug-highcpu.md)逐步介绍了如何调查高 CPU 使用率。 它使用 [dotnet-counters](dotnet-counters.md) 工具来确认高 CPU 使用率。 然后，它逐步介绍了如何使用[性能分析实用工具 (`dotnet-trace`) 跟踪](dotnet-trace.md)或 Linux `perf` 来收集和查看 CPU 使用率配置文件。

### <a name="debug-deadlock"></a>调试死锁

[教程：调试死锁](debug-deadlock.md)介绍了如何使用 [dotnet-dump](dotnet-dump.md) 工具来调查线程和锁。

### <a name="debug-a-stackoverflow"></a>调试 StackOverflow

[教程：调试 StackOverflow](debug-stackoverflow.md) 演示了如何在 Linux 上调试 <xref:System.StackOverflowException>。

### <a name="debug-linux-dumps"></a>调试 Linux 转储

[调试 Linux 转储](debug-linux-dumps.md)说明了如何收集和分析 Linux 上的转储。

### <a name="measure-performance-using-eventcounters"></a>使用 EventCounters 衡量性能

[教程：使用 .NET 中的 EventCounters 度量性能](event-counter-perf.md)演示了如何使用 <xref:System.Diagnostics.Tracing.EventCounter> API 来衡量 .NET 应用的性能。
