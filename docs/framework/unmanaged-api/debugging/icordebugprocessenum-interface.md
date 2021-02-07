---
description: 了解详细信息： ICorDebugProcessEnum 接口
title: ICorDebugProcessEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugProcessEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcessEnum
helpviewer_keywords:
- ICorDebugProcessEnum interface [.NET Framework debugging]
ms.assetid: b63a507a-ca97-4be0-8e4f-401cce2125f6
topic_type:
- apiref
ms.openlocfilehash: 3bb70d2a826be84ecb680014efe5ed918d98e861
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99691206"
---
# <a name="icordebugprocessenum-interface"></a><span data-ttu-id="d414b-103">ICorDebugProcessEnum 接口</span><span class="sxs-lookup"><span data-stu-id="d414b-103">ICorDebugProcessEnum Interface</span></span>

<span data-ttu-id="d414b-104">实现 ICorDebugEnum 方法并枚举 ICorDebugProcess 数组。</span><span class="sxs-lookup"><span data-stu-id="d414b-104">Implements ICorDebugEnum methods and enumerates ICorDebugProcess arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d414b-105">方法</span><span class="sxs-lookup"><span data-stu-id="d414b-105">Methods</span></span>  
  
|<span data-ttu-id="d414b-106">方法</span><span class="sxs-lookup"><span data-stu-id="d414b-106">Method</span></span>|<span data-ttu-id="d414b-107">说明</span><span class="sxs-lookup"><span data-stu-id="d414b-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d414b-108">下一方法</span><span class="sxs-lookup"><span data-stu-id="d414b-108">Next Method</span></span>](icordebugprocessenum-next-method.md)|<span data-ttu-id="d414b-109">`ICorDebugProcess`从当前位置开始，从枚举中获取指定数目的实例。</span><span class="sxs-lookup"><span data-stu-id="d414b-109">Gets the specified number of `ICorDebugProcess` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d414b-110">备注</span><span class="sxs-lookup"><span data-stu-id="d414b-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="d414b-111">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="d414b-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d414b-112">要求</span><span class="sxs-lookup"><span data-stu-id="d414b-112">Requirements</span></span>  

 <span data-ttu-id="d414b-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d414b-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d414b-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d414b-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d414b-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d414b-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d414b-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d414b-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d414b-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="d414b-117">See also</span></span>

- [<span data-ttu-id="d414b-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="d414b-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
