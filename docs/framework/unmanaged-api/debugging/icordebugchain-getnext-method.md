---
description: 了解详细信息： ICorDebugChain：： GetNext 方法
title: ICorDebugChain::GetNext 方法
ms.date: 03/30/2017
api_name:
- ICorDebugChain.GetNext
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::GetNext
helpviewer_keywords:
- GetNext method [.NET Framework debugging]
- ICorDebugChain::GetNext method [.NET Framework debugging]
ms.assetid: 8d9744a5-e08b-4ab2-9855-5c22711cc1e6
topic_type:
- apiref
ms.openlocfilehash: ced7032feffa4c14c07341242b854c08b8c897a5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99661319"
---
# <a name="icordebugchaingetnext-method"></a><span data-ttu-id="936d6-103">ICorDebugChain::GetNext 方法</span><span class="sxs-lookup"><span data-stu-id="936d6-103">ICorDebugChain::GetNext Method</span></span>

<span data-ttu-id="936d6-104">获取线程的下一个帧链。</span><span class="sxs-lookup"><span data-stu-id="936d6-104">Gets the next chain of frames for the thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="936d6-105">语法</span><span class="sxs-lookup"><span data-stu-id="936d6-105">Syntax</span></span>  
  
```cpp  
HRESULT GetNext (  
    [out] ICorDebugChain     **ppChain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="936d6-106">参数</span><span class="sxs-lookup"><span data-stu-id="936d6-106">Parameters</span></span>  

 `ppChain`  
 <span data-ttu-id="936d6-107">弄指向 ICorDebugChain 对象的地址的指针，该对象表示线程的下一个帧链。</span><span class="sxs-lookup"><span data-stu-id="936d6-107">[out] A pointer to the address of an ICorDebugChain object that represents the next chain of frames for the thread.</span></span> <span data-ttu-id="936d6-108">如果此链是最后一个链， `ppChain` 则为 null。</span><span class="sxs-lookup"><span data-stu-id="936d6-108">If this chain is the last chain, `ppChain` is null.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="936d6-109">要求</span><span class="sxs-lookup"><span data-stu-id="936d6-109">Requirements</span></span>  

 <span data-ttu-id="936d6-110">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="936d6-110">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="936d6-111">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="936d6-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="936d6-112">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="936d6-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="936d6-113">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="936d6-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
