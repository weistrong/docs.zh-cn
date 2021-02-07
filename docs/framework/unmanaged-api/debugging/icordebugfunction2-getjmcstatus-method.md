---
description: 了解详细信息： ICorDebugFunction2：： GetJMCStatus 方法
title: ICorDebugFunction2::GetJMCStatus 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFunction2.GetJMCStatus
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction2::GetJMCStatus
helpviewer_keywords:
- ICorDebugFunction2::GetJMCStatus method [.NET Framework debugging]
- GetJMCStatus method [.NET Framework debugging]
ms.assetid: 840a71ed-bf5a-4f5e-8ed6-762222b34493
topic_type:
- apiref
ms.openlocfilehash: 42c72256df57b96a52737f4a0e5e90d6ba5d4e0c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692285"
---
# <a name="icordebugfunction2getjmcstatus-method"></a><span data-ttu-id="f2e54-103">ICorDebugFunction2::GetJMCStatus 方法</span><span class="sxs-lookup"><span data-stu-id="f2e54-103">ICorDebugFunction2::GetJMCStatus Method</span></span>

<span data-ttu-id="f2e54-104">获取一个值，该值指示此 ICorDebugFunction2 对象表示的函数是否被标记为 "用户代码"。</span><span class="sxs-lookup"><span data-stu-id="f2e54-104">Gets a value that indicates whether the function that is represented by this ICorDebugFunction2 object is marked as user code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f2e54-105">语法</span><span class="sxs-lookup"><span data-stu-id="f2e54-105">Syntax</span></span>  
  
```cpp  
HRESULT GetJMCStatus (  
    [out] BOOL   *pbIsJustMyCode  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f2e54-106">参数</span><span class="sxs-lookup"><span data-stu-id="f2e54-106">Parameters</span></span>  

 `pbIsJustMyCode`  
 <span data-ttu-id="f2e54-107">弄 `true`如果此函数标记为用户代码，则为指向布尔值的指针; 否则，该值为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="f2e54-107">[out] A pointer to a Boolean value that is `true`, if this function is marked as user code; otherwise, the value is `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f2e54-108">备注</span><span class="sxs-lookup"><span data-stu-id="f2e54-108">Remarks</span></span>  

 <span data-ttu-id="f2e54-109">如果此表示的函数 `ICorDebugFunction2` 无法调试， `pbIsJustMyCode` 将始终为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="f2e54-109">If the function represented by this `ICorDebugFunction2` cannot be debugged, `pbIsJustMyCode` will always be `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f2e54-110">要求</span><span class="sxs-lookup"><span data-stu-id="f2e54-110">Requirements</span></span>  

 <span data-ttu-id="f2e54-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f2e54-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f2e54-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f2e54-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f2e54-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f2e54-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f2e54-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f2e54-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
