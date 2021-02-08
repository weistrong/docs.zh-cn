---
description: 了解详细信息： ICorDebugRegisterSet2：： GetRegistersAvailable 方法
title: ICorDebugRegisterSet2::GetRegistersAvailable 方法
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet2.GetRegistersAvailable
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet2::GetRegistersAvailable
helpviewer_keywords:
- GetRegistersAvailable method, ICorDebugRegisterSet2 interface [.NET Framework debugging]
- ICorDebugRegisterSet2::GetRegistersAvailable method [.NET Framework debugging]
ms.assetid: f3ed344b-0d3a-44e8-8000-2a97e0805a2c
topic_type:
- apiref
ms.openlocfilehash: 3839647e69efd63aefd1aa154c457f292e684336
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790716"
---
# <a name="icordebugregisterset2getregistersavailable-method"></a><span data-ttu-id="e457a-103">ICorDebugRegisterSet2::GetRegistersAvailable 方法</span><span class="sxs-lookup"><span data-stu-id="e457a-103">ICorDebugRegisterSet2::GetRegistersAvailable Method</span></span>

<span data-ttu-id="e457a-104">获取提供可用寄存器的位图的字节数组。</span><span class="sxs-lookup"><span data-stu-id="e457a-104">Gets an array of bytes that provides a bitmap of the available registers.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e457a-105">语法</span><span class="sxs-lookup"><span data-stu-id="e457a-105">Syntax</span></span>  
  
```cpp  
HRESULT GetRegistersAvailable (  
    [in] ULONG32 numChunks,  
    [out, size_is(numChunks)] BYTE availableRegChunks[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e457a-106">参数</span><span class="sxs-lookup"><span data-stu-id="e457a-106">Parameters</span></span>  

 `numChunks`  
 <span data-ttu-id="e457a-107">[in] `availableRegChunks` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="e457a-107">[in] The size of the `availableRegChunks` array.</span></span>  
  
 `availableRegChunks`  
 <span data-ttu-id="e457a-108">弄字节数组，其中每个位对应于寄存器。</span><span class="sxs-lookup"><span data-stu-id="e457a-108">[out] An array of bytes, each bit of which corresponds to a register.</span></span> <span data-ttu-id="e457a-109">如果寄存器可用，则会设置寄存器的相应位。</span><span class="sxs-lookup"><span data-stu-id="e457a-109">If a register is available, the register's corresponding bit is set.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e457a-110">备注</span><span class="sxs-lookup"><span data-stu-id="e457a-110">Remarks</span></span>  

 <span data-ttu-id="e457a-111">CorDebugRegister 枚举的值指定不同微处理器的寄存器。</span><span class="sxs-lookup"><span data-stu-id="e457a-111">The values of the CorDebugRegister enumeration specify the registers of different microprocessors.</span></span> <span data-ttu-id="e457a-112">每个值的前五位是字节数组中的索引 `availableRegChunks` 。</span><span class="sxs-lookup"><span data-stu-id="e457a-112">The upper five bits of each value are the index into the `availableRegChunks` array of bytes.</span></span> <span data-ttu-id="e457a-113">每个值的下三位标识索引字节内的位位置。</span><span class="sxs-lookup"><span data-stu-id="e457a-113">The lower three bits of each value identify the bit position within the indexed byte.</span></span> <span data-ttu-id="e457a-114">给定一个 `CorDebugRegister` 指定特定寄存器的值时，将按如下所示确定此寄存器在掩码中的位置：</span><span class="sxs-lookup"><span data-stu-id="e457a-114">Given a `CorDebugRegister` value that specifies a particular register, the register's position in the mask is determined as follows:</span></span>  
  
1. <span data-ttu-id="e457a-115">提取访问数组中正确字节所需的索引 `availableRegChunks` ：</span><span class="sxs-lookup"><span data-stu-id="e457a-115">Extract the index needed to access the correct byte in the `availableRegChunks` array:</span></span>  
  
     <span data-ttu-id="e457a-116">`CorDebugRegister` 值 >> 3</span><span class="sxs-lookup"><span data-stu-id="e457a-116">`CorDebugRegister` value >> 3</span></span>  
  
2. <span data-ttu-id="e457a-117">提取索引字节内的位位置，其中位零是最小有效位：</span><span class="sxs-lookup"><span data-stu-id="e457a-117">Extract the bit position within the indexed byte, where bit zero is the least significant bit:</span></span>  
  
     <span data-ttu-id="e457a-118">`CorDebugRegister` 值 & 7</span><span class="sxs-lookup"><span data-stu-id="e457a-118">`CorDebugRegister` value & 7</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e457a-119">要求</span><span class="sxs-lookup"><span data-stu-id="e457a-119">Requirements</span></span>  

 <span data-ttu-id="e457a-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e457a-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e457a-121">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="e457a-121">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e457a-122">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e457a-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e457a-123">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e457a-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e457a-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="e457a-124">See also</span></span>

- [<span data-ttu-id="e457a-125">ICorDebugRegisterSet2 接口</span><span class="sxs-lookup"><span data-stu-id="e457a-125">ICorDebugRegisterSet2 Interface</span></span>](icordebugregisterset2-interface.md)
- [<span data-ttu-id="e457a-126">ICorDebugRegisterSet 接口</span><span class="sxs-lookup"><span data-stu-id="e457a-126">ICorDebugRegisterSet Interface</span></span>](icordebugregisterset-interface.md)
