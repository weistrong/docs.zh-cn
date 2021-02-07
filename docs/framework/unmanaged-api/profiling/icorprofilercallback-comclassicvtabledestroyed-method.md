---
description: 了解详细信息： ICorProfilerCallback：： COMClassicVTableDestroyed 方法
title: ICorProfilerCallback::COMClassicVTableDestroyed 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.COMClassicVTableDestroyed
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::COMClassicVTableDestroyed
helpviewer_keywords:
- ICorProfilerCallback::COMClassicVTableDestroyed method [.NET Framework profiling]
- COMClassicVTableDestroyed method [.NET Framework profiling]
ms.assetid: 29da20ca-bf39-4356-8099-d9c3ac3423a9
topic_type:
- apiref
ms.openlocfilehash: 91ed5bb65d3a64f1f85a09a710b507974f51c79b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99706375"
---
# <a name="icorprofilercallbackcomclassicvtabledestroyed-method"></a><span data-ttu-id="84c47-103">ICorProfilerCallback::COMClassicVTableDestroyed 方法</span><span class="sxs-lookup"><span data-stu-id="84c47-103">ICorProfilerCallback::COMClassicVTableDestroyed Method</span></span>

<span data-ttu-id="84c47-104">通知探查器正在销毁 COM 互操作 vtable。</span><span class="sxs-lookup"><span data-stu-id="84c47-104">Notifies the profiler that a COM interop vtable is being destroyed.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="84c47-105">此回调很可能永远不会发生，因为 vtables 的销毁操作非常接近关闭。</span><span class="sxs-lookup"><span data-stu-id="84c47-105">This callback is likely never to occur, because the destruction of vtables occurs very close to shutdown.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="84c47-106">语法</span><span class="sxs-lookup"><span data-stu-id="84c47-106">Syntax</span></span>  
  
```cpp  
HRESULT COMClassicVTableDestroyed(  
    [in] ClassID wrappedClassId,  
    [in] REFGUID implementedIID,  
    [in] void    *pVTable);  
```  
  
## <a name="parameters"></a><span data-ttu-id="84c47-107">参数</span><span class="sxs-lookup"><span data-stu-id="84c47-107">Parameters</span></span>

- `wrappedClassId`

  <span data-ttu-id="84c47-108">\[in] 为其创建了此 vtable 的类的 ID。</span><span class="sxs-lookup"><span data-stu-id="84c47-108">\[in] The ID of the class for which this vtable was created.</span></span>

- `implementedIID`

  <span data-ttu-id="84c47-109">\[in] 类实现的接口的 ID。</span><span class="sxs-lookup"><span data-stu-id="84c47-109">\[in] The ID of the interface implemented by the class.</span></span> <span data-ttu-id="84c47-110">如果接口仅限内部接口，此值可能为 NULL。</span><span class="sxs-lookup"><span data-stu-id="84c47-110">This value may be NULL if the interface is internal only.</span></span>

- `pVTable`

  <span data-ttu-id="84c47-111">\[in] 指向 vtable 开头的指针。</span><span class="sxs-lookup"><span data-stu-id="84c47-111">\[in] A pointer to the start of the vtable.</span></span>

## <a name="remarks"></a><span data-ttu-id="84c47-112">备注</span><span class="sxs-lookup"><span data-stu-id="84c47-112">Remarks</span></span>  

 <span data-ttu-id="84c47-113">探查器不应在此方法的实现中被阻止，因为堆栈可能不处于允许垃圾回收的状态，因此无法启用抢先垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="84c47-113">The profiler should not block in its implementation of this method because the stack may not be in a state that allows garbage collection, and therefore preemptive garbage collection cannot be enabled.</span></span> <span data-ttu-id="84c47-114">如果探查器在此处阻止并且试图进行垃圾回收，则运行时将被阻止，直到此回调返回。</span><span class="sxs-lookup"><span data-stu-id="84c47-114">If the profiler blocks here and garbage collection is attempted, the runtime will block until this callback returns.</span></span>  
  
 <span data-ttu-id="84c47-115">探查器的此方法的实现不应调入托管代码或以任何方式导致托管内存分配。</span><span class="sxs-lookup"><span data-stu-id="84c47-115">The profiler's implementation of this method should not call into managed code or in any way cause a managed-memory allocation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="84c47-116">要求</span><span class="sxs-lookup"><span data-stu-id="84c47-116">Requirements</span></span>  

 <span data-ttu-id="84c47-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="84c47-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="84c47-118">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="84c47-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="84c47-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="84c47-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="84c47-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="84c47-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="84c47-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="84c47-121">See also</span></span>

- [<span data-ttu-id="84c47-122">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="84c47-122">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="84c47-123">COMClassicVTableCreated 方法</span><span class="sxs-lookup"><span data-stu-id="84c47-123">COMClassicVTableCreated Method</span></span>](icorprofilercallback-comclassicvtablecreated-method.md)
