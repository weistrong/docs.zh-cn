---
description: 了解详细信息： ICorDebugAssembly2：： IsFullyTrusted 方法
title: ICorDebugAssembly2::IsFullyTrusted 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAssembly2.IsFullyTrusted
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssembly2::IsFullyTrusted
helpviewer_keywords:
- ICorDebugAssembly2::IsFullyTrusted method [.NET Framework debugging]
- IsFullyTrusted method [.NET Framework debugging]
ms.assetid: 26cbd27d-12bf-444a-8197-ccd14d37dda3
topic_type:
- apiref
ms.openlocfilehash: bc1c4d9a4fa84bac3469aafe8aaa061473e50413
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754103"
---
# <a name="icordebugassembly2isfullytrusted-method"></a><span data-ttu-id="91244-103">ICorDebugAssembly2::IsFullyTrusted 方法</span><span class="sxs-lookup"><span data-stu-id="91244-103">ICorDebugAssembly2::IsFullyTrusted Method</span></span>

<span data-ttu-id="91244-104">获取一个值，该值指示运行时安全系统是否已向程序集授予完全信任。</span><span class="sxs-lookup"><span data-stu-id="91244-104">Gets a value that indicates whether the assembly has been granted full trust by the runtime security system.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="91244-105">语法</span><span class="sxs-lookup"><span data-stu-id="91244-105">Syntax</span></span>  
  
```cpp  
HRESULT IsFullyTrusted(  
    [out] BOOL *pbFullyTrusted  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="91244-106">参数</span><span class="sxs-lookup"><span data-stu-id="91244-106">Parameters</span></span>  

 `pbFullyTrusted`  
 <span data-ttu-id="91244-107">[out] `true` 如果程序集已被运行时安全系统授予完全信任，则为; 否则为。否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="91244-107">[out] `true` if the assembly has been granted full trust by the runtime security system; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="91244-108">备注</span><span class="sxs-lookup"><span data-stu-id="91244-108">Remarks</span></span>  

 <span data-ttu-id="91244-109">如果程序集的安全策略尚未解析（即，如果尚未运行程序集中的代码），则此方法将返回 CORDBG_E_NOTREADY 的 HRESULT。</span><span class="sxs-lookup"><span data-stu-id="91244-109">This method returns an HRESULT of CORDBG_E_NOTREADY if the security policy for the assembly has not yet been resolved, that is, if no code in the assembly has been run yet.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="91244-110">要求</span><span class="sxs-lookup"><span data-stu-id="91244-110">Requirements</span></span>  

 <span data-ttu-id="91244-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="91244-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="91244-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="91244-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="91244-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="91244-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="91244-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="91244-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
