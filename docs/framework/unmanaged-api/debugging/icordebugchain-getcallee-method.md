---
description: 了解详细信息： ICorDebugChain：： GetCallee 方法
title: ICorDebugChain::GetCallee 方法
ms.date: 03/30/2017
api_name:
- ICorDebugChain.GetCallee
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::GetCallee method
helpviewer_keywords:
- ICorDebugChain::GetCallee method [.NET Framework debugging]
- GetCallee method, ICorDebugChain interface [.NET Framework debugging]
ms.assetid: 19560c79-abdc-4bdf-a5fe-eb362a59edc0
topic_type:
- apiref
ms.openlocfilehash: 4787893c86804c648dae14bf2e6f7425808104b7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99661384"
---
# <a name="icordebugchaingetcallee-method"></a><span data-ttu-id="da6dc-103">ICorDebugChain::GetCallee 方法</span><span class="sxs-lookup"><span data-stu-id="da6dc-103">ICorDebugChain::GetCallee Method</span></span>

<span data-ttu-id="da6dc-104">获取此链调用的链。</span><span class="sxs-lookup"><span data-stu-id="da6dc-104">Gets the chain that was called by this chain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="da6dc-105">语法</span><span class="sxs-lookup"><span data-stu-id="da6dc-105">Syntax</span></span>  
  
```cpp  
HRESULT GetCallee (  
    [out] ICorDebugChain     **ppChain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="da6dc-106">参数</span><span class="sxs-lookup"><span data-stu-id="da6dc-106">Parameters</span></span>  

 `ppChain`  
 <span data-ttu-id="da6dc-107">弄指向 ICorDebugChain 对象的地址的指针，该对象表示调用的链。</span><span class="sxs-lookup"><span data-stu-id="da6dc-107">[out] A pointer to the address of an ICorDebugChain object that represents the called chain.</span></span> <span data-ttu-id="da6dc-108">如果此链当前正在执行 (即，如果此链未等待调用的链返回) ， `ppChain` 则将为 null。</span><span class="sxs-lookup"><span data-stu-id="da6dc-108">If this chain is currently executing (that is, if this chain is not waiting for a called chain to return), `ppChain` will be null.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="da6dc-109">备注</span><span class="sxs-lookup"><span data-stu-id="da6dc-109">Remarks</span></span>  

 <span data-ttu-id="da6dc-110">此链将等待调用的链返回，然后再继续执行。</span><span class="sxs-lookup"><span data-stu-id="da6dc-110">This chain will wait for the called chain to return before it resumes execution.</span></span> <span data-ttu-id="da6dc-111">对于跨线程封送调用，被调用的链可以在另一个线程上。</span><span class="sxs-lookup"><span data-stu-id="da6dc-111">The called chain may be on another thread in the case of cross-thread marshaled calls.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="da6dc-112">要求</span><span class="sxs-lookup"><span data-stu-id="da6dc-112">Requirements</span></span>  

 <span data-ttu-id="da6dc-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="da6dc-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="da6dc-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="da6dc-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="da6dc-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="da6dc-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="da6dc-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="da6dc-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
