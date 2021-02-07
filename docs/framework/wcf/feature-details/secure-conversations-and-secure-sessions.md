---
description: 了解详细信息：安全对话和安全会话
title: 安全对话和安全会话
ms.date: 03/30/2017
ms.assetid: 48cb104a-532d-40ae-aa57-769dae103fda
ms.openlocfilehash: dd935fd5de833dc2ba68b1aec3a2992dcba6a000
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99733107"
---
# <a name="secure-conversations-and-secure-sessions"></a><span data-ttu-id="beff8-103">安全对话和安全会话</span><span class="sxs-lookup"><span data-stu-id="beff8-103">Secure Conversations and Secure Sessions</span></span>

<span data-ttu-id="beff8-104">WCF) Windows Communication Foundation (的一项功能是能够在两个终结点之间建立安全会话，这些终结点彼此进行身份验证，并同意加密和数字签名过程。</span><span class="sxs-lookup"><span data-stu-id="beff8-104">A feature of Windows Communication Foundation (WCF) is the ability to establish secure sessions between two endpoints that authenticate each other and agree upon an encryption and digital signature process.</span></span> <span data-ttu-id="beff8-105">例如，服务终结点可能要求客户端终结点发送一个基于 X.509 证书的安全令牌，以便进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="beff8-105">For example, the service endpoint might require a client endpoint to send a security token based upon an X.509 certificate for authentication.</span></span> <span data-ttu-id="beff8-106">在对客户端进行身份验证之后，服务终结点将向客户端返回一个安全上下文令牌 (SCT)，该令牌随后将用于保护该会话中的所有后续消息。</span><span class="sxs-lookup"><span data-stu-id="beff8-106">Once the client is authenticated, the service endpoint returns a security context token (SCT) back to the client that is then used to secure all subsequent messages within the session.</span></span> <span data-ttu-id="beff8-107">通过建立这一安全会话，可使两个终结点之间交换的一组消息更有效率，因为 SCT 具有对称密钥。</span><span class="sxs-lookup"><span data-stu-id="beff8-107">Establishing this secure session enables the set of messages that are exchanged between the two endpoints to be more efficient, because the SCT has a symmetric key.</span></span> <span data-ttu-id="beff8-108">在生成数字签名或加密一组数据时，与对称密钥相比，作为 X.509 证书基础的非对称密钥明显需要更多的计算能力。</span><span class="sxs-lookup"><span data-stu-id="beff8-108">Asymmetric keys, which X.509 certificates are based upon, require significantly more computational power than symmetric keys when generating a digital signature or encrypting a set of data.</span></span>  
  
 <span data-ttu-id="beff8-109">[Ws-securitypolicy](https://docs.oasis-open.org/ws-sx/ws-securitypolicy/200702/ws-securitypolicy-1.2-spec-os.html)) 标准的6.2.7 部分中定义的启动策略 (包含用于保护通道的消息安全断言，并在 RST/SCT 和 RSTR/sct 交换之前对客户端进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="beff8-109">The bootstrap policy (defined in section 6.2.7 of the [WS-SecurityPolicy](https://docs.oasis-open.org/ws-sx/ws-securitypolicy/200702/ws-securitypolicy-1.2-spec-os.html) standard) contains the message security assertions used to secure the channel and authenticate the client prior to the RST/SCT and RSTR/SCT exchange.</span></span> <span data-ttu-id="beff8-110">某些 WCF 标准绑定具有一个 `Security.Message.EstablishSecurityContext` 属性，该属性控制是否使用安全对话。</span><span class="sxs-lookup"><span data-stu-id="beff8-110">Certain WCF standard bindings have a `Security.Message.EstablishSecurityContext` property which controls whether secure conversation is used.</span></span> <span data-ttu-id="beff8-111">使用自定义绑定时，可以通过 [\<secureConversationBootstrap>](../../configure-apps/file-schema/wcf/secureconversationbootstrap.md) 在配置文件中或通过 <xref:System.ServiceModel.Channels.SecurityBindingElement.CreateSecureConversationBindingElement%2A> 在代码中调用来嵌套安全绑定元素，来指示启动。</span><span class="sxs-lookup"><span data-stu-id="beff8-111">When using custom bindings the bootstrap is indicated by nesting security binding elements, either through [\<secureConversationBootstrap>](../../configure-apps/file-schema/wcf/secureconversationbootstrap.md) in the configuration file, or by calling <xref:System.ServiceModel.Channels.SecurityBindingElement.CreateSecureConversationBindingElement%2A> in code.</span></span>  
  
 <span data-ttu-id="beff8-112">有关会话的详细信息，请参阅 [使用会话](../using-sessions.md)。</span><span class="sxs-lookup"><span data-stu-id="beff8-112">For more information about sessions, see [Using Sessions](../using-sessions.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="beff8-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="beff8-113">See also</span></span>

- [<span data-ttu-id="beff8-114">会话、实例化和并发</span><span class="sxs-lookup"><span data-stu-id="beff8-114">Sessions, Instancing, and Concurrency</span></span>](sessions-instancing-and-concurrency.md)
- [<span data-ttu-id="beff8-115">如何：创建要求会话的服务</span><span class="sxs-lookup"><span data-stu-id="beff8-115">How to: Create a Service That Requires Sessions</span></span>](how-to-create-a-service-that-requires-sessions.md)
