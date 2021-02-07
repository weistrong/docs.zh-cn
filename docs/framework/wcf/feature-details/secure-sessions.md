---
description: 了解详细信息：安全会话
title: 安全会话
ms.date: 03/30/2017
ms.assetid: 7b50602f-d7b5-42e9-8e92-1f0413df0d8b
ms.openlocfilehash: 8a4a2d23d5a27f5066bd5f004582829e499f714c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99733068"
---
# <a name="secure-sessions"></a><span data-ttu-id="f9a1b-103">安全会话</span><span class="sxs-lookup"><span data-stu-id="f9a1b-103">Secure Sessions</span></span>

<span data-ttu-id="f9a1b-104">WCF) Windows Communication Foundation (的一项功能是可靠会话，可保证按消息发送顺序接收消息。</span><span class="sxs-lookup"><span data-stu-id="f9a1b-104">A feature of Windows Communication Foundation (WCF) is reliable sessions that guarantee messages are received in the order they were sent.</span></span> <span data-ttu-id="f9a1b-105">本节中的主题讨论在创建可靠会话时要考虑的安全性问题。</span><span class="sxs-lookup"><span data-stu-id="f9a1b-105">The topics in this section discuss the security implications to consider when creating a reliable session.</span></span> <span data-ttu-id="f9a1b-106">有关可靠会话的详细信息，请参阅 [使用会话](../using-sessions.md)。</span><span class="sxs-lookup"><span data-stu-id="f9a1b-106">For more information about reliable sessions, see [Using Sessions](../using-sessions.md).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="f9a1b-107">当需要在 Windows XP 上进行模拟时，请不要在安全会话中使用有状态安全令牌上下文 (SCT)。</span><span class="sxs-lookup"><span data-stu-id="f9a1b-107">When impersonation is required on Windows XP, use a secure session without a stateful security context token (SCT).</span></span> <span data-ttu-id="f9a1b-108">如果在模拟时使用有状态 SCT，则会引发 <xref:System.InvalidOperationException>。</span><span class="sxs-lookup"><span data-stu-id="f9a1b-108">When stateful SCTs are used with impersonation, an <xref:System.InvalidOperationException> is thrown.</span></span> <span data-ttu-id="f9a1b-109">有关详细信息，请参阅 [不支持的方案](unsupported-scenarios.md)。</span><span class="sxs-lookup"><span data-stu-id="f9a1b-109">For more information, see [Unsupported Scenarios](unsupported-scenarios.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="f9a1b-110">本节内容</span><span class="sxs-lookup"><span data-stu-id="f9a1b-110">In This Section</span></span>  
  
|||  
|-|-|  
|[<span data-ttu-id="f9a1b-111">安全对话和安全会话</span><span class="sxs-lookup"><span data-stu-id="f9a1b-111">Secure Conversations and Secure Sessions</span></span>](secure-conversations-and-secure-sessions.md)|<span data-ttu-id="f9a1b-112">安全对话和安全会话是同义词。</span><span class="sxs-lookup"><span data-stu-id="f9a1b-112">Secure conversations and secure sessions are synonymous.</span></span> <span data-ttu-id="f9a1b-113">本主题解释安全对话的工作方式以及使用该模式的时机和原因。</span><span class="sxs-lookup"><span data-stu-id="f9a1b-113">This topic explains the way a secure conversation works, and when and why to use the pattern.</span></span>|  
|[<span data-ttu-id="f9a1b-114">如何：创建安全会话</span><span class="sxs-lookup"><span data-stu-id="f9a1b-114">How to: Create a Secure Session</span></span>](how-to-create-a-secure-session.md)|<span data-ttu-id="f9a1b-115">演练创建安全会话的基本操作。</span><span class="sxs-lookup"><span data-stu-id="f9a1b-115">Walks through of the basics of creating a secure session.</span></span>|  
|[<span data-ttu-id="f9a1b-116">如何：为安全会话创建安全上下文令牌</span><span class="sxs-lookup"><span data-stu-id="f9a1b-116">How to: Create a Security Context Token for a Secure Session</span></span>](how-to-create-a-security-context-token-for-a-secure-session.md)|<span data-ttu-id="f9a1b-117">演练创建能够保持状态以及与客户端之间会话的网络场的步骤。</span><span class="sxs-lookup"><span data-stu-id="f9a1b-117">Walks through the steps of creating a Web farm that will maintain state and sessions with clients.</span></span>|  
|[<span data-ttu-id="f9a1b-118">安全会话的安全注意事项</span><span class="sxs-lookup"><span data-stu-id="f9a1b-118">Security Considerations for Secure Sessions</span></span>](security-considerations-for-secure-sessions.md)|<span data-ttu-id="f9a1b-119">描述安全会话的特殊注意事项。</span><span class="sxs-lookup"><span data-stu-id="f9a1b-119">Describes special considerations for secure sessions.</span></span>|  
  
## <a name="reference"></a><span data-ttu-id="f9a1b-120">参考</span><span class="sxs-lookup"><span data-stu-id="f9a1b-120">Reference</span></span>  

 <xref:System.ServiceModel>  
  
 <xref:System.ServiceModel.Channels>  
  
## <a name="related-sections"></a><span data-ttu-id="f9a1b-121">相关章节</span><span class="sxs-lookup"><span data-stu-id="f9a1b-121">Related Sections</span></span>  

 [<span data-ttu-id="f9a1b-122">会话、实例化和并发</span><span class="sxs-lookup"><span data-stu-id="f9a1b-122">Sessions, Instancing, and Concurrency</span></span>](sessions-instancing-and-concurrency.md)  
  
 [<span data-ttu-id="f9a1b-123">设计和实现服务</span><span class="sxs-lookup"><span data-stu-id="f9a1b-123">Designing and Implementing Services</span></span>](../designing-and-implementing-services.md)  
  
## <a name="see-also"></a><span data-ttu-id="f9a1b-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="f9a1b-124">See also</span></span>

- [<span data-ttu-id="f9a1b-125">如何：启用消息重放检测</span><span class="sxs-lookup"><span data-stu-id="f9a1b-125">How to: Enable Message Replay Detection</span></span>](how-to-enable-message-replay-detection.md)
- [<span data-ttu-id="f9a1b-126">重播攻击</span><span class="sxs-lookup"><span data-stu-id="f9a1b-126">Replay Attacks</span></span>](replay-attacks.md)
- [<span data-ttu-id="f9a1b-127">如何：创建要求会话的服务</span><span class="sxs-lookup"><span data-stu-id="f9a1b-127">How to: Create a Service That Requires Sessions</span></span>](how-to-create-a-service-that-requires-sessions.md)
