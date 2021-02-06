---
description: 了解详细信息： StrongNameTokenFromPublicKey 函数
title: StrongNameTokenFromPublicKey 函数
ms.date: 03/30/2017
api_name:
- StrongNameTokenFromPublicKey
api_location:
- mscoree.dll
- mscorsn.dll
- clr.dll
- mscorwks.dll
- mscoreei.dll
api_type:
- COM
f1_keywords:
- StrongNameTokenFromPublicKey
helpviewer_keywords:
- StrongNameTokenFromPublicKey function [.NET Framework strong naming]
ms.assetid: 997e9e57-abb2-4217-bf20-1df621a75add
topic_type:
- apiref
ms.openlocfilehash: f978c9b2727db4b293b9c92a8789fbf9ba749d41
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99636254"
---
# <a name="strongnametokenfrompublickey-function"></a><span data-ttu-id="88c45-103">StrongNameTokenFromPublicKey 函数</span><span class="sxs-lookup"><span data-stu-id="88c45-103">StrongNameTokenFromPublicKey Function</span></span>

<span data-ttu-id="88c45-104">获取表示公钥的令牌。</span><span class="sxs-lookup"><span data-stu-id="88c45-104">Gets a token representing a public key.</span></span> <span data-ttu-id="88c45-105">强名称标记是公钥的缩写形式。</span><span class="sxs-lookup"><span data-stu-id="88c45-105">A strong name token is the shortened form of a public key.</span></span>  
  
 <span data-ttu-id="88c45-106">此函数已弃用。</span><span class="sxs-lookup"><span data-stu-id="88c45-106">This function has been deprecated.</span></span> <span data-ttu-id="88c45-107">改为使用 [ICLRStrongName：： StrongNameTokenFromPublicKey](../hosting/iclrstrongname-strongnametokenfrompublickey-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="88c45-107">Use the [ICLRStrongName::StrongNameTokenFromPublicKey](../hosting/iclrstrongname-strongnametokenfrompublickey-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="88c45-108">语法</span><span class="sxs-lookup"><span data-stu-id="88c45-108">Syntax</span></span>  
  
```cpp  
BOOLEAN StrongNameTokenFromPublicKey (
    [in]  BYTE    *pbPublicKeyBlob,  
    [in]  ULONG   cbPublicKeyBlob,  
    [out] BYTE    **ppbStrongNameToken,  
    [out] ULONG   *pcbStrongNameToken  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="88c45-109">参数</span><span class="sxs-lookup"><span data-stu-id="88c45-109">Parameters</span></span>  

 `pbPublicKeyBlob`  
 <span data-ttu-id="88c45-110">中 [PublicKeyBlob](publickeyblob-structure.md) 类型的结构，它包含用于生成强名称签名的密钥对的公共部分。</span><span class="sxs-lookup"><span data-stu-id="88c45-110">[in] A structure of type [PublicKeyBlob](publickeyblob-structure.md) that contains the public portion of the key pair used to generate the strong name signature.</span></span>  
  
 `cbPublicKeyBlob`  
 <span data-ttu-id="88c45-111">中的大小（以字节为单位） `pbPublicKeyBlob` 。</span><span class="sxs-lookup"><span data-stu-id="88c45-111">[in] The size, in bytes, of `pbPublicKeyBlob`.</span></span>  
  
 `ppbStrongNameToken`  
 <span data-ttu-id="88c45-112">弄与传入的密钥对应的强名称标记 `pbPublicKeyBlob` 。</span><span class="sxs-lookup"><span data-stu-id="88c45-112">[out] The strong name token corresponding to the key passed in `pbPublicKeyBlob`.</span></span> <span data-ttu-id="88c45-113">公共语言运行时分配要在其中返回标记的内存。</span><span class="sxs-lookup"><span data-stu-id="88c45-113">The common language runtime allocates the memory in which to return the token.</span></span> <span data-ttu-id="88c45-114">调用方必须通过使用 [StrongNameFreeBuffer](strongnamefreebuffer-function.md) 函数来释放此内存。</span><span class="sxs-lookup"><span data-stu-id="88c45-114">The caller must free this memory by using the [StrongNameFreeBuffer](strongnamefreebuffer-function.md) function.</span></span>  
  
 `pcbStrongNameToken`  
 <span data-ttu-id="88c45-115">弄返回的强名称标记的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="88c45-115">[out] The size, in bytes, of the returned strong name token.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="88c45-116">返回值</span><span class="sxs-lookup"><span data-stu-id="88c45-116">Return Value</span></span>  

 <span data-ttu-id="88c45-117">`true` 成功完成时;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="88c45-117">`true` on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="88c45-118">备注</span><span class="sxs-lookup"><span data-stu-id="88c45-118">Remarks</span></span>  

 <span data-ttu-id="88c45-119">强名称标记是在元数据中存储密钥信息时用于节省空间的公钥的缩写形式。</span><span class="sxs-lookup"><span data-stu-id="88c45-119">A strong name token is the shortened form of a public key used to save space when storing key information in metadata.</span></span> <span data-ttu-id="88c45-120">具体而言，强名称令牌在程序集引用中用于引用依赖程序集。</span><span class="sxs-lookup"><span data-stu-id="88c45-120">Specifically, strong name tokens are used in assembly references to refer to the dependent assembly.</span></span>  
  
 <span data-ttu-id="88c45-121">如果 `StrongNameTokenFromPublicKey` 函数未成功完成，请调用 [StrongNameErrorInfo](strongnameerrorinfo-function.md) 函数来检索上次生成的错误。</span><span class="sxs-lookup"><span data-stu-id="88c45-121">If the `StrongNameTokenFromPublicKey` function does not complete successfully, call the [StrongNameErrorInfo](strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="88c45-122">要求</span><span class="sxs-lookup"><span data-stu-id="88c45-122">Requirements</span></span>  

 <span data-ttu-id="88c45-123">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="88c45-123">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="88c45-124">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="88c45-124">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="88c45-125">**库：** 作为中的资源包含 mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="88c45-125">**Library:** Included as a resource in mscoree.dll</span></span>  
  
 <span data-ttu-id="88c45-126">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="88c45-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="88c45-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="88c45-127">See also</span></span>

- [<span data-ttu-id="88c45-128">StrongNameTokenFromPublicKey 方法</span><span class="sxs-lookup"><span data-stu-id="88c45-128">StrongNameTokenFromPublicKey Method</span></span>](../hosting/iclrstrongname-strongnametokenfrompublickey-method.md)
- [<span data-ttu-id="88c45-129">StrongNameGetPublicKey 方法</span><span class="sxs-lookup"><span data-stu-id="88c45-129">StrongNameGetPublicKey Method</span></span>](../hosting/iclrstrongname-strongnamegetpublickey-method.md)
- [<span data-ttu-id="88c45-130">PublicKeyBlob 结构</span><span class="sxs-lookup"><span data-stu-id="88c45-130">PublicKeyBlob Structure</span></span>](publickeyblob-structure.md)
