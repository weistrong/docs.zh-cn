---
description: 了解详细信息： ICorDebugCodeEnum 接口
title: ICorDebugCodeEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugCodeEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCodeEnum
helpviewer_keywords:
- ICorDebugCodeEnum interface [.NET Framework debugging]
ms.assetid: b5589171-a4a0-4c00-bbdc-6e0a42233b75
topic_type:
- apiref
ms.openlocfilehash: c2bf2ae5bcdbb1cae3222d0b8ed1f775689d3b84
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710967"
---
# <a name="icordebugcodeenum-interface"></a><span data-ttu-id="26bf9-103">ICorDebugCodeEnum 接口</span><span class="sxs-lookup"><span data-stu-id="26bf9-103">ICorDebugCodeEnum Interface</span></span>

<span data-ttu-id="26bf9-104">实现 "ICorDebugEnum" 方法，并枚举 "ICorDebugCode" 数组。</span><span class="sxs-lookup"><span data-stu-id="26bf9-104">Implements "ICorDebugEnum" methods, and enumerates "ICorDebugCode" arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="26bf9-105">方法</span><span class="sxs-lookup"><span data-stu-id="26bf9-105">Methods</span></span>  
  
|<span data-ttu-id="26bf9-106">方法</span><span class="sxs-lookup"><span data-stu-id="26bf9-106">Method</span></span>|<span data-ttu-id="26bf9-107">说明</span><span class="sxs-lookup"><span data-stu-id="26bf9-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="26bf9-108">下一方法</span><span class="sxs-lookup"><span data-stu-id="26bf9-108">Next Method</span></span>](icordebugcodeenum-next-method.md)|<span data-ttu-id="26bf9-109">`ICorDebugCode`从当前位置开始，从枚举中获取指定数目的实例。</span><span class="sxs-lookup"><span data-stu-id="26bf9-109">Gets the specified number of `ICorDebugCode` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="26bf9-110">备注</span><span class="sxs-lookup"><span data-stu-id="26bf9-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="26bf9-111">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="26bf9-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="26bf9-112">要求</span><span class="sxs-lookup"><span data-stu-id="26bf9-112">Requirements</span></span>  

 <span data-ttu-id="26bf9-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="26bf9-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="26bf9-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="26bf9-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="26bf9-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="26bf9-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="26bf9-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="26bf9-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="26bf9-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="26bf9-117">See also</span></span>

- [<span data-ttu-id="26bf9-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="26bf9-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
