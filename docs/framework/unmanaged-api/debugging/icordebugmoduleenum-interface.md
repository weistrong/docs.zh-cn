---
description: 了解详细信息： ICorDebugModuleEnum 接口
title: ICorDebugModuleEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugModuleEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModuleEnum
helpviewer_keywords:
- ICorDebugModuleEnum interface [.NET Framework debugging]
ms.assetid: 2fb93cd6-6d47-4fdc-a9a0-047726fd03a1
topic_type:
- apiref
ms.openlocfilehash: c9c847f926984ed2b8aea87463e351cd97a62c80
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801041"
---
# <a name="icordebugmoduleenum-interface"></a><span data-ttu-id="6081a-103">ICorDebugModuleEnum 接口</span><span class="sxs-lookup"><span data-stu-id="6081a-103">ICorDebugModuleEnum Interface</span></span>

<span data-ttu-id="6081a-104">实现 ICorDebugEnum 方法，并枚举 ICorDebugModule 数组。</span><span class="sxs-lookup"><span data-stu-id="6081a-104">Implements ICorDebugEnum methods, and enumerates ICorDebugModule arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="6081a-105">方法</span><span class="sxs-lookup"><span data-stu-id="6081a-105">Methods</span></span>  
  
|<span data-ttu-id="6081a-106">方法</span><span class="sxs-lookup"><span data-stu-id="6081a-106">Method</span></span>|<span data-ttu-id="6081a-107">说明</span><span class="sxs-lookup"><span data-stu-id="6081a-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="6081a-108">下一方法</span><span class="sxs-lookup"><span data-stu-id="6081a-108">Next Method</span></span>](icordebugmoduleenum-next-method.md)|<span data-ttu-id="6081a-109">`ICorDebugModule`从当前位置开始，从枚举中获取指定数目的实例。</span><span class="sxs-lookup"><span data-stu-id="6081a-109">Gets the specified number of `ICorDebugModule` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6081a-110">备注</span><span class="sxs-lookup"><span data-stu-id="6081a-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="6081a-111">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="6081a-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6081a-112">要求</span><span class="sxs-lookup"><span data-stu-id="6081a-112">Requirements</span></span>  

 <span data-ttu-id="6081a-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6081a-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6081a-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6081a-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6081a-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6081a-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6081a-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6081a-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6081a-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="6081a-117">See also</span></span>

- [<span data-ttu-id="6081a-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="6081a-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
