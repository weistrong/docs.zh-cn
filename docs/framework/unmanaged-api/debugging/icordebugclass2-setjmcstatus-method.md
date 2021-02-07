---
description: 了解详细信息： ICorDebugClass2：： SetJMCStatus 方法
title: ICorDebugClass2::SetJMCStatus 方法
ms.date: 03/30/2017
api_name:
- ICorDebugClass2.SetJMCStatus
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugClass2::SetJMCStatus
helpviewer_keywords:
- ICorDebugClass2::SetJMCStatus method [.NET Framework debugging]
- SetJMCStatus method, ICorDebugClass2 interface [.NET Framework debugging]
ms.assetid: 077e6c7f-f857-480c-bebb-76ee1de4e8fc
topic_type:
- apiref
ms.openlocfilehash: 28859522052fd9587dc3890eb4137929dbdc6763
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711439"
---
# <a name="icordebugclass2setjmcstatus-method"></a><span data-ttu-id="5bfa1-103">ICorDebugClass2::SetJMCStatus 方法</span><span class="sxs-lookup"><span data-stu-id="5bfa1-103">ICorDebugClass2::SetJMCStatus Method</span></span>

<span data-ttu-id="5bfa1-104">对于类的每个方法，设置一个值，该值指示该方法是否为用户定义的代码。</span><span class="sxs-lookup"><span data-stu-id="5bfa1-104">For each method of the class, sets a value that indicates whether the method is user-defined code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5bfa1-105">语法</span><span class="sxs-lookup"><span data-stu-id="5bfa1-105">Syntax</span></span>  
  
```cpp  
HRESULT SetJMCStatus (  
    [in] BOOL   bIsJustMyCode  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5bfa1-106">参数</span><span class="sxs-lookup"><span data-stu-id="5bfa1-106">Parameters</span></span>  

 `bIsJustMyCode`  
 <span data-ttu-id="5bfa1-107">中如果设置为，则 `true` 指示该方法是用户定义的代码; 否则设置为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="5bfa1-107">[in] Set to `true` to indicate that the method is user-defined code; otherwise, set to `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5bfa1-108">备注</span><span class="sxs-lookup"><span data-stu-id="5bfa1-108">Remarks</span></span>  

 <span data-ttu-id="5bfa1-109">) 分档器 (JMC 的简单代码将跳过非用户定义的代码。</span><span class="sxs-lookup"><span data-stu-id="5bfa1-109">A just-my-code (JMC) stepper will skip non-user-defined code.</span></span> <span data-ttu-id="5bfa1-110">用户定义的代码必须是可调试代码的子集。</span><span class="sxs-lookup"><span data-stu-id="5bfa1-110">User-defined code must be a subset of debuggable code.</span></span>  
  
 <span data-ttu-id="5bfa1-111">`SetJMCStatus` 如果无法为任何方法设置值，则返回 S_FALSE 的 HRESULT 值，即使它成功设置了所有其他方法的值也是如此。</span><span class="sxs-lookup"><span data-stu-id="5bfa1-111">`SetJMCStatus` returns an HRESULT value of S_FALSE if it fails to set the value for any method, even if it successfully sets the value for all other methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5bfa1-112">要求</span><span class="sxs-lookup"><span data-stu-id="5bfa1-112">Requirements</span></span>  

 <span data-ttu-id="5bfa1-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5bfa1-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5bfa1-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5bfa1-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5bfa1-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5bfa1-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5bfa1-116">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5bfa1-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
