---
description: 了解详细信息： ICLRRuntimeHost 接口
title: ICLRRuntimeHost 接口
ms.date: 03/30/2017
api_name:
- ICLRRuntimeHost
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeHost
helpviewer_keywords:
- ICLRRuntimeHost interface [.NET Framework hosting]
ms.assetid: cb0c5f65-3791-47bc-b833-2f84f4101ba5
topic_type:
- apiref
ms.openlocfilehash: 92bab42fa1cf2cca5caa0eb039c88fec3e65390c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753882"
---
# <a name="iclrruntimehost-interface"></a><span data-ttu-id="48e27-103">ICLRRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="48e27-103">ICLRRuntimeHost Interface</span></span>

<span data-ttu-id="48e27-104">提供与 .NET Framework 版本1中提供的 [ICorRuntimeHost](icorruntimehost-interface.md) 接口类似的功能，其中包含以下更改：</span><span class="sxs-lookup"><span data-stu-id="48e27-104">Provides functionality similar to that of the [ICorRuntimeHost](icorruntimehost-interface.md) interface provided in the .NET Framework version 1, with the following changes:</span></span>  
  
- <span data-ttu-id="48e27-105">用于设置宿主控件接口的 [SetHostControl](iclrruntimehost-sethostcontrol-method.md) 方法的添加。</span><span class="sxs-lookup"><span data-stu-id="48e27-105">The addition of the [SetHostControl](iclrruntimehost-sethostcontrol-method.md) method to set the host control interface.</span></span>  
  
- <span data-ttu-id="48e27-106">省略提供的某些方法 `ICorRuntimeHost` 。</span><span class="sxs-lookup"><span data-stu-id="48e27-106">The omission of some methods provided by `ICorRuntimeHost`.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="48e27-107">方法</span><span class="sxs-lookup"><span data-stu-id="48e27-107">Methods</span></span>  
  
|<span data-ttu-id="48e27-108">方法</span><span class="sxs-lookup"><span data-stu-id="48e27-108">Method</span></span>|<span data-ttu-id="48e27-109">说明</span><span class="sxs-lookup"><span data-stu-id="48e27-109">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="48e27-110">ExecuteApplication 方法</span><span class="sxs-lookup"><span data-stu-id="48e27-110">ExecuteApplication Method</span></span>](iclrruntimehost-executeapplication-method.md)|<span data-ttu-id="48e27-111">在基于清单的 ClickOnce 部署方案中用于指定要在新域中激活的应用程序。</span><span class="sxs-lookup"><span data-stu-id="48e27-111">Used in manifest-based ClickOnce deployment scenarios to specify the application to be activated in a new domain.</span></span>|  
|[<span data-ttu-id="48e27-112">ExecuteInAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="48e27-112">ExecuteInAppDomain Method</span></span>](iclrruntimehost-executeinappdomain-method.md)|<span data-ttu-id="48e27-113">指定 <xref:System.AppDomain> 要在其中执行指定的托管代码的。</span><span class="sxs-lookup"><span data-stu-id="48e27-113">Specifies the <xref:System.AppDomain> in which to execute the specified managed code.</span></span>|  
|[<span data-ttu-id="48e27-114">ExecuteInDefaultAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="48e27-114">ExecuteInDefaultAppDomain Method</span></span>](iclrruntimehost-executeindefaultappdomain-method.md)|<span data-ttu-id="48e27-115">在指定的程序集中调用指定类型的指定方法。</span><span class="sxs-lookup"><span data-stu-id="48e27-115">Invokes the specified method of the specified type in the specified assembly.</span></span>|  
|[<span data-ttu-id="48e27-116">GetCLRControl 方法</span><span class="sxs-lookup"><span data-stu-id="48e27-116">GetCLRControl Method</span></span>](iclrruntimehost-getclrcontrol-method.md)|<span data-ttu-id="48e27-117">获取 [ICLRControl](iclrcontrol-interface.md) 类型的接口指针，宿主可使用该指针自定义公共语言运行时)  (CLR 的各个方面。</span><span class="sxs-lookup"><span data-stu-id="48e27-117">Gets an interface pointer of type [ICLRControl](iclrcontrol-interface.md) that hosts can use to customize aspects of the common language runtime (CLR).</span></span>|  
|[<span data-ttu-id="48e27-118">GetCurrentAppDomainId 方法</span><span class="sxs-lookup"><span data-stu-id="48e27-118">GetCurrentAppDomainId Method</span></span>](iclrruntimehost-getcurrentappdomainid-method.md)|<span data-ttu-id="48e27-119">获取当前正在执行的的数值标识符 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="48e27-119">Gets the numeric identifier of the <xref:System.AppDomain> that is currently executing.</span></span>|  
|[<span data-ttu-id="48e27-120">SetHostControl 方法</span><span class="sxs-lookup"><span data-stu-id="48e27-120">SetHostControl Method</span></span>](iclrruntimehost-sethostcontrol-method.md)|<span data-ttu-id="48e27-121">设置宿主控件接口。</span><span class="sxs-lookup"><span data-stu-id="48e27-121">Sets the host control interface.</span></span> <span data-ttu-id="48e27-122">`SetHostControl`调用之前必须调用 `Start` 。</span><span class="sxs-lookup"><span data-stu-id="48e27-122">You must call `SetHostControl` before calling `Start`.</span></span>|  
|[<span data-ttu-id="48e27-123">Start 方法</span><span class="sxs-lookup"><span data-stu-id="48e27-123">Start Method</span></span>](iclrruntimehost-start-method.md)|<span data-ttu-id="48e27-124">将 CLR 初始化为一个进程。</span><span class="sxs-lookup"><span data-stu-id="48e27-124">Initializes the CLR into a process.</span></span>|  
|[<span data-ttu-id="48e27-125">Stop 方法</span><span class="sxs-lookup"><span data-stu-id="48e27-125">Stop Method</span></span>](iclrruntimehost-stop-method.md)|<span data-ttu-id="48e27-126">停止由运行时执行的代码。</span><span class="sxs-lookup"><span data-stu-id="48e27-126">Stops the execution of code by the runtime.</span></span>|  
|[<span data-ttu-id="48e27-127">UnloadAppDomain 方法</span><span class="sxs-lookup"><span data-stu-id="48e27-127">UnloadAppDomain Method</span></span>](iclrruntimehost-unloadappdomain-method.md)|<span data-ttu-id="48e27-128">卸载 <xref:System.AppDomain> 对应于指定数值标识符的。</span><span class="sxs-lookup"><span data-stu-id="48e27-128">Unloads the <xref:System.AppDomain> that corresponds to the specified numeric identifier.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="48e27-129">备注</span><span class="sxs-lookup"><span data-stu-id="48e27-129">Remarks</span></span>  

 <span data-ttu-id="48e27-130">从 .NET Framework 4 开始，使用 [ICLRMetaHost](iclrmetahost-interface.md) 接口获取指向 [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) 接口的指针，然后调用 [ICLRRuntimeInfo：： GetInterface](iclrruntimeinfo-getinterface-method.md) 方法以获取指向的指针 `ICLRRuntimeHost` 。</span><span class="sxs-lookup"><span data-stu-id="48e27-130">Starting with the .NET Framework 4, use the [ICLRMetaHost](iclrmetahost-interface.md) interface to get a pointer to the [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) interface, and then call the [ICLRRuntimeInfo::GetInterface](iclrruntimeinfo-getinterface-method.md) method to get a pointer to `ICLRRuntimeHost`.</span></span> <span data-ttu-id="48e27-131">在 .NET Framework 的早期版本中，主机 `ICLRRuntimeHost` 通过调用 [CorBindToRuntimeEx](corbindtoruntimeex-function.md) 或 [CorBindToCurrentRuntime](corbindtocurrentruntime-function.md)获取指向实例的指针。</span><span class="sxs-lookup"><span data-stu-id="48e27-131">In earlier versions of the .NET Framework, the host gets a pointer to an `ICLRRuntimeHost` instance by calling [CorBindToRuntimeEx](corbindtoruntimeex-function.md) or [CorBindToCurrentRuntime](corbindtocurrentruntime-function.md).</span></span> <span data-ttu-id="48e27-132">若要提供 .NET Framework 版本2.0 中提供的任何技术的实现，必须使用 `ICLRRuntimeHost` 而不是 `ICorRuntimeHost` 。</span><span class="sxs-lookup"><span data-stu-id="48e27-132">To provide implementations of any of the technologies provided in the .NET Framework version 2.0, you must use `ICLRRuntimeHost` instead of `ICorRuntimeHost`.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="48e27-133">请不要在调用[ExecuteApplication](iclrruntimehost-executeapplication-method.md)方法之前调用[Start](iclrruntimehost-start-method.md)方法来激活基于清单的应用程序。</span><span class="sxs-lookup"><span data-stu-id="48e27-133">Do not call the [Start](iclrruntimehost-start-method.md) method before calling the [ExecuteApplication](iclrruntimehost-executeapplication-method.md) method to activate a manifest-based application.</span></span> <span data-ttu-id="48e27-134">如果 `Start` 首先调用方法， `ExecuteApplication` 方法调用将失败。</span><span class="sxs-lookup"><span data-stu-id="48e27-134">If the `Start` method is called first, the `ExecuteApplication` method call will fail.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="48e27-135">要求</span><span class="sxs-lookup"><span data-stu-id="48e27-135">Requirements</span></span>  

 <span data-ttu-id="48e27-136">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="48e27-136">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="48e27-137">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="48e27-137">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="48e27-138">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="48e27-138">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="48e27-139">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="48e27-139">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="48e27-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="48e27-140">See also</span></span>

- [<span data-ttu-id="48e27-141">CorBindToCurrentRuntime 函数</span><span class="sxs-lookup"><span data-stu-id="48e27-141">CorBindToCurrentRuntime Function</span></span>](corbindtocurrentruntime-function.md)
- [<span data-ttu-id="48e27-142">CorBindToRuntimeEx 函数</span><span class="sxs-lookup"><span data-stu-id="48e27-142">CorBindToRuntimeEx Function</span></span>](corbindtoruntimeex-function.md)
- [<span data-ttu-id="48e27-143">ICLRControl 接口</span><span class="sxs-lookup"><span data-stu-id="48e27-143">ICLRControl Interface</span></span>](iclrcontrol-interface.md)
- [<span data-ttu-id="48e27-144">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="48e27-144">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)
- [<span data-ttu-id="48e27-145">承载接口</span><span class="sxs-lookup"><span data-stu-id="48e27-145">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="48e27-146">CLRRuntimeHost 组件类</span><span class="sxs-lookup"><span data-stu-id="48e27-146">CLRRuntimeHost Coclass</span></span>](clrruntimehost-coclass.md)
