---
description: 了解详细信息： ICorConfiguration 接口
title: ICorConfiguration 接口
ms.date: 03/30/2017
api_name:
- ICorConfiguration
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICorConfiguration
helpviewer_keywords:
- ICorConfiguration interface [.NET Framework hosting]
ms.assetid: aaf96116-372b-4538-afb1-9e0fcdac1f98
topic_type:
- apiref
ms.openlocfilehash: f75e9e445c7fe4615abcae27756bcc420b5255b2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99636671"
---
# <a name="icorconfiguration-interface"></a><span data-ttu-id="43de5-103">ICorConfiguration 接口</span><span class="sxs-lookup"><span data-stu-id="43de5-103">ICorConfiguration Interface</span></span>

<span data-ttu-id="43de5-104">提供 (CLR) 配置公共语言运行时的方法。</span><span class="sxs-lookup"><span data-stu-id="43de5-104">Provides methods for configuring the common language runtime (CLR).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="43de5-105">方法</span><span class="sxs-lookup"><span data-stu-id="43de5-105">Methods</span></span>  
  
|<span data-ttu-id="43de5-106">方法</span><span class="sxs-lookup"><span data-stu-id="43de5-106">Method</span></span>|<span data-ttu-id="43de5-107">说明</span><span class="sxs-lookup"><span data-stu-id="43de5-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="43de5-108">AddDebuggerSpecialThread 方法</span><span class="sxs-lookup"><span data-stu-id="43de5-108">AddDebuggerSpecialThread Method</span></span>](icorconfiguration-adddebuggerspecialthread-method.md)|<span data-ttu-id="43de5-109">向调试服务指示当调试器在托管或非托管调试方案中停止应用程序时，应允许特定线程继续执行。</span><span class="sxs-lookup"><span data-stu-id="43de5-109">Indicates to the debugging services that a particular thread should be allowed to continue executing while the debugger has an application stopped during managed or unmanaged debugging scenarios.</span></span>|  
|[<span data-ttu-id="43de5-110">SetDebuggerThreadControl 方法</span><span class="sxs-lookup"><span data-stu-id="43de5-110">SetDebuggerThreadControl Method</span></span>](icorconfiguration-setdebuggerthreadcontrol-method.md)|<span data-ttu-id="43de5-111">设置在阻止和取消阻止 CLR 线程以进行调试时，调试服务将调用的回调接口。</span><span class="sxs-lookup"><span data-stu-id="43de5-111">Sets the callback interface that the debugging services will call as CLR threads are blocked and unblocked for debugging.</span></span>|  
|[<span data-ttu-id="43de5-112">SetGCHostControl 方法</span><span class="sxs-lookup"><span data-stu-id="43de5-112">SetGCHostControl Method</span></span>](icorconfiguration-setgchostcontrol-method.md)|<span data-ttu-id="43de5-113">设置垃圾回收器用于请求主机更改虚拟内存限制的回调接口。</span><span class="sxs-lookup"><span data-stu-id="43de5-113">Sets the callback interface to be used by the garbage collector to request the host to change the limits of virtual memory.</span></span>|  
|[<span data-ttu-id="43de5-114">SetGCThreadControl 方法</span><span class="sxs-lookup"><span data-stu-id="43de5-114">SetGCThreadControl Method</span></span>](icorconfiguration-setgcthreadcontrol-method.md)|<span data-ttu-id="43de5-115">设置回调接口，用于为非运行时任务计划线程，否则将阻止垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="43de5-115">Sets the callback interface for scheduling threads for non-runtime tasks that would otherwise be blocked for a garbage collection.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="43de5-116">要求</span><span class="sxs-lookup"><span data-stu-id="43de5-116">Requirements</span></span>  

 <span data-ttu-id="43de5-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="43de5-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="43de5-118">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="43de5-118">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="43de5-119">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="43de5-119">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="43de5-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="43de5-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="43de5-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="43de5-121">See also</span></span>

- [<span data-ttu-id="43de5-122">承载接口</span><span class="sxs-lookup"><span data-stu-id="43de5-122">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="43de5-123">CorRuntimeHost 组件类</span><span class="sxs-lookup"><span data-stu-id="43de5-123">CorRuntimeHost Coclass</span></span>](corruntimehost-coclass.md)
