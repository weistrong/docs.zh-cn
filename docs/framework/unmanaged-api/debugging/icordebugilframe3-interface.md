---
description: 了解详细信息： ICorDebugILFrame3 接口
title: ICorDebugILFrame3 接口
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame3
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 15212cb5-93d4-4025-bec9-d4b9919eb1fe
topic_type:
- apiref
ms.openlocfilehash: a34a3f0941871a2d0a63fb2d9f78ccb7ff455866
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791252"
---
# <a name="icordebugilframe3-interface"></a><span data-ttu-id="47279-103">ICorDebugILFrame3 接口</span><span class="sxs-lookup"><span data-stu-id="47279-103">ICorDebugILFrame3 Interface</span></span>

<span data-ttu-id="47279-104">提供用于封装函数的返回值的方法。</span><span class="sxs-lookup"><span data-stu-id="47279-104">Provides a method that encapsulates the return value of a function.</span></span> <span data-ttu-id="47279-105">`ICorDebugILFrame3` 是 ICorDebugILFrame 和 ICorDebugILFrame2 接口的逻辑扩展。</span><span class="sxs-lookup"><span data-stu-id="47279-105">`ICorDebugILFrame3` is a logical extension of the ICorDebugILFrame and ICorDebugILFrame2 interfaces.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="47279-106">方法</span><span class="sxs-lookup"><span data-stu-id="47279-106">Methods</span></span>  
  
|<span data-ttu-id="47279-107">方法</span><span class="sxs-lookup"><span data-stu-id="47279-107">Method</span></span>|<span data-ttu-id="47279-108">说明</span><span class="sxs-lookup"><span data-stu-id="47279-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="47279-109">GetReturnValueForILOffset 方法</span><span class="sxs-lookup"><span data-stu-id="47279-109">GetReturnValueForILOffset Method</span></span>](icordebugilframe3-getreturnvalueforiloffset-method.md)|<span data-ttu-id="47279-110">获取一个 ICorDebugValue 对象，该对象封装函数的返回值。</span><span class="sxs-lookup"><span data-stu-id="47279-110">Gets an ICorDebugValue object that encapsulates the return value of a function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="47279-111">备注</span><span class="sxs-lookup"><span data-stu-id="47279-111">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="47279-112">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="47279-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="47279-113">要求</span><span class="sxs-lookup"><span data-stu-id="47279-113">Requirements</span></span>  

 <span data-ttu-id="47279-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="47279-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="47279-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="47279-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="47279-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="47279-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="47279-117">**.NET Framework 版本：**[!INCLUDE[net_current_v451plus](../../../../includes/net-current-v451plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="47279-117">**.NET Framework Versions:** [!INCLUDE[net_current_v451plus](../../../../includes/net-current-v451plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="47279-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="47279-118">See also</span></span>

- [<span data-ttu-id="47279-119">ICorDebugCode3 接口</span><span class="sxs-lookup"><span data-stu-id="47279-119">ICorDebugCode3 Interface</span></span>](icordebugcode3-interface.md)
- [<span data-ttu-id="47279-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="47279-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
