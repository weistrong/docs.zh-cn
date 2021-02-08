---
description: 了解详细信息： StrongNameSignatureGenerationEx 函数
title: StrongNameSignatureGenerationEx 函数
ms.date: 03/30/2017
api_name:
- StrongNameSignatureGenerationEx
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameSignatureGenerationEx
helpviewer_keywords:
- StrongNameSignatureGenerationEx function [.NET Framework strong naming]
ms.assetid: 9a75469e-aa49-4e32-ad48-3bafd5202f09
topic_type:
- apiref
ms.openlocfilehash: e4d35cf51df6047d3a89d4146ceb8bf62e3f1b8b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99798870"
---
# <a name="strongnamesignaturegenerationex-function"></a><span data-ttu-id="96ad6-103">StrongNameSignatureGenerationEx 函数</span><span class="sxs-lookup"><span data-stu-id="96ad6-103">StrongNameSignatureGenerationEx Function</span></span>

<span data-ttu-id="96ad6-104">根据指定的标志，为指定的程序集生成强名称签名。</span><span class="sxs-lookup"><span data-stu-id="96ad6-104">Generates a strong name signature for the specified assembly, according to the specified flags.</span></span>  
  
 <span data-ttu-id="96ad6-105">此函数已弃用。</span><span class="sxs-lookup"><span data-stu-id="96ad6-105">This function has been deprecated.</span></span> <span data-ttu-id="96ad6-106">改为使用 [ICLRStrongName：： StrongNameSignatureGenerationEx](../hosting/iclrstrongname-strongnamesignaturegenerationex-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="96ad6-106">Use the [ICLRStrongName::StrongNameSignatureGenerationEx](../hosting/iclrstrongname-strongnamesignaturegenerationex-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="96ad6-107">语法</span><span class="sxs-lookup"><span data-stu-id="96ad6-107">Syntax</span></span>  
  
```cpp  
BOOLEAN StrongNameSignatureGenerationEx (  
    [in]  LPCWSTR   wszFilePath,  
    [in]  LPCWSTR   wszKeyContainer,  
    [in]  BYTE      *pbKeyBlob,  
    [in]  ULONG     cbKeyBlob,  
    [out] BYTE      **ppbSignatureBlob,  
    [out] ULONG     *pcbSignatureBlob,  
    [in]  DWORD     dwFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="96ad6-108">参数</span><span class="sxs-lookup"><span data-stu-id="96ad6-108">Parameters</span></span>  

 `wszFilePath`  
 <span data-ttu-id="96ad6-109">中包含要为其生成强名称签名的程序集清单的文件的路径。</span><span class="sxs-lookup"><span data-stu-id="96ad6-109">[in] The path to the file that contains the manifest of the assembly for which the strong name signature will be generated.</span></span>  
  
 `wszKeyContainer`  
 <span data-ttu-id="96ad6-110">中包含公钥/私钥对的密钥容器的名称。</span><span class="sxs-lookup"><span data-stu-id="96ad6-110">[in] The name of the key container that contains the public/private key pair.</span></span>  
  
 <span data-ttu-id="96ad6-111">如果 `pbKeyBlob` 为 null，则 `wszKeyContainer` 必须在加密服务提供程序 (CSP) 中指定有效容器。</span><span class="sxs-lookup"><span data-stu-id="96ad6-111">If `pbKeyBlob` is null, `wszKeyContainer` must specify a valid container within the cryptographic service provider (CSP).</span></span> <span data-ttu-id="96ad6-112">在这种情况下，存储在容器中的密钥对用于对文件进行签名。</span><span class="sxs-lookup"><span data-stu-id="96ad6-112">In this case, the key pair stored in the container is used to sign the file.</span></span>  
  
 <span data-ttu-id="96ad6-113">如果不为 `pbKeyBlob` null，则假定密钥对包含在关键的二进制大型对象 (BLOB) 中。</span><span class="sxs-lookup"><span data-stu-id="96ad6-113">If `pbKeyBlob` is not null, the key pair is assumed to be contained in the key binary large object (BLOB).</span></span>  
  
 `pbKeyBlob`  
 <span data-ttu-id="96ad6-114">中指向公钥/私钥对的指针。</span><span class="sxs-lookup"><span data-stu-id="96ad6-114">[in] A pointer to the public/private key pair.</span></span> <span data-ttu-id="96ad6-115">此对采用 Win32 函数创建的格式 `CryptExportKey` 。</span><span class="sxs-lookup"><span data-stu-id="96ad6-115">This pair is in the format created by the Win32 `CryptExportKey` function.</span></span> <span data-ttu-id="96ad6-116">如果 `pbKeyBlob` 为 null，则假定指定的密钥容器 `wszKeyContainer` 包含密钥对。</span><span class="sxs-lookup"><span data-stu-id="96ad6-116">If `pbKeyBlob` is null, the key container specified by `wszKeyContainer` is assumed to contain the key pair.</span></span>  
  
 `cbKeyBlob`  
 <span data-ttu-id="96ad6-117">中的大小（以字节为单位） `pbKeyBlob` 。</span><span class="sxs-lookup"><span data-stu-id="96ad6-117">[in] The size, in bytes, of `pbKeyBlob`.</span></span>  
  
 `ppbSignatureBlob`  
 <span data-ttu-id="96ad6-118">弄指向公共语言运行时返回签名的位置的指针。</span><span class="sxs-lookup"><span data-stu-id="96ad6-118">[out] A pointer to the location to which the common language runtime returns the signature.</span></span> <span data-ttu-id="96ad6-119">如果 `ppbSignatureBlob` 为 null，则运行时将签名存储在指定的文件中 `wszFilePath` 。</span><span class="sxs-lookup"><span data-stu-id="96ad6-119">If `ppbSignatureBlob` is null, the runtime stores the signature in the file specified by `wszFilePath`.</span></span>  
  
 <span data-ttu-id="96ad6-120">如果 `ppbSignatureBlob` 不为 null，则公共语言运行时将分配要在其中返回签名的空间。</span><span class="sxs-lookup"><span data-stu-id="96ad6-120">If `ppbSignatureBlob` is not null, the common language runtime allocates space in which to return the signature.</span></span> <span data-ttu-id="96ad6-121">调用方必须使用 [StrongNameFreeBuffer](strongnamefreebuffer-function.md) 函数释放此空间。</span><span class="sxs-lookup"><span data-stu-id="96ad6-121">The caller must free this space using the [StrongNameFreeBuffer](strongnamefreebuffer-function.md) function.</span></span>  
  
 `pcbSignatureBlob`  
 <span data-ttu-id="96ad6-122">弄返回签名的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="96ad6-122">[out] The size, in bytes, of the returned signature.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="96ad6-123">中以下一个或多个值：</span><span class="sxs-lookup"><span data-stu-id="96ad6-123">[in] One or more of the following values:</span></span>  
  
- <span data-ttu-id="96ad6-124">`SN_SIGN_ALL_FILES` (0x00000001) -重新计算链接模块的所有哈希。</span><span class="sxs-lookup"><span data-stu-id="96ad6-124">`SN_SIGN_ALL_FILES` (0x00000001) - Recompute all hashes for linked modules.</span></span>  
  
- <span data-ttu-id="96ad6-125">`SN_TEST_SIGN` (0x00000002) -对程序集进行测试签名。</span><span class="sxs-lookup"><span data-stu-id="96ad6-125">`SN_TEST_SIGN` (0x00000002) - Test-sign the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="96ad6-126">返回值</span><span class="sxs-lookup"><span data-stu-id="96ad6-126">Return Value</span></span>  

 <span data-ttu-id="96ad6-127">`true` 成功完成时;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="96ad6-127">`true` on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="96ad6-128">备注</span><span class="sxs-lookup"><span data-stu-id="96ad6-128">Remarks</span></span>  

 <span data-ttu-id="96ad6-129">指定 null 以 `wszFilePath` 计算签名大小，而不创建签名。</span><span class="sxs-lookup"><span data-stu-id="96ad6-129">Specify null for `wszFilePath` to calculate the size of the signature without creating the signature.</span></span>  
  
 <span data-ttu-id="96ad6-130">签名可以直接存储在文件中，也可以返回给调用方。</span><span class="sxs-lookup"><span data-stu-id="96ad6-130">The signature can be either stored directly in the file, or returned to the caller.</span></span>  
  
 <span data-ttu-id="96ad6-131">如果 `SN_SIGN_ALL_FILES` 指定了，但没有包含公钥，则 (`pbKeyBlob` 和 `wszFilePath` 均为 null) ，则会重新计算链接模块的哈希值，但不会对程序集进行重新签名。</span><span class="sxs-lookup"><span data-stu-id="96ad6-131">If `SN_SIGN_ALL_FILES` is specified but a public key is not included (both `pbKeyBlob` and `wszFilePath` are null), hashes for linked modules are recomputed, but the assembly is not re-signed.</span></span>  
  
 <span data-ttu-id="96ad6-132">如果 `SN_TEST_SIGN` 指定了，则不会修改公共语言运行时标头以指示程序集使用强名称进行签名。</span><span class="sxs-lookup"><span data-stu-id="96ad6-132">If `SN_TEST_SIGN` is specified, the common language runtime header is not modified to indicate that the assembly is signed with a strong name.</span></span>  
  
 <span data-ttu-id="96ad6-133">如果 `StrongNameSignatureGenerationEx` 函数未成功完成，请调用 [StrongNameErrorInfo](strongnameerrorinfo-function.md) 函数来检索上次生成的错误。</span><span class="sxs-lookup"><span data-stu-id="96ad6-133">If the `StrongNameSignatureGenerationEx` function does not complete successfully, call the [StrongNameErrorInfo](strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="96ad6-134">要求</span><span class="sxs-lookup"><span data-stu-id="96ad6-134">Requirements</span></span>  

 <span data-ttu-id="96ad6-135">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="96ad6-135">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="96ad6-136">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="96ad6-136">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="96ad6-137">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="96ad6-137">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="96ad6-138">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="96ad6-138">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="96ad6-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="96ad6-139">See also</span></span>

- [<span data-ttu-id="96ad6-140">StrongNameSignatureGenerationEx 方法</span><span class="sxs-lookup"><span data-stu-id="96ad6-140">StrongNameSignatureGenerationEx Method</span></span>](../hosting/iclrstrongname-strongnamesignaturegenerationex-method.md)
- [<span data-ttu-id="96ad6-141">StrongNameSignatureGeneration 方法</span><span class="sxs-lookup"><span data-stu-id="96ad6-141">StrongNameSignatureGeneration Method</span></span>](../hosting/iclrstrongname-strongnamesignaturegeneration-method.md)
- [<span data-ttu-id="96ad6-142">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="96ad6-142">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
