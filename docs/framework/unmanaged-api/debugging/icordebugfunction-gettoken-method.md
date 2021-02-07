---
description: 了解详细信息： ICorDebugFunction：： GetToken 方法
title: ICorDebugFunction::GetToken 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFunction.GetToken
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction::GetToken
helpviewer_keywords:
- ICorDebugFunction::GetToken method [.NET Framework debugging]
- GetToken method, ICorDebugFunction interface [.NET Framework debugging]
ms.assetid: c6bbf479-062e-48e9-9c70-0f92e293e36a
topic_type:
- apiref
ms.openlocfilehash: 75c8680252c5047aa7263940da76166597e5a283
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692415"
---
# <a name="icordebugfunctiongettoken-method"></a><span data-ttu-id="df46a-103">ICorDebugFunction::GetToken 方法</span><span class="sxs-lookup"><span data-stu-id="df46a-103">ICorDebugFunction::GetToken Method</span></span>

<span data-ttu-id="df46a-104">获取此函数的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="df46a-104">Gets the metadata token for this function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="df46a-105">语法</span><span class="sxs-lookup"><span data-stu-id="df46a-105">Syntax</span></span>  
  
```cpp  
HRESULT GetToken (  
    [out] mdMethodDef *pMethodDef  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="df46a-106">参数</span><span class="sxs-lookup"><span data-stu-id="df46a-106">Parameters</span></span>  

 `pMethodDef`  
 <span data-ttu-id="df46a-107">弄指向 `mdMethodDef` 引用此函数的元数据的标记的指针。</span><span class="sxs-lookup"><span data-stu-id="df46a-107">[out] A pointer to an `mdMethodDef` token that references the metadata for this function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="df46a-108">要求</span><span class="sxs-lookup"><span data-stu-id="df46a-108">Requirements</span></span>  

 <span data-ttu-id="df46a-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="df46a-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="df46a-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="df46a-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="df46a-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="df46a-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="df46a-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="df46a-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
