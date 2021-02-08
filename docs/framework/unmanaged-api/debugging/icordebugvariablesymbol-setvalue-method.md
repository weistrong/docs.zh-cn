---
description: 了解详细信息： ICorDebugVariableSymbol：： SetValue 方法
title: ICorDebugVariableSymbol::SetValue 方法
ms.date: 03/30/2017
ms.assetid: 4609418d-71fa-44bc-9618-4d529d25cabb
ms.openlocfilehash: aa36712defcf44039f17fe846113c15814549e09
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800846"
---
# <a name="icordebugvariablesymbolsetvalue-method"></a><span data-ttu-id="0fb77-103">ICorDebugVariableSymbol::SetValue 方法</span><span class="sxs-lookup"><span data-stu-id="0fb77-103">ICorDebugVariableSymbol::SetValue Method</span></span>

<span data-ttu-id="0fb77-104">将字节数组的值分配给变量。</span><span class="sxs-lookup"><span data-stu-id="0fb77-104">Assigns the value of a byte array to a variable.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0fb77-105">语法</span><span class="sxs-lookup"><span data-stu-id="0fb77-105">Syntax</span></span>  
  
```cpp  
HRESULT SetValue(  
   [in] ULONG32 offset,  
   [in] DWORD threadID,  
   [in] ULONG32 cbContext,  
   [in, size_is(cbContext)] BYTE context[],  
   [in] ULONG32 cbValue,  
   [in, size_is(cbValue)] BYTE pValue[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0fb77-106">参数</span><span class="sxs-lookup"><span data-stu-id="0fb77-106">Parameters</span></span>  

 `offset`  
 <span data-ttu-id="0fb77-107">[in] 设置值时变量中的起始偏移量。</span><span class="sxs-lookup"><span data-stu-id="0fb77-107">[in] The starting offset in the variable at which to set the value.</span></span> <span data-ttu-id="0fb77-108">在对象中写入成员字段时，则使用此参数。</span><span class="sxs-lookup"><span data-stu-id="0fb77-108">This parameter is used when writing to member fields in an object.</span></span>  
  
 `threadID`  
 <span data-ttu-id="0fb77-109">[in] 其上下文必须更新以反映新值的线程的线程标识符。</span><span class="sxs-lookup"><span data-stu-id="0fb77-109">[in] The thread identifier of the thread whose context must be updated to reflect the new value.</span></span>  
  
 `cbContext`  
 <span data-ttu-id="0fb77-110">[in] 线程上下文的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="0fb77-110">[in] The size in bytes of the thread context.</span></span>  
  
 `context`  
 <span data-ttu-id="0fb77-111">[in] 用于写入值的线程上下文。</span><span class="sxs-lookup"><span data-stu-id="0fb77-111">[in] The thread context used to write the value.</span></span>  
  
 `cbValue`  
 <span data-ttu-id="0fb77-112">[in] `pValue` 缓冲区的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="0fb77-112">[in] The size in bytes of the `pValue` buffer.</span></span>  
  
 `pValue`  
 <span data-ttu-id="0fb77-113">[in] 包含要设置的值的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="0fb77-113">[in] The buffer that contains the value to set.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0fb77-114">备注</span><span class="sxs-lookup"><span data-stu-id="0fb77-114">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="0fb77-115">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="0fb77-115">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0fb77-116">要求</span><span class="sxs-lookup"><span data-stu-id="0fb77-116">Requirements</span></span>  

 <span data-ttu-id="0fb77-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0fb77-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0fb77-118">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0fb77-118">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0fb77-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0fb77-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0fb77-120">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0fb77-120">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0fb77-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="0fb77-121">See also</span></span>

- [<span data-ttu-id="0fb77-122">ICorDebugVariableSymbol 接口</span><span class="sxs-lookup"><span data-stu-id="0fb77-122">ICorDebugVariableSymbol Interface</span></span>](icordebugvariablesymbol-interface.md)
- [<span data-ttu-id="0fb77-123">调试接口</span><span class="sxs-lookup"><span data-stu-id="0fb77-123">Debugging Interfaces</span></span>](debugging-interfaces.md)
