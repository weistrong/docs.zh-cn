---
description: 了解详细信息： ICorDebugBreakpointEnum 接口
title: ICorDebugBreakpointEnum 接口
ms.date: 03/30/2017
api_name:
- ICorDebugBreakpointEnum
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBreakpointEnum
helpviewer_keywords:
- ICorDebugBreakpointEnum interface [.NET Framework debugging]
ms.assetid: 4c6f4f6e-52cc-402e-881b-7b8526544c90
topic_type:
- apiref
ms.openlocfilehash: 71bd69c4fabba4a7d06f3b4cee5c0cf859d3c92b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711721"
---
# <a name="icordebugbreakpointenum-interface"></a><span data-ttu-id="d9aa3-103">ICorDebugBreakpointEnum 接口</span><span class="sxs-lookup"><span data-stu-id="d9aa3-103">ICorDebugBreakpointEnum Interface</span></span>

<span data-ttu-id="d9aa3-104">实现 ICorDebugEnum 方法，并枚举 ICorDebugBreakpoint 数组。</span><span class="sxs-lookup"><span data-stu-id="d9aa3-104">Implements ICorDebugEnum methods, and enumerates ICorDebugBreakpoint arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="d9aa3-105">方法</span><span class="sxs-lookup"><span data-stu-id="d9aa3-105">Methods</span></span>  
  
|<span data-ttu-id="d9aa3-106">方法</span><span class="sxs-lookup"><span data-stu-id="d9aa3-106">Method</span></span>|<span data-ttu-id="d9aa3-107">说明</span><span class="sxs-lookup"><span data-stu-id="d9aa3-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="d9aa3-108">下一方法</span><span class="sxs-lookup"><span data-stu-id="d9aa3-108">Next Method</span></span>](icordebugbreakpointenum-next-method.md)|<span data-ttu-id="d9aa3-109">`ICorDebugBreakpoint`从当前位置开始，从枚举中获取指定数目的实例。</span><span class="sxs-lookup"><span data-stu-id="d9aa3-109">Gets the specified number of `ICorDebugBreakpoint` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d9aa3-110">备注</span><span class="sxs-lookup"><span data-stu-id="d9aa3-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="d9aa3-111">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="d9aa3-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d9aa3-112">要求</span><span class="sxs-lookup"><span data-stu-id="d9aa3-112">Requirements</span></span>  

 <span data-ttu-id="d9aa3-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d9aa3-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d9aa3-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d9aa3-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d9aa3-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d9aa3-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d9aa3-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d9aa3-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d9aa3-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="d9aa3-117">See also</span></span>

- [<span data-ttu-id="d9aa3-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="d9aa3-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
