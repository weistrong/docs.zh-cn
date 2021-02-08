---
description: 了解详细信息： ICorDebugValueBreakpoint 接口
title: ICorDebugValueBreakpoint 接口
ms.date: 03/30/2017
api_name:
- ICorDebugValueBreakpoint
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValueBreakpoint
helpviewer_keywords:
- ICorDebugValueBreakpoint interface [.NET Framework debugging]
ms.assetid: c02338fe-da6c-467f-9567-70ebb387e901
topic_type:
- apiref
ms.openlocfilehash: ff53b1f6e1557a3e98cc642f80eaaa2feaeac473
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790680"
---
# <a name="icordebugvaluebreakpoint-interface"></a><span data-ttu-id="46a39-103">ICorDebugValueBreakpoint 接口</span><span class="sxs-lookup"><span data-stu-id="46a39-103">ICorDebugValueBreakpoint Interface</span></span>

<span data-ttu-id="46a39-104">扩展 ICorDebugBreakpoint 接口以提供对特定值的访问。</span><span class="sxs-lookup"><span data-stu-id="46a39-104">Extends the ICorDebugBreakpoint interface to provide access to specific values.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="46a39-105">方法</span><span class="sxs-lookup"><span data-stu-id="46a39-105">Methods</span></span>  
  
|<span data-ttu-id="46a39-106">方法</span><span class="sxs-lookup"><span data-stu-id="46a39-106">Method</span></span>|<span data-ttu-id="46a39-107">说明</span><span class="sxs-lookup"><span data-stu-id="46a39-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="46a39-108">GetValue 方法</span><span class="sxs-lookup"><span data-stu-id="46a39-108">GetValue Method</span></span>](icordebugvaluebreakpoint-getvalue-method.md)|<span data-ttu-id="46a39-109">获取一个指向 ICorDebugValue 对象的接口指针，该对象表示在其上设置断点的对象的值。</span><span class="sxs-lookup"><span data-stu-id="46a39-109">Gets an interface pointer to an ICorDebugValue object that represents the value of the object upon which the breakpoint is set.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="46a39-110">备注</span><span class="sxs-lookup"><span data-stu-id="46a39-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="46a39-111">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="46a39-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="46a39-112">要求</span><span class="sxs-lookup"><span data-stu-id="46a39-112">Requirements</span></span>  

 <span data-ttu-id="46a39-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="46a39-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="46a39-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="46a39-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="46a39-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="46a39-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="46a39-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="46a39-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46a39-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="46a39-117">See also</span></span>

- [<span data-ttu-id="46a39-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="46a39-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
