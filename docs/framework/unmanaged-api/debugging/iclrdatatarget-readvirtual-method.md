---
description: 了解详细信息： ICLRDataTarget：： ReadVirtual 方法
title: ICLRDataTarget::ReadVirtual 方法
ms.date: 03/30/2017
api_name:
- ICLRDataTarget.ReadVirtual
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget::ReadVirtual
helpviewer_keywords:
- ReadVirtual method, ICLRDataTarget interface [.NET Framework debugging]
- ICLRDataTarget::ReadVirtual method [.NET Framework debugging]
ms.assetid: da3769eb-1828-4aa1-b9ed-db4842136a43
topic_type:
- apiref
ms.openlocfilehash: 740a89c95092cfad7974d6bc708c5d8b0d2a9172
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99738177"
---
# <a name="iclrdatatargetreadvirtual-method"></a><span data-ttu-id="20f8b-103">ICLRDataTarget::ReadVirtual 方法</span><span class="sxs-lookup"><span data-stu-id="20f8b-103">ICLRDataTarget::ReadVirtual Method</span></span>

<span data-ttu-id="20f8b-104">将数据从指定的虚拟内存地址读入指定的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="20f8b-104">Reads data from the specified virtual memory address into the specified buffer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="20f8b-105">语法</span><span class="sxs-lookup"><span data-stu-id="20f8b-105">Syntax</span></span>  
  
```cpp  
HRESULT ReadVirtual (  
    [in] CLRDATA_ADDRESS    address,  
    [out, size_is(bytesRequested), length_is(*bytesRead)]
        BYTE                *buffer,  
    [in] ULONG32            bytesRequested,  
    [out] ULONG32           *bytesRead  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="20f8b-106">参数</span><span class="sxs-lookup"><span data-stu-id="20f8b-106">Parameters</span></span>  

 `address`  
 <span data-ttu-id="20f8b-107">中存储虚拟内存地址的 CLRDATA_ADDRESS。</span><span class="sxs-lookup"><span data-stu-id="20f8b-107">[in] A CLRDATA_ADDRESS that stores the virtual memory address.</span></span>  
  
 `buffer`  
 <span data-ttu-id="20f8b-108">弄指向接收数据的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="20f8b-108">[out] A pointer to a buffer that receives the data.</span></span>  
  
 `bytesRequested`  
 <span data-ttu-id="20f8b-109">中缓冲区的长度。</span><span class="sxs-lookup"><span data-stu-id="20f8b-109">[in] The length of the buffer.</span></span>  
  
 `bytesRead`  
 <span data-ttu-id="20f8b-110">弄指向返回的字节数的指针。</span><span class="sxs-lookup"><span data-stu-id="20f8b-110">[out] A pointer to the number of bytes returned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="20f8b-111">要求</span><span class="sxs-lookup"><span data-stu-id="20f8b-111">Requirements</span></span>  

 <span data-ttu-id="20f8b-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="20f8b-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="20f8b-113">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="20f8b-113">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="20f8b-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="20f8b-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="20f8b-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="20f8b-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="20f8b-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="20f8b-116">See also</span></span>

- [<span data-ttu-id="20f8b-117">ICLRDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="20f8b-117">ICLRDataTarget Interface</span></span>](iclrdatatarget-interface.md)
