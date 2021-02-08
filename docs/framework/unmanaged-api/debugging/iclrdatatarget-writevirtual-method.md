---
description: 了解详细信息： ICLRDataTarget：： WriteVirtual 方法
title: ICLRDataTarget::WriteVirtual 方法
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.WriteVirtual
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::WriteVirtual
helpviewer_keywords:
- ICLRDataTarget::WriteVirtual method [.NET Framework debugging]
- WriteVirtual method [.NET Framework debugging]
ms.assetid: d627e8b7-a605-40ac-b9bb-da9a3f1b66d9
topic_type:
- apiref
ms.openlocfilehash: 29ff8d629c5797099dab155802fff99786f4ce15
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794853"
---
# <a name="iclrdatatargetwritevirtual-method"></a><span data-ttu-id="6e8ee-103">ICLRDataTarget::WriteVirtual 方法</span><span class="sxs-lookup"><span data-stu-id="6e8ee-103">ICLRDataTarget::WriteVirtual Method</span></span>

<span data-ttu-id="6e8ee-104">将数据从指定的缓冲区写入指定的虚拟内存地址。</span><span class="sxs-lookup"><span data-stu-id="6e8ee-104">Writes data from the specified buffer to the specified virtual memory address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6e8ee-105">语法</span><span class="sxs-lookup"><span data-stu-id="6e8ee-105">Syntax</span></span>  
  
```cpp  
HRESULT WriteVirtual (  
    [in] CLRDATA_ADDRESS    address,  
    [in, size_is(bytesRequested)]
        BYTE                *buffer,  
    [in] ULONG32            bytesRequested,  
    [out] ULONG32           *bytesWritten  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6e8ee-106">参数</span><span class="sxs-lookup"><span data-stu-id="6e8ee-106">Parameters</span></span>  

 `address`  
 <span data-ttu-id="6e8ee-107">中存储虚拟内存地址的 CLRDATA_ADDRESS。</span><span class="sxs-lookup"><span data-stu-id="6e8ee-107">[in] A CLRDATA_ADDRESS that stores the virtual memory address.</span></span>  
  
 `buffer`  
 <span data-ttu-id="6e8ee-108">中指向存储要写入的数据的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="6e8ee-108">[in] A pointer to a buffer that stores the data to be written.</span></span>  
  
 `bytesRequested`  
 <span data-ttu-id="6e8ee-109">中要写入的字节数。</span><span class="sxs-lookup"><span data-stu-id="6e8ee-109">[in] The number of bytes to be written.</span></span>  
  
 `bytesWritten`  
 <span data-ttu-id="6e8ee-110">弄指向已写入的实际字节数的指针。</span><span class="sxs-lookup"><span data-stu-id="6e8ee-110">[out] A pointer to the actual number of bytes that were written.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6e8ee-111">要求</span><span class="sxs-lookup"><span data-stu-id="6e8ee-111">Requirements</span></span>  

 <span data-ttu-id="6e8ee-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6e8ee-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6e8ee-113">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="6e8ee-113">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="6e8ee-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6e8ee-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6e8ee-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6e8ee-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6e8ee-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="6e8ee-116">See also</span></span>

- [<span data-ttu-id="6e8ee-117">ICLRDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="6e8ee-117">ICLRDataTarget Interface</span></span>](iclrdatatarget-interface.md)
