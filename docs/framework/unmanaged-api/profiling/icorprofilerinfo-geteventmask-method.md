---
description: 了解详细信息： ICorProfilerInfo：： GetEventMask 方法
title: ICorProfilerInfo::GetEventMask 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.GetEventMask
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetEventMask
helpviewer_keywords:
- GetEventMask method [.NET Framework profiling]
- ICorProfilerInfo::GetEventMask method [.NET Framework profiling]
ms.assetid: ec34cc13-45a3-4695-abc3-b3347d4e6fc2
topic_type:
- apiref
ms.openlocfilehash: 8ae02a0ef98330207fa7ce6366342d5e0bcb4f19
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99647630"
---
# <a name="icorprofilerinfogeteventmask-method"></a><span data-ttu-id="499ed-103">ICorProfilerInfo::GetEventMask 方法</span><span class="sxs-lookup"><span data-stu-id="499ed-103">ICorProfilerInfo::GetEventMask Method</span></span>

<span data-ttu-id="499ed-104">获取探查器要从公共语言运行时 (CLR) 中接收其事件通知的当前事件类别。</span><span class="sxs-lookup"><span data-stu-id="499ed-104">Gets the current event categories for which the profiler wants to receive event notifications from the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="499ed-105">语法</span><span class="sxs-lookup"><span data-stu-id="499ed-105">Syntax</span></span>  
  
```cpp  
HRESULT GetEventMask(  
    [out] DWORD *pdwEvents);  
```  
  
## <a name="parameters"></a><span data-ttu-id="499ed-106">参数</span><span class="sxs-lookup"><span data-stu-id="499ed-106">Parameters</span></span>  

 `pdwEvents`  
 <span data-ttu-id="499ed-107">[out] 一个指向指定事件类别的 4 字节值的指针。</span><span class="sxs-lookup"><span data-stu-id="499ed-107">[out] A pointer to a 4-byte value that specifies the categories of events.</span></span> <span data-ttu-id="499ed-108">每个位都可控制不同的功能、行为或事件类型。</span><span class="sxs-lookup"><span data-stu-id="499ed-108">Each bit controls a different capability, behavior, or type of event.</span></span> <span data-ttu-id="499ed-109">[COR_PRF_MONITOR](cor-prf-monitor-enumeration.md)枚举中描述了这些位。</span><span class="sxs-lookup"><span data-stu-id="499ed-109">The bits are described in the [COR_PRF_MONITOR](cor-prf-monitor-enumeration.md) enumeration.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="499ed-110">备注</span><span class="sxs-lookup"><span data-stu-id="499ed-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="499ed-111">应调用 [GetEventMask2](icorprofilerinfo5-geteventmask2-method.md) 方法，而不是此方法。</span><span class="sxs-lookup"><span data-stu-id="499ed-111">You should call the [GetEventMask2](icorprofilerinfo5-geteventmask2-method.md) method instead of this method.</span></span> <span data-ttu-id="499ed-112">尽管此 `SetEventMask` 方法继续受支持，但 [GetEventMask2](icorprofilerinfo5-geteventmask2-method.md) 提供其他功能。</span><span class="sxs-lookup"><span data-stu-id="499ed-112">Although the `SetEventMask` method continues to be supported, [GetEventMask2](icorprofilerinfo5-geteventmask2-method.md) provides additional functionality.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="499ed-113">要求</span><span class="sxs-lookup"><span data-stu-id="499ed-113">Requirements</span></span>  

 <span data-ttu-id="499ed-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="499ed-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="499ed-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="499ed-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="499ed-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="499ed-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="499ed-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="499ed-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="499ed-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="499ed-118">See also</span></span>

- [<span data-ttu-id="499ed-119">GetEventMask2 方法</span><span class="sxs-lookup"><span data-stu-id="499ed-119">GetEventMask2 Method</span></span>](icorprofilerinfo5-geteventmask2-method.md)
- [<span data-ttu-id="499ed-120">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="499ed-120">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
