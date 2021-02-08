---
description: 了解更多： CLR 宿主接口
title: CLR 承载接口
ms.date: 03/30/2017
helpviewer_keywords:
- interfaces [.NET Framework hosting], version 2.0
- hosting interfaces [.NET Framework], version 2.0
- .NET Framework 2.0, hosting interfaces
ms.assetid: 703b8381-43db-4a4d-9faa-cca39302d922
ms.openlocfilehash: f42a74698607ffbed4a981f061d13ea4e9d634d8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799897"
---
# <a name="clr-hosting-interfaces"></a><span data-ttu-id="37074-103">CLR 承载接口</span><span class="sxs-lookup"><span data-stu-id="37074-103">CLR Hosting Interfaces</span></span>

<span data-ttu-id="37074-104">本部分介绍了非托管主机可用于将公共语言运行时 (CLR) 集成到其应用程序的接口。</span><span class="sxs-lookup"><span data-stu-id="37074-104">This section describes the interfaces that unmanaged hosts can use to integrate the common language runtime (CLR) into their applications.</span></span> <span data-ttu-id="37074-105">此信息适用于2.0 版及更高版本的 .NET Framework。</span><span class="sxs-lookup"><span data-stu-id="37074-105">The information pertains to the .NET Framework version 2.0 and later versions.</span></span> <span data-ttu-id="37074-106">这些接口使宿主能够控制运行时的更多方面，而不是在版本1.0 和1.1 中提供的，并且在 CLR 与宿主的执行模型之间提供了更紧密的集成。</span><span class="sxs-lookup"><span data-stu-id="37074-106">These interfaces enable the host to control many more aspects of the runtime than was possible in versions 1.0 and 1.1, and provide much tighter integration between the CLR and the host's execution model.</span></span>  
  
 <span data-ttu-id="37074-107">在 .NET Framework 版本1.0 和1.1 中，托管模型启用了一个非托管主机，用于将 CLR 加载到进程中、配置特定设置以及接收事件通知。</span><span class="sxs-lookup"><span data-stu-id="37074-107">In the .NET Framework version 1.0 and 1.1, the hosting model enabled an unmanaged host to load the CLR into a process, to configure certain settings, and to receive event notifications.</span></span> <span data-ttu-id="37074-108">不过，通常情况下，主机和 CLR 在该进程中单独运行。</span><span class="sxs-lookup"><span data-stu-id="37074-108">However, in general, the host and the CLR ran independently in that process.</span></span> <span data-ttu-id="37074-109">在 .NET Framework 版本2.0 及更高版本中，新的抽象层允许宿主提供当前由 Win32 程序集中的类型提供的多个资源，并扩展主机可配置的功能集。</span><span class="sxs-lookup"><span data-stu-id="37074-109">In the .NET Framework version 2.0 and later versions, new layers of abstraction let the host provide many of the resources currently provided by the types in the Win32 assembly, and extend the set of capabilities that the host can configure.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="37074-110">本节内容</span><span class="sxs-lookup"><span data-stu-id="37074-110">In This Section</span></span>  

 [<span data-ttu-id="37074-111">IActionOnCLREvent 接口</span><span class="sxs-lookup"><span data-stu-id="37074-111">IActionOnCLREvent Interface</span></span>](iactiononclrevent-interface.md)  
 <span data-ttu-id="37074-112">提供一个方法，该方法对已注册的事件执行回调。</span><span class="sxs-lookup"><span data-stu-id="37074-112">Provides a method that performs a callback for a registered event.</span></span>  
  
 [<span data-ttu-id="37074-113">IApartmentCallback 接口</span><span class="sxs-lookup"><span data-stu-id="37074-113">IApartmentCallback Interface</span></span>](iapartmentcallback-interface.md)  
 <span data-ttu-id="37074-114">提供用于在单元中进行回调的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-114">Provides methods for making callbacks within an apartment.</span></span>  
  
 [<span data-ttu-id="37074-115">IAppDomainBinding 接口</span><span class="sxs-lookup"><span data-stu-id="37074-115">IAppDomainBinding Interface</span></span>](iappdomainbinding-interface.md)  
 <span data-ttu-id="37074-116">提供设置运行时配置的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-116">Provides methods for setting run-time configuration.</span></span>  
  
 [<span data-ttu-id="37074-117">ICatalogServices 接口</span><span class="sxs-lookup"><span data-stu-id="37074-117">ICatalogServices Interface</span></span>](icatalogservices-interface.md)  
 <span data-ttu-id="37074-118">提供用于编录服务的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-118">Provides methods for cataloging services.</span></span> <span data-ttu-id="37074-119"> (此接口支持 .NET Framework 基础结构，不应在代码中直接使用。 ) </span><span class="sxs-lookup"><span data-stu-id="37074-119">(This interface supports the .NET Framework infrastructure and is not intended to be used directly from your code.)</span></span>  
  
 [<span data-ttu-id="37074-120">ICLRAssemblyIdentityManager 接口</span><span class="sxs-lookup"><span data-stu-id="37074-120">ICLRAssemblyIdentityManager Interface</span></span>](iclrassemblyidentitymanager-interface.md)  
 <span data-ttu-id="37074-121">提供一些方法，这些方法支持宿主与 CLR 之间的有关程序集的通信。</span><span class="sxs-lookup"><span data-stu-id="37074-121">Provides methods that support communication between the host and the CLR about assemblies.</span></span>  
  
 [<span data-ttu-id="37074-122">ICLRAssemblyReferenceList 接口</span><span class="sxs-lookup"><span data-stu-id="37074-122">ICLRAssemblyReferenceList Interface</span></span>](iclrassemblyreferencelist-interface.md)  
 <span data-ttu-id="37074-123">管理由 CLR （而不是由主机）加载的程序集的列表。</span><span class="sxs-lookup"><span data-stu-id="37074-123">Manages a list of assemblies that are loaded by the CLR and not by the host.</span></span>  
  
 [<span data-ttu-id="37074-124">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="37074-124">ICLRControl Interface</span></span>](iclrcontrol-interface.md)  
 <span data-ttu-id="37074-125">为宿主提供方法，以获取和配置 CLR 的各个方面。</span><span class="sxs-lookup"><span data-stu-id="37074-125">Provides methods for the host to gain access to, and configure various aspects of, the CLR.</span></span>  
  
 [<span data-ttu-id="37074-126">ICLRDebugManager 接口</span><span class="sxs-lookup"><span data-stu-id="37074-126">ICLRDebugManager Interface</span></span>](iclrdebugmanager-interface.md)  
 <span data-ttu-id="37074-127">提供使宿主可以将一组任务与标识符和友好名称关联的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-127">Provides methods that enable a host to associate a set of tasks with an identifier and a friendly name.</span></span>  
  
 [<span data-ttu-id="37074-128">ICLRErrorReportingManager 接口</span><span class="sxs-lookup"><span data-stu-id="37074-128">ICLRErrorReportingManager Interface</span></span>](iclrerrorreportingmanager-interface.md)  
 <span data-ttu-id="37074-129">提供使宿主可以配置自定义堆转储以用于错误报告的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-129">Provides methods that enable the host to configure custom heap dumps for error reporting.</span></span>  
  
 [<span data-ttu-id="37074-130">ICLRGCManager 接口</span><span class="sxs-lookup"><span data-stu-id="37074-130">ICLRGCManager Interface</span></span>](iclrgcmanager-interface.md)  
 <span data-ttu-id="37074-131">提供使宿主能够与 CLR 的垃圾回收系统交互的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-131">Provides methods that enable a host to interact with the CLR's garbage collection system.</span></span>  
  
 [<span data-ttu-id="37074-132">ICLRHostBindingPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="37074-132">ICLRHostBindingPolicyManager Interface</span></span>](iclrhostbindingpolicymanager-interface.md)  
 <span data-ttu-id="37074-133">为宿主提供方法，用于计算和传达程序集策略信息中的更改。</span><span class="sxs-lookup"><span data-stu-id="37074-133">Provides methods for the host to evaluate and communicate changes in policy information for assemblies.</span></span>  
  
 [<span data-ttu-id="37074-134">ICLRHostProtectionManager 接口</span><span class="sxs-lookup"><span data-stu-id="37074-134">ICLRHostProtectionManager Interface</span></span>](iclrhostprotectionmanager-interface.md)  
 <span data-ttu-id="37074-135">允许宿主阻止在部分受信任的代码中运行特定的托管类、方法、属性和字段。</span><span class="sxs-lookup"><span data-stu-id="37074-135">Enables the host to block specific managed classes, methods, properties, and fields from running in partially trusted code.</span></span>  
  
 [<span data-ttu-id="37074-136">ICLRIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="37074-136">ICLRIoCompletionManager Interface</span></span>](iclriocompletionmanager-interface.md)  
 <span data-ttu-id="37074-137">实现一个回调方法，该方法使宿主能够向 CLR 通知指定 i/o 请求的状态。</span><span class="sxs-lookup"><span data-stu-id="37074-137">Implements a callback method that enables the host to notify the CLR of the status of specified I/O requests.</span></span>  
  
 [<span data-ttu-id="37074-138">ICLRMemoryNotificationCallback 接口</span><span class="sxs-lookup"><span data-stu-id="37074-138">ICLRMemoryNotificationCallback Interface</span></span>](iclrmemorynotificationcallback-interface.md)  
 <span data-ttu-id="37074-139">允许主机使用类似于 Win32 函数的方法来报告内存压力情况 `CreateMemoryResourceNotification` 。</span><span class="sxs-lookup"><span data-stu-id="37074-139">Enables the host to report memory pressure conditions using an approach similar to that of the Win32 `CreateMemoryResourceNotification` function.</span></span>  
  
 [<span data-ttu-id="37074-140">ICLROnEventManager 接口</span><span class="sxs-lookup"><span data-stu-id="37074-140">ICLROnEventManager Interface</span></span>](iclroneventmanager-interface.md)  
 <span data-ttu-id="37074-141">提供使宿主能够注册和注销 CLR 事件的回调的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-141">Provides methods that enable the host to register and unregister callbacks for CLR events.</span></span>  
  
 [<span data-ttu-id="37074-142">ICLRPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="37074-142">ICLRPolicyManager Interface</span></span>](iclrpolicymanager-interface.md)  
 <span data-ttu-id="37074-143">提供使宿主可以指定在发生故障和超时时要执行的策略操作的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-143">Provides methods that enable the host to specify policy actions to be taken in the event of failures and timeouts.</span></span>  
  
 [<span data-ttu-id="37074-144">ICLRProbingAssemblyEnum 接口</span><span class="sxs-lookup"><span data-stu-id="37074-144">ICLRProbingAssemblyEnum Interface</span></span>](iclrprobingassemblyenum-interface.md)  
 <span data-ttu-id="37074-145">提供使宿主可以通过使用 CLR 内部的程序集的标识信息来获取程序集的探测标识的方法，无需创建或了解该标识。</span><span class="sxs-lookup"><span data-stu-id="37074-145">Provides methods that enable the host to get the probing identities of an assembly by using the assembly's identity information that is internal to the CLR, without needing to create or understand that identity.</span></span>  
  
 [<span data-ttu-id="37074-146">ICLRReferenceAssemblyEnum 接口</span><span class="sxs-lookup"><span data-stu-id="37074-146">ICLRReferenceAssemblyEnum Interface</span></span>](iclrreferenceassemblyenum-interface.md)  
 <span data-ttu-id="37074-147">提供一些方法，这些方法使宿主可以使用 CLR 内部的程序集标识数据来操作由文件或流引用的程序集集，而无需创建或了解这些标识。</span><span class="sxs-lookup"><span data-stu-id="37074-147">Provides methods that enable the host to manipulate the set of assemblies referenced by a file or stream using assembly identity data that is internal to the CLR, without needing to create or understand those identities.</span></span>  
  
 [<span data-ttu-id="37074-148">ICLRRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="37074-148">ICLRRuntimeHost Interface</span></span>](iclrruntimehost-interface.md)  
 <span data-ttu-id="37074-149">提供类似于 [ICorRuntimeHost](icorruntimehost-interface.md)的功能，另外还提供了一个用于设置宿主控件接口的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-149">Provides capabilities similar to [ICorRuntimeHost](icorruntimehost-interface.md), with an additional method to set the host control interface.</span></span>  
  
 [<span data-ttu-id="37074-150">ICLRSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="37074-150">ICLRSyncManager Interface</span></span>](iclrsyncmanager-interface.md)  
 <span data-ttu-id="37074-151">为宿主提供方法，以获取有关请求任务的信息，并在其同步实现中检测死锁。</span><span class="sxs-lookup"><span data-stu-id="37074-151">Provides methods for the host to get information about requested tasks and to detect deadlocks in its synchronization implementation.</span></span>  
  
 [<span data-ttu-id="37074-152">ICLRTask 接口</span><span class="sxs-lookup"><span data-stu-id="37074-152">ICLRTask Interface</span></span>](iclrtask-interface.md)  
 <span data-ttu-id="37074-153">提供一些方法，这些方法使宿主可以发出 CLR 请求，或向 CLR 提供有关关联任务的通知。</span><span class="sxs-lookup"><span data-stu-id="37074-153">Provides methods that enable the host to make requests of the CLR, or to provide notification to the CLR about the associated task.</span></span>  
  
 [<span data-ttu-id="37074-154">ICLRTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="37074-154">ICLRTaskManager Interface</span></span>](iclrtaskmanager-interface.md)  
 <span data-ttu-id="37074-155">提供使宿主能够显式请求 CLR 创建新任务、获取当前正在执行的任务以及设置任务的地理语言和区域性的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-155">Provides methods that enable the host to request explicitly that the CLR create a new task, get the currently executing task, and set the geographic language and culture for the task.</span></span>  
  
 [<span data-ttu-id="37074-156">ICLRValidator 接口</span><span class="sxs-lookup"><span data-stu-id="37074-156">ICLRValidator Interface</span></span>](iclrvalidator-interface.md)  
 <span data-ttu-id="37074-157">提供用于验证 (PE) 映像和报告验证错误的可移植可执行文件的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-157">Provides methods for validating portable executable (PE) images and reporting validation errors.</span></span>  
  
 [<span data-ttu-id="37074-158">ICorConfiguration 接口</span><span class="sxs-lookup"><span data-stu-id="37074-158">ICorConfiguration Interface</span></span>](icorconfiguration-interface.md)  
 <span data-ttu-id="37074-159">提供配置 CLR 的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-159">Provides methods for configuring the CLR.</span></span>  
  
 [<span data-ttu-id="37074-160">ICorThreadpool 接口</span><span class="sxs-lookup"><span data-stu-id="37074-160">ICorThreadpool Interface</span></span>](icorthreadpool-interface.md)  
 <span data-ttu-id="37074-161">提供用于访问线程池的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-161">Provides methods for accessing the thread pool.</span></span>  
  
 [<span data-ttu-id="37074-162">IDebuggerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="37074-162">IDebuggerInfo Interface</span></span>](idebuggerinfo-interface.md)  
 <span data-ttu-id="37074-163">提供用于获取有关调试服务状态的信息的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-163">Provides methods for obtaining information about the state of the debugging services.</span></span>  
  
 [<span data-ttu-id="37074-164">IDebuggerThreadControl 接口</span><span class="sxs-lookup"><span data-stu-id="37074-164">IDebuggerThreadControl Interface</span></span>](idebuggerthreadcontrol-interface.md)  
 <span data-ttu-id="37074-165">提供一些方法，用于通知宿主调试服务阻止和取消阻止线程。</span><span class="sxs-lookup"><span data-stu-id="37074-165">Provides methods for notifying the host about the blocking and unblocking of threads by the debugging services.</span></span>  
  
 [<span data-ttu-id="37074-166">IGCHost 接口</span><span class="sxs-lookup"><span data-stu-id="37074-166">IGCHost Interface</span></span>](igchost-interface.md)  
 <span data-ttu-id="37074-167">提供一些方法，用于获取有关垃圾回收系统的信息并控制垃圾回收的某些方面。</span><span class="sxs-lookup"><span data-stu-id="37074-167">Provides methods for obtaining information about the garbage collection system and for controlling some aspects of garbage collection.</span></span>  
  
 [<span data-ttu-id="37074-168">IGCHost2 接口</span><span class="sxs-lookup"><span data-stu-id="37074-168">IGCHost2 Interface</span></span>](igchost2-interface.md)  
 <span data-ttu-id="37074-169">提供 [SetGCStartupLimitsEx](igchost2-setgcstartuplimitsex-method.md) 方法，该方法使宿主可以将垃圾回收段的大小和垃圾回收系统的代零的最大大小设置为大于的值 `DWORD` 。</span><span class="sxs-lookup"><span data-stu-id="37074-169">Provides the [SetGCStartupLimitsEx](igchost2-setgcstartuplimitsex-method.md) method that enables a host to set the size of the garbage collection segment and the maximum size of the garbage collection system's generation zero to values greater than `DWORD`.</span></span>  
  
 [<span data-ttu-id="37074-170">IGCHostControl 接口</span><span class="sxs-lookup"><span data-stu-id="37074-170">IGCHostControl Interface</span></span>](igchostcontrol-interface.md)  
 <span data-ttu-id="37074-171">提供一个方法，该方法使垃圾回收器能够请求宿主更改虚拟内存的限制。</span><span class="sxs-lookup"><span data-stu-id="37074-171">Provides a method that enables the garbage collector to request the host to change the limits of virtual memory.</span></span>  
  
 [<span data-ttu-id="37074-172">IGCThreadControl 接口</span><span class="sxs-lookup"><span data-stu-id="37074-172">IGCThreadControl Interface</span></span>](igcthreadcontrol-interface.md)  
 <span data-ttu-id="37074-173">提供一些方法，这些方法用于参与要阻止垃圾回收的线程的计划。</span><span class="sxs-lookup"><span data-stu-id="37074-173">Provides methods for participating in the scheduling of threads that would otherwise be blocked for garbage collection.</span></span>  
  
 [<span data-ttu-id="37074-174">IHostAssemblyManager 接口</span><span class="sxs-lookup"><span data-stu-id="37074-174">IHostAssemblyManager Interface</span></span>](ihostassemblymanager-interface.md)  
 <span data-ttu-id="37074-175">提供使宿主可以指定应由 CLR 或由主机加载的程序集的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-175">Provides methods that enable a host to specify sets of assemblies that should be loaded by the CLR or by the host.</span></span>  
  
 [<span data-ttu-id="37074-176">IHostAssemblyStore 接口</span><span class="sxs-lookup"><span data-stu-id="37074-176">IHostAssemblyStore Interface</span></span>](ihostassemblystore-interface.md)  
 <span data-ttu-id="37074-177">提供使宿主可以独立于 CLR 加载程序集和模块的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-177">Provides methods that enable a host to load assemblies and modules independently of the CLR.</span></span>  
  
 [<span data-ttu-id="37074-178">IHostAutoEvent 接口</span><span class="sxs-lookup"><span data-stu-id="37074-178">IHostAutoEvent Interface</span></span>](ihostautoevent-interface.md)  
 <span data-ttu-id="37074-179">提供宿主实现的自动重置事件的表示形式。</span><span class="sxs-lookup"><span data-stu-id="37074-179">Provides a representation of an auto-reset event implemented by the host.</span></span>  
  
 [<span data-ttu-id="37074-180">IHostControl 接口</span><span class="sxs-lookup"><span data-stu-id="37074-180">IHostControl Interface</span></span>](ihostcontrol-interface.md)  
 <span data-ttu-id="37074-181">提供用于配置程序集加载和确定宿主支持哪些宿主接口的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-181">Provides methods for configuring the loading of assemblies, and for determining which hosting interfaces the host supports.</span></span>  
  
 [<span data-ttu-id="37074-182">IHostCrst 接口</span><span class="sxs-lookup"><span data-stu-id="37074-182">IHostCrst Interface</span></span>](ihostcrst-interface.md)  
 <span data-ttu-id="37074-183">用作线程的关键部分的宿主表示形式。</span><span class="sxs-lookup"><span data-stu-id="37074-183">Serves as the host's representation of a critical section for threading.</span></span>  
  
 [<span data-ttu-id="37074-184">IHostGCManager 接口</span><span class="sxs-lookup"><span data-stu-id="37074-184">IHostGCManager Interface</span></span>](ihostgcmanager-interface.md)  
 <span data-ttu-id="37074-185">提供一些方法，这些方法可向宿主通知 CLR 实现的垃圾回收机制中的事件。</span><span class="sxs-lookup"><span data-stu-id="37074-185">Provides methods that notify the host of events in the garbage collection mechanism implemented by the CLR.</span></span>  
  
 [<span data-ttu-id="37074-186">IHostIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="37074-186">IHostIoCompletionManager Interface</span></span>](ihostiocompletionmanager-interface.md)  
 <span data-ttu-id="37074-187">提供使 CLR 能够与主机提供的 i/o 完成端口进行交互的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-187">Provides methods that enable the CLR to interact with I/O completion ports provided by the host.</span></span>  
  
 [<span data-ttu-id="37074-188">IHostMalloc 接口</span><span class="sxs-lookup"><span data-stu-id="37074-188">IHostMalloc Interface</span></span>](ihostmalloc-interface.md)  
 <span data-ttu-id="37074-189">为 CLR 提供一些方法，用于通过宿主请求从堆中进行细粒度分配。</span><span class="sxs-lookup"><span data-stu-id="37074-189">Provides methods for the CLR to request fine-grained allocations from the heap through the host.</span></span>  
  
 [<span data-ttu-id="37074-190">IHostManualEvent 接口</span><span class="sxs-lookup"><span data-stu-id="37074-190">IHostManualEvent Interface</span></span>](ihostmanualevent-interface.md)  
 <span data-ttu-id="37074-191">提供宿主手动重置事件表示形式的实现。</span><span class="sxs-lookup"><span data-stu-id="37074-191">Provides the host's implementation of a representation of a manual reset event.</span></span>  
  
 [<span data-ttu-id="37074-192">IHostMemoryManager 接口</span><span class="sxs-lookup"><span data-stu-id="37074-192">IHostMemoryManager Interface</span></span>](ihostmemorymanager-interface.md)  
 <span data-ttu-id="37074-193">为 CLR 提供一些方法，用于通过主机进行虚拟内存请求，而不是使用标准 Win32 虚拟内存函数。</span><span class="sxs-lookup"><span data-stu-id="37074-193">Provides methods for the CLR to make virtual memory requests through the host, instead of using the standard Win32 virtual memory functions.</span></span>  
  
 [<span data-ttu-id="37074-194">IHostPolicyManager 接口</span><span class="sxs-lookup"><span data-stu-id="37074-194">IHostPolicyManager Interface</span></span>](ihostpolicymanager-interface.md)  
 <span data-ttu-id="37074-195">提供一些方法，这些方法在发生中止、超时或失败时通知 CLR 执行的操作。</span><span class="sxs-lookup"><span data-stu-id="37074-195">Provides methods that notify the host of the actions the CLR performs in case of aborts, timeouts, or failures.</span></span>  
  
 [<span data-ttu-id="37074-196">IHostSecurityContext 接口</span><span class="sxs-lookup"><span data-stu-id="37074-196">IHostSecurityContext Interface</span></span>](ihostsecuritycontext-interface.md)  
 <span data-ttu-id="37074-197">使 CLR 能够维护宿主实现的安全上下文信息。</span><span class="sxs-lookup"><span data-stu-id="37074-197">Enables the CLR to maintain security context information implemented by the host.</span></span>  
  
 [<span data-ttu-id="37074-198">IHostSecurityManager 接口</span><span class="sxs-lookup"><span data-stu-id="37074-198">IHostSecurityManager Interface</span></span>](ihostsecuritymanager-interface.md)  
 <span data-ttu-id="37074-199">提供允许访问和控制当前正在执行的线程的安全上下文的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-199">Provides methods that enable access to, and control over, the security context of the currently executing thread.</span></span>  
  
 [<span data-ttu-id="37074-200">IHostSemaphore 接口</span><span class="sxs-lookup"><span data-stu-id="37074-200">IHostSemaphore Interface</span></span>](ihostsemaphore-interface.md)  
 <span data-ttu-id="37074-201">提供由主机实现的信号量的表示形式。</span><span class="sxs-lookup"><span data-stu-id="37074-201">Provides a representation of a semaphore implemented by the host.</span></span>  
  
 [<span data-ttu-id="37074-202">IHostSyncManager 接口</span><span class="sxs-lookup"><span data-stu-id="37074-202">IHostSyncManager Interface</span></span>](ihostsyncmanager-interface.md)  
 <span data-ttu-id="37074-203">为 CLR 提供方法，以通过调用主机而不是使用 Win32 同步函数来创建同步基元。</span><span class="sxs-lookup"><span data-stu-id="37074-203">Provides methods for the CLR to create synchronization primitives by calling the host, instead of using the Win32 synchronization functions.</span></span>  
  
 [<span data-ttu-id="37074-204">IHostTask 接口</span><span class="sxs-lookup"><span data-stu-id="37074-204">IHostTask Interface</span></span>](ihosttask-interface.md)  
 <span data-ttu-id="37074-205">提供使 CLR 能够与宿主通信以管理任务的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-205">Provides methods that enable the CLR to communicate with the host to manage tasks.</span></span>  
  
 [<span data-ttu-id="37074-206">IHostTaskManager 接口</span><span class="sxs-lookup"><span data-stu-id="37074-206">IHostTaskManager Interface</span></span>](ihosttaskmanager-interface.md)  
 <span data-ttu-id="37074-207">提供一些方法，使 CLR 可以通过主机使用任务，而不是使用标准的操作系统线程或纤程函数。</span><span class="sxs-lookup"><span data-stu-id="37074-207">Provides methods that enable the CLR to work with tasks through the host instead of using the standard operating system threading or fiber functions.</span></span>  
  
 [<span data-ttu-id="37074-208">IHostThreadPoolManager 接口</span><span class="sxs-lookup"><span data-stu-id="37074-208">IHostThreadPoolManager Interface</span></span>](ihostthreadpoolmanager-interface.md)  
 <span data-ttu-id="37074-209">为 CLR 提供方法来配置线程池并将工作项排队到线程池。</span><span class="sxs-lookup"><span data-stu-id="37074-209">Provides methods for the CLR to configure the thread pool and to queue work items to the thread pool.</span></span>  
  
 [<span data-ttu-id="37074-210">IManagedObject 接口</span><span class="sxs-lookup"><span data-stu-id="37074-210">IManagedObject Interface</span></span>](imanagedobject-interface.md)  
 <span data-ttu-id="37074-211">提供用于控制托管对象的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-211">Provides methods for controlling a managed object.</span></span>  
  
 <span data-ttu-id="37074-212">IObjectHandle</span><span class="sxs-lookup"><span data-stu-id="37074-212">"IObjectHandle"</span></span>  
 <span data-ttu-id="37074-213">提供了一种方法，用于从间接寻址解包按值封送对象。</span><span class="sxs-lookup"><span data-stu-id="37074-213">Provides a method for unwrapping marshal-by-value objects from indirection.</span></span>  
  
 [<span data-ttu-id="37074-214">ITypeName 接口</span><span class="sxs-lookup"><span data-stu-id="37074-214">ITypeName Interface</span></span>](itypename-interface.md)  
 <span data-ttu-id="37074-215">提供用于获取类型名称信息的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-215">Provides methods for obtaining type name information.</span></span> <span data-ttu-id="37074-216"> (此接口支持 .NET Framework 基础结构，不应在代码中直接使用。 ) </span><span class="sxs-lookup"><span data-stu-id="37074-216">(This interface supports the .NET Framework infrastructure and is not intended to be used directly from your code.)</span></span>  
  
 [<span data-ttu-id="37074-217">ITypeNameBuilder 接口</span><span class="sxs-lookup"><span data-stu-id="37074-217">ITypeNameBuilder Interface</span></span>](itypenamebuilder-interface.md)  
 <span data-ttu-id="37074-218">提供用于生成类型名称的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-218">Provides methods for building a type name.</span></span> <span data-ttu-id="37074-219"> (此接口支持 .NET Framework 基础结构，不应在代码中直接使用。 ) </span><span class="sxs-lookup"><span data-stu-id="37074-219">(This interface supports the .NET Framework infrastructure and is not intended to be used directly from your code.)</span></span>  
  
 [<span data-ttu-id="37074-220">ITypeNameFactory 接口</span><span class="sxs-lookup"><span data-stu-id="37074-220">ITypeNameFactory Interface</span></span>](itypenamefactory-interface.md)  
 <span data-ttu-id="37074-221">提供用于析构类型名称的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-221">Provides methods for deconstructing a type name.</span></span> <span data-ttu-id="37074-222"> (此接口支持 .NET Framework 基础结构，不应在代码中直接使用。 ) </span><span class="sxs-lookup"><span data-stu-id="37074-222">(This interface supports the .NET Framework infrastructure and is not intended to be used directly from your code.)</span></span>  
  
 <span data-ttu-id="37074-223">IValidator</span><span class="sxs-lookup"><span data-stu-id="37074-223">"IValidator"</span></span>  
 <span data-ttu-id="37074-224">提供用于验证 (PE) 映像和报告验证错误的可移植可执行文件的方法。</span><span class="sxs-lookup"><span data-stu-id="37074-224">Provides methods for validating portable executable (PE) images and reporting validation errors.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="37074-225">相关章节</span><span class="sxs-lookup"><span data-stu-id="37074-225">Related Sections</span></span>  

 [<span data-ttu-id="37074-226">弃用的 CLR 承载接口和 Coclass</span><span class="sxs-lookup"><span data-stu-id="37074-226">Deprecated CLR Hosting Interfaces and Coclasses</span></span>](deprecated-clr-hosting-interfaces-and-coclasses.md)  
 <span data-ttu-id="37074-227">包含描述 .NET Framework 版本1.0 和1.1 中提供的托管接口的主题。</span><span class="sxs-lookup"><span data-stu-id="37074-227">Contains topics that describe the hosting interfaces provided in the .NET Framework version 1.0 and 1.1.</span></span>  
  
 [<span data-ttu-id="37074-228">.NET Framework 4 和 4.5 中添加的 CLR 承载接口</span><span class="sxs-lookup"><span data-stu-id="37074-228">CLR Hosting Interfaces Added in the .NET Framework 4 and 4.5</span></span>](clr-hosting-interfaces-added-in-the-net-framework-4-and-4-5.md)  
 <span data-ttu-id="37074-229">包含描述 .NET Framework 4 中提供的宿主接口的主题。</span><span class="sxs-lookup"><span data-stu-id="37074-229">Contains topics that describe the hosting interfaces provided in the .NET Framework 4.</span></span>
