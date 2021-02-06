---
description: 了解详细信息： ICorProfilerCallback：： AppDomainShutdownFinished 方法
title: ICorProfilerCallback::AppDomainShutdownFinished 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.AppDomainShutdownFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::AppDomainShutdownFinished
helpviewer_keywords:
- AppDomainShutdownFinished method [.NET Framework profiling]
- ICorProfilerCallback::AppDomainShutdownFinished method [.NET Framework profiling]
ms.assetid: 52794819-0a59-4bb1-a265-0f158cd5cd65
topic_type:
- apiref
ms.openlocfilehash: e08a4f7e03bfd18d9c6a2fdf56bfab8c68f9c379
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99648202"
---
# <a name="icorprofilercallbackappdomainshutdownfinished-method"></a><span data-ttu-id="9cd0a-103">ICorProfilerCallback::AppDomainShutdownFinished 方法</span><span class="sxs-lookup"><span data-stu-id="9cd0a-103">ICorProfilerCallback::AppDomainShutdownFinished Method</span></span>

<span data-ttu-id="9cd0a-104">通知探查器已从进程中卸载应用程序域。</span><span class="sxs-lookup"><span data-stu-id="9cd0a-104">Notifies the profiler that an application domain has been unloaded from a process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9cd0a-105">语法</span><span class="sxs-lookup"><span data-stu-id="9cd0a-105">Syntax</span></span>  
  
```cpp  
HRESULT AppDomainShutdownFinished(  
    [in] AppDomainID appDomainId,  
    [in] HRESULT     hrStatus);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9cd0a-106">参数</span><span class="sxs-lookup"><span data-stu-id="9cd0a-106">Parameters</span></span>

- `appDomainId`

  <span data-ttu-id="9cd0a-107">\[中的] 标识存储应用程序的程序集的域。</span><span class="sxs-lookup"><span data-stu-id="9cd0a-107">\[in] Identifies the domain in which the application's assemblies are stored.</span></span>

- `hrStatus`

  <span data-ttu-id="9cd0a-108">\[in] 一个 HRESULT，指示是否已成功卸载应用程序域。</span><span class="sxs-lookup"><span data-stu-id="9cd0a-108">\[in] An HRESULT that indicates whether the application domain was unloaded successfully.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cd0a-109">备注</span><span class="sxs-lookup"><span data-stu-id="9cd0a-109">Remarks</span></span>  

 <span data-ttu-id="9cd0a-110">在 `appDomainId` [ICorProfilerCallback：： AppDomainShutdownStarted](icorprofilercallback-appdomainshutdownstarted-method.md) 方法返回后，的值对信息请求无效。</span><span class="sxs-lookup"><span data-stu-id="9cd0a-110">The value of `appDomainId` is not valid for an information request after the [ICorProfilerCallback::AppDomainShutdownStarted](icorprofilercallback-appdomainshutdownstarted-method.md) method returns.</span></span>  
  
 <span data-ttu-id="9cd0a-111">在回调后，卸载应用程序域的某些部分可能会继续 `AppDomainCreationFinished` 。</span><span class="sxs-lookup"><span data-stu-id="9cd0a-111">Some parts of unloading the application domain might continue after the `AppDomainCreationFinished` callback.</span></span> <span data-ttu-id="9cd0a-112">中的 HRESULT 失败 `hrStatus` 表示失败。</span><span class="sxs-lookup"><span data-stu-id="9cd0a-112">A failure HRESULT in `hrStatus` indicates a failure.</span></span> <span data-ttu-id="9cd0a-113">但是，中的成功 HRESULT `hrStatus` 仅指示卸载应用程序域的第一部分已成功。</span><span class="sxs-lookup"><span data-stu-id="9cd0a-113">However, a success HRESULT in `hrStatus` indicates only that the first part of unloading the application domain has succeeded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9cd0a-114">要求</span><span class="sxs-lookup"><span data-stu-id="9cd0a-114">Requirements</span></span>  

 <span data-ttu-id="9cd0a-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9cd0a-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9cd0a-116">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="9cd0a-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="9cd0a-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9cd0a-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9cd0a-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9cd0a-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9cd0a-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="9cd0a-119">See also</span></span>

- [<span data-ttu-id="9cd0a-120">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="9cd0a-120">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
