---
description: 了解更多：服务：安全验证和身份验证失败
title: 服务：Security Validation and Authentication Failures（安全验证和身份验证失败次数）
ms.date: 03/30/2017
ms.assetid: 55c98268-b1ad-459d-851b-25ef52248187
ms.openlocfilehash: 8938c74e706526a02bf2ea5885951d067d6ebae9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99759479"
---
# <a name="service-security-validation-and-authentication-failures"></a><span data-ttu-id="b2e83-103">服务：Security Validation and Authentication Failures（安全验证和身份验证失败次数）</span><span class="sxs-lookup"><span data-stu-id="b2e83-103">Service: Security Validation and Authentication Failures</span></span>

<span data-ttu-id="b2e83-104">计数器名称：Security Validation and Authentication Failures（安全验证和身份验证失败次数）</span><span class="sxs-lookup"><span data-stu-id="b2e83-104">Counter name: Security Validation and Authentication Failures</span></span>  
  
## <a name="description"></a><span data-ttu-id="b2e83-105">说明</span><span class="sxs-lookup"><span data-stu-id="b2e83-105">Description</span></span>  

 <span data-ttu-id="b2e83-106">每当消息由于“Security Calls Not Authorized”（未授权的安全调用次数）计数器中未包括的安全问题而遭到拒绝时，此计数器即会递增。</span><span class="sxs-lookup"><span data-stu-id="b2e83-106">This counter is incremented whenever a message is rejected due to a security problem not covered by the "Security Calls Not Authorized" counter.</span></span> <span data-ttu-id="b2e83-107">此类问题包括：</span><span class="sxs-lookup"><span data-stu-id="b2e83-107">Such problems include:</span></span>  
  
- <span data-ttu-id="b2e83-108">无法从消息中读取客户端令牌。</span><span class="sxs-lookup"><span data-stu-id="b2e83-108">Client token cannot be read from the message.</span></span>  
  
- <span data-ttu-id="b2e83-109">客户端令牌身份验证失败（如密码错误）。</span><span class="sxs-lookup"><span data-stu-id="b2e83-109">Client token has failed authentication (for example, bad password).</span></span>  
  
- <span data-ttu-id="b2e83-110">签名验证失败（如消息已被篡改）。</span><span class="sxs-lookup"><span data-stu-id="b2e83-110">Signature verification has failed (for example, the message has been tampered).</span></span>  
  
- <span data-ttu-id="b2e83-111">消息与上一条消息重复，这种情况可能在重放攻击过程中发生。</span><span class="sxs-lookup"><span data-stu-id="b2e83-111">The message is a duplicate from a previous one, which can happen during a replay attack.</span></span>  
  
- <span data-ttu-id="b2e83-112">已发生解密失败。</span><span class="sxs-lookup"><span data-stu-id="b2e83-112">A decryption failure has occurred.</span></span>  
  
- <span data-ttu-id="b2e83-113">消息中缺少一些必需元素（如缺少时间戳或加密的数据块）。</span><span class="sxs-lookup"><span data-stu-id="b2e83-113">Some required elements (for example, missing timestamp or encrypted data block) are missing from the message.</span></span>  
  
- <span data-ttu-id="b2e83-114">TLSNEGO/SPNEGO 握手过程中已发生错误。</span><span class="sxs-lookup"><span data-stu-id="b2e83-114">Errors have occurred during TLSNEGO/SPNEGO handshake.</span></span>
