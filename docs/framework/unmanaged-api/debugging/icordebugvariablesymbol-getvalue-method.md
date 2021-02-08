---
description: 了解详细信息： ICorDebugVariableSymbol：： GetValue 方法
title: ICorDebugVariableSymbol::GetValue 方法
ms.date: 03/30/2017
ms.assetid: 90abece1-392e-4ade-94a1-30c75b0f7074
ms.openlocfilehash: ccd7eae5cc4740e83d0210a903ba0e7778aa8896
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790563"
---
# <a name="icordebugvariablesymbolgetvalue-method"></a><span data-ttu-id="38162-103">ICorDebugVariableSymbol::GetValue 方法</span><span class="sxs-lookup"><span data-stu-id="38162-103">ICorDebugVariableSymbol::GetValue Method</span></span>

<span data-ttu-id="38162-104">获取作为字节数组的变量的值。</span><span class="sxs-lookup"><span data-stu-id="38162-104">Gets the value of a variable as a byte array.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="38162-105">语法</span><span class="sxs-lookup"><span data-stu-id="38162-105">Syntax</span></span>  
  
```cpp  
HRESULT GetValue(  
   [in] ULONG32 offset,  
   [in] ULONG32 cbContext,  
   [in, size_is(cbContext)] BYTE context[],  
   [in] ULONG32 cbValue,  
   [out] ULONG32 *pcbValue,  
   [out, size_is(cbValue), length_is(*pcbValue)] BYTE pValue[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="38162-106">参数</span><span class="sxs-lookup"><span data-stu-id="38162-106">Parameters</span></span>  

 `offset`  
 <span data-ttu-id="38162-107">[in] 从其读取值的变量中的起始偏移量。</span><span class="sxs-lookup"><span data-stu-id="38162-107">[in] The starting offset in the variable from which to read the value.</span></span> <span data-ttu-id="38162-108">读取对象中的成员字段时使用此参数。</span><span class="sxs-lookup"><span data-stu-id="38162-108">This parameter is used when reading member fields in an object.</span></span>  
  
 `cbContext`  
 <span data-ttu-id="38162-109">[in] `context` 参数的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="38162-109">[in] The size in bytes of the `context` argument.</span></span>  
  
 `context`  
 <span data-ttu-id="38162-110">[in] 用于读取值的线程上下文。</span><span class="sxs-lookup"><span data-stu-id="38162-110">[in] The thread context used to read the value.</span></span>  
  
 `cbValue`  
 <span data-ttu-id="38162-111">[in] `pValue` 缓冲区的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="38162-111">[in] The size in bytes of the `pValue` buffer.</span></span>  
  
 `pcbValue`  
 <span data-ttu-id="38162-112">[out] 实际写入 `pValue` 缓冲区的字节数。</span><span class="sxs-lookup"><span data-stu-id="38162-112">[out] The number of bytes actually written to the `pValue` buffer.</span></span>  
  
 `pValue`  
 <span data-ttu-id="38162-113">[out] 包含变量值的字节数组。</span><span class="sxs-lookup"><span data-stu-id="38162-113">[out] A byte array that contains the value of the variable.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="38162-114">备注</span><span class="sxs-lookup"><span data-stu-id="38162-114">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="38162-115">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="38162-115">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="38162-116">要求</span><span class="sxs-lookup"><span data-stu-id="38162-116">Requirements</span></span>  

 <span data-ttu-id="38162-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="38162-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="38162-118">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="38162-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="38162-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="38162-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="38162-120">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="38162-120">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="38162-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="38162-121">See also</span></span>

- [<span data-ttu-id="38162-122">ICorDebugVariableSymbol 接口</span><span class="sxs-lookup"><span data-stu-id="38162-122">ICorDebugVariableSymbol Interface</span></span>](icordebugvariablesymbol-interface.md)
- [<span data-ttu-id="38162-123">调试接口</span><span class="sxs-lookup"><span data-stu-id="38162-123">Debugging Interfaces</span></span>](debugging-interfaces.md)
