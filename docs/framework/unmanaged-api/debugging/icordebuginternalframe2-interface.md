---
description: 了解详细信息： ICorDebugInternalFrame2 接口
title: ICorDebugInternalFrame2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugInternalFrame2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugInternalFrame2
helpviewer_keywords:
- ICorDebugInternalFrame2 interface [.NET Framework debugging]
ms.assetid: d4755569-85b8-4ff4-bf50-0e608e76429f
topic_type:
- apiref
ms.openlocfilehash: 3edc666c043513562b2fcece478b2879f294ce33
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791096"
---
# <a name="icordebuginternalframe2-interface"></a><span data-ttu-id="cfda7-103">ICorDebugInternalFrame2 接口</span><span class="sxs-lookup"><span data-stu-id="cfda7-103">ICorDebugInternalFrame2 Interface</span></span>

<span data-ttu-id="cfda7-104">提供有关内部帧的信息，包括堆栈地址和相对于 ICorDebugFrame 对象的位置。</span><span class="sxs-lookup"><span data-stu-id="cfda7-104">Provides information about internal frames, including stack address and position in relation to ICorDebugFrame objects.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="cfda7-105">方法</span><span class="sxs-lookup"><span data-stu-id="cfda7-105">Methods</span></span>  
  
|<span data-ttu-id="cfda7-106">方法</span><span class="sxs-lookup"><span data-stu-id="cfda7-106">Method</span></span>|<span data-ttu-id="cfda7-107">说明</span><span class="sxs-lookup"><span data-stu-id="cfda7-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="cfda7-108">GetFrameAddress 方法</span><span class="sxs-lookup"><span data-stu-id="cfda7-108">GetFrameAddress Method</span></span>](icordebuginternalframe2-getframeaddress-method.md)|<span data-ttu-id="cfda7-109">返回内部帧的堆栈地址。</span><span class="sxs-lookup"><span data-stu-id="cfda7-109">Returns the stack address of the internal frame.</span></span>|  
|[<span data-ttu-id="cfda7-110">IsCloserToLeaf 方法</span><span class="sxs-lookup"><span data-stu-id="cfda7-110">IsCloserToLeaf Method</span></span>](icordebuginternalframe2-isclosertoleaf-method.md)|<span data-ttu-id="cfda7-111">检查 `this` 内部帧是否接近于指定的 ICorDebugFrame 对象。</span><span class="sxs-lookup"><span data-stu-id="cfda7-111">Checks whether the `this` internal frame is closer to the leaf than the specified ICorDebugFrame object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="cfda7-112">备注</span><span class="sxs-lookup"><span data-stu-id="cfda7-112">Remarks</span></span>  

 <span data-ttu-id="cfda7-113">此接口扩展 ICorDebugInternalFrame 接口。</span><span class="sxs-lookup"><span data-stu-id="cfda7-113">This interface extends the ICorDebugInternalFrame interface.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="cfda7-114">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="cfda7-114">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cfda7-115">要求</span><span class="sxs-lookup"><span data-stu-id="cfda7-115">Requirements</span></span>  

 <span data-ttu-id="cfda7-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cfda7-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cfda7-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="cfda7-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="cfda7-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cfda7-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cfda7-119">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cfda7-119">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cfda7-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="cfda7-120">See also</span></span>

- [<span data-ttu-id="cfda7-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="cfda7-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="cfda7-122">调试</span><span class="sxs-lookup"><span data-stu-id="cfda7-122">Debugging</span></span>](index.md)
