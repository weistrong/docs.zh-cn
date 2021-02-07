---
description: 了解详细信息： ICorDebugFrame：： GetFunction 方法
title: ICorDebugFrame::GetFunction 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFrame.GetFunction
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::GetFunction
helpviewer_keywords:
- GetFunction method, ICorDebugFrame interface [.NET Framework debugging]
- ICorDebugFrame::GetFunction method [.NET Framework debugging]
ms.assetid: 879d2311-0ff1-4616-a8b3-959ea5868b2e
topic_type:
- apiref
ms.openlocfilehash: 0309a066f686e55d086de1cbb040eea58e031df3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692974"
---
# <a name="icordebugframegetfunction-method"></a><span data-ttu-id="c9335-103">ICorDebugFrame::GetFunction 方法</span><span class="sxs-lookup"><span data-stu-id="c9335-103">ICorDebugFrame::GetFunction Method</span></span>

<span data-ttu-id="c9335-104">获取一个函数，该函数包含与此堆栈帧关联的代码。</span><span class="sxs-lookup"><span data-stu-id="c9335-104">Gets the function that contains the code associated with this stack frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c9335-105">语法</span><span class="sxs-lookup"><span data-stu-id="c9335-105">Syntax</span></span>  
  
```cpp  
HRESULT GetFunction (  
    [out] ICorDebugFunction  **ppFunction  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c9335-106">参数</span><span class="sxs-lookup"><span data-stu-id="c9335-106">Parameters</span></span>  

 `ppFunction`  
 <span data-ttu-id="c9335-107">弄指向 ICorDebugFunction 对象的地址的指针，该对象表示包含与此堆栈帧关联的代码的函数。</span><span class="sxs-lookup"><span data-stu-id="c9335-107">[out] A pointer to the address of an ICorDebugFunction object that represents the function containing the code associated with this stack frame.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c9335-108">备注</span><span class="sxs-lookup"><span data-stu-id="c9335-108">Remarks</span></span>  

 <span data-ttu-id="c9335-109">`GetFunction`如果框架不与任何特定函数关联，则该方法可能会失败。</span><span class="sxs-lookup"><span data-stu-id="c9335-109">The `GetFunction` method may fail if the frame is not associated with any particular function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c9335-110">要求</span><span class="sxs-lookup"><span data-stu-id="c9335-110">Requirements</span></span>  

 <span data-ttu-id="c9335-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c9335-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c9335-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c9335-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c9335-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c9335-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c9335-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c9335-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
