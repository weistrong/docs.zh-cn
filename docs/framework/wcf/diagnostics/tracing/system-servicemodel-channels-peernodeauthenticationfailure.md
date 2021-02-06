---
description: 了解有关以下方面的详细信息： PeerNodeAuthenticationFailure
title: System.ServiceModel.Channels.PeerNodeAuthenticationFailure
ms.date: 03/30/2017
ms.assetid: 0b50f782-ca06-4a82-aa7f-71f78ddc5177
ms.openlocfilehash: 751202abd3e199a03fc4ee0bf1252d4a8027e0cb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99634929"
---
# <a name="systemservicemodelchannelspeernodeauthenticationfailure"></a><span data-ttu-id="ebc22-103">System.ServiceModel.Channels.PeerNodeAuthenticationFailure</span><span class="sxs-lookup"><span data-stu-id="ebc22-103">System.ServiceModel.Channels.PeerNodeAuthenticationFailure</span></span>

<span data-ttu-id="ebc22-104">与潜在邻居的安全握手没有成功。</span><span class="sxs-lookup"><span data-stu-id="ebc22-104">The security handshake with a potential neighbor was not successful.</span></span>  
  
## <a name="description"></a><span data-ttu-id="ebc22-105">说明</span><span class="sxs-lookup"><span data-stu-id="ebc22-105">Description</span></span>  

 <span data-ttu-id="ebc22-106">此跟踪在尝试建立安全邻居连接时发生。</span><span class="sxs-lookup"><span data-stu-id="ebc22-106">This trace occurs while attempting to establish a secure neighbor connection.</span></span> <span data-ttu-id="ebc22-107">凭据不充足或不正确可以导致出现此情况。</span><span class="sxs-lookup"><span data-stu-id="ebc22-107">This can happen due to insufficient or incorrect credentials.</span></span>  
  
 <span data-ttu-id="ebc22-108">对等通道只能识别一种强标识令牌类型，即 X.509 证书，X.509 证书基于可实现的身份验证和授权类型，提供强标识模型。</span><span class="sxs-lookup"><span data-stu-id="ebc22-108">PeerChannel recognizes a single token type for strong identification, X.509 certificates, which provide a strong identity model based on the type of authentication and authorization that can be implemented.</span></span> <span data-ttu-id="ebc22-109">对等通道还可通过使用密码为简单应用程序提供支持。</span><span class="sxs-lookup"><span data-stu-id="ebc22-109">PeerChannel also provides support for simple applications through the use of passwords.</span></span> <span data-ttu-id="ebc22-110">密码仅用于允许加入会话，不能用于执行消息身份验证。</span><span class="sxs-lookup"><span data-stu-id="ebc22-110">Passwords can be used only to allow entry to the session; they cannot be used to perform message authentication.</span></span> <span data-ttu-id="ebc22-111">这是因为对等端组共享的对称令牌难以、也不适合用于进行源身份验证。</span><span class="sxs-lookup"><span data-stu-id="ebc22-111">This is because a symmetric token that a group of peers share is difficult and inappropriate to use for source authentication.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="ebc22-112">疑难解答</span><span class="sxs-lookup"><span data-stu-id="ebc22-112">Troubleshooting</span></span>  

 <span data-ttu-id="ebc22-113">确保所有邻居都具有适当的安全凭据。</span><span class="sxs-lookup"><span data-stu-id="ebc22-113">Ensure that all neighbors have the appropriate security credentials.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ebc22-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="ebc22-114">See also</span></span>

- [<span data-ttu-id="ebc22-115">对等通道安全性</span><span class="sxs-lookup"><span data-stu-id="ebc22-115">Peer Channel Security</span></span>](../../feature-details/peer-channel-security.md)
- [<span data-ttu-id="ebc22-116">跟踪</span><span class="sxs-lookup"><span data-stu-id="ebc22-116">Tracing</span></span>](index.md)
- [<span data-ttu-id="ebc22-117">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="ebc22-117">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="ebc22-118">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="ebc22-118">Administration and Diagnostics</span></span>](../index.md)
