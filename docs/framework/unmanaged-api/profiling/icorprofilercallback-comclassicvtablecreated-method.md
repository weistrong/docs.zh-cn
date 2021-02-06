---
description: 了解详细信息： ICorProfilerCallback：： COMClassicVTableCreated 方法
title: ICorProfilerCallback::COMClassicVTableCreated 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.COMClassicVTableCreated
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::COMClassicVTableCreated
helpviewer_keywords:
- COMClassicVTableCreated method [.NET Framework profiling]
- ICorProfilerCallback::COMClassicVTableCreated method [.NET Framework profiling]
ms.assetid: 6e1834ab-c359-498a-b10b-984ae23cdda4
topic_type:
- apiref
ms.openlocfilehash: 134ca44cbcd7a275e3ad61a3dd4decaa92668b5b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99657679"
---
# <a name="icorprofilercallbackcomclassicvtablecreated-method"></a><span data-ttu-id="b4c75-103">ICorProfilerCallback::COMClassicVTableCreated 方法</span><span class="sxs-lookup"><span data-stu-id="b4c75-103">ICorProfilerCallback::COMClassicVTableCreated Method</span></span>

<span data-ttu-id="b4c75-104">通知探查器已创建指定 IID 和类的 COM 互操作 vtable。</span><span class="sxs-lookup"><span data-stu-id="b4c75-104">Notifies the profiler that a COM interop vtable for the specified IID and class has been created.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b4c75-105">语法</span><span class="sxs-lookup"><span data-stu-id="b4c75-105">Syntax</span></span>  
  
```cpp  
HRESULT COMClassicVTableCreated(  
    [in] ClassID wrappedClassId,  
    [in] REFGUID implementedIID,  
    [in] void    *pVTable,  
    [in] ULONG   cSlots);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b4c75-106">参数</span><span class="sxs-lookup"><span data-stu-id="b4c75-106">Parameters</span></span>

- `wrappedClasId`

  <span data-ttu-id="b4c75-107">\[in] 已为其创建 vtable 的类的 ID。</span><span class="sxs-lookup"><span data-stu-id="b4c75-107">\[in] The ID of the class for which the vtable has been created.</span></span>

- `implementedIID`

  <span data-ttu-id="b4c75-108">\[in] 类实现的接口的 ID。</span><span class="sxs-lookup"><span data-stu-id="b4c75-108">\[in] The ID of the interface implemented by the class.</span></span> <span data-ttu-id="b4c75-109">如果接口仅限内部接口，此值可能为 NULL。</span><span class="sxs-lookup"><span data-stu-id="b4c75-109">This value may be NULL if the interface is internal only.</span></span>

- `pVTable`

  <span data-ttu-id="b4c75-110">\[in] 指向 vtable 开头的指针。</span><span class="sxs-lookup"><span data-stu-id="b4c75-110">\[in] A pointer to the start of the vtable.</span></span>

- `cSlots`

  <span data-ttu-id="b4c75-111">\[in] vtable 中的槽数。</span><span class="sxs-lookup"><span data-stu-id="b4c75-111">\[in] The number of slots that are in the vtable.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4c75-112">备注</span><span class="sxs-lookup"><span data-stu-id="b4c75-112">Remarks</span></span>  

 <span data-ttu-id="b4c75-113">探查器不应在此方法的实现中被阻止，因为堆栈可能不处于允许垃圾回收的状态，因此无法启用抢先垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="b4c75-113">The profiler should not block in its implementation of this method because the stack may not be in a state that allows garbage collection, and therefore preemptive garbage collection cannot be enabled.</span></span> <span data-ttu-id="b4c75-114">如果探查器在此处阻止并且试图进行垃圾回收，则运行时将被阻止，直到此回调返回。</span><span class="sxs-lookup"><span data-stu-id="b4c75-114">If the profiler blocks here and garbage collection is attempted, the runtime will block until this callback returns.</span></span>  
  
 <span data-ttu-id="b4c75-115">探查器的此方法的实现不应调入托管代码或以任何方式导致托管内存分配。</span><span class="sxs-lookup"><span data-stu-id="b4c75-115">The profiler's implementation of this method should not call into managed code or in any way cause a managed-memory allocation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b4c75-116">要求</span><span class="sxs-lookup"><span data-stu-id="b4c75-116">Requirements</span></span>  

 <span data-ttu-id="b4c75-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b4c75-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b4c75-118">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b4c75-118">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b4c75-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b4c75-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b4c75-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b4c75-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b4c75-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="b4c75-121">See also</span></span>

- [<span data-ttu-id="b4c75-122">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="b4c75-122">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
- [<span data-ttu-id="b4c75-123">COMClassicVTableDestroyed 方法</span><span class="sxs-lookup"><span data-stu-id="b4c75-123">COMClassicVTableDestroyed Method</span></span>](icorprofilercallback-comclassicvtabledestroyed-method.md)
