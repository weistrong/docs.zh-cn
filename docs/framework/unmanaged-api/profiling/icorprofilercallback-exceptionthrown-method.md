---
description: 了解详细信息： ICorProfilerCallback：： ExceptionThrown 方法
title: ICorProfilerCallback::ExceptionThrown 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ExceptionThrown
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ExceptionThrown
helpviewer_keywords:
- ExceptionThrown method [.NET Framework profiling]
- ICorProfilerCallback::ExceptionThrown method [.NET Framework profiling]
ms.assetid: f1a23f3b-ac21-4905-8abf-8ea59f15af53
topic_type:
- apiref
ms.openlocfilehash: 77ebca8fbc52ed0c46a4f76fb5cdf6cb2923edaf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99706131"
---
# <a name="icorprofilercallbackexceptionthrown-method"></a><span data-ttu-id="b76b8-103">ICorProfilerCallback::ExceptionThrown 方法</span><span class="sxs-lookup"><span data-stu-id="b76b8-103">ICorProfilerCallback::ExceptionThrown Method</span></span>

<span data-ttu-id="b76b8-104">通知探查器引发了异常。</span><span class="sxs-lookup"><span data-stu-id="b76b8-104">Notifies the profiler that an exception has been thrown.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="b76b8-105">仅当异常到达托管代码时，才调用此函数。</span><span class="sxs-lookup"><span data-stu-id="b76b8-105">This function is called only if the exception reaches managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b76b8-106">语法</span><span class="sxs-lookup"><span data-stu-id="b76b8-106">Syntax</span></span>  
  
```cpp  
HRESULT ExceptionThrown(  
    [in] ObjectID thrownObjectId);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b76b8-107">参数</span><span class="sxs-lookup"><span data-stu-id="b76b8-107">Parameters</span></span>

- `thrownObjectId`

  <span data-ttu-id="b76b8-108">\[in] 导致引发异常的对象的 ID。</span><span class="sxs-lookup"><span data-stu-id="b76b8-108">\[in] The ID of the object that caused the exception to be thrown.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b76b8-109">备注</span><span class="sxs-lookup"><span data-stu-id="b76b8-109">Remarks</span></span>  

 <span data-ttu-id="b76b8-110">探查器不应在此方法的实现中被阻止，因为堆栈可能不处于允许垃圾回收的状态，因此无法启用抢先垃圾回收。</span><span class="sxs-lookup"><span data-stu-id="b76b8-110">The profiler should not block in its implementation of this method because the stack may not be in a state that allows garbage collection, and therefore preemptive garbage collection cannot be enabled.</span></span> <span data-ttu-id="b76b8-111">如果探查器在此处阻止并且试图进行垃圾回收，则运行时将被阻止，直到此回调返回。</span><span class="sxs-lookup"><span data-stu-id="b76b8-111">If the profiler blocks here and garbage collection is attempted, the runtime will block until this callback returns.</span></span>  
  
 <span data-ttu-id="b76b8-112">探查器的此方法的实现不应调入托管代码或以任何方式导致托管内存分配。</span><span class="sxs-lookup"><span data-stu-id="b76b8-112">The profiler's implementation of this method should not call into managed code or in any way cause a managed-memory allocation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b76b8-113">要求</span><span class="sxs-lookup"><span data-stu-id="b76b8-113">Requirements</span></span>  

 <span data-ttu-id="b76b8-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b76b8-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b76b8-115">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b76b8-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b76b8-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b76b8-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b76b8-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b76b8-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b76b8-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="b76b8-118">See also</span></span>

- [<span data-ttu-id="b76b8-119">ICorProfilerCallback 接口</span><span class="sxs-lookup"><span data-stu-id="b76b8-119">ICorProfilerCallback Interface</span></span>](icorprofilercallback-interface.md)
