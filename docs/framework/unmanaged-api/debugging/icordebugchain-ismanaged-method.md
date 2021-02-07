---
description: 了解详细信息： ICorDebugChain：： IsManaged 方法
title: ICorDebugChain::IsManaged 方法
ms.date: 03/30/2017
api_name:
- ICorDebugChain.IsManaged
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::IsManaged
helpviewer_keywords:
- ICorDebugChain::IsManaged method [.NET Framework debugging]
- IsManaged method, ICorDebugChain interface [.NET Framework debugging]
ms.assetid: 17b389a0-1a4d-4e8a-8613-9bc1769930f9
topic_type:
- apiref
ms.openlocfilehash: 200b76350d474645a40f8ee35859c2db5420ea0a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99694847"
---
# <a name="icordebugchainismanaged-method"></a><span data-ttu-id="bd2d7-103">ICorDebugChain::IsManaged 方法</span><span class="sxs-lookup"><span data-stu-id="bd2d7-103">ICorDebugChain::IsManaged Method</span></span>

<span data-ttu-id="bd2d7-104">获取一个值，该值指示此链是否正在运行托管代码。</span><span class="sxs-lookup"><span data-stu-id="bd2d7-104">Gets a value that indicates whether this chain is running managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bd2d7-105">语法</span><span class="sxs-lookup"><span data-stu-id="bd2d7-105">Syntax</span></span>  
  
```cpp  
HRESULT IsManaged (  
    [out] BOOL               *pManaged  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bd2d7-106">参数</span><span class="sxs-lookup"><span data-stu-id="bd2d7-106">Parameters</span></span>  

 `pManaged`  
 <span data-ttu-id="bd2d7-107">[out] `true` 如果此链正在运行托管代码，则为;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="bd2d7-107">[out] `true` if this chain is running managed code; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bd2d7-108">要求</span><span class="sxs-lookup"><span data-stu-id="bd2d7-108">Requirements</span></span>  

 <span data-ttu-id="bd2d7-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bd2d7-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bd2d7-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="bd2d7-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="bd2d7-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bd2d7-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bd2d7-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bd2d7-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
