---
description: 了解详细信息： ICorDebugCode4 接口
title: ICorDebugCode4 接口
ms.date: 03/30/2017
api_name:
- ICorDebugCode4
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode4
helpviewer_keywords:
- ICorDebugCode4 interface [.NET Framework debugging]
ms.assetid: a3fdf523-274a-449c-920b-9fcb0aed1d97
topic_type:
- apiref
ms.openlocfilehash: 1276db5c55c3d98e5ffa379f6126f700d93c1670
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99764718"
---
# <a name="icordebugcode4-interface"></a><span data-ttu-id="58fb5-103">ICorDebugCode4 接口</span><span class="sxs-lookup"><span data-stu-id="58fb5-103">ICorDebugCode4 Interface</span></span>

<span data-ttu-id="58fb5-104">提供一个方法，该方法使调试器可以枚举函数中的局部变量和参数。</span><span class="sxs-lookup"><span data-stu-id="58fb5-104">Provides a method that enables a debugger to enumerate the local variables and arguments in a function.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="58fb5-105">方法</span><span class="sxs-lookup"><span data-stu-id="58fb5-105">Methods</span></span>  
  
|<span data-ttu-id="58fb5-106">方法</span><span class="sxs-lookup"><span data-stu-id="58fb5-106">Method</span></span>|<span data-ttu-id="58fb5-107">说明</span><span class="sxs-lookup"><span data-stu-id="58fb5-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="58fb5-108">EnumerateVariableHomes 方法</span><span class="sxs-lookup"><span data-stu-id="58fb5-108">EnumerateVariableHomes Method</span></span>](icordebugcode4-enumeratevariablehomes-method.md)|<span data-ttu-id="58fb5-109">获取函数中局部变量和参数的枚举器。</span><span class="sxs-lookup"><span data-stu-id="58fb5-109">Gets an enumerator to the local variables and arguments in a function.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="58fb5-110">备注</span><span class="sxs-lookup"><span data-stu-id="58fb5-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="58fb5-111">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="58fb5-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="58fb5-112">要求</span><span class="sxs-lookup"><span data-stu-id="58fb5-112">Requirements</span></span>  

 <span data-ttu-id="58fb5-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="58fb5-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="58fb5-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="58fb5-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="58fb5-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="58fb5-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="58fb5-116">**.NET Framework 版本：**[!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="58fb5-116">**.NET Framework Versions:** [!INCLUDE[net_current_v462plus](../../../../includes/net-current-v462plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="58fb5-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="58fb5-117">See also</span></span>

- [<span data-ttu-id="58fb5-118">ICorDebugCode3 接口</span><span class="sxs-lookup"><span data-stu-id="58fb5-118">ICorDebugCode3 Interface</span></span>](icordebugcode3-interface.md)
- [<span data-ttu-id="58fb5-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="58fb5-119">Debugging Interfaces</span></span>](debugging-interfaces.md)
