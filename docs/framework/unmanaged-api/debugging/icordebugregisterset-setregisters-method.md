---
description: 了解详细信息： ICorDebugRegisterSet：： SetRegisters 方法
title: ICorDebugRegisterSet::SetRegisters 方法
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet.SetRegisters
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet::SetRegisters
helpviewer_keywords:
- SetRegisters method, ICorDebugRegisterSet interface [.NET Framework debugging]
- ICorDebugRegisterSet::SetRegisters method [.NET Framework debugging]
ms.assetid: ac6244b9-54ba-475f-b72a-abed6afc46ec
topic_type:
- apiref
ms.openlocfilehash: 7a83d9d01a392d7ed435292f45ee0c75765ced36
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99690673"
---
# <a name="icordebugregistersetsetregisters-method"></a><span data-ttu-id="b1059-103">ICorDebugRegisterSet::SetRegisters 方法</span><span class="sxs-lookup"><span data-stu-id="b1059-103">ICorDebugRegisterSet::SetRegisters Method</span></span>

<span data-ttu-id="b1059-104">`SetRegisters` 在 .NET Framework 版本2.0 中未实现。</span><span class="sxs-lookup"><span data-stu-id="b1059-104">`SetRegisters` is not implemented in the .NET Framework version 2.0.</span></span> <span data-ttu-id="b1059-105">请勿调用此方法。</span><span class="sxs-lookup"><span data-stu-id="b1059-105">Do not call this method.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="b1059-106">使用较高级别的操作，如 [ICorDebugILFrame：： setip](icordebugilframe-setip-method.md) 或 [ICorDebugNativeFrame：： setip](icordebugnativeframe-setip-method.md)。</span><span class="sxs-lookup"><span data-stu-id="b1059-106">Use the higher-level operations such as [ICorDebugILFrame::SetIP](icordebugilframe-setip-method.md) or [ICorDebugNativeFrame::SetIP](icordebugnativeframe-setip-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b1059-107">语法</span><span class="sxs-lookup"><span data-stu-id="b1059-107">Syntax</span></span>  
  
```cpp  
HRESULT SetRegisters (  
    [in] ULONG64   mask,  
    [in] ULONG32   regCount,  
    [in, size_is(regCount)] CORDB_REGISTER regBuffer[]  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="b1059-108">要求</span><span class="sxs-lookup"><span data-stu-id="b1059-108">Requirements</span></span>  

 <span data-ttu-id="b1059-109">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b1059-109">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b1059-110">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="b1059-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b1059-111">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b1059-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b1059-112">**.NET Framework 版本：** 1.1、1。0</span><span class="sxs-lookup"><span data-stu-id="b1059-112">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b1059-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="b1059-113">See also</span></span>

- [<span data-ttu-id="b1059-114">ICorDebugRegisterSet 接口</span><span class="sxs-lookup"><span data-stu-id="b1059-114">ICorDebugRegisterSet Interface</span></span>](icordebugregisterset-interface.md)
- [<span data-ttu-id="b1059-115">ICorDebugRegisterSet2 接口</span><span class="sxs-lookup"><span data-stu-id="b1059-115">ICorDebugRegisterSet2 Interface</span></span>](icordebugregisterset2-interface.md)
