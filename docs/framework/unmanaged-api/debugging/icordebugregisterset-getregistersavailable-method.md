---
description: 了解详细信息： ICorDebugRegisterSet：： GetRegistersAvailable 方法
title: ICorDebugRegisterSet::GetRegistersAvailable 方法
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet.GetRegistersAvailable
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet::GetRegistersAvailable
helpviewer_keywords:
- ICorDebugRegisterSet::GetRegistersAvailable method [.NET Framework debugging]
- GetRegistersAvailable method, ICorDebugRegisterSet interface [.NET Framework debugging]
ms.assetid: 4ba08ffa-55a2-4662-9d6d-4738f1db60c9
topic_type:
- apiref
ms.openlocfilehash: a1727c594733fe6529fe1e78f341723623b68be2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99690816"
---
# <a name="icordebugregistersetgetregistersavailable-method"></a><span data-ttu-id="03d18-103">ICorDebugRegisterSet::GetRegistersAvailable 方法</span><span class="sxs-lookup"><span data-stu-id="03d18-103">ICorDebugRegisterSet::GetRegistersAvailable Method</span></span>

<span data-ttu-id="03d18-104">获取指示此 [ICorDebugRegisterSet](icordebugregisterset-interface.md) 中的哪些寄存器当前可用的位掩码。</span><span class="sxs-lookup"><span data-stu-id="03d18-104">Gets a bit mask indicating which registers in this [ICorDebugRegisterSet](icordebugregisterset-interface.md) are currently available.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="03d18-105">语法</span><span class="sxs-lookup"><span data-stu-id="03d18-105">Syntax</span></span>  
  
```cpp  
HRESULT GetRegistersAvailable (  
    [out] ULONG64   *pAvailable  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="03d18-106">参数</span><span class="sxs-lookup"><span data-stu-id="03d18-106">Parameters</span></span>  

 `pAvailable`  
 <span data-ttu-id="03d18-107">弄一个位掩码，用于指示当前可用的注册。</span><span class="sxs-lookup"><span data-stu-id="03d18-107">[out] A bit mask that indicates which registers are currently available.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="03d18-108">备注</span><span class="sxs-lookup"><span data-stu-id="03d18-108">Remarks</span></span>  

 <span data-ttu-id="03d18-109">如果无法为给定情况确定其值，则寄存器可能不可用。</span><span class="sxs-lookup"><span data-stu-id="03d18-109">A register may be unavailable if its value cannot be determined for the given situation.</span></span>  
  
 <span data-ttu-id="03d18-110">对于每个寄存器 (1 << 注册索引) ，返回的掩码包含一个位。</span><span class="sxs-lookup"><span data-stu-id="03d18-110">The returned mask contains a bit for each register (1 << the register index).</span></span> <span data-ttu-id="03d18-111">如果寄存器可用，则位值为 1; 否则为0。</span><span class="sxs-lookup"><span data-stu-id="03d18-111">The bit value is 1 if the register is available, or 0 if it is not available.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="03d18-112">要求</span><span class="sxs-lookup"><span data-stu-id="03d18-112">Requirements</span></span>  

 <span data-ttu-id="03d18-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="03d18-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="03d18-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="03d18-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="03d18-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="03d18-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="03d18-116">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="03d18-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="03d18-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="03d18-117">See also</span></span>

- [<span data-ttu-id="03d18-118">ICorDebugRegisterSet 接口</span><span class="sxs-lookup"><span data-stu-id="03d18-118">ICorDebugRegisterSet Interface</span></span>](icordebugregisterset-interface.md)
- [<span data-ttu-id="03d18-119">ICorDebugRegisterSet2 接口</span><span class="sxs-lookup"><span data-stu-id="03d18-119">ICorDebugRegisterSet2 Interface</span></span>](icordebugregisterset2-interface.md)
