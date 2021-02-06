---
description: 了解详细信息： ICLRStrongName：： GetHashFromBlob 方法
title: ICLRStrongName::GetHashFromBlob 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName.GetHashFromBlob
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::GetHashFromBlob
helpviewer_keywords:
- ICLRStrongName::GetHashFromBlob method [.NET Framework hosting]
- GetHashFromBlob method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: f91d0f89-f356-49ac-aafb-50fad963c13d
topic_type:
- apiref
ms.openlocfilehash: 20d03184f57e77741e656575038e426ee37968f9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637061"
---
# <a name="iclrstrongnamegethashfromblob-method"></a><span data-ttu-id="63371-103">ICLRStrongName::GetHashFromBlob 方法</span><span class="sxs-lookup"><span data-stu-id="63371-103">ICLRStrongName::GetHashFromBlob Method</span></span>

<span data-ttu-id="63371-104">使用指定的哈希算法获取指定内存地址处的程序集的哈希。</span><span class="sxs-lookup"><span data-stu-id="63371-104">Gets a hash of the assembly at the specified memory address, using the specified hash algorithm.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="63371-105">语法</span><span class="sxs-lookup"><span data-stu-id="63371-105">Syntax</span></span>  
  
```cpp  
HRESULT GetHashFromBlob (  
    [in]  BYTE    *pbBlob,  
    [in]  DWORD   cchBlob,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE    *pbHash,  
    [in]  DWORD   cchHash,  
    [out] DWORD   *pchHash  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="63371-106">参数</span><span class="sxs-lookup"><span data-stu-id="63371-106">Parameters</span></span>  

 `pbBlob`  
 <span data-ttu-id="63371-107">中一个指针，指向要进行哈希处理的内存块的地址。</span><span class="sxs-lookup"><span data-stu-id="63371-107">[in] A pointer to the address of the memory block to be hashed.</span></span>  
  
 `cchBlob`  
 <span data-ttu-id="63371-108">中内存块的长度（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="63371-108">[in] The length, in bytes, of the memory block.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="63371-109">[in，out]指定哈希算法的常量。</span><span class="sxs-lookup"><span data-stu-id="63371-109">[in, out] A constant that specifies the hash algorithm.</span></span> <span data-ttu-id="63371-110">对于默认算法，使用零。</span><span class="sxs-lookup"><span data-stu-id="63371-110">Use zero for the default algorithm.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="63371-111">弄返回的哈希缓冲区。</span><span class="sxs-lookup"><span data-stu-id="63371-111">[out] The returned hash buffer.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="63371-112">中请求的最大大小 `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="63371-112">[in] The requested maximum size of `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="63371-113">弄返回的的大小（以字节为单位） `pbHash` 。</span><span class="sxs-lookup"><span data-stu-id="63371-113">[out] The size, in bytes, of the returned `pbHash`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="63371-114">返回值</span><span class="sxs-lookup"><span data-stu-id="63371-114">Return Value</span></span>  

 <span data-ttu-id="63371-115">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="63371-115">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="63371-116">要求</span><span class="sxs-lookup"><span data-stu-id="63371-116">Requirements</span></span>  

 <span data-ttu-id="63371-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="63371-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="63371-118">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="63371-118">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="63371-119">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="63371-119">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="63371-120">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="63371-120">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="63371-121">另请参阅</span><span class="sxs-lookup"><span data-stu-id="63371-121">See also</span></span>

- [<span data-ttu-id="63371-122">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="63371-122">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
