---
description: 了解详细信息： STARTUP_FLAGS 枚举
title: STARTUP_FLAGS 枚举
ms.date: 03/30/2017
api_name:
- STARTUP_FLAGS
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- STARTUP_FLAGS
helpviewer_keywords:
- STARTUP_FLAGS enumeration [.NET Framework hosting]
ms.assetid: 4f043594-0c45-4bc6-988e-a6793f0d8d06
topic_type:
- apiref
ms.openlocfilehash: 2136f1c43545342f2cdc7cde884999a2f2c11bdd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99679311"
---
# <a name="startup_flags-enumeration"></a><span data-ttu-id="f0af4-103">STARTUP_FLAGS 枚举</span><span class="sxs-lookup"><span data-stu-id="f0af4-103">STARTUP_FLAGS Enumeration</span></span>

<span data-ttu-id="f0af4-104">包含指示公共语言运行时 (CLR) 的启动行为的值。</span><span class="sxs-lookup"><span data-stu-id="f0af4-104">Contains values that indicate the startup behavior of the common language runtime (CLR).</span></span> <span data-ttu-id="f0af4-105">默认情况下，垃圾回收不是并发的，并且仅将基类库加载到非特定于域的区域。</span><span class="sxs-lookup"><span data-stu-id="f0af4-105">By default, garbage collection is non-concurrent, and only the base class library is loaded into the domain-neutral area.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f0af4-106">语法</span><span class="sxs-lookup"><span data-stu-id="f0af4-106">Syntax</span></span>  
  
```cpp  
typedef enum {  
    STARTUP_CONCURRENT_GC                         = 0x1,  
    STARTUP_LOADER_OPTIMIZATION_MASK              = 0x3<<1,  
    STARTUP_LOADER_OPTIMIZATION_SINGLE_DOMAIN     = 0x1<<1,  
    STARTUP_LOADER_OPTIMIZATION_MULTI_DOMAIN      = 0x2<<1,  
    STARTUP_LOADER_OPTIMIZATION_MULTI_DOMAIN_HOST = 0x3<<1,  
  
    STARTUP_LOADER_SAFEMODE                       = 0x10,  
    STARTUP_LOADER_SETPREFERENCE                  = 0x100,  
  
    STARTUP_SERVER_GC                             = 0x1000,  
    STARTUP_HOARD_GC_VM                           = 0x2000,  
  
    STARTUP_SINGLE_VERSION_HOSTING_INTERFACE      = 0x4000,  
    STARTUP_LEGACY_IMPERSONATION                  = 0x10000,  
    STARTUP_DISABLE_COMMITTHREADSTACK             = 0x20000,  
    STARTUP_ALWAYSFLOW_IMPERSONATION              = 0x40000,  
    STARTUP_TRIM_GC_COMMIT                        = 0x80000,  
  
    STARTUP_ETW                                   = 0x100000,  
    STARTUP_ARM                                   = 0x400000  
} STARTUP_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="f0af4-107">成员</span><span class="sxs-lookup"><span data-stu-id="f0af4-107">Members</span></span>  
  
|<span data-ttu-id="f0af4-108">成员</span><span class="sxs-lookup"><span data-stu-id="f0af4-108">Member</span></span>|<span data-ttu-id="f0af4-109">说明</span><span class="sxs-lookup"><span data-stu-id="f0af4-109">Description</span></span>|  
|------------|-----------------|  
|`STARTUP_CONCURRENT_GC`|<span data-ttu-id="f0af4-110">指定应使用并发垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="f0af4-110">Specifies that concurrent garbage collection should be used.</span></span> <span data-ttu-id="f0af4-111">如果调用方请求单处理器计算机上的服务器生成和并发垃圾回收，则会改为运行工作站构建和非并发垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="f0af4-111">If the caller asks for the server build and concurrent garbage collection on a single-processor machine, the workstation build and non-concurrent garbage collection are run instead.</span></span> <span data-ttu-id="f0af4-112">**注意：**  在实施了64位系统上的 WOW64 x86 模拟器的应用程序中不支持并发垃圾回收，该程序实现了以前称为 IA-64) 的 Intel Itanium 架构 (。</span><span class="sxs-lookup"><span data-stu-id="f0af4-112">**Note:**  Concurrent garbage collection is not supported in applications that are running the WOW64 x86 emulator on 64-bit systems that implement the Intel Itanium architecture (formerly called IA-64).</span></span> <span data-ttu-id="f0af4-113">有关在64位 Windows 系统上使用 WOW64 的详细信息，请参阅 [运行32位应用程序](/windows/desktop/WinProg64/running-32-bit-applications)。</span><span class="sxs-lookup"><span data-stu-id="f0af4-113">For more information about using WOW64 on 64-bit Windows systems, see [Running 32-bit Applications](/windows/desktop/WinProg64/running-32-bit-applications).</span></span>|  
|`STARTUP_LOADER_OPTIMIZATION_MASK`|<span data-ttu-id="f0af4-114">指定应执行加载程序优化。</span><span class="sxs-lookup"><span data-stu-id="f0af4-114">Specifies that loader optimization shall occur.</span></span>|  
|`STARTUP_LOADER_OPTIMIZATION_SINGLE_DOMAIN`|<span data-ttu-id="f0af4-115">指定不以非特定于域的形式加载程序集。</span><span class="sxs-lookup"><span data-stu-id="f0af4-115">Specifies that no assemblies are loaded as domain-neutral.</span></span>|  
|`STARTUP_LOADER_OPTIMIZATION_MULTI_DOMAIN`|<span data-ttu-id="f0af4-116">指定以非特定于域的形式加载所有程序集。</span><span class="sxs-lookup"><span data-stu-id="f0af4-116">Specifies that all assemblies are loaded as domain-neutral.</span></span>|  
|`STARTUP_LOADER_OPTIMIZATION_MULTI_DOMAIN_HOST`|<span data-ttu-id="f0af4-117">指定以非特定于域的形式加载所有强名称程序集。</span><span class="sxs-lookup"><span data-stu-id="f0af4-117">Specifies that all strong-named assemblies are loaded as domain-neutral.</span></span>|  
|`STARTUP_LOADER_SAFEMODE`|<span data-ttu-id="f0af4-118">指定将不将 CLR 版本策略应用于传入的版本。</span><span class="sxs-lookup"><span data-stu-id="f0af4-118">Specifies that CLR version policy will not be applied to the version passed in.</span></span> <span data-ttu-id="f0af4-119">将加载指定的 CLR 的确切版本。</span><span class="sxs-lookup"><span data-stu-id="f0af4-119">The exact version specified of the CLR will be loaded.</span></span> <span data-ttu-id="f0af4-120">填充码不会评估策略来确定最新的兼容版本。</span><span class="sxs-lookup"><span data-stu-id="f0af4-120">The shim does not evaluate policy to determine the latest compatible version.</span></span>|  
|`STARTUP_LOADER_SETPREFERENCE`|<span data-ttu-id="f0af4-121">指定将设置首选运行时，但实际不会启动。</span><span class="sxs-lookup"><span data-stu-id="f0af4-121">Specifies that the preferred runtime will be set, but not actually started.</span></span>|  
|`STARTUP_SERVER_GC`|<span data-ttu-id="f0af4-122">指定将使用服务器垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="f0af4-122">Specifies that the server garbage collection will be used.</span></span>|  
|`STARTUP_HOARD_GC_VM`|<span data-ttu-id="f0af4-123">指定垃圾回收将保留使用的虚拟地址。</span><span class="sxs-lookup"><span data-stu-id="f0af4-123">Specifies that garbage collection will keep the virtual address used.</span></span>|  
|`STARTUP_SINGLE_VERSION_HOSTING_INTERFACE`|<span data-ttu-id="f0af4-124">指定将不允许混合宿主接口。</span><span class="sxs-lookup"><span data-stu-id="f0af4-124">Specifies that mixing a hosting interface will not be allowed.</span></span>|  
|`STARTUP_LEGACY_IMPERSONATION`|<span data-ttu-id="f0af4-125">指定模拟应默认情况下不流经异步点。</span><span class="sxs-lookup"><span data-stu-id="f0af4-125">Specifies that impersonation should not flow across asynchronous points by default.</span></span>|  
|`STARTUP_DISABLE_COMMITTHREADSTACK`|<span data-ttu-id="f0af4-126">指定当线程开始运行时，不应提交完整线程堆栈。</span><span class="sxs-lookup"><span data-stu-id="f0af4-126">Specifies that the full thread stack should not be committed when the thread starts running.</span></span>|  
|`STARTUP_ALWAYSFLOW_IMPERSONATION`|<span data-ttu-id="f0af4-127">指定通过平台调用实现的托管模拟和模拟将流经异步点。</span><span class="sxs-lookup"><span data-stu-id="f0af4-127">Specifies that managed impersonations and impersonations achieved through platform invoke will flow across asynchronous points.</span></span> <span data-ttu-id="f0af4-128">默认情况下，仅托管模拟将流经异步点。</span><span class="sxs-lookup"><span data-stu-id="f0af4-128">By default, only managed impersonations will flow across asynchronous points.</span></span>|  
|`STARTUP_TRIM_GC_COMMIT`|<span data-ttu-id="f0af4-129">指定在系统内存不足时垃圾回收将使用较少的已提交空间。</span><span class="sxs-lookup"><span data-stu-id="f0af4-129">Specifies that garbage collection will use less committed space when system memory is low.</span></span> <span data-ttu-id="f0af4-130">请 `gcTrimCommitOnLowMemory` 参阅 [针对共享 Web 托管的优化](../../../standard/garbage-collection/optimization-for-shared-web-hosting.md)。</span><span class="sxs-lookup"><span data-stu-id="f0af4-130">See `gcTrimCommitOnLowMemory` in [Optimization for Shared Web Hosting](../../../standard/garbage-collection/optimization-for-shared-web-hosting.md).</span></span>|  
|`STARTUP_ETW`|<span data-ttu-id="f0af4-131">指定为 Windows (ETW) 启用了公共语言运行时事件的事件跟踪。</span><span class="sxs-lookup"><span data-stu-id="f0af4-131">Specifies that event tracing for Windows (ETW) is enabled for common language runtime events.</span></span> <span data-ttu-id="f0af4-132">从 Windows Vista 开始，始终启用事件跟踪，因此该标志不起作用。</span><span class="sxs-lookup"><span data-stu-id="f0af4-132">Beginning with Windows Vista, event tracing is always enabled, so this flag has no effect.</span></span> <span data-ttu-id="f0af4-133">请参阅 [控制 .NET Framework 日志记录](../../performance/controlling-logging.md)。</span><span class="sxs-lookup"><span data-stu-id="f0af4-133">See [Controlling .NET Framework Logging](../../performance/controlling-logging.md).</span></span>|  
|`STARTUP_ARM`|<span data-ttu-id="f0af4-134">指定启用应用程序域资源监视。</span><span class="sxs-lookup"><span data-stu-id="f0af4-134">Specifies that application domain resource monitoring is enabled.</span></span> <span data-ttu-id="f0af4-135">请参见 <xref:System.AppDomain.MonitoringIsEnabled%2A?displayProperty=nameWithType> 属性和[ \<appDomainResourceMonitoring> 元素](../../configure-apps/file-schema/runtime/appdomainresourcemonitoring-element.md)。</span><span class="sxs-lookup"><span data-stu-id="f0af4-135">See the <xref:System.AppDomain.MonitoringIsEnabled%2A?displayProperty=nameWithType> property and [\<appDomainResourceMonitoring> Element](../../configure-apps/file-schema/runtime/appdomainresourcemonitoring-element.md).</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f0af4-136">要求</span><span class="sxs-lookup"><span data-stu-id="f0af4-136">Requirements</span></span>  

 <span data-ttu-id="f0af4-137">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f0af4-137">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f0af4-138">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="f0af4-138">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f0af4-139">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f0af4-139">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f0af4-140">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f0af4-140">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f0af4-141">请参阅</span><span class="sxs-lookup"><span data-stu-id="f0af4-141">See also</span></span>

- [<span data-ttu-id="f0af4-142">承载枚举</span><span class="sxs-lookup"><span data-stu-id="f0af4-142">Hosting Enumerations</span></span>](hosting-enumerations.md)
