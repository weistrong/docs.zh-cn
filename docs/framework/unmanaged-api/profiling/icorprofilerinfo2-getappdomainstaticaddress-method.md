---
description: 了解详细信息： ICorProfilerInfo2：： GetAppDomainStaticAddress 方法
title: ICorProfilerInfo2::GetAppDomainStaticAddress 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetAppDomainStaticAddress
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetAppDomainStaticAddress
helpviewer_keywords:
- ICorProfilerInfo2::GetAppDomainStaticAddress method [.NET Framework profiling]
- GetAppDomainStaticAddress method [.NET Framework profiling]
ms.assetid: 2a9e0ea7-a9e2-4817-b1c4-fcf15b215ea9
topic_type:
- apiref
ms.openlocfilehash: 4ef8511e75a18f7626fa7a30ea194140de051bb2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753228"
---
# <a name="icorprofilerinfo2getappdomainstaticaddress-method"></a><span data-ttu-id="b7655-103">ICorProfilerInfo2::GetAppDomainStaticAddress 方法</span><span class="sxs-lookup"><span data-stu-id="b7655-103">ICorProfilerInfo2::GetAppDomainStaticAddress Method</span></span>

<span data-ttu-id="b7655-104">获取指定应用程序域静态字段在指定应用程序域范围内的地址。</span><span class="sxs-lookup"><span data-stu-id="b7655-104">Gets the address of the specified application domain-static field that is in the scope of the specified application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b7655-105">语法</span><span class="sxs-lookup"><span data-stu-id="b7655-105">Syntax</span></span>  
  
```cpp  
RESULT GetAppDomainStaticAddress(  
    [in] ClassID classId,  
    [in] mdFieldDef fieldToken,  
    [in] AppDomainID appDomainId,  
    [out] void **ppAddress);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b7655-106">参数</span><span class="sxs-lookup"><span data-stu-id="b7655-106">Parameters</span></span>  

 `classId`  
 <span data-ttu-id="b7655-107">中包含请求的应用程序域静态字段的类的类 ID。</span><span class="sxs-lookup"><span data-stu-id="b7655-107">[in] The class ID of the class that contains the requested application domain-static field.</span></span>  
  
 `fieldToken`  
 <span data-ttu-id="b7655-108">中请求的应用程序域静态字段的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="b7655-108">[in] The metadata token for the requested application domain-static field.</span></span>  
  
 `appDomainId`  
 <span data-ttu-id="b7655-109">中作为所请求的静态字段的作用域的应用程序域的 ID。</span><span class="sxs-lookup"><span data-stu-id="b7655-109">[in] The ID of the application domain that is the scope for the requested static field.</span></span>  
  
 `ppAddress`  
 <span data-ttu-id="b7655-110">弄指向指定应用程序域中的静态字段的地址的指针。</span><span class="sxs-lookup"><span data-stu-id="b7655-110">[out] A pointer to the address of the static field that is within the specified application domain.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b7655-111">备注</span><span class="sxs-lookup"><span data-stu-id="b7655-111">Remarks</span></span>  

 <span data-ttu-id="b7655-112">此 `GetAppDomainStaticAddress` 方法可能会返回以下内容之一：</span><span class="sxs-lookup"><span data-stu-id="b7655-112">The `GetAppDomainStaticAddress` method may return one of the following:</span></span>  
  
- <span data-ttu-id="b7655-113">如果未在指定的上下文中为给定的静态字段分配地址，则 CORPROF_E_DATAINCOMPLETE HRESULT。</span><span class="sxs-lookup"><span data-stu-id="b7655-113">A CORPROF_E_DATAINCOMPLETE HRESULT if the given static field has not been assigned an address in the specified context.</span></span>  
  
- <span data-ttu-id="b7655-114">可能位于垃圾回收堆中的对象的地址。</span><span class="sxs-lookup"><span data-stu-id="b7655-114">The addresses of objects that may be in the garbage collection heap.</span></span> <span data-ttu-id="b7655-115">这些地址可能会在垃圾回收后失效，因此，在垃圾回收后，探查器不应假定它们是有效的。</span><span class="sxs-lookup"><span data-stu-id="b7655-115">These addresses may become invalid after garbage collection, so after garbage collection, profilers should not assume that they are valid.</span></span>  
  
 <span data-ttu-id="b7655-116">在类的类构造函数完成之前， `GetAppDomainStaticAddress` 将为其所有静态字段返回 CORPROF_E_DATAINCOMPLETE，不过，某些静态字段可能已经初始化并为垃圾回收对象提供了根。</span><span class="sxs-lookup"><span data-stu-id="b7655-116">Before a class’s class constructor is completed, `GetAppDomainStaticAddress` will return CORPROF_E_DATAINCOMPLETE for all its static fields, although some of the static fields may already be initialized and rooting garbage collection objects.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b7655-117">要求</span><span class="sxs-lookup"><span data-stu-id="b7655-117">Requirements</span></span>  

 <span data-ttu-id="b7655-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b7655-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b7655-119">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b7655-119">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b7655-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b7655-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b7655-121">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b7655-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b7655-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="b7655-122">See also</span></span>

- [<span data-ttu-id="b7655-123">ICorProfilerInfo 接口</span><span class="sxs-lookup"><span data-stu-id="b7655-123">ICorProfilerInfo Interface</span></span>](icorprofilerinfo-interface.md)
- [<span data-ttu-id="b7655-124">ICorProfilerInfo2 接口</span><span class="sxs-lookup"><span data-stu-id="b7655-124">ICorProfilerInfo2 Interface</span></span>](icorprofilerinfo2-interface.md)
