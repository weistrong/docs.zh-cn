---
description: 了解详细信息： ICorDebugFrameEnum 接口
title: ICorDebugFrameEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugFrameEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrameEnum
helpviewer_keywords:
- ICorDebugFrameEnum interface [.NET Framework debugging]
ms.assetid: ee3f85d3-044e-46b8-945c-93ebfa5d9e91
topic_type:
- apiref
ms.openlocfilehash: 61a83bd960182c28888d3c5459cf43c9bc7f2be3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692805"
---
# <a name="icordebugframeenum-interface"></a><span data-ttu-id="b3d59-103">ICorDebugFrameEnum 接口</span><span class="sxs-lookup"><span data-stu-id="b3d59-103">ICorDebugFrameEnum Interface</span></span>

<span data-ttu-id="b3d59-104">实现 ICorDebugEnum 方法，并枚举 ICorDebugFrame 数组。</span><span class="sxs-lookup"><span data-stu-id="b3d59-104">Implements ICorDebugEnum methods, and enumerates ICorDebugFrame arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b3d59-105">方法</span><span class="sxs-lookup"><span data-stu-id="b3d59-105">Methods</span></span>  
  
|<span data-ttu-id="b3d59-106">方法</span><span class="sxs-lookup"><span data-stu-id="b3d59-106">Method</span></span>|<span data-ttu-id="b3d59-107">说明</span><span class="sxs-lookup"><span data-stu-id="b3d59-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b3d59-108">下一方法</span><span class="sxs-lookup"><span data-stu-id="b3d59-108">Next Method</span></span>](icordebugframeenum-next-method.md)|<span data-ttu-id="b3d59-109">`ICorDebugFrame`从当前位置开始，从枚举中获取指定数目的实例。</span><span class="sxs-lookup"><span data-stu-id="b3d59-109">Gets the specified number of `ICorDebugFrame` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b3d59-110">备注</span><span class="sxs-lookup"><span data-stu-id="b3d59-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="b3d59-111">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="b3d59-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b3d59-112">要求</span><span class="sxs-lookup"><span data-stu-id="b3d59-112">Requirements</span></span>  

 <span data-ttu-id="b3d59-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b3d59-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b3d59-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b3d59-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b3d59-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b3d59-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b3d59-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b3d59-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b3d59-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="b3d59-117">See also</span></span>

- [<span data-ttu-id="b3d59-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="b3d59-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
