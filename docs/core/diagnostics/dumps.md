---
title: 转储 - .NET
description: 介绍 .NET 中的转储。
ms.date: 10/12/2020
ms.openlocfilehash: 7a4c7bf54b3e9ea43e685eafbd00b4a373326520
ms.sourcegitcommit: c0b803bffaf101e12f071faf94ca21b46d04ff30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/24/2020
ms.locfileid: "97764937"
---
# <a name="dumps"></a><span data-ttu-id="bd517-103">转储</span><span class="sxs-lookup"><span data-stu-id="bd517-103">Dumps</span></span>

<span data-ttu-id="bd517-104">转储是一种文件，其中包含创建进程时该进程的快照，可用于检查应用程序的状态。</span><span class="sxs-lookup"><span data-stu-id="bd517-104">A dump is a file that contains a snapshot of the process at the time it was created and can be useful for examining the state of your application.</span></span> <span data-ttu-id="bd517-105">当很难将调试程序附加到 .NET 应用程序（如生产或 CI 环境）时，可使用转储来调试该应用程序。</span><span class="sxs-lookup"><span data-stu-id="bd517-105">Dumps can be used to debug your .NET application when it is difficult to attach a debugger to it such as production or CI environments.</span></span> <span data-ttu-id="bd517-106">使用转储可以捕获有问题进程的状态，并且可以直接检查状态而无需停止应用程序。</span><span class="sxs-lookup"><span data-stu-id="bd517-106">Using dumps allows you to capture the state of the problematic process and examine it without having to stop the application.</span></span>

## <a name="collect-dumps"></a><span data-ttu-id="bd517-107">收集转储</span><span class="sxs-lookup"><span data-stu-id="bd517-107">Collect dumps</span></span>

<span data-ttu-id="bd517-108">可以通过多种方式收集转储，具体取决于运行应用的平台。</span><span class="sxs-lookup"><span data-stu-id="bd517-108">Dumps can be collected in a variety of ways depending on which platform you are running your app on.</span></span>

> [!NOTE]
> <span data-ttu-id="bd517-109">在容器内收集转储需要 PTRACE 功能，可通过 `--cap-add=SYS_PTRACE` 或 `--privileged` 添加该功能。</span><span class="sxs-lookup"><span data-stu-id="bd517-109">Collecting a dump inside a container requires PTRACE capability, which can be added via `--cap-add=SYS_PTRACE` or `--privileged`.</span></span>

> [!NOTE]
> <span data-ttu-id="bd517-110">转储可能包含敏感信息，因为它们可以包含正在运行进程的全部内存。</span><span class="sxs-lookup"><span data-stu-id="bd517-110">Dumps may contain sensitive information because they can contain the full memory of the running process.</span></span> <span data-ttu-id="bd517-111">处理它们时请考虑所有安全限制和指导。</span><span class="sxs-lookup"><span data-stu-id="bd517-111">Handle them with any security restrictions and guidances in mind.</span></span>

### <a name="collecting-dumps-on-crash"></a><span data-ttu-id="bd517-112">在发生故障时收集转储</span><span class="sxs-lookup"><span data-stu-id="bd517-112">Collecting dumps on crash</span></span>

<span data-ttu-id="bd517-113">可以使用环境变量将应用程序配置为在发生故障时收集转储。</span><span class="sxs-lookup"><span data-stu-id="bd517-113">You can use environment variables to configure your application to collect a dump upon a crash.</span></span> <span data-ttu-id="bd517-114">如果想要了解故障原因，这将很有帮助。</span><span class="sxs-lookup"><span data-stu-id="bd517-114">This is helpful when you want to get an understanding of why a crash happened.</span></span> <span data-ttu-id="bd517-115">例如，在引发异常时捕获转储有助于通过在应用发生故障时检查应用状态来确定问题。</span><span class="sxs-lookup"><span data-stu-id="bd517-115">For example, capturing a dump when an exception is thrown helps you identify an issue by examining the state of the app when it crashed.</span></span>

<span data-ttu-id="bd517-116">下表显示了可用于将应用程序配置为在发生故障时收集转储的环境变量。</span><span class="sxs-lookup"><span data-stu-id="bd517-116">The following table shows the environment variables you can configure for collecting dumps on a crash.</span></span>

|<span data-ttu-id="bd517-117">环境变量</span><span class="sxs-lookup"><span data-stu-id="bd517-117">Environment variable</span></span>|<span data-ttu-id="bd517-118">说明</span><span class="sxs-lookup"><span data-stu-id="bd517-118">Description</span></span>|<span data-ttu-id="bd517-119">默认值</span><span class="sxs-lookup"><span data-stu-id="bd517-119">Default value</span></span>|
|-------|---------|---|
|`COMPlus_DbgEnableMiniDump`|<span data-ttu-id="bd517-120">如果设置为 1，则启用核心转储生成。</span><span class="sxs-lookup"><span data-stu-id="bd517-120">If set to 1, enable core dump generation.</span></span>|<span data-ttu-id="bd517-121">0</span><span class="sxs-lookup"><span data-stu-id="bd517-121">0</span></span>|
|`COMPlus_DbgMiniDumpType`|<span data-ttu-id="bd517-122">要收集的转储类型。</span><span class="sxs-lookup"><span data-stu-id="bd517-122">Type of dump to be collected.</span></span> <span data-ttu-id="bd517-123">有关详细信息，请参阅下表</span><span class="sxs-lookup"><span data-stu-id="bd517-123">For more information, see the table below</span></span>|<span data-ttu-id="bd517-124">2 (`MiniDumpWithPrivateReadWriteMemory`)</span><span class="sxs-lookup"><span data-stu-id="bd517-124">2 (`MiniDumpWithPrivateReadWriteMemory`)</span></span>|
|`COMPlus_DbgMiniDumpName`|<span data-ttu-id="bd517-125">写入转储的文件路径。</span><span class="sxs-lookup"><span data-stu-id="bd517-125">Path to a file to write the dump to.</span></span>|`/tmp/coredump.<pid>`|
|`COMPlus_CreateDumpDiagnostics`|<span data-ttu-id="bd517-126">如果设置为 1，则启用转储进程的诊断日志记录。</span><span class="sxs-lookup"><span data-stu-id="bd517-126">If set to 1, enable diagnostic logging of dump process.</span></span>|<span data-ttu-id="bd517-127">0</span><span class="sxs-lookup"><span data-stu-id="bd517-127">0</span></span>|

<span data-ttu-id="bd517-128">下表显示了可用于 `COMPlus_DbgMiniDumpType`（可指定为值）的所有选项。</span><span class="sxs-lookup"><span data-stu-id="bd517-128">The table below shows all the options you may use for `COMPlus_DbgMiniDumpType` which can be specified as a value.</span></span> <span data-ttu-id="bd517-129">例如，将 `COMPlus_DbgMiniDumpType` 设置为 1 意味着在发生故障时将收集 `MiniDumpNormal` 类型的转储。</span><span class="sxs-lookup"><span data-stu-id="bd517-129">For example, setting `COMPlus_DbgMiniDumpType` to 1 means `MiniDumpNormal` type dump will be collected on a crash.</span></span>

|<span data-ttu-id="bd517-130">值</span><span class="sxs-lookup"><span data-stu-id="bd517-130">Value</span></span>|<span data-ttu-id="bd517-131">名称</span><span class="sxs-lookup"><span data-stu-id="bd517-131">Name</span></span>|<span data-ttu-id="bd517-132">描述</span><span class="sxs-lookup"><span data-stu-id="bd517-132">Description</span></span>|
|-----|----|-----------|
|<span data-ttu-id="bd517-133">1</span><span class="sxs-lookup"><span data-stu-id="bd517-133">1</span></span>|`MiniDumpNormal`|<span data-ttu-id="bd517-134">只包含为进程中的所有现有线程捕获堆栈跟踪所需的信息。</span><span class="sxs-lookup"><span data-stu-id="bd517-134">Include just the information necessary to capture stack traces for all existing threads in a process.</span></span> <span data-ttu-id="bd517-135">有限的 GC 堆内存和信息。</span><span class="sxs-lookup"><span data-stu-id="bd517-135">Limited GC heap memory and information.</span></span>|
|<span data-ttu-id="bd517-136">2</span><span class="sxs-lookup"><span data-stu-id="bd517-136">2</span></span>|`MiniDumpWithPrivateReadWriteMemory`|<span data-ttu-id="bd517-137">包含 GC 堆以及为进程中的所有现有线程捕获堆栈跟踪所需的信息。</span><span class="sxs-lookup"><span data-stu-id="bd517-137">Includes the GC heaps and information necessary to capture stack traces for all existing threads in a process.</span></span>|
|<span data-ttu-id="bd517-138">3</span><span class="sxs-lookup"><span data-stu-id="bd517-138">3</span></span>|`MiniDumpFilterTriage`|<span data-ttu-id="bd517-139">只包含为进程中的所有现有线程捕获堆栈跟踪所需的信息。</span><span class="sxs-lookup"><span data-stu-id="bd517-139">Include just the information necessary to capture stack traces for all existing threads in a process.</span></span> <span data-ttu-id="bd517-140">有限的 GC 堆内存和信息。</span><span class="sxs-lookup"><span data-stu-id="bd517-140">Limited GC heap memory and information.</span></span>|
|<span data-ttu-id="bd517-141">4</span><span class="sxs-lookup"><span data-stu-id="bd517-141">4</span></span>|`MiniDumpWithFullMemory`|<span data-ttu-id="bd517-142">包含进程中的所有可访问内存。</span><span class="sxs-lookup"><span data-stu-id="bd517-142">Include all accessible memory in the process.</span></span> <span data-ttu-id="bd517-143">原始内存数据包含在末尾，因此无需原始内存信息即可直接映射初始结构。</span><span class="sxs-lookup"><span data-stu-id="bd517-143">The raw memory data is included at the end, so that the initial structures can be mapped directly without the raw memory information.</span></span> <span data-ttu-id="bd517-144">此选项可能会导致文件非常大。</span><span class="sxs-lookup"><span data-stu-id="bd517-144">This option can result in a very large file.</span></span>|

### <a name="collecting-dumps-at-specific-point-in-time"></a><span data-ttu-id="bd517-145">在特定时间点收集转储</span><span class="sxs-lookup"><span data-stu-id="bd517-145">Collecting dumps at specific point in time</span></span>

<span data-ttu-id="bd517-146">你可能需要在应用尚未发生故障时收集转储。</span><span class="sxs-lookup"><span data-stu-id="bd517-146">You may want to collect a dump when the app hasn't crashed yet.</span></span> <span data-ttu-id="bd517-147">例如，如果想要检查似乎处于死锁状态的应用程序的状态，则配置环境变量以在发生故障时收集转储将不起作用，因为应用仍在运行。</span><span class="sxs-lookup"><span data-stu-id="bd517-147">For example, if you want to examine the state of an application that seems to be in a deadlock, configuring the environment variables to collect dumps on crash will not be helpful because the app is still running.</span></span>

<span data-ttu-id="bd517-148">若要在自己的请求时收集转储，可以使用 `dotnet-dump`，这是一种用于收集和分析转储的 CLI 工具。</span><span class="sxs-lookup"><span data-stu-id="bd517-148">To collect dump at your own request, you can use `dotnet-dump`, which is a CLI tool for collecting and analyzing dumps.</span></span> <span data-ttu-id="bd517-149">若要详细了解如何使用 `dotnet-dump` 来收集转储，请参阅[转储收集和分析实用工具](dotnet-dump.md)。</span><span class="sxs-lookup"><span data-stu-id="bd517-149">For more information on how to use it to collect dumps with `dotnet-dump`, see [Dump collection and analysis utility](dotnet-dump.md).</span></span>

## <a name="analyze-dumps"></a><span data-ttu-id="bd517-150">分析转储</span><span class="sxs-lookup"><span data-stu-id="bd517-150">Analyze dumps</span></span>

<span data-ttu-id="bd517-151">可以使用 [`dotnet-dump`](dotnet-dump.md) CLI 工具或 [Visual Studio](https://docs.microsoft.com/visualstudio/debugger/using-dump-files) 分析转储。</span><span class="sxs-lookup"><span data-stu-id="bd517-151">You can anlayze dumps using the [`dotnet-dump`](dotnet-dump.md) CLI tool or with [Visual Studio](https://docs.microsoft.com/visualstudio/debugger/using-dump-files).</span></span>

> [!NOTE]
> <span data-ttu-id="bd517-152">Visual Studio 16.8 及更高版本允许[打开在 .NET Core 3.1.7 或更高版本上生成的 Linux 转储](https://devblogs.microsoft.com/visualstudio/linux-managed-memory-dump-debugging/)。</span><span class="sxs-lookup"><span data-stu-id="bd517-152">Visual Studio version 16.8 and later allows you to [open Linux dumps](https://devblogs.microsoft.com/visualstudio/linux-managed-memory-dump-debugging/) generated on .NET Core 3.1.7 or later.</span></span>  

> [!NOTE]
> <span data-ttu-id="bd517-153">如果需要进行原生调试，则可以对 [Linux 和 macOS 上的 LLDB](debug-linux-dumps.md#analyze-dumps-on-linux) 使用 [SOS 调试器扩展](sos-debugging-extension.md)。</span><span class="sxs-lookup"><span data-stu-id="bd517-153">If native debugging is necessary, the [SOS debugger extension](sos-debugging-extension.md) can be used with [LLDB on Linux and macOS](debug-linux-dumps.md#analyze-dumps-on-linux).</span></span> <span data-ttu-id="bd517-154">尽管建议使用 Visual Studio，但 Windows 上的 [Windbg/cdb](/windows-hardware/drivers/debugger/debugger-download-tools) 也支持 SOS。</span><span class="sxs-lookup"><span data-stu-id="bd517-154">SOS is also supported with [Windbg/cdb](/windows-hardware/drivers/debugger/debugger-download-tools) on Windows, although Visual Studio is recommended.</span></span>

## <a name="see-also"></a><span data-ttu-id="bd517-155">请参阅</span><span class="sxs-lookup"><span data-stu-id="bd517-155">See also</span></span>

<span data-ttu-id="bd517-156">详细了解如何利用转储来帮助诊断 .NET 应用程序中的问题。</span><span class="sxs-lookup"><span data-stu-id="bd517-156">Learn more about how you can leverage dumps to help diagnosing problems in your .NET application.</span></span>

* <span data-ttu-id="bd517-157">[调试 Linux 转储](debug-linux-dumps.md)这一教程分步演示了如何调试在 Linux 中收集的转储。</span><span class="sxs-lookup"><span data-stu-id="bd517-157">[Debug Linux dumps](debug-linux-dumps.md) tutorial walks you through how to debug a dump that was collected in Linux.</span></span>

* <span data-ttu-id="bd517-158">[调试死锁](debug-deadlock.md)这一教程分步演示了如何使用转储来调试 .NET 应用程序中的死锁。</span><span class="sxs-lookup"><span data-stu-id="bd517-158">[Debug deadlock](debug-deadlock.md) tutorial walks you through how to debug a deadlock in your .NET application using dumps.</span></span>
