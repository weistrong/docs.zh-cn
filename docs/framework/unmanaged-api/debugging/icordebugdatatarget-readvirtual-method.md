---
description: 了解详细信息： ICorDebugDataTarget：： ReadVirtual 方法
title: ICorDebugDataTarget::ReadVirtual 方法
ms.date: 03/30/2017
api_name:
- ICorDebugDataTarget.ReadVirtual Method
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugDataTarget::ReadVirtual
helpviewer_keywords:
- ICorDebugDataTarget::ReadVirtual method [.NET Framework debugging]
- ReadVirtual method, ICorDebugDataTarget interface [.NET Framework debugging]
ms.assetid: 55e57640-b3d2-413d-b4f4-fbc27fb8e37c
topic_type:
- apiref
ms.openlocfilehash: 4525ba1e5dc685813d963dab96879b886987f38f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710590"
---
# <a name="icordebugdatatargetreadvirtual-method"></a><span data-ttu-id="ae54d-103">ICorDebugDataTarget::ReadVirtual 方法</span><span class="sxs-lookup"><span data-stu-id="ae54d-103">ICorDebugDataTarget::ReadVirtual Method</span></span>

<span data-ttu-id="ae54d-104">获取从指定地址开始的连续内存块，并将其返回到提供的缓冲区中。</span><span class="sxs-lookup"><span data-stu-id="ae54d-104">Gets a block of contiguous memory starting at the specified address, and returns it in the supplied buffer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ae54d-105">语法</span><span class="sxs-lookup"><span data-stu-id="ae54d-105">Syntax</span></span>  
  
```cpp  
HRESULT ReadVirtual(  
    [in] CORDB_ADDRESS   address,  
    [out, size_is(bytesRequested), length_is(*pBytesRead)]  
          BYTE *     pBuffer,  
    [in]  ULONG32    bytesRequested,  
    [out] ULONG32 *  pBytesRead);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ae54d-106">参数</span><span class="sxs-lookup"><span data-stu-id="ae54d-106">Parameters</span></span>  

 `address`  
 <span data-ttu-id="ae54d-107">中请求的内存的开始地址。</span><span class="sxs-lookup"><span data-stu-id="ae54d-107">[in] The start address of requested memory.</span></span>  
  
 `pbuffer`  
 <span data-ttu-id="ae54d-108">弄内存将存储到的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="ae54d-108">[out] The buffer where the memory will be stored.</span></span>  
  
 `bytesRequested`  
 <span data-ttu-id="ae54d-109">中要从目标地址获取的字节数。</span><span class="sxs-lookup"><span data-stu-id="ae54d-109">[in] The number of bytes to get from the target address.</span></span>  
  
 `pBytesRead`  
 <span data-ttu-id="ae54d-110">弄实际从目标地址中读取的字节数。</span><span class="sxs-lookup"><span data-stu-id="ae54d-110">[out] The number of bytes actually read from the target address.</span></span> <span data-ttu-id="ae54d-111">该值可以少于 `bytesRequested` 。</span><span class="sxs-lookup"><span data-stu-id="ae54d-111">This can be fewer than `bytesRequested`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ae54d-112">备注</span><span class="sxs-lookup"><span data-stu-id="ae54d-112">Remarks</span></span>  

 <span data-ttu-id="ae54d-113">如果可以读取指定开始地址处的第一个字节 () ，则调用应返回成功 (，以支持通过自描述长度有效读取数据结构，如) 以 null 结尾的字符串。</span><span class="sxs-lookup"><span data-stu-id="ae54d-113">If the first byte (at the specified start address) can be read, the call should return success (to support efficient reading of data structures with self-describing length, like null-terminated strings).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ae54d-114">要求</span><span class="sxs-lookup"><span data-stu-id="ae54d-114">Requirements</span></span>  

 <span data-ttu-id="ae54d-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ae54d-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ae54d-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="ae54d-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ae54d-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ae54d-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ae54d-118">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ae54d-118">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae54d-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="ae54d-119">See also</span></span>

- [<span data-ttu-id="ae54d-120">ICorDebugDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="ae54d-120">ICorDebugDataTarget Interface</span></span>](icordebugdatatarget-interface.md)
- [<span data-ttu-id="ae54d-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="ae54d-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="ae54d-122">调试</span><span class="sxs-lookup"><span data-stu-id="ae54d-122">Debugging</span></span>](index.md)
