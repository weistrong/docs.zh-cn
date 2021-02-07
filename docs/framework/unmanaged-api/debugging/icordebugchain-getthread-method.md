---
description: 了解详细信息： ICorDebugChain：： GetThread 方法
title: ICorDebugChain::GetThread 方法
ms.date: 03/30/2017
api_name:
- ICorDebugChain.GetThread
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::GetThread
helpviewer_keywords:
- GetThread method, ICorDebugChain interface [.NET Framework debugging]
- ICorDebugChain::GetThread method [.NET Framework debugging]
ms.assetid: b3390319-6366-418c-ba80-b552ac4dfc1e
topic_type:
- apiref
ms.openlocfilehash: 090cb40c3681792ce4a30cd342e65dc02ac3f381
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99694912"
---
# <a name="icordebugchaingetthread-method"></a><span data-ttu-id="a74b3-103">ICorDebugChain::GetThread 方法</span><span class="sxs-lookup"><span data-stu-id="a74b3-103">ICorDebugChain::GetThread Method</span></span>

<span data-ttu-id="a74b3-104">获取此调用链所属的物理线程。</span><span class="sxs-lookup"><span data-stu-id="a74b3-104">Gets the physical thread this call chain is part of.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a74b3-105">语法</span><span class="sxs-lookup"><span data-stu-id="a74b3-105">Syntax</span></span>  
  
```cpp  
HRESULT GetThread (  
    [out] ICorDebugThread    **ppThread  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a74b3-106">参数</span><span class="sxs-lookup"><span data-stu-id="a74b3-106">Parameters</span></span>  

 `ppThread`  
 <span data-ttu-id="a74b3-107">弄指向 ICorDebugThread 对象的指针，该对象表示此调用链所属的物理线程。</span><span class="sxs-lookup"><span data-stu-id="a74b3-107">[out] A pointer to an ICorDebugThread object that represents the physical thread this call chain is part of.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a74b3-108">要求</span><span class="sxs-lookup"><span data-stu-id="a74b3-108">Requirements</span></span>  

 <span data-ttu-id="a74b3-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a74b3-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a74b3-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="a74b3-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a74b3-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a74b3-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a74b3-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a74b3-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
