---
description: 了解详细信息： StrongNameGetPublicKeyEx 方法
title: StrongNameGetPublicKeyEx 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName2.StrongNameGetPublicKeyEx
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- StrongNameGetPublicKeyEx
helpviewer_keywords:
- StrongNameGetPublicKeyEx method, ICLRStrongName2 interface [.NET Framework hosting]
- ICLRStrongName2::StrongNameGetPublicKeyEx method [.NET Framework hosting]
ms.assetid: 63d8260c-fb32-4f8f-a357-768afd570f68
topic_type:
- apiref
ms.openlocfilehash: bc9d40afc34509f852a0961823e264255125fa16
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99679298"
---
# <a name="strongnamegetpublickeyex-method"></a><span data-ttu-id="cc8d9-103">StrongNameGetPublicKeyEx 方法</span><span class="sxs-lookup"><span data-stu-id="cc8d9-103">StrongNameGetPublicKeyEx Method</span></span>

<span data-ttu-id="cc8d9-104">获取公钥/私钥对中的公钥，并指定哈希算法和签名算法。</span><span class="sxs-lookup"><span data-stu-id="cc8d9-104">Gets the public key from a public/private key pair, and specifies a hash algorithm and a signature algorithm.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cc8d9-105">语法</span><span class="sxs-lookup"><span data-stu-id="cc8d9-105">Syntax</span></span>  
  
```cpp  
HRESULT StrongNameGetPublicKey (
    [in]  LPCWSTR   pwzKeyContainer,  
    [in]  BYTE      *pbKeyBlob,  
    [in]  ULONG     cbKeyBlob,  
    [out] BYTE      **ppbPublicKeyBlob,  
    [out] ULONG     *pcbPublicKeyBlob  
    [in]  ULONG     uHashAlgId,  
    [in]  ULONG     uReserved,  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cc8d9-106">参数</span><span class="sxs-lookup"><span data-stu-id="cc8d9-106">Parameters</span></span>  

 `pwzKeyContainer`  
 <span data-ttu-id="cc8d9-107">中包含公钥/私钥对的密钥容器的名称。</span><span class="sxs-lookup"><span data-stu-id="cc8d9-107">[in] The name of the key container that contains the public/private key pair.</span></span> <span data-ttu-id="cc8d9-108">如果 `pbKeyBlob` 为 null，则 `szKeyContainer` 必须在加密服务提供程序 (CSP) 中指定有效容器。</span><span class="sxs-lookup"><span data-stu-id="cc8d9-108">If `pbKeyBlob` is null, `szKeyContainer` must specify a valid container within the cryptographic service provider (CSP).</span></span> <span data-ttu-id="cc8d9-109">在这种情况下，该 `StrongNameGetPublicKeyEx` 方法将从存储在容器中的密钥对中提取公钥。</span><span class="sxs-lookup"><span data-stu-id="cc8d9-109">In this case, the `StrongNameGetPublicKeyEx` method extracts the public key from the key pair stored in the container.</span></span>  
  
 <span data-ttu-id="cc8d9-110">如果不为 `pbKeyBlob` null，则假定密钥对包含在关键的二进制大型对象 (BLOB) 中。</span><span class="sxs-lookup"><span data-stu-id="cc8d9-110">If `pbKeyBlob` is not null, the key pair is assumed to be contained in the key binary large object (BLOB).</span></span>  
  
 <span data-ttu-id="cc8d9-111">密钥必须是1024位 Rivest-Rivest-shamir-adleman (RSA) 签名密钥。</span><span class="sxs-lookup"><span data-stu-id="cc8d9-111">The keys must be 1024-bit Rivest-Shamir-Adleman (RSA) signing keys.</span></span> <span data-ttu-id="cc8d9-112">此时不支持其他类型的密钥。</span><span class="sxs-lookup"><span data-stu-id="cc8d9-112">No other types of keys are supported at this time.</span></span>  
  
 `pbKeyBlob`  
 <span data-ttu-id="cc8d9-113">中指向公钥/私钥对的指针。</span><span class="sxs-lookup"><span data-stu-id="cc8d9-113">[in] A pointer to the public/private key pair.</span></span> <span data-ttu-id="cc8d9-114">此对采用 Win32 函数创建的格式 `CryptExportKey` 。</span><span class="sxs-lookup"><span data-stu-id="cc8d9-114">This pair is in the format created by the Win32 `CryptExportKey` function.</span></span> <span data-ttu-id="cc8d9-115">如果 `pbKeyBlob` 为 null，则假定指定的密钥容器 `szKeyContainer` 包含密钥对。</span><span class="sxs-lookup"><span data-stu-id="cc8d9-115">If `pbKeyBlob` is null, the key container specified by `szKeyContainer` is assumed to contain the key pair.</span></span>  
  
 `cbKeyBlob`  
 <span data-ttu-id="cc8d9-116">中的大小（以字节为单位） `pbKeyBlob` 。</span><span class="sxs-lookup"><span data-stu-id="cc8d9-116">[in] The size, in bytes, of `pbKeyBlob`.</span></span>  
  
 `ppbPublicKeyBlob`  
 <span data-ttu-id="cc8d9-117">弄返回的公钥 BLOB。</span><span class="sxs-lookup"><span data-stu-id="cc8d9-117">[out] The returned public key BLOB.</span></span> <span data-ttu-id="cc8d9-118">`ppbPublicKeyBlob`参数由公共语言运行时分配并返回给调用方。</span><span class="sxs-lookup"><span data-stu-id="cc8d9-118">The `ppbPublicKeyBlob` parameter is allocated by the common language runtime and returned to the caller.</span></span> <span data-ttu-id="cc8d9-119">调用方必须使用 [ICLRStrongName：： StrongNameFreeBuffer](iclrstrongname-strongnamefreebuffer-method.md) 方法释放内存。</span><span class="sxs-lookup"><span data-stu-id="cc8d9-119">The caller must free the memory by using the [ICLRStrongName::StrongNameFreeBuffer](iclrstrongname-strongnamefreebuffer-method.md) method.</span></span>  
  
 `pcbPublicKeyBlob`  
 <span data-ttu-id="cc8d9-120">弄返回的公钥 BLOB 的大小。</span><span class="sxs-lookup"><span data-stu-id="cc8d9-120">[out] The size of the returned public key BLOB.</span></span>  
  
 `uHashAlgId`  
 <span data-ttu-id="cc8d9-121">中程序集哈希算法。</span><span class="sxs-lookup"><span data-stu-id="cc8d9-121">[in] The assembly hash algorithm.</span></span> <span data-ttu-id="cc8d9-122">有关接受值的列表，请参阅 "备注" 部分。</span><span class="sxs-lookup"><span data-stu-id="cc8d9-122">See the Remarks section for a list of accepted values.</span></span>  
  
 `uReserved`  
 <span data-ttu-id="cc8d9-123">中保留以供将来使用;默认值为 null。</span><span class="sxs-lookup"><span data-stu-id="cc8d9-123">[in] Reserved for future use; defaults to null.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cc8d9-124">返回值</span><span class="sxs-lookup"><span data-stu-id="cc8d9-124">Return Value</span></span>  

 <span data-ttu-id="cc8d9-125">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="cc8d9-125">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cc8d9-126">备注</span><span class="sxs-lookup"><span data-stu-id="cc8d9-126">Remarks</span></span>  

 <span data-ttu-id="cc8d9-127">公钥包含在 [PublicKeyBlob](../strong-naming/publickeyblob-structure.md) 结构中。</span><span class="sxs-lookup"><span data-stu-id="cc8d9-127">The public key is contained in a [PublicKeyBlob](../strong-naming/publickeyblob-structure.md) structure.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cc8d9-128">备注</span><span class="sxs-lookup"><span data-stu-id="cc8d9-128">Remarks</span></span>  

 <span data-ttu-id="cc8d9-129">下表显示了该参数的接受值集 `uHashAlgId` 。</span><span class="sxs-lookup"><span data-stu-id="cc8d9-129">The following table shows the set of accepted values for the `uHashAlgId` parameter.</span></span>  
  
|<span data-ttu-id="cc8d9-130">名称</span><span class="sxs-lookup"><span data-stu-id="cc8d9-130">Name</span></span>|<span data-ttu-id="cc8d9-131">值</span><span class="sxs-lookup"><span data-stu-id="cc8d9-131">Value</span></span>|  
|----------|-----------|  
|<span data-ttu-id="cc8d9-132">无</span><span class="sxs-lookup"><span data-stu-id="cc8d9-132">None</span></span>|<span data-ttu-id="cc8d9-133">0</span><span class="sxs-lookup"><span data-stu-id="cc8d9-133">0</span></span>|  
|<span data-ttu-id="cc8d9-134">SHA-1</span><span class="sxs-lookup"><span data-stu-id="cc8d9-134">SHA-1</span></span>|<span data-ttu-id="cc8d9-135">0x8004</span><span class="sxs-lookup"><span data-stu-id="cc8d9-135">0x8004</span></span>|  
|<span data-ttu-id="cc8d9-136">SHA-256</span><span class="sxs-lookup"><span data-stu-id="cc8d9-136">SHA-256</span></span>|<span data-ttu-id="cc8d9-137">0x800c</span><span class="sxs-lookup"><span data-stu-id="cc8d9-137">0x800c</span></span>|  
|<span data-ttu-id="cc8d9-138">SHA-384</span><span class="sxs-lookup"><span data-stu-id="cc8d9-138">SHA-384</span></span>|<span data-ttu-id="cc8d9-139">0x800d</span><span class="sxs-lookup"><span data-stu-id="cc8d9-139">0x800d</span></span>|  
|<span data-ttu-id="cc8d9-140">SHA-512</span><span class="sxs-lookup"><span data-stu-id="cc8d9-140">SHA-512</span></span>|<span data-ttu-id="cc8d9-141">0x800e</span><span class="sxs-lookup"><span data-stu-id="cc8d9-141">0x800e</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="cc8d9-142">要求</span><span class="sxs-lookup"><span data-stu-id="cc8d9-142">Requirements</span></span>  

 <span data-ttu-id="cc8d9-143">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="cc8d9-143">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="cc8d9-144">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="cc8d9-144">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="cc8d9-145">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="cc8d9-145">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="cc8d9-146">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="cc8d9-146">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cc8d9-147">请参阅</span><span class="sxs-lookup"><span data-stu-id="cc8d9-147">See also</span></span>

- [<span data-ttu-id="cc8d9-148">StrongNameTokenFromPublicKey 方法</span><span class="sxs-lookup"><span data-stu-id="cc8d9-148">StrongNameTokenFromPublicKey Method</span></span>](iclrstrongname-strongnametokenfrompublickey-method.md)
- [<span data-ttu-id="cc8d9-149">PublicKeyBlob 结构</span><span class="sxs-lookup"><span data-stu-id="cc8d9-149">PublicKeyBlob Structure</span></span>](../strong-naming/publickeyblob-structure.md)
- [<span data-ttu-id="cc8d9-150">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="cc8d9-150">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
- [<span data-ttu-id="cc8d9-151">StrongNameGetPublicKey 方法</span><span class="sxs-lookup"><span data-stu-id="cc8d9-151">StrongNameGetPublicKey Method</span></span>](iclrstrongname-strongnamegetpublickey-method.md)
