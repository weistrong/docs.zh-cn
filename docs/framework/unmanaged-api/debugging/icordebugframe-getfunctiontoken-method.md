---
description: 了解详细信息： ICorDebugFrame：： GetFunctionToken 方法
title: ICorDebugFrame::GetFunctionToken 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFrame.GetFunctionToken
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::GetFunctionToken
helpviewer_keywords:
- ICorDebugFrame::GetFunctionToken method [.NET Framework debugging]
- GetFunctionToken method [.NET Framework debugging]
ms.assetid: a46925b3-3bf8-404f-9f30-a86ae41032c1
topic_type:
- apiref
ms.openlocfilehash: c64bb8d59c8de03c3d8c667384ffe4118c996d8e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692935"
---
# <a name="icordebugframegetfunctiontoken-method"></a><span data-ttu-id="e0dfc-103">ICorDebugFrame::GetFunctionToken 方法</span><span class="sxs-lookup"><span data-stu-id="e0dfc-103">ICorDebugFrame::GetFunctionToken Method</span></span>

<span data-ttu-id="e0dfc-104">获取包含与此堆栈帧关联的代码的函数的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="e0dfc-104">Gets the metadata token for the function that contains the code associated with this stack frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e0dfc-105">语法</span><span class="sxs-lookup"><span data-stu-id="e0dfc-105">Syntax</span></span>  
  
```cpp  
HRESULT GetFunctionToken (  
    [out] mdMethodDef        *pToken  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e0dfc-106">参数</span><span class="sxs-lookup"><span data-stu-id="e0dfc-106">Parameters</span></span>  

 `pToken`  
 <span data-ttu-id="e0dfc-107">弄指向 `mdMethodDef` 引用函数的元数据的标记的指针。</span><span class="sxs-lookup"><span data-stu-id="e0dfc-107">[out] A pointer to an `mdMethodDef` token that references the metadata for the function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e0dfc-108">要求</span><span class="sxs-lookup"><span data-stu-id="e0dfc-108">Requirements</span></span>  

 <span data-ttu-id="e0dfc-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e0dfc-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e0dfc-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e0dfc-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e0dfc-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e0dfc-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e0dfc-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e0dfc-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
