---
description: 了解详细信息： ICorDebugEval：： GetThread 方法
title: ICorDebugEval::GetThread 方法
ms.date: 03/30/2017
api_name:
- ICorDebugEval.GetThread
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::GetThread
helpviewer_keywords:
- GetThread method, ICorDebugEval interface [.NET Framework debugging]
- ICorDebugEval::GetThread method [.NET Framework debugging]
ms.assetid: 57163b0d-c8a7-44af-9078-e7a895d29f9a
topic_type:
- apiref
ms.openlocfilehash: 3e7120f618abce31b9940a886fd6b2b2f8639d2d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99694144"
---
# <a name="icordebugevalgetthread-method"></a><span data-ttu-id="d76ec-103">ICorDebugEval::GetThread 方法</span><span class="sxs-lookup"><span data-stu-id="d76ec-103">ICorDebugEval::GetThread Method</span></span>

<span data-ttu-id="d76ec-104">获取在其中执行或将执行此计算的线程。</span><span class="sxs-lookup"><span data-stu-id="d76ec-104">Gets the thread in which this evaluation is executing or will execute.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d76ec-105">语法</span><span class="sxs-lookup"><span data-stu-id="d76ec-105">Syntax</span></span>  
  
```cpp  
HRESULT GetThread (  
    [out] ICorDebugThread   **ppThread  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d76ec-106">参数</span><span class="sxs-lookup"><span data-stu-id="d76ec-106">Parameters</span></span>  

 `ppThread`  
 <span data-ttu-id="d76ec-107">弄指向表示线程的 ICorDebugThread 对象的地址的指针。</span><span class="sxs-lookup"><span data-stu-id="d76ec-107">[out] A pointer to the address of an ICorDebugThread object that represents the thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d76ec-108">要求</span><span class="sxs-lookup"><span data-stu-id="d76ec-108">Requirements</span></span>  

 <span data-ttu-id="d76ec-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d76ec-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d76ec-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="d76ec-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d76ec-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d76ec-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d76ec-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d76ec-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
