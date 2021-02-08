---
description: 了解详细信息： AXL_AUTHENTICODE_SIGNER_INFO 结构
title: AXL_AUTHENTICODE_SIGNER_INFO 结构
ms.date: 03/30/2017
ms.assetid: 81c0f8b4-ce35-4716-8651-b642d40648a2
ms.openlocfilehash: 940652cf184e26f141df806b060c391333d1bb95
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781956"
---
# <a name="axl_authenticode_signer_info-structure"></a><span data-ttu-id="d5661-103">AXL_AUTHENTICODE_SIGNER_INFO 结构</span><span class="sxs-lookup"><span data-stu-id="d5661-103">AXL_AUTHENTICODE_SIGNER_INFO Structure</span></span>

<span data-ttu-id="d5661-104">定义验证码签署人的信息。</span><span class="sxs-lookup"><span data-stu-id="d5661-104">Defines the Authenticode signer information.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d5661-105">语法</span><span class="sxs-lookup"><span data-stu-id="d5661-105">Syntax</span></span>  
  
```cpp  
typedef struct _AXL_AUTHENTICODE_SIGNER_INFO {  
    DWORD cbSize;  
    HRESULT dwError;  
    ALG_ID algHash;  
    LPCWSTR pwszHash  
    LPCWSTR pwszDescription;  
    LPCWSTR pwszDescriptionUrl;  
    PCCERT_CHAIN_CONTEXT pChainContext  
} AXL_AUTHENTICODE_SIGNER_INFO, * PAXL_AUTHENTICODE_SIGNER_INFO;  
```  
  
## <a name="members"></a><span data-ttu-id="d5661-106">成员</span><span class="sxs-lookup"><span data-stu-id="d5661-106">Members</span></span>  
  
|<span data-ttu-id="d5661-107">成员</span><span class="sxs-lookup"><span data-stu-id="d5661-107">Member</span></span>|<span data-ttu-id="d5661-108">说明</span><span class="sxs-lookup"><span data-stu-id="d5661-108">Description</span></span>|  
|------------|-----------------|  
|`cbSize`|<span data-ttu-id="d5661-109">此结构的大小。</span><span class="sxs-lookup"><span data-stu-id="d5661-109">The size of this structure.</span></span>|  
|`dwError`|<span data-ttu-id="d5661-110">错误代码。</span><span class="sxs-lookup"><span data-stu-id="d5661-110">The error code.</span></span>|  
|`algHash`|<span data-ttu-id="d5661-111">哈希算法。</span><span class="sxs-lookup"><span data-stu-id="d5661-111">The hash algorithm.</span></span>|  
|`pwszHash`|<span data-ttu-id="d5661-112">哈希。</span><span class="sxs-lookup"><span data-stu-id="d5661-112">The hash.</span></span>|  
|`pwszDescription`|<span data-ttu-id="d5661-113">说明。</span><span class="sxs-lookup"><span data-stu-id="d5661-113">The description.</span></span>|  
|`pwszDescriptionUrl`|<span data-ttu-id="d5661-114">说明的 URL。</span><span class="sxs-lookup"><span data-stu-id="d5661-114">The URL of the description.</span></span>|  
|`pChainContext`|<span data-ttu-id="d5661-115">签署人的链上下文。</span><span class="sxs-lookup"><span data-stu-id="d5661-115">The chain context of the signer.</span></span> <span data-ttu-id="d5661-116">请参阅 [CERT_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) 结构。</span><span class="sxs-lookup"><span data-stu-id="d5661-116">See the [CERT_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) structure.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d5661-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="d5661-117">See also</span></span>

- [<span data-ttu-id="d5661-118">验证码</span><span class="sxs-lookup"><span data-stu-id="d5661-118">Authenticode</span></span>](index.md)
