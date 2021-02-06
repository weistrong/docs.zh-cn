---
description: 了解详细信息： ICorProfilerCallback：： AppDomainCreationFinished 方法
title: ICorProfilerCallback::AppDomainCreationFinished 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.AppDomainCreationFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::AppDomainCreationFinished
helpviewer_keywords:
- AppDomainCreationFinished method [.NET Framework profiling]
- ICorProfilerCallback::AppDomainCreationFinished method [.NET Framework profiling]
ms.assetid: dbab7d90-d515-4dc9-8195-294d5d04bab6
topic_type:
- apiref
ms.openlocfilehash: 6995c6cda168b5be5815e6f7b2b4d900ae0d4d67
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99648358"
---
# <a name="icorprofilercallbackappdomaincreationfinished-method"></a><span data-ttu-id="44ed6-103">ICorProfilerCallback::AppDomainCreationFinished 方法</span><span class="sxs-lookup"><span data-stu-id="44ed6-103">ICorProfilerCallback::AppDomainCreationFinished Method</span></span>

<span data-ttu-id="44ed6-104">通知探查器已创建应用程序域。</span><span class="sxs-lookup"><span data-stu-id="44ed6-104">Notifies the profiler that an application domain has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="44ed6-105">语法</span><span class="sxs-lookup"><span data-stu-id="44ed6-105">Syntax</span></span>  
  
```cpp  
HRESULT AppDomainCreationFinished(  
    [in] AppDomainID appDomainId,  
    [in] HRESULT     hrStatus);
```  
  
## <a name="parameters"></a><span data-ttu-id="44ed6-106">参数</span><span class="sxs-lookup"><span data-stu-id="44ed6-106">Parameters</span></span>

- `appDomainId`

  <span data-ttu-id="44ed6-107">\[中的] 标识已创建的域。</span><span class="sxs-lookup"><span data-stu-id="44ed6-107">\[in] Identifies the domain which has been created.</span></span>

- `hrStatus`

  <span data-ttu-id="44ed6-108">\[in] 一个 HRESULT，指示是否已成功完成创建应用程序域。</span><span class="sxs-lookup"><span data-stu-id="44ed6-108">\[in] An HRESULT that indicates whether creation of the application domain completed successfully.</span></span>

## <a name="remarks"></a><span data-ttu-id="44ed6-109">备注</span><span class="sxs-lookup"><span data-stu-id="44ed6-109">Remarks</span></span>  

 <span data-ttu-id="44ed6-110">在调用方法之前，应用程序 ID 对于任何信息请求均无效 `AppDomainCreationFinished` 。</span><span class="sxs-lookup"><span data-stu-id="44ed6-110">The application ID is not valid for any information request until the `AppDomainCreationFinished` method is called.</span></span>  
  
 <span data-ttu-id="44ed6-111">在回调后，某些加载应用程序域的部分可能会继续 `AppDomainCreationFinished` 。</span><span class="sxs-lookup"><span data-stu-id="44ed6-111">Some parts of loading the application domain might continue after the `AppDomainCreationFinished` callback.</span></span> <span data-ttu-id="44ed6-112">中的 HRESULT 失败 `hrStatus` 表示失败。</span><span class="sxs-lookup"><span data-stu-id="44ed6-112">A failure HRESULT in `hrStatus` indicates a failure.</span></span> <span data-ttu-id="44ed6-113">但是，中的成功 HRESULT `hrStatus` 仅指示创建应用程序域的第一部分已成功。</span><span class="sxs-lookup"><span data-stu-id="44ed6-113">However, a success HRESULT in `hrStatus` indicates only that the first part of creating the application domain has succeeded.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="44ed6-114">要求</span><span class="sxs-lookup"><span data-stu-id="44ed6-114">Requirements</span></span>  

 <span data-ttu-id="44ed6-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="44ed6-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="44ed6-116">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="44ed6-116">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="44ed6-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="44ed6-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="44ed6-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="44ed6-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="44ed6-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="44ed6-119">See also</span></span>

- [<span data-ttu-id="44ed6-120">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="44ed6-120">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
