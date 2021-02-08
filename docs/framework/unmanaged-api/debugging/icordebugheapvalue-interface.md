---
description: 了解详细信息： ICorDebugHeapValue 接口
title: ICorDebugHeapValue 接口
ms.date: 03/30/2017
api_name:
- ICorDebugHeapValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugHeapValue
helpviewer_keywords:
- ICorDebugHeapValue interface [.NET Framework debugging]
ms.assetid: 1bca66db-0359-4ae8-846e-e35f7e547e8b
topic_type:
- apiref
ms.openlocfilehash: 7c65cbce530f0d1f00d8610031fb604a0118ee29
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803667"
---
# <a name="icordebugheapvalue-interface"></a><span data-ttu-id="e649c-103">ICorDebugHeapValue 接口</span><span class="sxs-lookup"><span data-stu-id="e649c-103">ICorDebugHeapValue Interface</span></span>

<span data-ttu-id="e649c-104">"ICorDebugValue" 的子类，它表示公共语言运行时 (CLR) 垃圾回收器收集的对象。</span><span class="sxs-lookup"><span data-stu-id="e649c-104">A subclass of "ICorDebugValue" that represents an object that has been collected by the common language runtime (CLR) garbage collector.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="e649c-105">方法</span><span class="sxs-lookup"><span data-stu-id="e649c-105">Methods</span></span>  
  
|<span data-ttu-id="e649c-106">方法</span><span class="sxs-lookup"><span data-stu-id="e649c-106">Method</span></span>|<span data-ttu-id="e649c-107">说明</span><span class="sxs-lookup"><span data-stu-id="e649c-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="e649c-108">CreateRelocBreakpoint 方法</span><span class="sxs-lookup"><span data-stu-id="e649c-108">CreateRelocBreakpoint Method</span></span>](icordebugheapvalue-createrelocbreakpoint-method.md)|<span data-ttu-id="e649c-109">未实现。</span><span class="sxs-lookup"><span data-stu-id="e649c-109">Not implemented.</span></span>|  
|[<span data-ttu-id="e649c-110">IsValid 方法</span><span class="sxs-lookup"><span data-stu-id="e649c-110">IsValid Method</span></span>](icordebugheapvalue-isvalid-method.md)|<span data-ttu-id="e649c-111">获取一个值，该值指示由此表示的对象是否 `ICorDebugHeapValue` 有效，或者是否已被垃圾回收器回收。</span><span class="sxs-lookup"><span data-stu-id="e649c-111">Gets a value that indicates whether the object represented by this `ICorDebugHeapValue` is valid, or has been reclaimed by the garbage collector.</span></span> <span data-ttu-id="e649c-112">此方法在 .NET Framework 版本2.0 中已弃用。</span><span class="sxs-lookup"><span data-stu-id="e649c-112">This method has been deprecated in the .NET Framework version 2.0.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e649c-113">备注</span><span class="sxs-lookup"><span data-stu-id="e649c-113">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="e649c-114">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="e649c-114">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e649c-115">要求</span><span class="sxs-lookup"><span data-stu-id="e649c-115">Requirements</span></span>  

 <span data-ttu-id="e649c-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e649c-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e649c-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e649c-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e649c-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e649c-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e649c-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e649c-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e649c-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="e649c-120">See also</span></span>

- [<span data-ttu-id="e649c-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="e649c-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
