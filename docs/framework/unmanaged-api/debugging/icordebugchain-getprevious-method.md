---
description: 了解详细信息： ICorDebugChain：： GetPrevious 方法
title: ICorDebugChain::GetPrevious 方法
ms.date: 03/30/2017
api_name:
- ICorDebugChain.GetPrevious
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::GetPrevious
helpviewer_keywords:
- ICorDebugChain::GetPrevious method [.NET Framework debugging]
- GetPrevious method [.NET Framework debugging]
ms.assetid: 58eed4c8-d80c-4c6a-a875-967a90dd926c
topic_type:
- apiref
ms.openlocfilehash: 169c46afd545835e6da87686a8e74ecd12173904
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99661254"
---
# <a name="icordebugchaingetprevious-method"></a><span data-ttu-id="22c46-103">ICorDebugChain::GetPrevious 方法</span><span class="sxs-lookup"><span data-stu-id="22c46-103">ICorDebugChain::GetPrevious Method</span></span>

<span data-ttu-id="22c46-104">获取线程的上一个帧链。</span><span class="sxs-lookup"><span data-stu-id="22c46-104">Gets the previous chain of frames for the thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="22c46-105">语法</span><span class="sxs-lookup"><span data-stu-id="22c46-105">Syntax</span></span>  
  
```cpp  
HRESULT GetPrevious (  
    [out] ICorDebugChain     **ppChain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="22c46-106">参数</span><span class="sxs-lookup"><span data-stu-id="22c46-106">Parameters</span></span>  

 `ppChain`  
 <span data-ttu-id="22c46-107">弄指向 ICorDebugChain 对象的地址的指针，该对象表示此线程的上一个帧链。</span><span class="sxs-lookup"><span data-stu-id="22c46-107">[out] A pointer to the address of an ICorDebugChain object that represents the previous chain of frames for this thread.</span></span> <span data-ttu-id="22c46-108">如果此链是第一个链， `ppChain` 则为 null。</span><span class="sxs-lookup"><span data-stu-id="22c46-108">If this chain is the first chain, `ppChain` is null.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="22c46-109">要求</span><span class="sxs-lookup"><span data-stu-id="22c46-109">Requirements</span></span>  

 <span data-ttu-id="22c46-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="22c46-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="22c46-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="22c46-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="22c46-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="22c46-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="22c46-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="22c46-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
