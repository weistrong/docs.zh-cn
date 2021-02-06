---
description: 了解详细信息： ICorProfilerCallback：： AppDomainShutdownStarted 方法
title: ICorProfilerCallback::AppDomainShutdownStarted 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.AppDomainShutdownStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::AppDomainShutdownStarted
helpviewer_keywords:
- AppDomainShutdownStarted method [.NET Framework profiling]
- ICorProfilerCallback::AppDomainShutdownStarted method [.NET Framework profiling]
ms.assetid: d23a3408-b525-4aec-a186-2ac7ca65d7a4
topic_type:
- apiref
ms.openlocfilehash: 16545142a512ca1c5f4167f61b81ea949e3d14e4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99648111"
---
# <a name="icorprofilercallbackappdomainshutdownstarted-method"></a><span data-ttu-id="8f19c-103">ICorProfilerCallback::AppDomainShutdownStarted 方法</span><span class="sxs-lookup"><span data-stu-id="8f19c-103">ICorProfilerCallback::AppDomainShutdownStarted Method</span></span>

<span data-ttu-id="8f19c-104">通知探查器正在从进程中卸载应用程序域。</span><span class="sxs-lookup"><span data-stu-id="8f19c-104">Notifies the profiler that an application domain is being unloaded from a process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8f19c-105">语法</span><span class="sxs-lookup"><span data-stu-id="8f19c-105">Syntax</span></span>  
  
```cpp  
HRESULT AppDomainShutdownStarted(  
    [in] AppDomainID appDomainId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="8f19c-106">参数</span><span class="sxs-lookup"><span data-stu-id="8f19c-106">Parameters</span></span>

- `appDomainId`

  <span data-ttu-id="8f19c-107">\[中的] 标识存储应用程序的程序集的域。</span><span class="sxs-lookup"><span data-stu-id="8f19c-107">\[in] Identifies the domain in which the application's assemblies are stored.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f19c-108">备注</span><span class="sxs-lookup"><span data-stu-id="8f19c-108">Remarks</span></span>  

 <span data-ttu-id="8f19c-109">`appDomainId`此方法返回后，的值对任何信息请求都无效 `AppDomainShutdownStarted` -这是探查器获取有关此应用程序域的信息的最后机会。</span><span class="sxs-lookup"><span data-stu-id="8f19c-109">The value of `appDomainId` is not valid for any information request after the `AppDomainShutdownStarted` method returns — this is the profiler's last chance to get information about this application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8f19c-110">要求</span><span class="sxs-lookup"><span data-stu-id="8f19c-110">Requirements</span></span>  

 <span data-ttu-id="8f19c-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8f19c-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8f19c-112">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="8f19c-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="8f19c-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8f19c-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8f19c-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8f19c-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8f19c-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="8f19c-115">See also</span></span>

- [<span data-ttu-id="8f19c-116">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="8f19c-116">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
