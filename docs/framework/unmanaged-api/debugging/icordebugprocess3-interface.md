---
description: 了解详细信息： ICorDebugProcess3 接口
title: ICorDebugProcess3 接口
ms.date: 03/30/2017
api_name:
- ICorDebugProcess3
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess3
helpviewer_keywords:
- ICorDebugProcess3 interface [.NET Framework debugging]
ms.assetid: ced9c82e-d7b0-4806-a151-98b6611d3097
topic_type:
- apiref
ms.openlocfilehash: 28b588bb4718f841e78b89ce44821971800b1f6f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99649970"
---
# <a name="icordebugprocess3-interface"></a><span data-ttu-id="3b7a0-103">ICorDebugProcess3 接口</span><span class="sxs-lookup"><span data-stu-id="3b7a0-103">ICorDebugProcess3 Interface</span></span>

<span data-ttu-id="3b7a0-104">控制自定义调试器通知。</span><span class="sxs-lookup"><span data-stu-id="3b7a0-104">Controls custom debugger notifications.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3b7a0-105">方法</span><span class="sxs-lookup"><span data-stu-id="3b7a0-105">Methods</span></span>  
  
|<span data-ttu-id="3b7a0-106">方法</span><span class="sxs-lookup"><span data-stu-id="3b7a0-106">Method</span></span>|<span data-ttu-id="3b7a0-107">说明</span><span class="sxs-lookup"><span data-stu-id="3b7a0-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3b7a0-108">SetEnableCustomNotification 方法</span><span class="sxs-lookup"><span data-stu-id="3b7a0-108">SetEnableCustomNotification Method</span></span>](icordebugprocess3-setenablecustomnotification-method.md)|<span data-ttu-id="3b7a0-109">启用和禁用指定类型的自定义调试器通知。</span><span class="sxs-lookup"><span data-stu-id="3b7a0-109">Enables and disables custom debugger notifications of the specified type.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3b7a0-110">备注</span><span class="sxs-lookup"><span data-stu-id="3b7a0-110">Remarks</span></span>  

 <span data-ttu-id="3b7a0-111">此接口以逻辑方式扩展 ICorDebugProcess 和 ICorDebugProcess2 接口。</span><span class="sxs-lookup"><span data-stu-id="3b7a0-111">This interface logically extends the ICorDebugProcess and ICorDebugProcess2 interfaces.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="3b7a0-112">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="3b7a0-112">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3b7a0-113">要求</span><span class="sxs-lookup"><span data-stu-id="3b7a0-113">Requirements</span></span>  

 <span data-ttu-id="3b7a0-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3b7a0-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3b7a0-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3b7a0-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3b7a0-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3b7a0-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3b7a0-117">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3b7a0-117">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3b7a0-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="3b7a0-118">See also</span></span>

- [<span data-ttu-id="3b7a0-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="3b7a0-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="3b7a0-120">调试</span><span class="sxs-lookup"><span data-stu-id="3b7a0-120">Debugging</span></span>](index.md)
