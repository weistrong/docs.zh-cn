---
description: 了解详细信息： WCF 中的安全注意事项
title: WCF 中的安全注意事项
ms.date: 03/30/2017
helpviewer_keywords:
- security [WCF]
- Windows Communication Foundation, security
- WCF, security
ms.assetid: 42055ee0-6d0c-443d-9d89-788dfc345d6d
ms.openlocfilehash: d75ff0d6eede4a46a5b795873e83445a04532993
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99632472"
---
# <a name="security-considerations-in-wcf"></a><span data-ttu-id="26fa0-103">WCF 中的安全注意事项</span><span class="sxs-lookup"><span data-stu-id="26fa0-103">Security Considerations in WCF</span></span>

<span data-ttu-id="26fa0-104">本节中的主题列出了在设计 Windows Communication Foundation (WCF) 应用程序时要考虑的各种安全相关项。</span><span class="sxs-lookup"><span data-stu-id="26fa0-104">The topics in this section list various security-related items to consider when designing a Windows Communication Foundation (WCF) application.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="26fa0-105">本节内容</span><span class="sxs-lookup"><span data-stu-id="26fa0-105">In This Section</span></span>  

 [<span data-ttu-id="26fa0-106">信息泄露</span><span class="sxs-lookup"><span data-stu-id="26fa0-106">Information Disclosure</span></span>](information-disclosure.md)  
 <span data-ttu-id="26fa0-107">讨论信息可能泄露或受到攻击的各种方式，以及如何缓解这些问题。</span><span class="sxs-lookup"><span data-stu-id="26fa0-107">Discusses the various ways that information can be disclosed or attacked, and how to mitigate this.</span></span>  
  
 [<span data-ttu-id="26fa0-108">权限提升</span><span class="sxs-lookup"><span data-stu-id="26fa0-108">Elevation of Privilege</span></span>](elevation-of-privilege.md)  
 <span data-ttu-id="26fa0-109">讨论给予攻击者的权限超出最初授予的权限范围的后果，以及如何减轻这种后果。</span><span class="sxs-lookup"><span data-stu-id="26fa0-109">Discusses the effects of giving an attacker authorization permissions beyond those initially granted and how to mitigate this.</span></span>  
  
 [<span data-ttu-id="26fa0-110">拒绝服务</span><span class="sxs-lookup"><span data-stu-id="26fa0-110">Denial of Service</span></span>](denial-of-service.md)  
 <span data-ttu-id="26fa0-111">讨论当系统无法正确处理消息时所发生的情况，以及如何缓解这一问题。</span><span class="sxs-lookup"><span data-stu-id="26fa0-111">Discusses what happens when a system is unable to process messages appropriately and how to mitigate it.</span></span>  
  
 [<span data-ttu-id="26fa0-112">篡改</span><span class="sxs-lookup"><span data-stu-id="26fa0-112">Tampering</span></span>](tampering.md)  
 <span data-ttu-id="26fa0-113">讨论消息或消息传递的篡改以及如何缓解这种问题。</span><span class="sxs-lookup"><span data-stu-id="26fa0-113">Discusses the altering of messages or the delivery of messages and how to mitigate it.</span></span>  
  
 [<span data-ttu-id="26fa0-114">重播攻击</span><span class="sxs-lookup"><span data-stu-id="26fa0-114">Replay Attacks</span></span>](replay-attacks.md)  
 <span data-ttu-id="26fa0-115">讨论当攻击者复制通信双方之间的消息流并将该消息流向一方或多方重播时将发生的情况，以及如何缓解这一问题。</span><span class="sxs-lookup"><span data-stu-id="26fa0-115">Discusses what happens when an attacker copies a stream of messages between two parties and replays the stream to one or more of the parties, and how to mitigate this.</span></span>  
  
 [<span data-ttu-id="26fa0-116">安全会话的安全注意事项</span><span class="sxs-lookup"><span data-stu-id="26fa0-116">Security Considerations for Secure Sessions</span></span>](security-considerations-for-secure-sessions.md)  
 <span data-ttu-id="26fa0-117">讨论在实现安全会话时影响安全的下列事项。</span><span class="sxs-lookup"><span data-stu-id="26fa0-117">Discusses the following items that affect security when implementing secure sessions.</span></span>  
  
 [<span data-ttu-id="26fa0-118">不受支持的方案</span><span class="sxs-lookup"><span data-stu-id="26fa0-118">Unsupported Scenarios</span></span>](unsupported-scenarios.md)  
 <span data-ttu-id="26fa0-119">列出不支持某个特定安全方面的各种方案，应当避免或谨慎考虑这些方案。</span><span class="sxs-lookup"><span data-stu-id="26fa0-119">Lists various scenarios that do not support a particular aspect of security and should be avoided or considered.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="26fa0-120">参考</span><span class="sxs-lookup"><span data-stu-id="26fa0-120">Reference</span></span>  

 <xref:System.IdentityModel.Tokens>  
  
 <xref:System.IdentityModel.Claims>  
  
 <xref:System.ServiceModel.Security>  
  
 <xref:System.ServiceModel>  
  
## <a name="related-sections"></a><span data-ttu-id="26fa0-121">相关章节</span><span class="sxs-lookup"><span data-stu-id="26fa0-121">Related Sections</span></span>  

 [<span data-ttu-id="26fa0-122">安全指导和最佳做法</span><span class="sxs-lookup"><span data-stu-id="26fa0-122">Security Guidance and Best Practices</span></span>](security-guidance-and-best-practices.md)  
  
## <a name="see-also"></a><span data-ttu-id="26fa0-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="26fa0-123">See also</span></span>

- [<span data-ttu-id="26fa0-124">安全性</span><span class="sxs-lookup"><span data-stu-id="26fa0-124">Security</span></span>](security.md)
