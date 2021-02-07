---
description: 了解详细信息： ICorDebugRegisterSet：： GetRegisters 方法
title: ICorDebugRegisterSet::GetRegisters 方法
ms.date: 03/30/2017
api_name:
- ICorDebugRegisterSet.GetRegisters
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugRegisterSet::GetRegisters
helpviewer_keywords:
- GetRegisters method, ICorDebugRegisterSet interface [.NET Framework debugging]
- ICorDebugRegisterSet::GetRegisters method [.NET Framework debugging]
ms.assetid: fdf91864-48ea-4aa6-b70c-361b7a3184c7
topic_type:
- apiref
ms.openlocfilehash: efb0f19fe9eb823912203b82267803739fc3e2cd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99690842"
---
# <a name="icordebugregistersetgetregisters-method"></a><span data-ttu-id="10c1f-103">ICorDebugRegisterSet::GetRegisters 方法</span><span class="sxs-lookup"><span data-stu-id="10c1f-103">ICorDebugRegisterSet::GetRegisters Method</span></span>

<span data-ttu-id="10c1f-104">获取计算机上每个寄存器 (的值，该计算机当前正在执行位掩码指定的代码) 。</span><span class="sxs-lookup"><span data-stu-id="10c1f-104">Gets the value of each register (on the computer that is currently executing code) that is specified by the bit mask.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="10c1f-105">语法</span><span class="sxs-lookup"><span data-stu-id="10c1f-105">Syntax</span></span>  
  
```cpp  
HRESULT GetRegisters (  
    [in] ULONG64       mask,
    [in] ULONG32       regCount,  
    [out, size_is(regCount), length_is(regCount)]  
        CORDB_REGISTER regBuffer[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="10c1f-106">参数</span><span class="sxs-lookup"><span data-stu-id="10c1f-106">Parameters</span></span>  

 `mask`  
 <span data-ttu-id="10c1f-107">中指定要检索的寄存器值的位掩码。</span><span class="sxs-lookup"><span data-stu-id="10c1f-107">[in] A bit mask that specifies which register values are to be retrieved.</span></span> <span data-ttu-id="10c1f-108">每个位对应于一个寄存器。</span><span class="sxs-lookup"><span data-stu-id="10c1f-108">Each bit corresponds to a register.</span></span> <span data-ttu-id="10c1f-109">如果将位设置为1，则将检索寄存器的值;否则，不检索寄存器的值。</span><span class="sxs-lookup"><span data-stu-id="10c1f-109">If a bit is set to one, the register's value is retrieved; otherwise, the register's value is not retrieved.</span></span>  
  
 `regCount`  
 <span data-ttu-id="10c1f-110">中要检索的寄存器值的数目。</span><span class="sxs-lookup"><span data-stu-id="10c1f-110">[in] The number of register values to be retrieved.</span></span>  
  
 `regBuffer`  
 <span data-ttu-id="10c1f-111">弄对象的数组 `CORDB_REGISTER` ，其中每个对象都接收寄存器的值。</span><span class="sxs-lookup"><span data-stu-id="10c1f-111">[out] An array of `CORDB_REGISTER` objects, each of which receives a value of a register.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="10c1f-112">备注</span><span class="sxs-lookup"><span data-stu-id="10c1f-112">Remarks</span></span>  

 <span data-ttu-id="10c1f-113">数组的大小应等于位掩码中设置为1的位数。</span><span class="sxs-lookup"><span data-stu-id="10c1f-113">The size of the array should be equal to the number of bits set to one in the bit mask.</span></span> <span data-ttu-id="10c1f-114">`regCount`参数指定将接收寄存器值的缓冲区中的元素数。</span><span class="sxs-lookup"><span data-stu-id="10c1f-114">The `regCount` parameter specifies the number of elements in the buffer that will receive the register values.</span></span> <span data-ttu-id="10c1f-115">如果 `regCount` 该值对于掩码所指示的寄存器数量太小，则将从该集中截断编号较高的寄存器。</span><span class="sxs-lookup"><span data-stu-id="10c1f-115">If the `regCount` value is too small for the number of registers indicated by the mask, the higher numbered registers will be truncated from the set.</span></span> <span data-ttu-id="10c1f-116">如果 `regCount` 值太大，则 `regBuffer` 不会修改未使用的元素。</span><span class="sxs-lookup"><span data-stu-id="10c1f-116">If the `regCount` value is too large, the unused `regBuffer` elements will be unmodified.</span></span>  
  
 <span data-ttu-id="10c1f-117">如果位掩码指定的寄存器不可用，则 `GetRegisters` 返回该寄存器的不确定值。</span><span class="sxs-lookup"><span data-stu-id="10c1f-117">If the bit mask specifies a register that is unavailable, `GetRegisters` returns an indeterminate value for that register.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="10c1f-118">要求</span><span class="sxs-lookup"><span data-stu-id="10c1f-118">Requirements</span></span>  

 <span data-ttu-id="10c1f-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="10c1f-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="10c1f-120">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="10c1f-120">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="10c1f-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="10c1f-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="10c1f-122">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="10c1f-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="10c1f-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="10c1f-123">See also</span></span>

- [<span data-ttu-id="10c1f-124">ICorDebugRegisterSet 接口</span><span class="sxs-lookup"><span data-stu-id="10c1f-124">ICorDebugRegisterSet Interface</span></span>](icordebugregisterset-interface.md)
- [<span data-ttu-id="10c1f-125">ICorDebugRegisterSet2 接口</span><span class="sxs-lookup"><span data-stu-id="10c1f-125">ICorDebugRegisterSet2 Interface</span></span>](icordebugregisterset2-interface.md)
