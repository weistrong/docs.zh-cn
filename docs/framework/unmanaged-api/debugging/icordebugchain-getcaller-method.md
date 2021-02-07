---
description: 了解详细信息： ICorDebugChain：： GetCaller 方法
title: ICorDebugChain::GetCaller 方法
ms.date: 03/30/2017
api_name:
- ICorDebugChain.GetCaller
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::GetCaller
helpviewer_keywords:
- ICorDebugChain::GetCaller method [.NET Framework debugging]
- GetCaller method, ICorDebugChain interface [.NET Framework debugging]
ms.assetid: d0b8ab4b-d7d2-4fa0-945f-3d2b87e7e991
topic_type:
- apiref
ms.openlocfilehash: 5af2132b7fec9e70704db980b95221db6eb273f8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99695016"
---
# <a name="icordebugchaingetcaller-method"></a><span data-ttu-id="9acf4-103">ICorDebugChain::GetCaller 方法</span><span class="sxs-lookup"><span data-stu-id="9acf4-103">ICorDebugChain::GetCaller Method</span></span>

<span data-ttu-id="9acf4-104">获取调用此链的链。</span><span class="sxs-lookup"><span data-stu-id="9acf4-104">Gets the chain that called this chain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9acf4-105">语法</span><span class="sxs-lookup"><span data-stu-id="9acf4-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCaller (  
    [out] ICorDebugChain      **ppChain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9acf4-106">参数</span><span class="sxs-lookup"><span data-stu-id="9acf4-106">Parameters</span></span>  

 `ppChain`  
 <span data-ttu-id="9acf4-107">弄指向表示调用链的 ICorDebugChain 对象地址的指针。</span><span class="sxs-lookup"><span data-stu-id="9acf4-107">[out] A pointer to the address of an ICorDebugChain object that represents the calling chain.</span></span>  
  
 <span data-ttu-id="9acf4-108">如果此链被自发地称为 (如此链或调试器初始化调用堆栈) ，将为 `ppChain` null。</span><span class="sxs-lookup"><span data-stu-id="9acf4-108">If this chain was spontaneously called (as would be the case if this chain or the debugger initialized the call stack), `ppChain` will be null.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9acf4-109">备注</span><span class="sxs-lookup"><span data-stu-id="9acf4-109">Remarks</span></span>  

 <span data-ttu-id="9acf4-110">如果调用是在线程间封送的，则调用链可能位于不同的线程上。</span><span class="sxs-lookup"><span data-stu-id="9acf4-110">The calling chain may be on a different thread, if the call was marshaled across threads.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9acf4-111">要求</span><span class="sxs-lookup"><span data-stu-id="9acf4-111">Requirements</span></span>  

 <span data-ttu-id="9acf4-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9acf4-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9acf4-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9acf4-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9acf4-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9acf4-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9acf4-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9acf4-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
