---
description: 了解详细信息： ICorProfilerInfo5：： GetEventMask2 方法
title: ICorProfilerInfo5::GetEventMask2 方法
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorProfilerInfo5.GetEventMask2
api_location:
- mscorwks.dll
api_type:
- COM
ms.assetid: f854b68f-009c-4ffb-89cd-ca874d1c0fb7
topic_type:
- apiref
ms.openlocfilehash: c6652ffe1b8fd0d99ce5493c8ba27a971363c423
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99646655"
---
# <a name="icorprofilerinfo5geteventmask2-method"></a><span data-ttu-id="79d32-103">ICorProfilerInfo5::GetEventMask2 方法</span><span class="sxs-lookup"><span data-stu-id="79d32-103">ICorProfilerInfo5::GetEventMask2 Method</span></span>

<span data-ttu-id="79d32-104">[仅在 .NET Framework 4.5.2 及更高版本中受支持]</span><span class="sxs-lookup"><span data-stu-id="79d32-104">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="79d32-105">获取探查器要从公共语言运行时 (CLR) 中接收通知的当前事件类别。</span><span class="sxs-lookup"><span data-stu-id="79d32-105">Gets the current event categories for which the profiler wants to receive notifications from the common language runtime (CLR).</span></span>  <span data-ttu-id="79d32-106">它提供 [ICorProfilerInfo：： GetEventMask](icorprofilerinfo-geteventmask-method.md) 方法未提供的功能。</span><span class="sxs-lookup"><span data-stu-id="79d32-106">It provides functionality not provided by the [ICorProfilerInfo::GetEventMask](icorprofilerinfo-geteventmask-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79d32-107">语法</span><span class="sxs-lookup"><span data-stu-id="79d32-107">Syntax</span></span>  
  
```cpp
HRESULT GetEventMask2(  
        [out] DWORD* pdwEventsLow,  
        [out] DWORD* pdwEventsHigh  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="79d32-108">参数</span><span class="sxs-lookup"><span data-stu-id="79d32-108">Parameters</span></span>  

 `pdwEventsLow`  
 <span data-ttu-id="79d32-109">[out] 一个指向指定事件类别的 4 字节值的指针。</span><span class="sxs-lookup"><span data-stu-id="79d32-109">[out] A pointer to a 4-byte value that specifies the categories of events.</span></span> <span data-ttu-id="79d32-110">每个位都可控制不同的功能、行为或事件类型。</span><span class="sxs-lookup"><span data-stu-id="79d32-110">Each bit controls a different capability, behavior, or type of event.</span></span> <span data-ttu-id="79d32-111">[COR_PRF_MONITOR](cor-prf-monitor-enumeration.md)枚举中描述了这些位。</span><span class="sxs-lookup"><span data-stu-id="79d32-111">The bits are described in the [COR_PRF_MONITOR](cor-prf-monitor-enumeration.md) enumeration.</span></span>  
  
 `pdwEventsHigh`  
 <span data-ttu-id="79d32-112">[out] 一个指向指定事件类别的 4 字节值的指针。</span><span class="sxs-lookup"><span data-stu-id="79d32-112">[out] A pointer to a 4-byte value that specifies the categories of events.</span></span>  <span data-ttu-id="79d32-113">每个位都可控制不同的功能、行为或事件类型。</span><span class="sxs-lookup"><span data-stu-id="79d32-113">Each bit controls a different capability, behavior, or type of event.</span></span> <span data-ttu-id="79d32-114">[COR_PRF_HIGH_MONITOR](cor-prf-high-monitor-enumeration.md)枚举中描述了这些位。</span><span class="sxs-lookup"><span data-stu-id="79d32-114">The bits are described in the [COR_PRF_HIGH_MONITOR](cor-prf-high-monitor-enumeration.md) enumeration.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="79d32-115">备注</span><span class="sxs-lookup"><span data-stu-id="79d32-115">Remarks</span></span>  

 <span data-ttu-id="79d32-116">`GetEventMask2` 方法用于确定探查器已订阅了哪些回调。</span><span class="sxs-lookup"><span data-stu-id="79d32-116">The `GetEventMask2` method is used to determine which callbacks the profiler has subscribed to.</span></span> <span data-ttu-id="79d32-117">通常，您 `pdwEventsLow` 需要对和 `pdwEventsHigh` 值以及要设置的任何新位执行逻辑 "或"，然后调用 [SetEventMask2](icorprofilerinfo5-seteventmask2-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="79d32-117">Typically, you perform a logical OR of the `pdwEventsLow` and `pdwEventsHigh` values and any new bits you want to set, and then call the [SetEventMask2](icorprofilerinfo5-seteventmask2-method.md) method.</span></span>  
  
 <span data-ttu-id="79d32-118">此方法是 [GetEventMask](icorprofilerinfo-geteventmask-method.md) 方法的建议替代方法。</span><span class="sxs-lookup"><span data-stu-id="79d32-118">This method is the recommended alternative to the [GetEventMask](icorprofilerinfo-geteventmask-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="79d32-119">要求</span><span class="sxs-lookup"><span data-stu-id="79d32-119">Requirements</span></span>  

 <span data-ttu-id="79d32-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="79d32-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="79d32-121">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="79d32-121">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="79d32-122">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="79d32-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="79d32-123">**.NET Framework 版本：**[!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="79d32-123">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="79d32-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="79d32-124">See also</span></span>

- [<span data-ttu-id="79d32-125">ICorProfilerInfo5 接口</span><span class="sxs-lookup"><span data-stu-id="79d32-125">ICorProfilerInfo5 Interface</span></span>](icorprofilerinfo5-interface.md)
- [<span data-ttu-id="79d32-126">SetEventMask2 方法</span><span class="sxs-lookup"><span data-stu-id="79d32-126">SetEventMask2 Method</span></span>](icorprofilerinfo5-seteventmask2-method.md)
