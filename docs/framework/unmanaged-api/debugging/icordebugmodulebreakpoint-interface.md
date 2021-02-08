---
description: 了解详细信息： ICorDebugModuleBreakpoint 接口
title: ICorDebugModuleBreakpoint 接口
ms.date: 03/30/2017
api_name:
- ICorDebugModuleBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModuleBreakpoint
helpviewer_keywords:
- ICorDebugModuleBreakpoint interface [.NET Framework debugging]
ms.assetid: 34667162-f314-475f-ae1b-ce9cb0fcbb83
topic_type:
- apiref
ms.openlocfilehash: c864850400471c9a3580de9bb94262c62656edf0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790745"
---
# <a name="icordebugmodulebreakpoint-interface"></a><span data-ttu-id="d2826-103">ICorDebugModuleBreakpoint 接口</span><span class="sxs-lookup"><span data-stu-id="d2826-103">ICorDebugModuleBreakpoint Interface</span></span>

<span data-ttu-id="d2826-104">提供对特定模块的访问权限。</span><span class="sxs-lookup"><span data-stu-id="d2826-104">Provides access to specific modules.</span></span> <span data-ttu-id="d2826-105">此接口是 ICorDebugBreakpoint 接口的子类。</span><span class="sxs-lookup"><span data-stu-id="d2826-105">This interface is a subclass of the ICorDebugBreakpoint interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d2826-106">方法</span><span class="sxs-lookup"><span data-stu-id="d2826-106">Methods</span></span>  
  
|<span data-ttu-id="d2826-107">方法</span><span class="sxs-lookup"><span data-stu-id="d2826-107">Method</span></span>|<span data-ttu-id="d2826-108">说明</span><span class="sxs-lookup"><span data-stu-id="d2826-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d2826-109">GetModule 方法</span><span class="sxs-lookup"><span data-stu-id="d2826-109">GetModule Method</span></span>](icordebugmodulebreakpoint-getmodule-method.md)|<span data-ttu-id="d2826-110">获取一个指向 ICorDebugModule 的接口指针，该指针引用设置此断点的模块。</span><span class="sxs-lookup"><span data-stu-id="d2826-110">Gets an interface pointer to an ICorDebugModule that references the module where this breakpoint is set.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d2826-111">备注</span><span class="sxs-lookup"><span data-stu-id="d2826-111">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="d2826-112">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="d2826-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d2826-113">要求</span><span class="sxs-lookup"><span data-stu-id="d2826-113">Requirements</span></span>  

 <span data-ttu-id="d2826-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d2826-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d2826-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d2826-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d2826-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d2826-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d2826-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d2826-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d2826-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="d2826-118">See also</span></span>

- [<span data-ttu-id="d2826-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="d2826-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
