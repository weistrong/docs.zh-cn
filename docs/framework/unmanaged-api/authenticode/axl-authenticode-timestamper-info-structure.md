---
description: 了解详细信息： AXL_AUTHENTICODE_TIMESTAMPER_INFO 结构
title: AXL_AUTHENTICODE_TIMESTAMPER_INFO 结构
ms.date: 03/30/2017
ms.assetid: 89e41a81-0f41-45ad-8f20-a120e4ff24fb
ms.openlocfilehash: 35e30241c3c3b5747e247c57183e28e726c0cae3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99747408"
---
# <a name="axl_authenticode_timestamper_info-structure"></a><span data-ttu-id="cc132-103">AXL_AUTHENTICODE_TIMESTAMPER_INFO 结构</span><span class="sxs-lookup"><span data-stu-id="cc132-103">AXL_AUTHENTICODE_TIMESTAMPER_INFO Structure</span></span>

<span data-ttu-id="cc132-104">定义验证码时间戳签署人的信息。</span><span class="sxs-lookup"><span data-stu-id="cc132-104">Defines the Authenticode time stamper information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cc132-105">语法</span><span class="sxs-lookup"><span data-stu-id="cc132-105">Syntax</span></span>  
  
```cpp  
typedef struct _AXL_AUTHENTICODE_SIGNER_INFO {  
    DWORD cbSize;  
    HRESULT dwError;  
    ALG_ID algHash;  
    FILETIME ftTimestamp  
    PCCERT_CHAIN_CONTEXT pChainContext;  
} AXL_AUTHENTICODE_TIMESTAMPER_INFO, * PAXL_AUTHENTICODE_TIMESTAMPER_INFO;  
```  
  
## <a name="members"></a><span data-ttu-id="cc132-106">成员</span><span class="sxs-lookup"><span data-stu-id="cc132-106">Members</span></span>  
  
|<span data-ttu-id="cc132-107">成员</span><span class="sxs-lookup"><span data-stu-id="cc132-107">Member</span></span>|<span data-ttu-id="cc132-108">说明</span><span class="sxs-lookup"><span data-stu-id="cc132-108">Description</span></span>|  
|------------|-----------------|  
|`cbSize`|<span data-ttu-id="cc132-109">此结构的大小。</span><span class="sxs-lookup"><span data-stu-id="cc132-109">The size of this structure.</span></span>|  
|`dwError`|<span data-ttu-id="cc132-110">错误代码。</span><span class="sxs-lookup"><span data-stu-id="cc132-110">The error code.</span></span>|  
|`algHash`|<span data-ttu-id="cc132-111">哈希算法。</span><span class="sxs-lookup"><span data-stu-id="cc132-111">The hash algorithm.</span></span>|  
|`ftTimestamp`|<span data-ttu-id="cc132-112">时间戳的时间。</span><span class="sxs-lookup"><span data-stu-id="cc132-112">The time of the time stamp.</span></span>|  
|`pChainContext`|<span data-ttu-id="cc132-113">时间戳签署人的链上下文。</span><span class="sxs-lookup"><span data-stu-id="cc132-113">The time stamper’s chain context.</span></span>  <span data-ttu-id="cc132-114">请参阅 [CERT_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) 结构。</span><span class="sxs-lookup"><span data-stu-id="cc132-114">See the [CERT_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) structure.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="cc132-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="cc132-115">See also</span></span>

- [<span data-ttu-id="cc132-116">验证码</span><span class="sxs-lookup"><span data-stu-id="cc132-116">Authenticode</span></span>](index.md)
