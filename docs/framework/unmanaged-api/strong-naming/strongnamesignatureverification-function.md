---
description: 了解详细信息： StrongNameSignatureVerification 函数
title: StrongNameSignatureVerification 函数
ms.date: 03/30/2017
api_name:
- StrongNameSignatureVerification
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameSignatureVerification
helpviewer_keywords:
- StrongNameSignatureVerification function [.NET Framework strong naming]
ms.assetid: 933758dd-231e-4382-8819-242c0a13a4b7
topic_type:
- apiref
ms.openlocfilehash: 74130cda96f38218d2fd296ff8804f86a9a18cd8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99636243"
---
# <a name="strongnamesignatureverification-function"></a><span data-ttu-id="2294a-103">StrongNameSignatureVerification 函数</span><span class="sxs-lookup"><span data-stu-id="2294a-103">StrongNameSignatureVerification Function</span></span>

<span data-ttu-id="2294a-104">获取一个值，该值指示提供的路径中的程序集清单是否包含根据指定标志验证的强名称签名。</span><span class="sxs-lookup"><span data-stu-id="2294a-104">Gets a value indicating whether the assembly manifest at the supplied path contains a strong name signature, which is verified according to the specified flags.</span></span>  
  
 <span data-ttu-id="2294a-105">此函数已弃用。</span><span class="sxs-lookup"><span data-stu-id="2294a-105">This function has been deprecated.</span></span> <span data-ttu-id="2294a-106">改为使用 [ICLRStrongName：： StrongNameSignatureVerification](../hosting/iclrstrongname-strongnamesignatureverification-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="2294a-106">Use the [ICLRStrongName::StrongNameSignatureVerification](../hosting/iclrstrongname-strongnamesignatureverification-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2294a-107">语法</span><span class="sxs-lookup"><span data-stu-id="2294a-107">Syntax</span></span>  
  
```cpp  
BOOLEAN StrongNameSignatureVerification (  
    [in]  LPCWSTR   wszFilePath,  
    [in]  DWORD     dwInFlags,  
    [out] DWORD     *pdwOutFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2294a-108">参数</span><span class="sxs-lookup"><span data-stu-id="2294a-108">Parameters</span></span>  

 `wszFilePath`  
 <span data-ttu-id="2294a-109">中要验证的程序集的可移植可执行文件 ( .dll 或 .exe) 文件的路径。</span><span class="sxs-lookup"><span data-stu-id="2294a-109">[in] The path to the portable executable (.dll or .exe) file for the assembly to verify.</span></span>  
  
 `dwInFlags`  
 <span data-ttu-id="2294a-110">中用于修改验证行为的标志。</span><span class="sxs-lookup"><span data-stu-id="2294a-110">[in] Flags to modify the verification behavior.</span></span> <span data-ttu-id="2294a-111">支持以下值：</span><span class="sxs-lookup"><span data-stu-id="2294a-111">The following values are supported:</span></span>  
  
- <span data-ttu-id="2294a-112">`SN_INFLAG_FORCE_VER` (0x00000001) -即使需要重写注册表设置，也强制进行验证。</span><span class="sxs-lookup"><span data-stu-id="2294a-112">`SN_INFLAG_FORCE_VER` (0x00000001) - Forces verification even if it is necessary to override registry settings.</span></span>  
  
- <span data-ttu-id="2294a-113">`SN_INFLAG_INSTALL` (0x00000002) -指定这是第一次验证清单。</span><span class="sxs-lookup"><span data-stu-id="2294a-113">`SN_INFLAG_INSTALL` (0x00000002) - Specifies that this is the first time the manifest is verified.</span></span>  
  
- <span data-ttu-id="2294a-114">`SN_INFLAG_ADMIN_ACCESS` (0x00000004) -指定缓存只允许具有管理权限的用户访问。</span><span class="sxs-lookup"><span data-stu-id="2294a-114">`SN_INFLAG_ADMIN_ACCESS` (0x00000004) - Specifies that the cache will allow access only to users who have administrative privileges.</span></span>  
  
- <span data-ttu-id="2294a-115">`SN_INFLAG_USER_ACCESS` (0x00000008) -指定只能向当前用户访问程序集。</span><span class="sxs-lookup"><span data-stu-id="2294a-115">`SN_INFLAG_USER_ACCESS` (0x00000008) - Specifies that the assembly will be accessible only to the current user.</span></span>  
  
- <span data-ttu-id="2294a-116">`SN_INFLAG_ALL_ACCESS` (0x00000010) -指定缓存将不提供访问限制。</span><span class="sxs-lookup"><span data-stu-id="2294a-116">`SN_INFLAG_ALL_ACCESS` (0x00000010) - Specifies that the cache will provide no guarantees of access restriction.</span></span>  
  
- <span data-ttu-id="2294a-117">`SN_INFLAG_RUNTIME` (0x80000000) 为内部调试保留。</span><span class="sxs-lookup"><span data-stu-id="2294a-117">`SN_INFLAG_RUNTIME` (0x80000000) - Reserved for internal debugging.</span></span>  
  
 `pdwOutFlags`  
 <span data-ttu-id="2294a-118">弄指示强名称签名是否已验证的标志。</span><span class="sxs-lookup"><span data-stu-id="2294a-118">[out] Flags indicating whether the strong name signature was verified.</span></span> <span data-ttu-id="2294a-119">支持以下值：</span><span class="sxs-lookup"><span data-stu-id="2294a-119">The following value is supported:</span></span>  
  
- <span data-ttu-id="2294a-120">`SN_OUTFLAG_WAS_VERIFIED` (0x00000001) -将此值设置为， `false` 以指定验证是否由于注册表设置而成功。</span><span class="sxs-lookup"><span data-stu-id="2294a-120">`SN_OUTFLAG_WAS_VERIFIED` (0x00000001) - This value is set to `false` to specify that the verification succeeded due to registry settings.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2294a-121">返回值</span><span class="sxs-lookup"><span data-stu-id="2294a-121">Return Value</span></span>  

 <span data-ttu-id="2294a-122">`true` 如果验证成功，则为;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="2294a-122">`true` if the verification was successful; otherwise, `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2294a-123">要求</span><span class="sxs-lookup"><span data-stu-id="2294a-123">Requirements</span></span>  

 <span data-ttu-id="2294a-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2294a-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2294a-125">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="2294a-125">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="2294a-126">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2294a-126">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="2294a-127">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2294a-127">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2294a-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="2294a-128">See also</span></span>

- [<span data-ttu-id="2294a-129">StrongNameSignatureVerification 方法</span><span class="sxs-lookup"><span data-stu-id="2294a-129">StrongNameSignatureVerification Method</span></span>](../hosting/iclrstrongname-strongnamesignatureverification-method.md)
- [<span data-ttu-id="2294a-130">StrongNameSignatureVerificationEx 方法</span><span class="sxs-lookup"><span data-stu-id="2294a-130">StrongNameSignatureVerificationEx Method</span></span>](../hosting/iclrstrongname-strongnamesignatureverificationex-method.md)
- [<span data-ttu-id="2294a-131">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="2294a-131">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
