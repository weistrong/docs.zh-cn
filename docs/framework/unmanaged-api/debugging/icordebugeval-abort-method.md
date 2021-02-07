---
description: 了解详细信息： ICorDebugEval：： Abort 方法
title: ICorDebugEval::Abort 方法
ms.date: 03/30/2017
api_name:
- ICorDebugEval.Abort
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::Abort
helpviewer_keywords:
- Abort method, ICorDebugEval interface [.NET Framework debugging]
- ICorDebugEval::Abort method [.NET Framework debugging]
ms.assetid: 7070b6d0-f2e0-44ff-b124-0944cd807e69
topic_type:
- apiref
ms.openlocfilehash: d61cb0d696a8a134d992bc8dbbfdb61103ef469f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99694313"
---
# <a name="icordebugevalabort-method"></a><span data-ttu-id="6ef2f-103">ICorDebugEval::Abort 方法</span><span class="sxs-lookup"><span data-stu-id="6ef2f-103">ICorDebugEval::Abort Method</span></span>

<span data-ttu-id="6ef2f-104">中止此 ICorDebugEval 对象当前正在执行的计算。</span><span class="sxs-lookup"><span data-stu-id="6ef2f-104">Aborts the computation this ICorDebugEval object is currently performing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6ef2f-105">语法</span><span class="sxs-lookup"><span data-stu-id="6ef2f-105">Syntax</span></span>  
  
```cpp  
HRESULT Abort ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="6ef2f-106">备注</span><span class="sxs-lookup"><span data-stu-id="6ef2f-106">Remarks</span></span>  

 <span data-ttu-id="6ef2f-107">如果计算是嵌套的，并且不是最新的，则该 `Abort` 方法可能会失败。</span><span class="sxs-lookup"><span data-stu-id="6ef2f-107">If the evaluation is nested and it is not the most recent one, the `Abort` method may fail.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6ef2f-108">要求</span><span class="sxs-lookup"><span data-stu-id="6ef2f-108">Requirements</span></span>  

 <span data-ttu-id="6ef2f-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6ef2f-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6ef2f-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6ef2f-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6ef2f-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6ef2f-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6ef2f-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6ef2f-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
