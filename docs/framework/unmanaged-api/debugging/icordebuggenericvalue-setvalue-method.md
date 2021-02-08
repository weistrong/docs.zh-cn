---
description: 了解详细信息： ICorDebugGenericValue：： SetValue 方法
title: ICorDebugGenericValue::SetValue 方法
ms.date: 03/30/2017
api_name:
- ICorDebugGenericValue.SetValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugGenericValue::SetValue
helpviewer_keywords:
- ICorDebugGenericValue::SetValue method [.NET Framework debugging]
- SetValue method, ICorDebugGenericValue interface [.NET Framework debugging]
ms.assetid: ed4c6458-0435-44fc-8e78-8ba00be362f2
topic_type:
- apiref
ms.openlocfilehash: e284d9987c8428fadedde0024fd3c65a0d8fe7a0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791473"
---
# <a name="icordebuggenericvaluesetvalue-method"></a><span data-ttu-id="79e14-103">ICorDebugGenericValue::SetValue 方法</span><span class="sxs-lookup"><span data-stu-id="79e14-103">ICorDebugGenericValue::SetValue Method</span></span>

<span data-ttu-id="79e14-104">从指定的缓冲区复制新值。</span><span class="sxs-lookup"><span data-stu-id="79e14-104">Copies a new value from the specified buffer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79e14-105">语法</span><span class="sxs-lookup"><span data-stu-id="79e14-105">Syntax</span></span>  
  
```cpp  
HRESULT SetValue (  
    [in] void      *pFrom  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="79e14-106">参数</span><span class="sxs-lookup"><span data-stu-id="79e14-106">Parameters</span></span>  

 `pFrom`  
 <span data-ttu-id="79e14-107">中指向要从中复制值的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="79e14-107">[in] A pointer to the buffer from which to copy the value.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="79e14-108">备注</span><span class="sxs-lookup"><span data-stu-id="79e14-108">Remarks</span></span>  

 <span data-ttu-id="79e14-109">对于引用类型，该值是引用，而不是内容。</span><span class="sxs-lookup"><span data-stu-id="79e14-109">For reference types, the value is the reference, not the content.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="79e14-110">要求</span><span class="sxs-lookup"><span data-stu-id="79e14-110">Requirements</span></span>  

 <span data-ttu-id="79e14-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="79e14-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="79e14-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="79e14-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="79e14-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="79e14-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="79e14-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="79e14-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
