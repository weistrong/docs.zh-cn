---
description: 了解详细信息： ICLRStrongName2 接口
title: ICLRStrongName2 接口
ms.date: 03/30/2017
api_name:
- ICLRStrongName2
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName2
helpviewer_keywords:
- ICLRStrongName2 interface [.NET Framework hosting]
ms.assetid: 9f098a74-201e-4628-a468-8dee9ab99b4a
topic_type:
- apiref
ms.openlocfilehash: 7442bd054af735e9f1b75b05feb8724dfa993f73
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781787"
---
# <a name="iclrstrongname2-interface"></a><span data-ttu-id="16181-103">ICLRStrongName2 接口</span><span class="sxs-lookup"><span data-stu-id="16181-103">ICLRStrongName2 Interface</span></span>

<span data-ttu-id="16181-104">提供使用 SHA-256、SHA-384 和 SHA-512)  (sha-1 安全哈希算法组创建强名称的功能。</span><span class="sxs-lookup"><span data-stu-id="16181-104">Provides the ability to create strong names using the SHA-2 group of Secure Hash Algorithms (SHA-256, SHA-384, and SHA-512).</span></span>  
  
## <a name="methods"></a><span data-ttu-id="16181-105">方法</span><span class="sxs-lookup"><span data-stu-id="16181-105">Methods</span></span>  
  
|<span data-ttu-id="16181-106">方法</span><span class="sxs-lookup"><span data-stu-id="16181-106">Method</span></span>|<span data-ttu-id="16181-107">说明</span><span class="sxs-lookup"><span data-stu-id="16181-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="16181-108">StrongNameGetPublicKeyEx 方法</span><span class="sxs-lookup"><span data-stu-id="16181-108">StrongNameGetPublicKeyEx Method</span></span>](strongnamegetpublickeyex-method.md)|<span data-ttu-id="16181-109">获取公钥/私钥对中的公钥，并指定哈希算法和签名算法。</span><span class="sxs-lookup"><span data-stu-id="16181-109">Gets the public key from a public/private key pair, and specifies a hash algorithm and a signature algorithm.</span></span>|  
|[<span data-ttu-id="16181-110">StrongNameSignatureVerificationEx2 方法</span><span class="sxs-lookup"><span data-stu-id="16181-110">StrongNameSignatureVerificationEx2 Method</span></span>](strongnamesignatureverificationex2-method.md)|<span data-ttu-id="16181-111">验证强名称程序集的签名，并提供从 ECMA 密钥到实际密钥的映射。</span><span class="sxs-lookup"><span data-stu-id="16181-111">Verifies the signature of a strongly named assembly, and provides a mapping from the ECMA key to a real key.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="16181-112">备注</span><span class="sxs-lookup"><span data-stu-id="16181-112">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="16181-113">要求</span><span class="sxs-lookup"><span data-stu-id="16181-113">Requirements</span></span>  

 <span data-ttu-id="16181-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="16181-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="16181-115">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="16181-115">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="16181-116">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="16181-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="16181-117">**.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="16181-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>
