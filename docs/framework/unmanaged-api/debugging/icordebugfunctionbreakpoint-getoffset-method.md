---
description: 了解详细信息： ICorDebugFunctionBreakpoint：： GetOffset 方法
title: ICorDebugFunctionBreakpoint::GetOffset 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFunctionBreakpoint.GetOffset
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunctionBreakpoint::GetOffset
helpviewer_keywords:
- ICorDebugFunctionBreakpoint::GetOffset method [.NET Framework debugging]
- GetOffset method, ICorDebugFunctionBreakpoint interface [.NET Framework debugging]
ms.assetid: e619eae4-3ac3-4c37-bba4-55e59989b9cb
topic_type:
- apiref
ms.openlocfilehash: 94238b761e0a42a72037f7d44d5e9609f86ac03b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99661157"
---
# <a name="icordebugfunctionbreakpointgetoffset-method"></a><span data-ttu-id="cf2ad-103">ICorDebugFunctionBreakpoint::GetOffset 方法</span><span class="sxs-lookup"><span data-stu-id="cf2ad-103">ICorDebugFunctionBreakpoint::GetOffset Method</span></span>

<span data-ttu-id="cf2ad-104">获取函数内断点的偏移量。</span><span class="sxs-lookup"><span data-stu-id="cf2ad-104">Gets the offset of the breakpoint within the function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cf2ad-105">语法</span><span class="sxs-lookup"><span data-stu-id="cf2ad-105">Syntax</span></span>  
  
```cpp  
HRESULT GetOffset (  
    [out] ULONG32  *pnOffset  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cf2ad-106">参数</span><span class="sxs-lookup"><span data-stu-id="cf2ad-106">Parameters</span></span>  

 `pnOffset`  
 <span data-ttu-id="cf2ad-107">弄指向断点偏移量的指针。</span><span class="sxs-lookup"><span data-stu-id="cf2ad-107">[out] A pointer to the offset of the breakpoint.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cf2ad-108">要求</span><span class="sxs-lookup"><span data-stu-id="cf2ad-108">Requirements</span></span>  

 <span data-ttu-id="cf2ad-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cf2ad-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cf2ad-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="cf2ad-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="cf2ad-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="cf2ad-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="cf2ad-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cf2ad-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
