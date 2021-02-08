---
description: 了解详细信息： ICorDebugRegisterSet2：： SetRegisters 方法
title: ICorDebugRegisterSet2::SetRegisters 方法
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet2.SetRegisters
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet2::SetRegisters
helpviewer_keywords:
- ICorDebugRegisterSet2::SetRegisters method [.NET Framework debugging]
- SetRegisters method, ICorDebugRegisterSet2 interface [.NET Framework debugging]
ms.assetid: fe0ac7e7-c9e1-4ec1-9f4e-1c56d63d73ac
topic_type:
- apiref
ms.openlocfilehash: d58717be34e146def2a54bb49d6cd58dde7564c8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794749"
---
# <a name="icordebugregisterset2setregisters-method"></a><span data-ttu-id="44e88-103">ICorDebugRegisterSet2::SetRegisters 方法</span><span class="sxs-lookup"><span data-stu-id="44e88-103">ICorDebugRegisterSet2::SetRegisters Method</span></span>

<span data-ttu-id="44e88-104">`SetRegisters` 在 .NET Framework 版本2.0 中未实现。</span><span class="sxs-lookup"><span data-stu-id="44e88-104">`SetRegisters` is not implemented in the .NET Framework version 2.0.</span></span> <span data-ttu-id="44e88-105">请勿调用此方法。</span><span class="sxs-lookup"><span data-stu-id="44e88-105">Do not call this method.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="44e88-106">使用较高级别的操作，如 [ICorDebugILFrame：： setip](icordebugilframe-setip-method.md) 或 [ICorDebugNativeFrame：： setip](icordebugnativeframe-setip-method.md)。</span><span class="sxs-lookup"><span data-stu-id="44e88-106">Use the higher-level operations such as [ICorDebugILFrame::SetIP](icordebugilframe-setip-method.md) or [ICorDebugNativeFrame::SetIP](icordebugnativeframe-setip-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="44e88-107">语法</span><span class="sxs-lookup"><span data-stu-id="44e88-107">Syntax</span></span>  
  
```cpp  
HRESULT SetRegisters (  
    [in] ULONG32 maskCount,  
    [in, size_is(maskCount)] BYTE mask[],  
    [in] ULONG32 regCount,  
    [in, size_is(regCount)] CORDB_REGISTER regBuffer[]  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="44e88-108">要求</span><span class="sxs-lookup"><span data-stu-id="44e88-108">Requirements</span></span>  

 <span data-ttu-id="44e88-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="44e88-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="44e88-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="44e88-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="44e88-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="44e88-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="44e88-112">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="44e88-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="44e88-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="44e88-113">See also</span></span>

- [<span data-ttu-id="44e88-114">ICorDebugRegisterSet2 接口</span><span class="sxs-lookup"><span data-stu-id="44e88-114">ICorDebugRegisterSet2 Interface</span></span>](icordebugregisterset2-interface.md)
- [<span data-ttu-id="44e88-115">ICorDebugRegisterSet 接口</span><span class="sxs-lookup"><span data-stu-id="44e88-115">ICorDebugRegisterSet Interface</span></span>](icordebugregisterset-interface.md)
