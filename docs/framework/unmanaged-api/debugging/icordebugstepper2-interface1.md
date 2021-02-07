---
description: 了解详细信息： ICorDebugStepper2 接口
title: ICorDebugStepper2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugStepper2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugStepper2
helpviewer_keywords:
- ICorDebugStepper2 interface [.NET Framework debugging]
ms.assetid: 7a191c2a-95ea-4d47-83b0-44de2b632d63
topic_type:
- apiref
ms.openlocfilehash: 31e9216535da239573a7a4ecde8cb2e670ad5418
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99717545"
---
# <a name="icordebugstepper2-interface"></a><span data-ttu-id="be49e-103">ICorDebugStepper2 接口</span><span class="sxs-lookup"><span data-stu-id="be49e-103">ICorDebugStepper2 Interface</span></span>

<span data-ttu-id="be49e-104"> (JMC) 调试提供 "仅我的代码" 支持。</span><span class="sxs-lookup"><span data-stu-id="be49e-104">Provides support for just my code (JMC) debugging.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="be49e-105">方法</span><span class="sxs-lookup"><span data-stu-id="be49e-105">Methods</span></span>  
  
|<span data-ttu-id="be49e-106">方法</span><span class="sxs-lookup"><span data-stu-id="be49e-106">Method</span></span>|<span data-ttu-id="be49e-107">说明</span><span class="sxs-lookup"><span data-stu-id="be49e-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="be49e-108">SetJMC 方法</span><span class="sxs-lookup"><span data-stu-id="be49e-108">SetJMC Method</span></span>](icordebugstepper2-setjmc-method.md)|<span data-ttu-id="be49e-109">设置一个值，该值指定此 ICorDebugStepper 是否仅通过应用程序开发人员编写的代码执行步骤。</span><span class="sxs-lookup"><span data-stu-id="be49e-109">Sets a value that specifies whether this ICorDebugStepper steps only through code that is authored by an application's developer.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="be49e-110">备注</span><span class="sxs-lookup"><span data-stu-id="be49e-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="be49e-111">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="be49e-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="be49e-112">要求</span><span class="sxs-lookup"><span data-stu-id="be49e-112">Requirements</span></span>  

 <span data-ttu-id="be49e-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="be49e-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="be49e-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="be49e-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="be49e-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="be49e-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="be49e-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="be49e-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="be49e-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="be49e-117">See also</span></span>

- [<span data-ttu-id="be49e-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="be49e-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
