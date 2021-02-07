---
description: 了解详细信息： ICorDebugCode3 接口
title: ICorDebugCode3 接口
ms.date: 03/30/2017
api_name:
- ICorDebugCode3
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode3
helpviewer_keywords:
- ICorDebugCode3 interface [.NET Framework debugging]
ms.assetid: 70f07c9e-0614-4bee-ac34-09fe6c51c5a9
topic_type:
- apiref
ms.openlocfilehash: 378141395ab4d23e3e33a84c3b14ca4a75d847dc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99764835"
---
# <a name="icordebugcode3-interface"></a><span data-ttu-id="9ce4e-103">ICorDebugCode3 接口</span><span class="sxs-lookup"><span data-stu-id="9ce4e-103">ICorDebugCode3 Interface</span></span>

<span data-ttu-id="9ce4e-104">提供一个方法，该方法将 "ICorDebugCode" 和 "ICorDebugCode2" 扩展为提供有关托管返回值的信息。</span><span class="sxs-lookup"><span data-stu-id="9ce4e-104">Provides a method that extends "ICorDebugCode" and "ICorDebugCode2" to provide information about a managed return value.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="9ce4e-105">方法</span><span class="sxs-lookup"><span data-stu-id="9ce4e-105">Methods</span></span>  
  
|<span data-ttu-id="9ce4e-106">方法</span><span class="sxs-lookup"><span data-stu-id="9ce4e-106">Method</span></span>|<span data-ttu-id="9ce4e-107">说明</span><span class="sxs-lookup"><span data-stu-id="9ce4e-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="9ce4e-108">GetReturnValueLiveOffset 方法</span><span class="sxs-lookup"><span data-stu-id="9ce4e-108">GetReturnValueLiveOffset Method</span></span>](icordebugcode3-getreturnvalueliveoffset-method.md)|<span data-ttu-id="9ce4e-109">对于指定的 IL 偏移量，获取应放置断点的本机偏移量，以便调试器可以从函数中获取返回值。</span><span class="sxs-lookup"><span data-stu-id="9ce4e-109">For a specified IL offset, gets the native offsets where a breakpoint should be placed so that the debugger can obtain the return value from a function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9ce4e-110">备注</span><span class="sxs-lookup"><span data-stu-id="9ce4e-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="9ce4e-111">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="9ce4e-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9ce4e-112">要求</span><span class="sxs-lookup"><span data-stu-id="9ce4e-112">Requirements</span></span>  

 <span data-ttu-id="9ce4e-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9ce4e-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9ce4e-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9ce4e-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9ce4e-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9ce4e-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9ce4e-116">**.NET Framework 版本：**[!INCLUDE[net_current_v451plus](../../../../includes/net-current-v451plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9ce4e-116">**.NET Framework Versions:** [!INCLUDE[net_current_v451plus](../../../../includes/net-current-v451plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9ce4e-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="9ce4e-117">See also</span></span>

- [<span data-ttu-id="9ce4e-118">ICorDebugILFrame3 接口</span><span class="sxs-lookup"><span data-stu-id="9ce4e-118">ICorDebugILFrame3 Interface</span></span>](icordebugilframe3-interface.md)
- [<span data-ttu-id="9ce4e-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="9ce4e-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
