---
description: 了解详细信息： ICLRStrongName：： StrongNameKeyGen 方法
title: ICLRStrongName::StrongNameKeyGen 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameKeyGen
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameKeyGen
helpviewer_keywords:
- StrongNameKeyGen method, ICLRStrongName interface [.NET Framework hosting]
- ICLRStrongName::StrongNameKeyGen method [.NET Framework hosting]
ms.assetid: ac5c1245-9acf-4271-9c08-3d9b7c670df3
topic_type:
- apiref
ms.openlocfilehash: c445e1f0290d907f7820c0000f602f2668f59103
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799547"
---
# <a name="iclrstrongnamestrongnamekeygen-method"></a><span data-ttu-id="2337e-103">ICLRStrongName::StrongNameKeyGen 方法</span><span class="sxs-lookup"><span data-stu-id="2337e-103">ICLRStrongName::StrongNameKeyGen Method</span></span>

<span data-ttu-id="2337e-104">创建新的公钥/私钥对，以便强名称使用。</span><span class="sxs-lookup"><span data-stu-id="2337e-104">Creates a new public/private key pair for strong name use.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2337e-105">语法</span><span class="sxs-lookup"><span data-stu-id="2337e-105">Syntax</span></span>  
  
```cpp  
HRESULT StrongNameKeyGen (  
    [in]  LPCWSTR   wszKeyContainer,  
    [in]  DWORD     dwFlags,  
    [out] BYTE      **ppbKeyBlob,  
    [out] ULONG     *pcbKeyBlob  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2337e-106">参数</span><span class="sxs-lookup"><span data-stu-id="2337e-106">Parameters</span></span>  

 `wszKeyContainer`  
 <span data-ttu-id="2337e-107">中请求的密钥容器名称。</span><span class="sxs-lookup"><span data-stu-id="2337e-107">[in] The requested key container name.</span></span> <span data-ttu-id="2337e-108">`wszKeyContainer` 必须为非空字符串，或者为 null 以生成临时名称。</span><span class="sxs-lookup"><span data-stu-id="2337e-108">`wszKeyContainer` must either be a non-empty string or null to generate a temporary name.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="2337e-109">中一个值，该值指定是否保留注册的密钥。</span><span class="sxs-lookup"><span data-stu-id="2337e-109">[in] A value that specifies whether to leave the key registered.</span></span> <span data-ttu-id="2337e-110">支持以下值：</span><span class="sxs-lookup"><span data-stu-id="2337e-110">The following values are supported:</span></span>  
  
- <span data-ttu-id="2337e-111">0x00000000-在 `wszKeyContainer` 为 null 时用于生成临时密钥容器名称。</span><span class="sxs-lookup"><span data-stu-id="2337e-111">0x00000000 - Used when `wszKeyContainer` is null to generate a temporary key container name.</span></span>  
  
- <span data-ttu-id="2337e-112">0x00000001 (`SN_LEAVE_KEY`) -指定应保持注册该密钥。</span><span class="sxs-lookup"><span data-stu-id="2337e-112">0x00000001 (`SN_LEAVE_KEY`) - Specifies that the key should be left registered.</span></span>  
  
 `ppbKeyBlob`  
 <span data-ttu-id="2337e-113">弄返回的公钥/私钥对。</span><span class="sxs-lookup"><span data-stu-id="2337e-113">[out] The returned public/private key pair.</span></span>  
  
 `pcbKeyBlob`  
 <span data-ttu-id="2337e-114">弄的大小（以字节为单位） `ppbKeyBlob` 。</span><span class="sxs-lookup"><span data-stu-id="2337e-114">[out] The size, in bytes, of `ppbKeyBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2337e-115">返回值</span><span class="sxs-lookup"><span data-stu-id="2337e-115">Return Value</span></span>  

 <span data-ttu-id="2337e-116">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="2337e-116">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2337e-117">备注</span><span class="sxs-lookup"><span data-stu-id="2337e-117">Remarks</span></span>  

 <span data-ttu-id="2337e-118">[ICLRStrongName：： StrongNameKeyGen](iclrstrongname-strongnamekeygen-method.md)方法创建1024位键。</span><span class="sxs-lookup"><span data-stu-id="2337e-118">The [ICLRStrongName::StrongNameKeyGen](iclrstrongname-strongnamekeygen-method.md) method creates a 1024-bit key.</span></span> <span data-ttu-id="2337e-119">检索到密钥后，应调用 [ICLRStrongName：： StrongNameFreeBuffer](iclrstrongname-strongnamefreebuffer-method.md) 方法来释放已分配的内存。</span><span class="sxs-lookup"><span data-stu-id="2337e-119">After the key is retrieved, you should call the [ICLRStrongName::StrongNameFreeBuffer](iclrstrongname-strongnamefreebuffer-method.md) method to release the allocated memory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2337e-120">要求</span><span class="sxs-lookup"><span data-stu-id="2337e-120">Requirements</span></span>  

 <span data-ttu-id="2337e-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2337e-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2337e-122">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="2337e-122">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="2337e-123">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2337e-123">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2337e-124">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2337e-124">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2337e-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="2337e-125">See also</span></span>

- [<span data-ttu-id="2337e-126">StrongNameKeyGenEx 方法</span><span class="sxs-lookup"><span data-stu-id="2337e-126">StrongNameKeyGenEx Method</span></span>](iclrstrongname-strongnamekeygenex-method.md)
- [<span data-ttu-id="2337e-127">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="2337e-127">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
