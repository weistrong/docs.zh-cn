---
description: 了解详细信息： StrongNameSignatureVerificationEx 函数
title: StrongNameSignatureVerificationEx 函数
ms.date: 03/30/2017
api_name:
- StrongNameSignatureVerificationEx
api_location:
- mscoree.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameSignatureVerificationEx
helpviewer_keywords:
- StrongNameSignatureVerificationEx function [.NET Framework strong naming]
ms.assetid: cfe4b634-18bf-44b8-9773-d94fb7e8a480
topic_type:
- apiref
ms.openlocfilehash: 9e20044e9c3caef8c2276ac5f390269ee978d55b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794515"
---
# <a name="strongnamesignatureverificationex-function"></a><span data-ttu-id="5ee0e-103">StrongNameSignatureVerificationEx 函数</span><span class="sxs-lookup"><span data-stu-id="5ee0e-103">StrongNameSignatureVerificationEx Function</span></span>

<span data-ttu-id="5ee0e-104">获取一个值，该值指示提供的路径中的程序集清单是否包含强名称签名。</span><span class="sxs-lookup"><span data-stu-id="5ee0e-104">Gets a value indicating whether the assembly manifest at the supplied path contains a strong name signature.</span></span>  
  
 <span data-ttu-id="5ee0e-105">此函数已弃用。</span><span class="sxs-lookup"><span data-stu-id="5ee0e-105">This function has been deprecated.</span></span> <span data-ttu-id="5ee0e-106">改为使用 [ICLRStrongName：： StrongNameSignatureVerificationEx](../hosting/iclrstrongname-strongnamesignatureverificationex-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="5ee0e-106">Use the [ICLRStrongName::StrongNameSignatureVerificationEx](../hosting/iclrstrongname-strongnamesignatureverificationex-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5ee0e-107">语法</span><span class="sxs-lookup"><span data-stu-id="5ee0e-107">Syntax</span></span>  
  
```cpp  
BOOLEAN StrongNameSignatureVerificationEx (  
    [in]  LPCWSTR   wszFilePath,  
    [in]  BOOLEAN   fForceVerification,  
    [out] BOOLEAN   *pfWasVerified  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="5ee0e-108">参数</span><span class="sxs-lookup"><span data-stu-id="5ee0e-108">Parameters</span></span>  

 `wszFilePath`  
 <span data-ttu-id="5ee0e-109">中要验证的程序集的可移植可执行文件的路径 ( .exe 或 .dll) 文件。</span><span class="sxs-lookup"><span data-stu-id="5ee0e-109">[in] The path to the portable executable (.exe or .dll) file for the assembly to be verified.</span></span>  
  
 `fForceVerification`  
 <span data-ttu-id="5ee0e-110">[in] `true` 若要执行验证，即使需要重写注册表设置，否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="5ee0e-110">[in] `true` to perform verification, even if it is necessary to override registry settings; otherwise, `false`.</span></span>  
  
 `pfWasVerified`  
 <span data-ttu-id="5ee0e-111">[out] `true` 如果验证了强名称签名，则为;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="5ee0e-111">[out] `true` if the strong name signature was verified; otherwise, `false`.</span></span> <span data-ttu-id="5ee0e-112">`pfWasVerified``false`如果验证因为注册表设置而成功，则也会设置为。</span><span class="sxs-lookup"><span data-stu-id="5ee0e-112">`pfWasVerified` is also set to `false` if the verification was successful due to registry settings.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="5ee0e-113">返回值</span><span class="sxs-lookup"><span data-stu-id="5ee0e-113">Return Value</span></span>  

 <span data-ttu-id="5ee0e-114">`true` 如果验证成功，则为;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="5ee0e-114">`true` if the verification was successful; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="5ee0e-115">备注</span><span class="sxs-lookup"><span data-stu-id="5ee0e-115">Remarks</span></span>  

 <span data-ttu-id="5ee0e-116">`StrongNameSignatureVerificationEx` 提供与 [StrongNameSignatureVerification](strongnamesignatureverification-function.md) 函数相似的功能。</span><span class="sxs-lookup"><span data-stu-id="5ee0e-116">`StrongNameSignatureVerificationEx` provides a capability similar to the [StrongNameSignatureVerification](strongnamesignatureverification-function.md) function.</span></span> <span data-ttu-id="5ee0e-117">但是，的第二个输入参数和输出参数 `StrongNameSignatureVerificationEx` 的类型为， `BOOLEAN` 而不是 `DWORD` 。</span><span class="sxs-lookup"><span data-stu-id="5ee0e-117">However, the second input parameter and the output parameter for `StrongNameSignatureVerificationEx` are of type `BOOLEAN` instead of `DWORD`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="5ee0e-118">要求</span><span class="sxs-lookup"><span data-stu-id="5ee0e-118">Requirements</span></span>  

 <span data-ttu-id="5ee0e-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5ee0e-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5ee0e-120">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="5ee0e-120">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="5ee0e-121">**库：** 作为中的资源包含 mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="5ee0e-121">**Library:** Included as a resource in mscoree.dll</span></span>  
  
 <span data-ttu-id="5ee0e-122">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5ee0e-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5ee0e-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="5ee0e-123">See also</span></span>

- [<span data-ttu-id="5ee0e-124">StrongNameSignatureVerificationEx 方法</span><span class="sxs-lookup"><span data-stu-id="5ee0e-124">StrongNameSignatureVerificationEx Method</span></span>](../hosting/iclrstrongname-strongnamesignatureverificationex-method.md)
- [<span data-ttu-id="5ee0e-125">StrongNameSignatureVerification 方法</span><span class="sxs-lookup"><span data-stu-id="5ee0e-125">StrongNameSignatureVerification Method</span></span>](../hosting/iclrstrongname-strongnamesignatureverification-method.md)
- [<span data-ttu-id="5ee0e-126">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="5ee0e-126">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
