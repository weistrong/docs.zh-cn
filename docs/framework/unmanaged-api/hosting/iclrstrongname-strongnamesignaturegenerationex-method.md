---
description: 了解详细信息： ICLRStrongName：： StrongNameSignatureGenerationEx 方法
title: ICLRStrongName::StrongNameSignatureGenerationEx 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameSignatureGenerationEx
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameSignatureGenerationEx
helpviewer_keywords:
- ICLRStrongName::StrongNameSignatureGenerationEx method [.NET Framework hosting]
- StrongNameSignatureGenerationEx method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: c3f34584-c6e2-41fd-bb44-e44da8546309
topic_type:
- apiref
ms.openlocfilehash: 911f55aa509c25eb0d95d6d2a31c9f715af2080d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781865"
---
# <a name="iclrstrongnamestrongnamesignaturegenerationex-method"></a><span data-ttu-id="3f9b9-103">ICLRStrongName::StrongNameSignatureGenerationEx 方法</span><span class="sxs-lookup"><span data-stu-id="3f9b9-103">ICLRStrongName::StrongNameSignatureGenerationEx Method</span></span>

<span data-ttu-id="3f9b9-104">根据指定的标志，为指定的程序集生成强名称签名。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-104">Generates a strong name signature for the specified assembly, according to the specified flags.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3f9b9-105">语法</span><span class="sxs-lookup"><span data-stu-id="3f9b9-105">Syntax</span></span>  
  
```cpp
HRESULT StrongNameSignatureGenerationEx (  
    [in]  LPCWSTR   wszFilePath,  
    [in]  LPCWSTR   wszKeyContainer,  
    [in]  BYTE      *pbKeyBlob,  
    [in]  ULONG     cbKeyBlob,  
    [out] BYTE      **ppbSignatureBlob,  
    [out] ULONG     *pcbSignatureBlob,  
    [in]  DWORD     dwFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3f9b9-106">参数</span><span class="sxs-lookup"><span data-stu-id="3f9b9-106">Parameters</span></span>  

 `wszFilePath`  
 <span data-ttu-id="3f9b9-107">中包含要为其生成强名称签名的程序集清单的文件的路径。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-107">[in] The path to the file that contains the manifest of the assembly for which the strong name signature will be generated.</span></span>  
  
 `wszKeyContainer`  
 <span data-ttu-id="3f9b9-108">中包含公钥/私钥对的密钥容器的名称。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-108">[in] The name of the key container that contains the public/private key pair.</span></span>  
  
 <span data-ttu-id="3f9b9-109">如果 `pbKeyBlob` 为 null，则 `wszKeyContainer` 必须在加密服务提供程序 (CSP) 中指定有效容器。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-109">If `pbKeyBlob` is null, `wszKeyContainer` must specify a valid container within the cryptographic service provider (CSP).</span></span> <span data-ttu-id="3f9b9-110">在这种情况下，存储在容器中的密钥对用于对文件进行签名。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-110">In this case, the key pair stored in the container is used to sign the file.</span></span>  
  
 <span data-ttu-id="3f9b9-111">如果不为 `pbKeyBlob` null，则假定密钥对包含在关键的二进制大型对象 (BLOB) 中。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-111">If `pbKeyBlob` is not null, the key pair is assumed to be contained in the key binary large object (BLOB).</span></span>  
  
 `pbKeyBlob`  
 <span data-ttu-id="3f9b9-112">中指向公钥/私钥对的指针。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-112">[in] A pointer to the public/private key pair.</span></span> <span data-ttu-id="3f9b9-113">此对采用 Win32 函数创建的格式 `CryptExportKey` 。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-113">This pair is in the format created by the Win32 `CryptExportKey` function.</span></span> <span data-ttu-id="3f9b9-114">如果 `pbKeyBlob` 为 null，则假定指定的密钥容器 `wszKeyContainer` 包含密钥对。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-114">If `pbKeyBlob` is null, the key container specified by `wszKeyContainer` is assumed to contain the key pair.</span></span>  
  
 `cbKeyBlob`  
 <span data-ttu-id="3f9b9-115">中的大小（以字节为单位） `pbKeyBlob` 。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-115">[in] The size, in bytes, of `pbKeyBlob`.</span></span>  
  
 `ppbSignatureBlob`  
 <span data-ttu-id="3f9b9-116">弄指向公共语言运行时返回签名的位置的指针。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-116">[out] A pointer to the location to which the common language runtime returns the signature.</span></span> <span data-ttu-id="3f9b9-117">如果 `ppbSignatureBlob` 为 null，则运行时将签名存储在指定的文件中 `wszFilePath` 。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-117">If `ppbSignatureBlob` is null, the runtime stores the signature in the file specified by `wszFilePath`.</span></span>  
  
 <span data-ttu-id="3f9b9-118">如果 `ppbSignatureBlob` 不为 null，则公共语言运行时将分配要在其中返回签名的空间。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-118">If `ppbSignatureBlob` is not null, the common language runtime allocates space in which to return the signature.</span></span> <span data-ttu-id="3f9b9-119">调用方必须使用 [ICLRStrongName：： StrongNameFreeBuffer](iclrstrongname-strongnamefreebuffer-method.md) 方法释放此空间。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-119">The caller must free this space using the [ICLRStrongName::StrongNameFreeBuffer](iclrstrongname-strongnamefreebuffer-method.md) method.</span></span>  
  
 `pcbSignatureBlob`  
 <span data-ttu-id="3f9b9-120">弄返回签名的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-120">[out] The size, in bytes, of the returned signature.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="3f9b9-121">中以下一个或多个值：</span><span class="sxs-lookup"><span data-stu-id="3f9b9-121">[in] One or more of the following values:</span></span>  
  
- <span data-ttu-id="3f9b9-122">`SN_SIGN_ALL_FILES` (0x00000001) -重新计算链接模块的所有哈希。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-122">`SN_SIGN_ALL_FILES` (0x00000001) - Recompute all hashes for linked modules.</span></span>  
  
- <span data-ttu-id="3f9b9-123">`SN_TEST_SIGN` (0x00000002) -对程序集进行测试签名。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-123">`SN_TEST_SIGN` (0x00000002) - Test-sign the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3f9b9-124">返回值</span><span class="sxs-lookup"><span data-stu-id="3f9b9-124">Return Value</span></span>  

 <span data-ttu-id="3f9b9-125">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-125">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3f9b9-126">备注</span><span class="sxs-lookup"><span data-stu-id="3f9b9-126">Remarks</span></span>  

 <span data-ttu-id="3f9b9-127">指定 null 以 `wszFilePath` 计算签名大小，而不创建签名。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-127">Specify null for `wszFilePath` to calculate the size of the signature without creating the signature.</span></span>  
  
 <span data-ttu-id="3f9b9-128">签名可以直接存储在文件中，也可以返回给调用方。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-128">The signature can be either stored directly in the file, or returned to the caller.</span></span>  
  
 <span data-ttu-id="3f9b9-129">如果 `SN_SIGN_ALL_FILES` 指定了，但没有包含公钥，则 (`pbKeyBlob` 和 `wszFilePath` 均为 null) ，则会重新计算链接模块的哈希值，但不会对程序集进行重新签名。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-129">If `SN_SIGN_ALL_FILES` is specified but a public key is not included (both `pbKeyBlob` and `wszFilePath` are null), hashes for linked modules are recomputed, but the assembly is not re-signed.</span></span>  
  
 <span data-ttu-id="3f9b9-130">如果 `SN_TEST_SIGN` 指定了，则不会修改公共语言运行时标头以指示程序集使用强名称进行签名。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-130">If `SN_TEST_SIGN` is specified, the common language runtime header is not modified to indicate that the assembly is signed with a strong name.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3f9b9-131">要求</span><span class="sxs-lookup"><span data-stu-id="3f9b9-131">Requirements</span></span>  

 <span data-ttu-id="3f9b9-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3f9b9-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3f9b9-133">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="3f9b9-133">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="3f9b9-134">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3f9b9-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3f9b9-135">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3f9b9-135">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3f9b9-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="3f9b9-136">See also</span></span>

- [<span data-ttu-id="3f9b9-137">StrongNameSignatureGeneration 方法</span><span class="sxs-lookup"><span data-stu-id="3f9b9-137">StrongNameSignatureGeneration Method</span></span>](iclrstrongname-strongnamesignaturegeneration-method.md)
- [<span data-ttu-id="3f9b9-138">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="3f9b9-138">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
