---
description: 详细了解：对等协作
title: 对等协作
ms.date: 03/30/2017
ms.assetid: b6216d88-bccb-4a59-9f1c-9f751708e811
ms.openlocfilehash: 824ab3152c1ad765c2d19f5c6e719242255f606d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99738274"
---
# <a name="peer-to-peer-collaboration"></a><span data-ttu-id="334fd-103">对等协作</span><span class="sxs-lookup"><span data-stu-id="334fd-103">Peer-to-peer collaboration</span></span>

<span data-ttu-id="334fd-104">对等网络服务利用存在于 Internet 边缘的相对强大的计算机（个人计算机）完成各项任务，不仅仅是基于客户端的计算任务。</span><span class="sxs-lookup"><span data-stu-id="334fd-104">Peer-to-peer networking is the utilization of the relatively powerful computers (personal computers) that exist at the edge of the Internet for more than just client-based computing tasks.</span></span> <span data-ttu-id="334fd-105">现代个人电脑 (PC) 具有超快处理器、大量存储和大型硬盘，在执行电子邮件和 Web 浏览等常见计算任务时，并未充分利用这些优势。</span><span class="sxs-lookup"><span data-stu-id="334fd-105">The modern personal computer (PC) has a very fast processor, vast memory, and a large hard disk, none of which are being fully utilized when performing common computing tasks such as email and Web browsing.</span></span> <span data-ttu-id="334fd-106">现代 PC 可以轻松地充当许多类型的应用程序的客户端和服务器（对等机）。</span><span class="sxs-lookup"><span data-stu-id="334fd-106">The modern PC can easily act as both a client and server (a peer) for many types of applications.</span></span>  
  
<span data-ttu-id="334fd-107">对等协作基础架构是 Microsoft Windows 对等基础架构的简化实现，它利用了 Windows Vista 及更高版本平台中的网络邻居服务。</span><span class="sxs-lookup"><span data-stu-id="334fd-107">The Peer-to-Peer Collaboration Infrastructure is a simplified implementation of the Microsoft Windows Peer-to-Peer Infrastructure that leverages the People Near Me service in Windows Vista and later platforms.</span></span> <span data-ttu-id="334fd-108">它最适用于网络邻居服务运行的子网内启用了对等的应用程序，尽管它也可为 Internet 终结点或联系人提供服务。</span><span class="sxs-lookup"><span data-stu-id="334fd-108">It is best used for peer-enabled applications within a subnet for which the People Near Me service operates, although it can service internet endpoints or contacts as well.</span></span> <span data-ttu-id="334fd-109">它集成了 Live Messenger 和其他 Live 感知应用程序使用的常见联系人管理器，以确定联系人终结点、可用性和状态。</span><span class="sxs-lookup"><span data-stu-id="334fd-109">It incorporates the common Contact Manager that is used by Live Messenger and other Live-aware applications to determine contact endpoints, availability, and presence.</span></span>  
  
## <a name="collaboration-applications"></a><span data-ttu-id="334fd-110">协作应用程序</span><span class="sxs-lookup"><span data-stu-id="334fd-110">Collaboration applications</span></span>

 <span data-ttu-id="334fd-111">典型的对等协作应用程序包含以下步骤：</span><span class="sxs-lookup"><span data-stu-id="334fd-111">A typical peer-to-peer collaboration application is comprised of the following steps:</span></span>  
  
- <span data-ttu-id="334fd-112">对等机确定有兴趣托管协作会话的对等机身份</span><span class="sxs-lookup"><span data-stu-id="334fd-112">Peer determines the identity of a peer who is interested in hosting a collaboration session</span></span>  
  
- <span data-ttu-id="334fd-113">以某种方式发送托管会话请求，主机对等机同意管理协作活动。</span><span class="sxs-lookup"><span data-stu-id="334fd-113">A request to host a session is sent, somehow, and the host peer agrees to manage collaboration activity.</span></span>  
  
- <span data-ttu-id="334fd-114">主机邀请子网联系人（包括请求者）参与会话。</span><span class="sxs-lookup"><span data-stu-id="334fd-114">The host invites contacts on the subnet (including the requestor) to a session.</span></span>  
  
- <span data-ttu-id="334fd-115">希望协作的所有对等机均可将主机添加到其联系人管理器。</span><span class="sxs-lookup"><span data-stu-id="334fd-115">All peers who want to collaborate may add the host to their contact managers.</span></span>  
  
- <span data-ttu-id="334fd-116">无论接受还是拒绝，大多数对等机将及时向主机对等机发回邀请回复。</span><span class="sxs-lookup"><span data-stu-id="334fd-116">Most peers will send invitation responses, whether accepted or declined, back to the host peer in a timely fashion.</span></span>  
  
- <span data-ttu-id="334fd-117">所有希望协作的对等机都将订阅主机对等机。</span><span class="sxs-lookup"><span data-stu-id="334fd-117">All peers who want to collaborate will subscribe to the host peer.</span></span>  
  
- <span data-ttu-id="334fd-118">当对等机正在执行其初始协作活动时，主机对等机可向其联系人管理器添加远程对等机。</span><span class="sxs-lookup"><span data-stu-id="334fd-118">While the peers are performing their initial collaboration activity, the host peer may add remote peers to its contact manager.</span></span> <span data-ttu-id="334fd-119">它还处理所有邀请回复，以确定接受者、拒绝者、未答复者。</span><span class="sxs-lookup"><span data-stu-id="334fd-119">It also processes all invitation responses to determine who has accepted, who has declined, and who has not answered.</span></span>  <span data-ttu-id="334fd-120">它可能会取消邀请那些尚未答复或执行一些其他活动的人。</span><span class="sxs-lookup"><span data-stu-id="334fd-120">It may cancel invitations to those who have not answered, or perform some other activity.</span></span>  
  
- <span data-ttu-id="334fd-121">此时，主机对等机可与所有受邀对等机开始协作会话，或向协作基础架构注册应用程序。</span><span class="sxs-lookup"><span data-stu-id="334fd-121">At this point, the host peer can start a collaboration session with all invited peers, or register an application with the collaboration infrastructure.</span></span>  <span data-ttu-id="334fd-122">P2P 应用程序使用对等协作基础架构和 <xref:System.Net.PeerToPeer.Collaboration> 命名空间来协调游戏、公告牌、会议和其他无服务器状态应用程序的通信。</span><span class="sxs-lookup"><span data-stu-id="334fd-122">P2P applications use the Peer-to-Peer Collaboration Infrastructure and the <xref:System.Net.PeerToPeer.Collaboration> namespace to coordinate communications for games, bulletin boards, conferencing, and other serverless presence applications.</span></span>  
  
## <a name="peer-to-peer-networking-security"></a><span data-ttu-id="334fd-123">对等网络安全</span><span class="sxs-lookup"><span data-stu-id="334fd-123">Peer-to-peer networking security</span></span>  

 <span data-ttu-id="334fd-124">在 Active Directory 域中，域控制器使用 Kerberos 提供身份验证服务。</span><span class="sxs-lookup"><span data-stu-id="334fd-124">In an Active Directory domain, domain controllers provide authentication services using Kerberos.</span></span> <span data-ttu-id="334fd-125">在无服务器对等环境中，对等机必须提供其自身的身份验证。</span><span class="sxs-lookup"><span data-stu-id="334fd-125">In a serverless peer environment, the peers must provide their own authentication.</span></span> <span data-ttu-id="334fd-126">对于对等网络，任何节点都可充当 CA，无需要求每个对等机受信任根存储中存在根证书。</span><span class="sxs-lookup"><span data-stu-id="334fd-126">For Peer-to-Peer Networking, any node can act as a CA, removing the requirement of a root certificate in each peer's trusted root store.</span></span> <span data-ttu-id="334fd-127">使用自签名证书提供身份验证，格式为 X.509 证书。</span><span class="sxs-lookup"><span data-stu-id="334fd-127">Authentication is provided using self-signed certificates, formatted as X.509 certificates.</span></span> <span data-ttu-id="334fd-128">这些是由每个对等机创建的证书，其生成公钥/私钥对以及使用私钥签名的证书。</span><span class="sxs-lookup"><span data-stu-id="334fd-128">These are certificates that are created by each peer, which generates the public key/private key pair and the certificate that is signed using the private key.</span></span> <span data-ttu-id="334fd-129">自签名证书用于身份验证，并提供有关对等机实体的信息。</span><span class="sxs-lookup"><span data-stu-id="334fd-129">The self-signed certificate is used for authentication and to provide information about the peer entity.</span></span> <span data-ttu-id="334fd-130">如 X.509 身份验证一样，对等机网络身份验证依赖于一系列追溯受信任公钥的证书。</span><span class="sxs-lookup"><span data-stu-id="334fd-130">Like X.509 authentication, peer networking authentication relies upon a chain of certificates tracing back to a public key that is trusted.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="334fd-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="334fd-131">See also</span></span>

- <xref:System.Net.PeerToPeer.Collaboration>
- [<span data-ttu-id="334fd-132">关于 System.Net.PeerToPeer.Collaboration 命名空间</span><span class="sxs-lookup"><span data-stu-id="334fd-132">About the System.Net.PeerToPeer.Collaboration Namespace</span></span>](about-the-system-net-peertopeer-collaboration-namespace.md)
