---
description: 了解详细信息：终结点：每秒安全验证和身份验证失败数
title: 终结点：Security Validation and Authentication Failures Per Second（每秒安全验证和身份验证失败次数）
ms.date: 03/30/2017
ms.assetid: 89a70b90-d7e4-4b03-9b84-4dc88ce3d605
ms.openlocfilehash: aa5ccc4049dc81a7c2d545cfc70e9078ac72d87a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99655429"
---
# <a name="endpoint-security-validation-and-authentication-failures-per-second"></a><span data-ttu-id="81556-103">终结点：Security Validation and Authentication Failures Per Second（每秒安全验证和身份验证失败次数）</span><span class="sxs-lookup"><span data-stu-id="81556-103">Endpoint: Security Validation and Authentication Failures Per Second</span></span>

<span data-ttu-id="81556-104">计数器名称：Security Validation and Authentication Failures Per Second（每秒安全验证和身份验证失败次数）</span><span class="sxs-lookup"><span data-stu-id="81556-104">Counter name: Security Validation and Authentication Failures Per Second</span></span>  
  
## <a name="description"></a><span data-ttu-id="81556-105">说明</span><span class="sxs-lookup"><span data-stu-id="81556-105">Description</span></span>  

 <span data-ttu-id="81556-106">每当消息由于“Security Calls Not Authorized”（未授权的安全调用次数）计数器中未包括的安全问题而遭到拒绝时，此计数器即会递增。</span><span class="sxs-lookup"><span data-stu-id="81556-106">This counter is incremented whenever a message is rejected due to a security problem not covered by the "Security Calls Not Authorized" counter.</span></span> <span data-ttu-id="81556-107">此类问题包括：</span><span class="sxs-lookup"><span data-stu-id="81556-107">Such problems include:</span></span>  
  
- <span data-ttu-id="81556-108">无法从消息中读取客户端令牌。</span><span class="sxs-lookup"><span data-stu-id="81556-108">Client token cannot be read from the message.</span></span>  
  
- <span data-ttu-id="81556-109">客户端令牌身份验证失败（如密码错误）。</span><span class="sxs-lookup"><span data-stu-id="81556-109">Client token has failed authentication (for example, bad password).</span></span>  
  
- <span data-ttu-id="81556-110">签名验证失败（如消息已被篡改）。</span><span class="sxs-lookup"><span data-stu-id="81556-110">Signature verification has failed (for example, the message has been tampered).</span></span>  
  
- <span data-ttu-id="81556-111">消息与上一条消息重复，这种情况可能在重放攻击过程中发生。</span><span class="sxs-lookup"><span data-stu-id="81556-111">The message is a duplicate from a previous one, which can happen during a replay attack.</span></span>  
  
- <span data-ttu-id="81556-112">已发生解密失败。</span><span class="sxs-lookup"><span data-stu-id="81556-112">A decryption failure has occurred.</span></span>  
  
- <span data-ttu-id="81556-113">消息中缺少一些必需元素（如缺少时间戳或加密的数据块）。</span><span class="sxs-lookup"><span data-stu-id="81556-113">Some required elements (for example, missing timestamp or encrypted data block) are missing from the message.</span></span>  
  
- <span data-ttu-id="81556-114">TLSNEGO/SPNEGO 握手过程中已发生错误。</span><span class="sxs-lookup"><span data-stu-id="81556-114">Errors have occurred during TLSNEGO/SPNEGO handshake.</span></span>  
  
 <span data-ttu-id="81556-115">此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算：</span><span class="sxs-lookup"><span data-stu-id="81556-115">This counter is of performance counter type [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10)), whose value is calculated using the following formula:</span></span>  
  
 <span data-ttu-id="81556-116">(N1-N0)/((D1-D0)/F)</span><span class="sxs-lookup"><span data-stu-id="81556-116">(N1-N0)/((D1-D0)/F)</span></span>
