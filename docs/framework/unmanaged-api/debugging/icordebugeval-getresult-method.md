---
description: 了解详细信息： ICorDebugEval：： GetResult 方法
title: ICorDebugEval::GetResult 方法
ms.date: 03/30/2017
api_name:
- ICorDebugEval.GetResult
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::GetResult
helpviewer_keywords:
- ICorDebugEval::GetResult method [.NET Framework debugging]
- GetResult method [.NET Framework debugging]
ms.assetid: 50dbb9af-58a1-41f4-b56d-3da20011884f
topic_type:
- apiref
ms.openlocfilehash: 03ab00f5c9a538e11a2046da9cbfd5ad7225231c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99694209"
---
# <a name="icordebugevalgetresult-method"></a><span data-ttu-id="bcb90-103">ICorDebugEval::GetResult 方法</span><span class="sxs-lookup"><span data-stu-id="bcb90-103">ICorDebugEval::GetResult Method</span></span>

<span data-ttu-id="bcb90-104">获取此计算的结果。</span><span class="sxs-lookup"><span data-stu-id="bcb90-104">Gets the results of this evaluation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bcb90-105">语法</span><span class="sxs-lookup"><span data-stu-id="bcb90-105">Syntax</span></span>  
  
```cpp  
HRESULT GetResult (  
    [out] ICorDebugValue    **ppResult  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bcb90-106">参数</span><span class="sxs-lookup"><span data-stu-id="bcb90-106">Parameters</span></span>  

 `ppResult`  
 <span data-ttu-id="bcb90-107">弄一个指针，指向表示此计算结果的 ICorDebugValue 对象的地址（如果计算正常完成）。</span><span class="sxs-lookup"><span data-stu-id="bcb90-107">[out] Pointer to the address of an ICorDebugValue object that represents the results of this evaluation, if the evaluation completes normally.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bcb90-108">备注</span><span class="sxs-lookup"><span data-stu-id="bcb90-108">Remarks</span></span>  

 <span data-ttu-id="bcb90-109">此 `GetResult` 方法仅在计算完成后有效。</span><span class="sxs-lookup"><span data-stu-id="bcb90-109">The `GetResult` method is valid only after the evaluation is completed.</span></span>  
  
 <span data-ttu-id="bcb90-110">如果计算正常完成，则 `ppResult` 指定结果。</span><span class="sxs-lookup"><span data-stu-id="bcb90-110">If the evaluation completes normally, `ppResult` specifies the results.</span></span> <span data-ttu-id="bcb90-111">如果终止时出现异常，则结果为引发的异常。</span><span class="sxs-lookup"><span data-stu-id="bcb90-111">If it terminates with an exception, the result is the exception thrown.</span></span> <span data-ttu-id="bcb90-112">如果计算为新的对象，则结果是对新的对象的引用。</span><span class="sxs-lookup"><span data-stu-id="bcb90-112">If the evaluation was for a new object, the result is the reference to the new object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bcb90-113">要求</span><span class="sxs-lookup"><span data-stu-id="bcb90-113">Requirements</span></span>  

 <span data-ttu-id="bcb90-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bcb90-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bcb90-115">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="bcb90-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="bcb90-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bcb90-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bcb90-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bcb90-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
