---
description: 了解详细信息： ICorDebugFrame：： GetChain 方法
title: ICorDebugFrame::GetChain 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFrame.GetChain
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::GetChain
helpviewer_keywords:
- ICorDebugFrame::GetChain method [.NET Framework debugging]
- GetChain method [.NET Framework debugging]
ms.assetid: e28e51d3-8f73-494f-bcd4-48bac239fbe1
topic_type:
- apiref
ms.openlocfilehash: d162d484a54f107fb5937e57f60e2b82cad90ca1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693052"
---
# <a name="icordebugframegetchain-method"></a><span data-ttu-id="a6228-103">ICorDebugFrame::GetChain 方法</span><span class="sxs-lookup"><span data-stu-id="a6228-103">ICorDebugFrame::GetChain Method</span></span>

<span data-ttu-id="a6228-104">获取一个指针，该指针指向此帧所属的链。</span><span class="sxs-lookup"><span data-stu-id="a6228-104">Gets a pointer to the chain this frame is a part of.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a6228-105">语法</span><span class="sxs-lookup"><span data-stu-id="a6228-105">Syntax</span></span>  
  
```cpp  
HRESULT GetChain (  
    [out] ICorDebugChain     **ppChain  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a6228-106">参数</span><span class="sxs-lookup"><span data-stu-id="a6228-106">Parameters</span></span>  

 `ppChain`  
 <span data-ttu-id="a6228-107">弄指向 ICorDebugChain 对象的地址的指针，该对象表示包含此帧的链。</span><span class="sxs-lookup"><span data-stu-id="a6228-107">[out] A pointer to the address of an ICorDebugChain object that represents the chain containing this frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a6228-108">要求</span><span class="sxs-lookup"><span data-stu-id="a6228-108">Requirements</span></span>  

 <span data-ttu-id="a6228-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a6228-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a6228-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a6228-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a6228-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a6228-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a6228-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a6228-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
