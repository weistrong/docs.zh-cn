---
description: 了解详细信息： ICorDebugUnmanagedCallback 接口
title: ICorDebugUnmanagedCallback 接口
ms.date: 03/30/2017
api_name:
- ICorDebugUnmanagedCallback
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugUnmanagedCallback
helpviewer_keywords:
- ICorDebugUnmanagedCallback interface [.NET Framework debugging]
ms.assetid: bc71cbca-7d73-40e5-84dd-2109fade3c2a
topic_type:
- apiref
ms.openlocfilehash: 6d8aa398ff7121e360c3da66671781cd169b6228
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99690543"
---
# <a name="icordebugunmanagedcallback-interface"></a><span data-ttu-id="3286d-103">ICorDebugUnmanagedCallback 接口</span><span class="sxs-lookup"><span data-stu-id="3286d-103">ICorDebugUnmanagedCallback Interface</span></span>

<span data-ttu-id="3286d-104">提供与公共语言运行时 (CLR) 不直接相关的本机事件的通知。</span><span class="sxs-lookup"><span data-stu-id="3286d-104">Provides notification of native events that are not directly related to the common language runtime (CLR).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="3286d-105">方法</span><span class="sxs-lookup"><span data-stu-id="3286d-105">Methods</span></span>  
  
|<span data-ttu-id="3286d-106">方法</span><span class="sxs-lookup"><span data-stu-id="3286d-106">Method</span></span>|<span data-ttu-id="3286d-107">说明</span><span class="sxs-lookup"><span data-stu-id="3286d-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="3286d-108">DebugEvent 方法</span><span class="sxs-lookup"><span data-stu-id="3286d-108">DebugEvent Method</span></span>](icordebugunmanagedcallback-debugevent-method.md)|<span data-ttu-id="3286d-109">通知调试器已激发本机事件。</span><span class="sxs-lookup"><span data-stu-id="3286d-109">Notifies the debugger that a native event has been fired.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3286d-110">备注</span><span class="sxs-lookup"><span data-stu-id="3286d-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="3286d-111">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="3286d-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3286d-112">要求</span><span class="sxs-lookup"><span data-stu-id="3286d-112">Requirements</span></span>  

 <span data-ttu-id="3286d-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3286d-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3286d-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="3286d-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3286d-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3286d-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3286d-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3286d-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3286d-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="3286d-117">See also</span></span>

- [<span data-ttu-id="3286d-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="3286d-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
