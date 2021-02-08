---
description: 了解详细信息： ICorDebugModuleBreakpoint：： GetModule 方法
title: ICorDebugModuleBreakpoint::GetModule 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModuleBreakpoint.GetModule
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModuleBreakpoint::GetModule
helpviewer_keywords:
- ICorDebugModuleBreakpoint::GetModule method [.NET Framework debugging]
- GetModule method, ICorDebugModuleBreakpoint interface [.NET Framework debugging]
ms.assetid: ffd5d9ec-4564-4200-b625-b306eec0ebd7
topic_type:
- apiref
ms.openlocfilehash: 3498f9d644d6195f2cd0f83d30417c447d200f3e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790784"
---
# <a name="icordebugmodulebreakpointgetmodule-method"></a><span data-ttu-id="24b06-103">ICorDebugModuleBreakpoint::GetModule 方法</span><span class="sxs-lookup"><span data-stu-id="24b06-103">ICorDebugModuleBreakpoint::GetModule Method</span></span>

<span data-ttu-id="24b06-104">获取一个指向 "ICorDebugModule" 的接口指针，该指针引用设置此断点的模块。</span><span class="sxs-lookup"><span data-stu-id="24b06-104">Gets an interface pointer to an "ICorDebugModule" that references the module in which this breakpoint is set.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="24b06-105">语法</span><span class="sxs-lookup"><span data-stu-id="24b06-105">Syntax</span></span>  
  
```cpp  
HRESULT GetModule (  
    [out] ICorDebugModule   **ppModule  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="24b06-106">参数</span><span class="sxs-lookup"><span data-stu-id="24b06-106">Parameters</span></span>  

 `ppModule`  
 <span data-ttu-id="24b06-107">弄指向接口的地址的指针 `ICorDebugModule` ，该接口引用在其中设置断点的模块。</span><span class="sxs-lookup"><span data-stu-id="24b06-107">[out] A pointer to the address of an `ICorDebugModule` interface that references the module in which the breakpoint is set.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="24b06-108">要求</span><span class="sxs-lookup"><span data-stu-id="24b06-108">Requirements</span></span>  

 <span data-ttu-id="24b06-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="24b06-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="24b06-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="24b06-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="24b06-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="24b06-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="24b06-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="24b06-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="24b06-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="24b06-113">See also</span></span>
