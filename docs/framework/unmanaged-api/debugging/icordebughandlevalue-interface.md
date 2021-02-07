---
description: 了解详细信息： ICorDebugHandleValue 接口
title: ICorDebugHandleValue 接口
ms.date: 03/30/2017
api_name:
- ICorDebugHandleValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHandleValue
helpviewer_keywords:
- ICorDebugHandleValue interface [.NET Framework debugging]
ms.assetid: 66fcd2b8-ac66-414b-83a8-75a925e17772
topic_type:
- apiref
ms.openlocfilehash: 3bdb1f5668be283d8722c15f4779adfe4d7b3a2d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692030"
---
# <a name="icordebughandlevalue-interface"></a><span data-ttu-id="beedf-103">ICorDebugHandleValue 接口</span><span class="sxs-lookup"><span data-stu-id="beedf-103">ICorDebugHandleValue Interface</span></span>

<span data-ttu-id="beedf-104">ICorDebugReferenceValue 的子类，表示调试器已为其创建了垃圾回收句柄的引用值。</span><span class="sxs-lookup"><span data-stu-id="beedf-104">A subclass of ICorDebugReferenceValue that represents a reference value to which the debugger has created a handle for garbage collection.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="beedf-105">方法</span><span class="sxs-lookup"><span data-stu-id="beedf-105">Methods</span></span>  
  
|<span data-ttu-id="beedf-106">方法</span><span class="sxs-lookup"><span data-stu-id="beedf-106">Method</span></span>|<span data-ttu-id="beedf-107">说明</span><span class="sxs-lookup"><span data-stu-id="beedf-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="beedf-108">Dispose 方法</span><span class="sxs-lookup"><span data-stu-id="beedf-108">Dispose Method</span></span>](icordebughandlevalue-dispose-method.md)|<span data-ttu-id="beedf-109">释放此对象所引用的句柄， `ICorDebugHandleValue` 而不显式释放接口指针。</span><span class="sxs-lookup"><span data-stu-id="beedf-109">Releases the handle referenced by this `ICorDebugHandleValue` object without explicitly releasing the interface pointer.</span></span>|  
|[<span data-ttu-id="beedf-110">GetHandleType 方法</span><span class="sxs-lookup"><span data-stu-id="beedf-110">GetHandleType Method</span></span>](icordebughandlevalue-gethandletype-method.md)|<span data-ttu-id="beedf-111">获取一个 CorDebugHandleType 值，该值描述此所引用的句柄的类型 `ICorDebugHandleValue` 。</span><span class="sxs-lookup"><span data-stu-id="beedf-111">Gets a CorDebugHandleType value that describes the kind of handle referenced by this `ICorDebugHandleValue`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="beedf-112">备注</span><span class="sxs-lookup"><span data-stu-id="beedf-112">Remarks</span></span>  

 <span data-ttu-id="beedf-113">当 `ICorDebugReferenceValue` 执行调试的代码时，对象会失效。</span><span class="sxs-lookup"><span data-stu-id="beedf-113">An `ICorDebugReferenceValue` object is invalidated by a break in the execution of debugged code.</span></span> <span data-ttu-id="beedf-114">`ICorDebugHandleValue`通过中断和继续来维护其引用，直到显式释放它。</span><span class="sxs-lookup"><span data-stu-id="beedf-114">An `ICorDebugHandleValue` maintains its reference through breaks and continuations, until it is explicitly released.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="beedf-115">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="beedf-115">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="beedf-116">要求</span><span class="sxs-lookup"><span data-stu-id="beedf-116">Requirements</span></span>  

 <span data-ttu-id="beedf-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="beedf-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="beedf-118">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="beedf-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="beedf-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="beedf-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="beedf-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="beedf-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="beedf-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="beedf-121">See also</span></span>

- [<span data-ttu-id="beedf-122">调试接口</span><span class="sxs-lookup"><span data-stu-id="beedf-122">Debugging Interfaces</span></span>](debugging-interfaces.md)
