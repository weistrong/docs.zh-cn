---
description: 了解详细信息： ICorDebugBreakpoint：： IsActive 方法
title: ICorDebugBreakpoint::IsActive 方法
ms.date: 03/30/2017
api_name:
- ICorDebugBreakpoint.IsActive
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBreakpoint::IsActive
helpviewer_keywords:
- ICorDebugBreakpoint::IsActive method [.NET Framework debugging]
- IsActive method, ICorDebugBreakpoint interface [.NET Framework debugging]
ms.assetid: 06e583d6-d88a-4ff5-bb95-5c48618a461c
topic_type:
- apiref
ms.openlocfilehash: 49e98ccc3722c37b3ff5968215ef3f658601ea10
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711786"
---
# <a name="icordebugbreakpointisactive-method"></a><span data-ttu-id="848c7-103">ICorDebugBreakpoint::IsActive 方法</span><span class="sxs-lookup"><span data-stu-id="848c7-103">ICorDebugBreakpoint::IsActive Method</span></span>

<span data-ttu-id="848c7-104">获取一个值，该值指示此是否处于 `ICorDebugBreakpoint` 活动状态。</span><span class="sxs-lookup"><span data-stu-id="848c7-104">Gets a value that indicates whether this `ICorDebugBreakpoint` is active.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="848c7-105">语法</span><span class="sxs-lookup"><span data-stu-id="848c7-105">Syntax</span></span>  
  
```cpp  
HRESULT IsActive (  
    [out] BOOL *pbActive  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="848c7-106">参数</span><span class="sxs-lookup"><span data-stu-id="848c7-106">Parameters</span></span>  

 `pbActive`  
 <span data-ttu-id="848c7-107">[out] `true` 如果此断点处于活动状态，则为;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="848c7-107">[out] `true` if this breakpoint is active; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="848c7-108">要求</span><span class="sxs-lookup"><span data-stu-id="848c7-108">Requirements</span></span>  

 <span data-ttu-id="848c7-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="848c7-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="848c7-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="848c7-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="848c7-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="848c7-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="848c7-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="848c7-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
