---
description: 了解详细信息： ICorProfilerInfo2：： GetRVAStaticAddress 方法
title: ICorProfilerInfo2::GetRVAStaticAddress 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetRVAStaticAddress
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetRVAStaticAddress
helpviewer_keywords:
- GetRVAStaticAddress method [.NET Framework profiling]
- ICorProfilerInfo2::GetRVAStaticAddress method [.NET Framework profiling]
ms.assetid: a25a8f8b-5cfa-440d-9376-a1a1c3a9fc11
topic_type:
- apiref
ms.openlocfilehash: e72a136ca0d8462d19c57da021e9429528555dac
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99716401"
---
# <a name="icorprofilerinfo2getrvastaticaddress-method"></a><span data-ttu-id="cd06a-103">ICorProfilerInfo2::GetRVAStaticAddress 方法</span><span class="sxs-lookup"><span data-stu-id="cd06a-103">ICorProfilerInfo2::GetRVAStaticAddress Method</span></span>

<span data-ttu-id="cd06a-104">获取 (RVA) 静态字段的指定相对虚拟地址的地址。</span><span class="sxs-lookup"><span data-stu-id="cd06a-104">Gets the address of the specified relative virtual address (RVA) static field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cd06a-105">语法</span><span class="sxs-lookup"><span data-stu-id="cd06a-105">Syntax</span></span>  
  
```cpp  
HRESULT GetRVAStaticAddress(  
    [in] ClassID classId,  
    [in] mdFieldDef fieldToken,  
    [out] void **ppAddress);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cd06a-106">参数</span><span class="sxs-lookup"><span data-stu-id="cd06a-106">Parameters</span></span>  

 `classId`  
 <span data-ttu-id="cd06a-107">中包含请求的 RVA 静态字段的类的 ID。</span><span class="sxs-lookup"><span data-stu-id="cd06a-107">[in] The ID of the class that contains the requested RVA-static field.</span></span>  
  
 `fieldToken`  
 <span data-ttu-id="cd06a-108">中请求的 RVA 静态字段的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="cd06a-108">[in] Metadata token for the requested RVA-static field.</span></span>  
  
 `ppAddress`  
 <span data-ttu-id="cd06a-109">弄指向 RVA 静态字段的地址的指针。</span><span class="sxs-lookup"><span data-stu-id="cd06a-109">[out] A pointer to the address of the RVA-static field.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cd06a-110">备注</span><span class="sxs-lookup"><span data-stu-id="cd06a-110">Remarks</span></span>  

 <span data-ttu-id="cd06a-111">此 `GetRVAStaticAddress` 方法可能会返回以下内容之一：</span><span class="sxs-lookup"><span data-stu-id="cd06a-111">The `GetRVAStaticAddress` method may return one of the following:</span></span>  
  
- <span data-ttu-id="cd06a-112">如果未在指定的上下文中为给定的静态字段分配地址，则 CORPROF_E_DATAINCOMPLETE HRESULT。</span><span class="sxs-lookup"><span data-stu-id="cd06a-112">A CORPROF_E_DATAINCOMPLETE HRESULT if the given static field has not been assigned an address in the specified context.</span></span>  
  
- <span data-ttu-id="cd06a-113">可能位于垃圾回收堆中的对象的地址。</span><span class="sxs-lookup"><span data-stu-id="cd06a-113">The addresses of objects that may be in the garbage collection heap.</span></span> <span data-ttu-id="cd06a-114">这些地址可能会在垃圾回收后失效，因此，在垃圾回收后，探查器不应假定它们是有效的。</span><span class="sxs-lookup"><span data-stu-id="cd06a-114">These addresses may become invalid after garbage collection, so after garbage collection, profilers should not assume that they are valid.</span></span>  
  
 <span data-ttu-id="cd06a-115">在类的类构造函数完成之前， `GetRVAStaticAddress` 将为其所有静态字段返回 CORPROF_E_DATAINCOMPLETE，不过，某些静态字段可能已经初始化并且可能是对垃圾回收对象的根。</span><span class="sxs-lookup"><span data-stu-id="cd06a-115">Before a class’s class constructor is completed, `GetRVAStaticAddress` will return CORPROF_E_DATAINCOMPLETE for all its static fields, although some of the static fields may already be initialized and may be rooting garbage collection objects.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cd06a-116">要求</span><span class="sxs-lookup"><span data-stu-id="cd06a-116">Requirements</span></span>  

 <span data-ttu-id="cd06a-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cd06a-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cd06a-118">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="cd06a-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="cd06a-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cd06a-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cd06a-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cd06a-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cd06a-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="cd06a-121">See also</span></span>

- [<span data-ttu-id="cd06a-122">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="cd06a-122">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
- [<span data-ttu-id="cd06a-123">ICorProfilerInfo2 接口</span><span class="sxs-lookup"><span data-stu-id="cd06a-123">ICorProfilerInfo2 Interface</span></span>](icorprofilerinfo2-interface.md)
