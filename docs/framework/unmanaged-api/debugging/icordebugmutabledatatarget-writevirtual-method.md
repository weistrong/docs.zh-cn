---
description: 了解详细信息： ICorDebugMutableDataTarget：： WriteVirtual 方法
title: ICorDebugMutableDataTarget::WriteVirtual 方法
ms.date: 03/30/2017
ms.assetid: 80833648-58a7-491a-8dc8-9a48e9bb3adc
ms.openlocfilehash: 3f3400456b7af51f4b24d7e14e35d641f03a8bfd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637815"
---
# <a name="icordebugmutabledatatargetwritevirtual-method"></a><span data-ttu-id="07b28-103">ICorDebugMutableDataTarget::WriteVirtual 方法</span><span class="sxs-lookup"><span data-stu-id="07b28-103">ICorDebugMutableDataTarget::WriteVirtual Method</span></span>

<span data-ttu-id="07b28-104">将内存写入目标进程地址空间。</span><span class="sxs-lookup"><span data-stu-id="07b28-104">Writes memory into the target process address space.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="07b28-105">语法</span><span class="sxs-lookup"><span data-stu-id="07b28-105">Syntax</span></span>  
  
```cpp  
HRESULT WriteVirtual(  
   [in] CORDB_ADDRESS address,  
   [in, size_is(bytesRequested)] const BYTE * pBuffer,  
   [in] ULONG32 bytesRequested);  
```  
  
## <a name="parameters"></a><span data-ttu-id="07b28-106">参数</span><span class="sxs-lookup"><span data-stu-id="07b28-106">Parameters</span></span>  

 `address`  
 <span data-ttu-id="07b28-107">[in] 要在此处写入 `pBuffer` 的内容的地址。</span><span class="sxs-lookup"><span data-stu-id="07b28-107">[in] The address at which to write the contents of `pBuffer`.</span></span>  
  
 `pBuffer`  
 <span data-ttu-id="07b28-108">[in] 指向包含要写入字节的字节数组的指针。</span><span class="sxs-lookup"><span data-stu-id="07b28-108">[in] A pointer to a byte array that contains the bytes to be written.</span></span>  
  
 `address`  
 <span data-ttu-id="07b28-109">[in] `pBuffer` 中的字节数。</span><span class="sxs-lookup"><span data-stu-id="07b28-109">[in] The number of bytes in `pBuffer`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="07b28-110">返回值</span><span class="sxs-lookup"><span data-stu-id="07b28-110">Return Value</span></span>  

 <span data-ttu-id="07b28-111">若成功，则为`S_OK`若失败，则为 `HRESULT`。</span><span class="sxs-lookup"><span data-stu-id="07b28-111">`S_OK` on success, or any other `HRESULT` on failure.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="07b28-112">备注</span><span class="sxs-lookup"><span data-stu-id="07b28-112">Remarks</span></span>  

 <span data-ttu-id="07b28-113">如果无法写入任何字节，方法调用失败且不更改目标地址空间中的任何字节。</span><span class="sxs-lookup"><span data-stu-id="07b28-113">If any bytes cannot be written, the method call fails without changing any bytes in the target address space.</span></span> <span data-ttu-id="07b28-114">（否则，目标状态不一致，从而使进一步的调试不可靠。）</span><span class="sxs-lookup"><span data-stu-id="07b28-114">(Otherwise, the target would be in an inconsistent state that makes further debugging unreliable.)</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="07b28-115">要求</span><span class="sxs-lookup"><span data-stu-id="07b28-115">Requirements</span></span>  

 <span data-ttu-id="07b28-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="07b28-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="07b28-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="07b28-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="07b28-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="07b28-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="07b28-119">**.NET Framework 版本：**[!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="07b28-119">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="07b28-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="07b28-120">See also</span></span>

- [<span data-ttu-id="07b28-121">ICorDebugMutableDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="07b28-121">ICorDebugMutableDataTarget Interface</span></span>](icordebugmutabledatatarget-interface.md)
- [<span data-ttu-id="07b28-122">调试接口</span><span class="sxs-lookup"><span data-stu-id="07b28-122">Debugging Interfaces</span></span>](debugging-interfaces.md)
