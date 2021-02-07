---
description: 了解详细信息： ICorProfilerInfo：： SetEventMask 方法
title: ICorProfilerInfo::SetEventMask 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo.SetEventMask
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::SetEventMask
helpviewer_keywords:
- ICorProfilerInfo::SetEventMask method [.NET Framework profiling]
- SetEventMask method [.NET Framework profiling]
ms.assetid: 44bc0f56-32fa-491e-a62d-52fc96d48125
topic_type:
- apiref
ms.openlocfilehash: e389d25abfecfc9a5dec8834e412fe618324e311
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99687189"
---
# <a name="icorprofilerinfoseteventmask-method"></a><span data-ttu-id="e67f4-103">ICorProfilerInfo::SetEventMask 方法</span><span class="sxs-lookup"><span data-stu-id="e67f4-103">ICorProfilerInfo::SetEventMask Method</span></span>

<span data-ttu-id="e67f4-104">设置一个值，用于指定探查器需要从公共语言运行时 (CLR) 接收其相关通知的事件的类型。</span><span class="sxs-lookup"><span data-stu-id="e67f4-104">Sets a value that specifies the types of events for which the profiler wants to receive notification from the common language runtime (CLR).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e67f4-105">语法</span><span class="sxs-lookup"><span data-stu-id="e67f4-105">Syntax</span></span>  
  
```cpp  
HRESULT SetEventMask(  
    [in] DWORD dwEvents);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e67f4-106">参数</span><span class="sxs-lookup"><span data-stu-id="e67f4-106">Parameters</span></span>  

 `dwEvents`  
 <span data-ttu-id="e67f4-107">[in] 一个指定事件类别的 4 字节的值。</span><span class="sxs-lookup"><span data-stu-id="e67f4-107">[in] A 4-byte value that specifies the categories of events.</span></span> <span data-ttu-id="e67f4-108">每个位都可控制不同的功能、行为或事件类型。</span><span class="sxs-lookup"><span data-stu-id="e67f4-108">Each bit controls a different capability, behavior, or type of event.</span></span> <span data-ttu-id="e67f4-109">[COR_PRF_MONITOR](cor-prf-monitor-enumeration.md)枚举中描述了这些位。</span><span class="sxs-lookup"><span data-stu-id="e67f4-109">The bits are described in the [COR_PRF_MONITOR](cor-prf-monitor-enumeration.md) enumeration.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e67f4-110">备注</span><span class="sxs-lookup"><span data-stu-id="e67f4-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="e67f4-111">应调用 [SetEventMask2](icorprofilerinfo5-seteventmask2-method.md) 方法，而不是此方法。</span><span class="sxs-lookup"><span data-stu-id="e67f4-111">You should call the [SetEventMask2](icorprofilerinfo5-seteventmask2-method.md) method instead of this method.</span></span> <span data-ttu-id="e67f4-112">尽管此 `SetEventMask` 方法继续受支持，但 [SetEventMask2](icorprofilerinfo5-seteventmask2-method.md) 提供其他功能。</span><span class="sxs-lookup"><span data-stu-id="e67f4-112">Although the `SetEventMask` method continues to be supported, [SetEventMask2](icorprofilerinfo5-seteventmask2-method.md) provides additional functionality.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e67f4-113">要求</span><span class="sxs-lookup"><span data-stu-id="e67f4-113">Requirements</span></span>  

 <span data-ttu-id="e67f4-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e67f4-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e67f4-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e67f4-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e67f4-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e67f4-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e67f4-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e67f4-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e67f4-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="e67f4-118">See also</span></span>

- [<span data-ttu-id="e67f4-119">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="e67f4-119">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
- [<span data-ttu-id="e67f4-120">SetEventMask2 方法</span><span class="sxs-lookup"><span data-stu-id="e67f4-120">SetEventMask2 Method</span></span>](icorprofilerinfo5-seteventmask2-method.md)
