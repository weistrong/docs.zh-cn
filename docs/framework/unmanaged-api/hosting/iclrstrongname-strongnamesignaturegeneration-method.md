---
description: 了解详细信息： ICLRStrongName：： StrongNameSignatureGeneration 方法
title: ICLRStrongName::StrongNameSignatureGeneration 方法
ms.date: 03/30/2017
api_name:
- ICLRStrongName.StrongNameSignatureGeneration
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameSignatureGeneration
helpviewer_keywords:
- StrongNameSignatureGeneration method, ICLRStrongName interface [.NET Framework hosting]
- ICLRStrongName::StrongNameSignatureGeneration method [.NET Framework hosting]
ms.assetid: 4cdb1284-947a-4ed4-94c1-c5ff5cdfce56
topic_type:
- apiref
ms.openlocfilehash: ea8a6a9ea1e85af9d4e78cc950a02dbbc6815e4c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781878"
---
# <a name="iclrstrongnamestrongnamesignaturegeneration-method"></a><span data-ttu-id="a7e45-103">ICLRStrongName::StrongNameSignatureGeneration 方法</span><span class="sxs-lookup"><span data-stu-id="a7e45-103">ICLRStrongName::StrongNameSignatureGeneration Method</span></span>

<span data-ttu-id="a7e45-104">为指定的程序集生成强名称签名。</span><span class="sxs-lookup"><span data-stu-id="a7e45-104">Generates a strong name signature for the specified assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a7e45-105">语法</span><span class="sxs-lookup"><span data-stu-id="a7e45-105">Syntax</span></span>  
  
```cpp  
HRESULT StrongNameSignatureGeneration (
    [in]  LPCWSTR   wszFilePath,  
    [in]  LPCWSTR   wszKeyContainer,  
    [in]  BYTE      *pbKeyBlob,  
    [in]  ULONG     cbKeyBlob,  
    [out] BYTE      **ppbSignatureBlob,  
    [out] ULONG     *pcbSignatureBlob  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a7e45-106">参数</span><span class="sxs-lookup"><span data-stu-id="a7e45-106">Parameters</span></span>  

 `wszFilePath`  
 <span data-ttu-id="a7e45-107">中包含要为其生成强名称签名的程序集清单的文件的路径。</span><span class="sxs-lookup"><span data-stu-id="a7e45-107">[in] The path to the file that contains the manifest of the assembly for which the strong name signature will be generated.</span></span>  
  
 `wszKeyContainer`  
 <span data-ttu-id="a7e45-108">中包含公钥/私钥对的密钥容器的名称。</span><span class="sxs-lookup"><span data-stu-id="a7e45-108">[in] The name of the key container that contains the public/private key pair.</span></span>  
  
 <span data-ttu-id="a7e45-109">如果 `pbKeyBlob` 为 null，则 `wszKeyContainer` 必须在加密服务提供程序 (CSP) 中指定有效容器。</span><span class="sxs-lookup"><span data-stu-id="a7e45-109">If `pbKeyBlob` is null, `wszKeyContainer` must specify a valid container within the cryptographic service provider (CSP).</span></span> <span data-ttu-id="a7e45-110">在这种情况下，存储在容器中的密钥对用于对文件进行签名。</span><span class="sxs-lookup"><span data-stu-id="a7e45-110">In this case, the key pair stored in the container is used to sign the file.</span></span>  
  
 <span data-ttu-id="a7e45-111">如果不为 `pbKeyBlob` null，则假定密钥对包含在关键的二进制大型对象 (BLOB) 中。</span><span class="sxs-lookup"><span data-stu-id="a7e45-111">If `pbKeyBlob` is not null, the key pair is assumed to be contained in the key binary large object (BLOB).</span></span>  
  
 <span data-ttu-id="a7e45-112">密钥必须是1024位 Rivest-Rivest-shamir-adleman (RSA) 签名密钥。</span><span class="sxs-lookup"><span data-stu-id="a7e45-112">The keys must be 1024-bit Rivest-Shamir-Adleman (RSA) signing keys.</span></span> <span data-ttu-id="a7e45-113">此时不支持其他类型的密钥。</span><span class="sxs-lookup"><span data-stu-id="a7e45-113">No other types of keys are supported at this time.</span></span>  
  
 `pbKeyBlob`  
 <span data-ttu-id="a7e45-114">中指向公钥/私钥对的指针。</span><span class="sxs-lookup"><span data-stu-id="a7e45-114">[in] A pointer to the public/private key pair.</span></span> <span data-ttu-id="a7e45-115">此对采用 Win32 函数创建的格式 `CryptExportKey` 。</span><span class="sxs-lookup"><span data-stu-id="a7e45-115">This pair is in the format created by the Win32 `CryptExportKey` function.</span></span> <span data-ttu-id="a7e45-116">如果 `pbKeyBlob` 为 null，则假定指定的密钥容器 `wszKeyContainer` 包含密钥对。</span><span class="sxs-lookup"><span data-stu-id="a7e45-116">If `pbKeyBlob` is null, the key container specified by `wszKeyContainer` is assumed to contain the key pair.</span></span>  
  
 `cbKeyBlob`  
 <span data-ttu-id="a7e45-117">中的大小（以字节为单位） `pbKeyBlob` 。</span><span class="sxs-lookup"><span data-stu-id="a7e45-117">[in] The size, in bytes, of `pbKeyBlob`.</span></span>  
  
 `ppbSignatureBlob`  
 <span data-ttu-id="a7e45-118">弄指向公共语言运行时返回签名的位置的指针。</span><span class="sxs-lookup"><span data-stu-id="a7e45-118">[out] A pointer to the location to which the common language runtime returns the signature.</span></span> <span data-ttu-id="a7e45-119">如果 `ppbSignatureBlob` 为 null，则运行时将签名存储在指定的文件中 `wszFilePath` 。</span><span class="sxs-lookup"><span data-stu-id="a7e45-119">If `ppbSignatureBlob` is null, the runtime stores the signature in the file specified by `wszFilePath`.</span></span>  
  
 <span data-ttu-id="a7e45-120">如果 `ppbSignatureBlob` 不为 null，则公共语言运行时将分配要在其中返回签名的空间。</span><span class="sxs-lookup"><span data-stu-id="a7e45-120">If `ppbSignatureBlob` is not null, the common language runtime allocates space in which to return the signature.</span></span> <span data-ttu-id="a7e45-121">调用方必须通过使用 [ICLRStrongName：： StrongNameFreeBuffer](iclrstrongname-strongnamefreebuffer-method.md) 方法释放此空间。</span><span class="sxs-lookup"><span data-stu-id="a7e45-121">The caller must free this space by using the [ICLRStrongName::StrongNameFreeBuffer](iclrstrongname-strongnamefreebuffer-method.md) method.</span></span>  
  
 `pcbSignatureBlob`  
 <span data-ttu-id="a7e45-122">弄返回签名的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="a7e45-122">[out] The size, in bytes, of the returned signature.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a7e45-123">返回值</span><span class="sxs-lookup"><span data-stu-id="a7e45-123">Return Value</span></span>  

 <span data-ttu-id="a7e45-124">`S_OK` 如果该方法已成功完成，则为;否则，表示失败的 HRESULT 值 (参阅) 列表的 [常见 HRESULT 值](/windows/win32/seccrypto/common-hresult-values) 。</span><span class="sxs-lookup"><span data-stu-id="a7e45-124">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](/windows/win32/seccrypto/common-hresult-values) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a7e45-125">备注</span><span class="sxs-lookup"><span data-stu-id="a7e45-125">Remarks</span></span>  

 <span data-ttu-id="a7e45-126">指定 null 以 `wszFilePath` 计算签名大小，而不创建签名。</span><span class="sxs-lookup"><span data-stu-id="a7e45-126">Specify null for `wszFilePath` to calculate the size of the signature without creating the signature.</span></span>  
  
 <span data-ttu-id="a7e45-127">签名可以直接存储在文件中，也可以返回给调用方。</span><span class="sxs-lookup"><span data-stu-id="a7e45-127">The signature can be stored either directly in the file, or returned to the caller.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a7e45-128">要求</span><span class="sxs-lookup"><span data-stu-id="a7e45-128">Requirements</span></span>  

 <span data-ttu-id="a7e45-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a7e45-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a7e45-130">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="a7e45-130">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="a7e45-131">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="a7e45-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="a7e45-132">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a7e45-132">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a7e45-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="a7e45-133">See also</span></span>

- [<span data-ttu-id="a7e45-134">StrongNameSignatureGenerationEx 方法</span><span class="sxs-lookup"><span data-stu-id="a7e45-134">StrongNameSignatureGenerationEx Method</span></span>](iclrstrongname-strongnamesignaturegenerationex-method.md)
- [<span data-ttu-id="a7e45-135">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="a7e45-135">ICLRStrongName Interface</span></span>](iclrstrongname-interface.md)
