---
description: 了解详细信息： ICorDebugBreakpoint：： Activate 方法
title: ICorDebugBreakpoint::Activate 方法
ms.date: 03/30/2017
api_name:
- ICorDebugBreakpoint.Activate
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBreakpoint::Activate
helpviewer_keywords:
- ICorDebugBreakpoint::Activate method [.NET Framework debugging]
- Activate method [.NET Framework debugging]
ms.assetid: e30c29f7-3f19-4081-b572-a731aa14cd44
topic_type:
- apiref
ms.openlocfilehash: 1a3613ae071b3fc6c4f1005eafd515946d6b2685
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711840"
---
# <a name="icordebugbreakpointactivate-method"></a><span data-ttu-id="f18eb-103">ICorDebugBreakpoint::Activate 方法</span><span class="sxs-lookup"><span data-stu-id="f18eb-103">ICorDebugBreakpoint::Activate Method</span></span>

<span data-ttu-id="f18eb-104">设置此的活动状态 `ICorDebugBreakpoint` 。</span><span class="sxs-lookup"><span data-stu-id="f18eb-104">Sets the active state of this `ICorDebugBreakpoint`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f18eb-105">语法</span><span class="sxs-lookup"><span data-stu-id="f18eb-105">Syntax</span></span>  
  
```cpp  
HRESULT Activate (  
    [in] BOOL bActive  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f18eb-106">参数</span><span class="sxs-lookup"><span data-stu-id="f18eb-106">Parameters</span></span>  

 `bActive`  
 <span data-ttu-id="f18eb-107">中将此值设置为 `true` 可将状态指定为活动; 否则，请将此值设置为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="f18eb-107">[in] Set this value to `true` to specify the state as active; otherwise, set this value to `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f18eb-108">要求</span><span class="sxs-lookup"><span data-stu-id="f18eb-108">Requirements</span></span>  

 <span data-ttu-id="f18eb-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f18eb-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f18eb-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f18eb-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f18eb-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f18eb-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f18eb-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f18eb-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
