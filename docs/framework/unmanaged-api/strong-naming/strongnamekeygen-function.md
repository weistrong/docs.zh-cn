---
description: 了解详细信息： StrongNameKeyGen 函数
title: StrongNameKeyGen 函数
ms.date: 03/30/2017
api_name:
- StrongNameKeyGen
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameKeyGen
helpviewer_keywords:
- StrongNameKeyGen function [.NET Framework strong naming]
ms.assetid: 883e413a-ad2f-4f7f-b1b9-aeb8fe5b65f8
topic_type:
- apiref
ms.openlocfilehash: c5f4cfcfa9030ae856acf5fd59ab34a2b8338670
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99636244"
---
# <a name="strongnamekeygen-function"></a><span data-ttu-id="bb72c-103">StrongNameKeyGen 函数</span><span class="sxs-lookup"><span data-stu-id="bb72c-103">StrongNameKeyGen Function</span></span>

<span data-ttu-id="bb72c-104">创建新的公钥/私钥对，以便强名称使用。</span><span class="sxs-lookup"><span data-stu-id="bb72c-104">Creates a new public/private key pair for strong name use.</span></span>  
  
 <span data-ttu-id="bb72c-105">此函数已弃用。</span><span class="sxs-lookup"><span data-stu-id="bb72c-105">This function has been deprecated.</span></span> <span data-ttu-id="bb72c-106">改为使用 [ICLRStrongName：： StrongNameKeyGen](../hosting/iclrstrongname-strongnamekeygen-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="bb72c-106">Use the [ICLRStrongName::StrongNameKeyGen](../hosting/iclrstrongname-strongnamekeygen-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bb72c-107">语法</span><span class="sxs-lookup"><span data-stu-id="bb72c-107">Syntax</span></span>  
  
```cpp  
BOOLEAN StrongNameKeyGen (  
    [in]  LPCWSTR   wszKeyContainer,  
    [in]  DWORD     dwFlags,  
    [out] BYTE      **ppbKeyBlob,  
    [out] ULONG     *pcbKeyBlob  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="bb72c-108">参数</span><span class="sxs-lookup"><span data-stu-id="bb72c-108">Parameters</span></span>  

 `wszKeyContainer`  
 <span data-ttu-id="bb72c-109">中请求的密钥容器名称。</span><span class="sxs-lookup"><span data-stu-id="bb72c-109">[in] The requested key container name.</span></span> <span data-ttu-id="bb72c-110">`wszKeyContainer` 必须为非空字符串，或者为 null 以生成临时名称。</span><span class="sxs-lookup"><span data-stu-id="bb72c-110">`wszKeyContainer` must be a non-empty string, or null to generate a temporary name.</span></span>  
  
 `dwFlags`  
 <span data-ttu-id="bb72c-111">中指定是否保留注册的密钥。</span><span class="sxs-lookup"><span data-stu-id="bb72c-111">[in] Specifies whether to leave the key registered.</span></span> <span data-ttu-id="bb72c-112">支持以下值：</span><span class="sxs-lookup"><span data-stu-id="bb72c-112">The following values are supported:</span></span>  
  
- <span data-ttu-id="bb72c-113">0x00000000-在 `wszKeyContainer` 为 null 时用于生成临时密钥容器名称。</span><span class="sxs-lookup"><span data-stu-id="bb72c-113">0x00000000 - Used when `wszKeyContainer` is null to generate a temporary key container name.</span></span>  
  
- <span data-ttu-id="bb72c-114">0x00000001 (`SN_LEAVE_KEY`) -指定应保持注册该密钥。</span><span class="sxs-lookup"><span data-stu-id="bb72c-114">0x00000001 (`SN_LEAVE_KEY`) - Specifies that the key should be left registered.</span></span>  
  
 `ppbKeyBlob`  
 <span data-ttu-id="bb72c-115">弄返回的公钥/私钥对。</span><span class="sxs-lookup"><span data-stu-id="bb72c-115">[out] The returned public/private key pair.</span></span>  
  
 `pcbKeyBlob`  
 <span data-ttu-id="bb72c-116">弄的大小（以字节为单位） `ppbKeyBlob` 。</span><span class="sxs-lookup"><span data-stu-id="bb72c-116">[out] The size, in bytes, of `ppbKeyBlob`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="bb72c-117">返回值</span><span class="sxs-lookup"><span data-stu-id="bb72c-117">Return Value</span></span>  

 <span data-ttu-id="bb72c-118">`true` 成功完成时;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="bb72c-118">`true` on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="bb72c-119">备注</span><span class="sxs-lookup"><span data-stu-id="bb72c-119">Remarks</span></span>  

 <span data-ttu-id="bb72c-120">`StrongNameKeyGen`函数创建1024位键。</span><span class="sxs-lookup"><span data-stu-id="bb72c-120">The `StrongNameKeyGen` function creates a 1024-bit key.</span></span> <span data-ttu-id="bb72c-121">检索到密钥后，应调用 [StrongNameFreeBuffer](strongnamefreebuffer-function.md) 函数以释放已分配的内存。</span><span class="sxs-lookup"><span data-stu-id="bb72c-121">After the key is retrieved, you should call the [StrongNameFreeBuffer](strongnamefreebuffer-function.md) function to release the allocated memory.</span></span>  
  
 <span data-ttu-id="bb72c-122">如果 `StrongNameKeyGen` 函数未成功完成，请调用 [StrongNameErrorInfo](strongnameerrorinfo-function.md) 函数来检索上次生成的错误。</span><span class="sxs-lookup"><span data-stu-id="bb72c-122">If the `StrongNameKeyGen` function does not complete successfully, call the [StrongNameErrorInfo](strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bb72c-123">要求</span><span class="sxs-lookup"><span data-stu-id="bb72c-123">Requirements</span></span>  

 <span data-ttu-id="bb72c-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bb72c-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bb72c-125">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="bb72c-125">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="bb72c-126">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bb72c-126">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="bb72c-127">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bb72c-127">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bb72c-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="bb72c-128">See also</span></span>

- [<span data-ttu-id="bb72c-129">StrongNameKeyGen 方法</span><span class="sxs-lookup"><span data-stu-id="bb72c-129">StrongNameKeyGen Method</span></span>](../hosting/iclrstrongname-strongnamekeygen-method.md)
- [<span data-ttu-id="bb72c-130">StrongNameKeyGenEx 方法</span><span class="sxs-lookup"><span data-stu-id="bb72c-130">StrongNameKeyGenEx Method</span></span>](../hosting/iclrstrongname-strongnamekeygenex-method.md)
- [<span data-ttu-id="bb72c-131">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="bb72c-131">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
