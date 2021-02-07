---
description: 了解详细信息： ICorDebugCode：： GetFunction 方法
title: ICorDebugCode::GetFunction 方法
ms.date: 03/30/2017
api_name:
- ICorDebugCode.GetFunction
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::GetFunction
helpviewer_keywords:
- GetFunction method, ICorDebugCode interface [.NET Framework debugging]
- ICorDebugCode::GetFunction method [.NET Framework debugging]
ms.assetid: c568b737-fdb2-4816-accd-051f5ab760f1
topic_type:
- apiref
ms.openlocfilehash: c90635bf1821d70d6d056d5cbd495ddfa2d2a2ff
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99711201"
---
# <a name="icordebugcodegetfunction-method"></a><span data-ttu-id="5aa24-103">ICorDebugCode::GetFunction 方法</span><span class="sxs-lookup"><span data-stu-id="5aa24-103">ICorDebugCode::GetFunction Method</span></span>

<span data-ttu-id="5aa24-104">获取与此 "ICorDebugCode" 关联的 "ICorDebugFunction"。</span><span class="sxs-lookup"><span data-stu-id="5aa24-104">Gets the "ICorDebugFunction" associated with this "ICorDebugCode".</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5aa24-105">语法</span><span class="sxs-lookup"><span data-stu-id="5aa24-105">Syntax</span></span>  
  
```cpp  
HRESULT GetFunction (  
    [out] ICorDebugFunction **ppFunction  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5aa24-106">参数</span><span class="sxs-lookup"><span data-stu-id="5aa24-106">Parameters</span></span>  

 `ppFunction`  
 <span data-ttu-id="5aa24-107">弄指向函数的地址的指针。</span><span class="sxs-lookup"><span data-stu-id="5aa24-107">[out] A pointer to the address of the function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5aa24-108">备注</span><span class="sxs-lookup"><span data-stu-id="5aa24-108">Remarks</span></span>  

 <span data-ttu-id="5aa24-109">`ICorDebugCode` 和 `ICorDebugFunction` 保持一对一关系。</span><span class="sxs-lookup"><span data-stu-id="5aa24-109">`ICorDebugCode` and `ICorDebugFunction` maintain a one-to-one relationship.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5aa24-110">要求</span><span class="sxs-lookup"><span data-stu-id="5aa24-110">Requirements</span></span>  

 <span data-ttu-id="5aa24-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5aa24-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5aa24-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="5aa24-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="5aa24-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5aa24-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5aa24-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5aa24-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
