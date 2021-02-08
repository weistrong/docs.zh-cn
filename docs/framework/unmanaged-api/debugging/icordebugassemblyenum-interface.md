---
description: 了解详细信息： ICorDebugAssemblyEnum 接口
title: ICorDebugAssemblyEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugAssemblyEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssemblyEnum
helpviewer_keywords:
- ICorDebugAssemblyEnum interface [.NET Framework debugging]
ms.assetid: 891ceb43-5161-421e-a0bf-299962fd7efd
topic_type:
- apiref
ms.openlocfilehash: e9dab7560da10efcb33fc48f5718f26b960cdaa3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791486"
---
# <a name="icordebugassemblyenum-interface"></a><span data-ttu-id="d8b02-103">ICorDebugAssemblyEnum 接口</span><span class="sxs-lookup"><span data-stu-id="d8b02-103">ICorDebugAssemblyEnum Interface</span></span>

<span data-ttu-id="d8b02-104">实现 ICorDebugEnum 方法并枚举 ICorDebugAssembly 数组。</span><span class="sxs-lookup"><span data-stu-id="d8b02-104">Implements ICorDebugEnum methods and enumerates ICorDebugAssembly arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d8b02-105">方法</span><span class="sxs-lookup"><span data-stu-id="d8b02-105">Methods</span></span>  
  
|<span data-ttu-id="d8b02-106">方法</span><span class="sxs-lookup"><span data-stu-id="d8b02-106">Method</span></span>|<span data-ttu-id="d8b02-107">说明</span><span class="sxs-lookup"><span data-stu-id="d8b02-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d8b02-108">下一方法</span><span class="sxs-lookup"><span data-stu-id="d8b02-108">Next Method</span></span>](icordebugassemblyenum-next-method.md)|<span data-ttu-id="d8b02-109">`ICorDebugAssembly`从当前位置开始，获取枚举中指定数量的实例。</span><span class="sxs-lookup"><span data-stu-id="d8b02-109">Gets the specified number of `ICorDebugAssembly` instances in the enumeration, starting from the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d8b02-110">备注</span><span class="sxs-lookup"><span data-stu-id="d8b02-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="d8b02-111">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="d8b02-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d8b02-112">要求</span><span class="sxs-lookup"><span data-stu-id="d8b02-112">Requirements</span></span>  

 <span data-ttu-id="d8b02-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d8b02-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d8b02-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d8b02-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d8b02-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d8b02-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d8b02-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d8b02-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d8b02-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="d8b02-117">See also</span></span>

- [<span data-ttu-id="d8b02-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="d8b02-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
