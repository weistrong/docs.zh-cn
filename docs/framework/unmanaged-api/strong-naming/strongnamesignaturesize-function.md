---
description: 了解详细信息： StrongNameSignatureSize 函数
title: StrongNameSignatureSize 函数
ms.date: 03/30/2017
api_name:
- StrongNameSignatureSize
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameSignatureSize
helpviewer_keywords:
- StrongNameSignatureSize function [.NET Framework strong naming]
ms.assetid: 4fde4cd0-f53e-4411-a2fe-fc5c54472f95
topic_type:
- apiref
ms.openlocfilehash: b3f22a6a4d5455af4dd17cb75edfd18befed7de3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99670510"
---
# <a name="strongnamesignaturesize-function"></a><span data-ttu-id="6cb63-103">StrongNameSignatureSize 函数</span><span class="sxs-lookup"><span data-stu-id="6cb63-103">StrongNameSignatureSize Function</span></span>

<span data-ttu-id="6cb63-104">返回强名称签名的大小。</span><span class="sxs-lookup"><span data-stu-id="6cb63-104">Returns the size of the strong name signature.</span></span> <span data-ttu-id="6cb63-105">`StrongNameSignatureSize` 通常由编译器用来确定在创建延迟签名程序集时要在文件中保留多少空间。</span><span class="sxs-lookup"><span data-stu-id="6cb63-105">`StrongNameSignatureSize` is typically used by compilers to determine how much space to reserve in the file when creating a delay-signed assembly.</span></span>  
  
 <span data-ttu-id="6cb63-106">此函数已弃用。</span><span class="sxs-lookup"><span data-stu-id="6cb63-106">This function has been deprecated.</span></span> <span data-ttu-id="6cb63-107">改为使用 [ICLRStrongName：： StrongNameSignatureSize](../hosting/iclrstrongname-strongnamesignaturesize-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="6cb63-107">Use the [ICLRStrongName::StrongNameSignatureSize](../hosting/iclrstrongname-strongnamesignaturesize-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6cb63-108">语法</span><span class="sxs-lookup"><span data-stu-id="6cb63-108">Syntax</span></span>  
  
```cpp  
BOOLEAN StrongNameSignatureSize (
    [in]  BYTE   *pbPublicKeyBlob,  
    [in]  ULONG  cbPublicKeyBlob,
    [in]  DWORD  *pcbSize  
);
```  
  
## <a name="parameters"></a><span data-ttu-id="6cb63-109">参数</span><span class="sxs-lookup"><span data-stu-id="6cb63-109">Parameters</span></span>  

 `pbPublicKeyBlob`  
 <span data-ttu-id="6cb63-110">中 [PublicKeyBlob](publickeyblob-structure.md) 类型的结构，它包含用于生成强名称签名的密钥对的公共部分。</span><span class="sxs-lookup"><span data-stu-id="6cb63-110">[in] A structure of type [PublicKeyBlob](publickeyblob-structure.md) that contains the public portion of the key pair used to generate the strong name signature.</span></span>  
  
 `cbPublicKeyBlob`  
 <span data-ttu-id="6cb63-111">中的大小（以字节为单位） `pbPublicKeyBlob` 。</span><span class="sxs-lookup"><span data-stu-id="6cb63-111">[in] The size, in bytes, of `pbPublicKeyBlob`.</span></span>  
  
 `pcbSize`  
 <span data-ttu-id="6cb63-112">中存储强名称签名所需的字节数。</span><span class="sxs-lookup"><span data-stu-id="6cb63-112">[in] The number of bytes required to store the strong name signature.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6cb63-113">返回值</span><span class="sxs-lookup"><span data-stu-id="6cb63-113">Return Value</span></span>  

 <span data-ttu-id="6cb63-114">`true` 成功完成时;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="6cb63-114">`true` on successful completion; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6cb63-115">备注</span><span class="sxs-lookup"><span data-stu-id="6cb63-115">Remarks</span></span>  

 <span data-ttu-id="6cb63-116">如果 `StrongNameSignatureSize` 函数未成功完成，请调用 [StrongNameErrorInfo](strongnameerrorinfo-function.md) 函数来检索上次生成的错误。</span><span class="sxs-lookup"><span data-stu-id="6cb63-116">If the `StrongNameSignatureSize` function does not complete successfully, call the [StrongNameErrorInfo](strongnameerrorinfo-function.md) function to retrieve the last generated error.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6cb63-117">要求</span><span class="sxs-lookup"><span data-stu-id="6cb63-117">Requirements</span></span>  

 <span data-ttu-id="6cb63-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6cb63-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6cb63-119">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="6cb63-119">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="6cb63-120">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="6cb63-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="6cb63-121">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6cb63-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6cb63-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="6cb63-122">See also</span></span>

- [<span data-ttu-id="6cb63-123">StrongNameSignatureSize 方法</span><span class="sxs-lookup"><span data-stu-id="6cb63-123">StrongNameSignatureSize Method</span></span>](../hosting/iclrstrongname-strongnamesignaturesize-method.md)
- [<span data-ttu-id="6cb63-124">ICLRStrongName 接口</span><span class="sxs-lookup"><span data-stu-id="6cb63-124">ICLRStrongName Interface</span></span>](../hosting/iclrstrongname-interface.md)
