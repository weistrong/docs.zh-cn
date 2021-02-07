---
description: 了解详细信息： ICorDebugChain：： GetRegisterSet 方法
title: ICorDebugChain::GetRegisterSet 方法
ms.date: 03/30/2017
api_name:
- ICorDebugChain.GetRegisterSet
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::GetRegisterSet
helpviewer_keywords:
- ICorDebugChain::GetRegisterSet method [.NET Framework debugging]
- GetRegisterSet method, ICorDebugChain interface [.NET Framework debugging]
ms.assetid: bc4288b6-3331-4ae3-990d-e1d6e62ecb67
topic_type:
- apiref
ms.openlocfilehash: 75c77838cb4ef49dd922a4e39b41e622693e928d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99694938"
---
# <a name="icordebugchaingetregisterset-method"></a><span data-ttu-id="e40d6-103">ICorDebugChain::GetRegisterSet 方法</span><span class="sxs-lookup"><span data-stu-id="e40d6-103">ICorDebugChain::GetRegisterSet Method</span></span>

<span data-ttu-id="e40d6-104">获取此链的活动部分的寄存器集。</span><span class="sxs-lookup"><span data-stu-id="e40d6-104">Gets the register set for the active part of this chain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e40d6-105">语法</span><span class="sxs-lookup"><span data-stu-id="e40d6-105">Syntax</span></span>  
  
```cpp  
HRESULT GetRegisterSet (  
    [out] ICorDebugRegisterSet **ppRegisters  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e40d6-106">参数</span><span class="sxs-lookup"><span data-stu-id="e40d6-106">Parameters</span></span>  

 `ppRegisters`  
 <span data-ttu-id="e40d6-107">弄指向 [ICorDebugRegisterSet](icordebugregisterset-interface.md) 对象的地址的指针，该对象表示此链的活动部分的寄存器集。</span><span class="sxs-lookup"><span data-stu-id="e40d6-107">[out] A pointer to the address of an [ICorDebugRegisterSet](icordebugregisterset-interface.md) object that represents the register set for the active part of this chain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e40d6-108">要求</span><span class="sxs-lookup"><span data-stu-id="e40d6-108">Requirements</span></span>  

 <span data-ttu-id="e40d6-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e40d6-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e40d6-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e40d6-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e40d6-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e40d6-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e40d6-112">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e40d6-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
