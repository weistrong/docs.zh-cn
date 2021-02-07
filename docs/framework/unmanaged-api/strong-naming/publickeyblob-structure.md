---
description: 了解详细信息： PublicKeyBlob 结构
title: PublicKeyBlob 结构
ms.date: 03/30/2017
api_name:
- PublicKeyBlob
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- PublicKeyBlob
helpviewer_keywords:
- PublicKeyBlob structure [.NET Framework strong naming]
ms.assetid: b9240712-829c-4c8d-9a09-a6e7aa63f63a
topic_type:
- apiref
ms.openlocfilehash: 94c1ea3d5a41bbb8941658e87f97cd6d6336187a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99736474"
---
# <a name="publickeyblob-structure"></a><span data-ttu-id="bc01d-103">PublicKeyBlob 结构</span><span class="sxs-lookup"><span data-stu-id="bc01d-103">PublicKeyBlob Structure</span></span>

<span data-ttu-id="bc01d-104">表示公钥/私钥对的公钥，采用二进制格式。</span><span class="sxs-lookup"><span data-stu-id="bc01d-104">Represents, in binary format, the public key of a public/private key pair.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bc01d-105">语法</span><span class="sxs-lookup"><span data-stu-id="bc01d-105">Syntax</span></span>  
  
```cpp  
typedef struct {  
    unsigned int SigAlgId;  
    unsigned int HashAlgId;  
    ULONG cbPublicKey;  
    BYTE PublicKey[1]  
} PublicKeyBlob;
```  
  
## <a name="members"></a><span data-ttu-id="bc01d-106">成员</span><span class="sxs-lookup"><span data-stu-id="bc01d-106">Members</span></span>  
  
|<span data-ttu-id="bc01d-107">成员</span><span class="sxs-lookup"><span data-stu-id="bc01d-107">Member</span></span>|<span data-ttu-id="bc01d-108">说明</span><span class="sxs-lookup"><span data-stu-id="bc01d-108">Description</span></span>|  
|------------|-----------------|  
|`SigAlgId`|<span data-ttu-id="bc01d-109"> (类型的签名算法的标识符 `ALG_ID` ，在公钥的 wincrypt.h) 中定义。</span><span class="sxs-lookup"><span data-stu-id="bc01d-109">The identifier for the signature algorithm (of type `ALG_ID`, as defined in WinCrypt.h) of the public key.</span></span>|  
|`HashAlgId`|<span data-ttu-id="bc01d-110"> (类型的哈希算法的标识符 `ALG_ID` ，在公钥的 wincrypt.h) 中定义。</span><span class="sxs-lookup"><span data-stu-id="bc01d-110">The identifier for the hash algorithm (of type `ALG_ID`, as defined in WinCrypt.h) of the public key.</span></span>|  
|`cbPublicKey`|<span data-ttu-id="bc01d-111">密钥的长度（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="bc01d-111">The length of the key in bytes.</span></span>|  
|`PublicKey`|<span data-ttu-id="bc01d-112">可变长度的字节数组，其中包含由 CryptoAPI 返回的格式的键值。</span><span class="sxs-lookup"><span data-stu-id="bc01d-112">A variable-length byte array that contains the key value in the format returned by the CryptoAPI.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bc01d-113">备注</span><span class="sxs-lookup"><span data-stu-id="bc01d-113">Remarks</span></span>  

 <span data-ttu-id="bc01d-114">`PublicKeyBlob`结构由[StrongNameGetPublicKey](strongnamegetpublickey-function.md)、 [StrongNameSignatureGeneration](strongnamesignaturegeneration-function.md)和其他强名称函数用来表示公钥/私钥对的公钥。</span><span class="sxs-lookup"><span data-stu-id="bc01d-114">The `PublicKeyBlob` structure is used by [StrongNameGetPublicKey](strongnamegetpublickey-function.md), [StrongNameSignatureGeneration](strongnamesignaturegeneration-function.md), and other strong name functions to represent the public key of a public/private key pair.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bc01d-115">要求</span><span class="sxs-lookup"><span data-stu-id="bc01d-115">Requirements</span></span>  

 <span data-ttu-id="bc01d-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bc01d-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bc01d-117">**标头：** Stackexchange.redis.strongname</span><span class="sxs-lookup"><span data-stu-id="bc01d-117">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="bc01d-118">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bc01d-118">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="bc01d-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bc01d-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bc01d-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="bc01d-120">See also</span></span>

- [<span data-ttu-id="bc01d-121">StrongNameGetPublicKey 函数</span><span class="sxs-lookup"><span data-stu-id="bc01d-121">StrongNameGetPublicKey Function</span></span>](strongnamegetpublickey-function.md)
- [<span data-ttu-id="bc01d-122">StrongNameSignatureGeneration 函数</span><span class="sxs-lookup"><span data-stu-id="bc01d-122">StrongNameSignatureGeneration Function</span></span>](strongnamesignaturegeneration-function.md)
