---
description: 了解更多：常见安全方案
title: 常用安全方案
ms.date: 03/30/2017
helpviewer_keywords:
- security [WCF], scenarios
ms.assetid: 201923b5-5162-4a8a-8d4c-e7bd242748d5
ms.openlocfilehash: ad4e3964a4a018793653b5eb48b91ca566840abb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99743507"
---
# <a name="common-security-scenarios"></a><span data-ttu-id="96bbb-103">常用安全方案</span><span class="sxs-lookup"><span data-stu-id="96bbb-103">Common Security Scenarios</span></span>

<span data-ttu-id="96bbb-104">本节中的主题对众多可能的客户端和服务安全配置进行分类。</span><span class="sxs-lookup"><span data-stu-id="96bbb-104">The topics in this section catalog a number of possible client and service security configurations.</span></span> <span data-ttu-id="96bbb-105">配置会随多种因素而变化。</span><span class="sxs-lookup"><span data-stu-id="96bbb-105">Configurations vary according to a number of factors.</span></span> <span data-ttu-id="96bbb-106">例如，服务或客户端是否位于 Intranet 上，或者安全性是由 Windows 提供还是由传输（如 HTTPS）提供。</span><span class="sxs-lookup"><span data-stu-id="96bbb-106">For example, whether a service or client is on an intranet, or whether the security is provided by Windows or transport (such as HTTPS).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="96bbb-107">本节内容</span><span class="sxs-lookup"><span data-stu-id="96bbb-107">In This Section</span></span>  

 [<span data-ttu-id="96bbb-108">不安全的 Internet 客户端和服务</span><span class="sxs-lookup"><span data-stu-id="96bbb-108">Internet Unsecured Client and Service</span></span>](internet-unsecured-client-and-service.md)  
 <span data-ttu-id="96bbb-109">一个公共的、不安全的客户端和服务的示例。</span><span class="sxs-lookup"><span data-stu-id="96bbb-109">An example of a public, unsecured client and service.</span></span>  
  
 [<span data-ttu-id="96bbb-110">不安全的 Intranet 客户端和服务</span><span class="sxs-lookup"><span data-stu-id="96bbb-110">Intranet Unsecured Client and Service</span></span>](intranet-unsecured-client-and-service.md)  
 <span data-ttu-id="96bbb-111">基本 Windows Communication Foundation (WCF) 服务，旨在为 WCF 应用程序提供有关安全的专用网络的信息。</span><span class="sxs-lookup"><span data-stu-id="96bbb-111">A basic Windows Communication Foundation (WCF) service developed to provide information on a secure private network to a WCF application.</span></span>  
  
 [<span data-ttu-id="96bbb-112">通过基本身份验证确保的传输安全</span><span class="sxs-lookup"><span data-stu-id="96bbb-112">Transport Security with Basic Authentication</span></span>](transport-security-with-basic-authentication.md)  
 <span data-ttu-id="96bbb-113">应用程序允许客户端使用自定义身份验证进行登录。</span><span class="sxs-lookup"><span data-stu-id="96bbb-113">The application allows clients to log on using custom authentication.</span></span>  
  
 [<span data-ttu-id="96bbb-114">通过 Windows 身份验证确保的传输安全</span><span class="sxs-lookup"><span data-stu-id="96bbb-114">Transport Security with Windows Authentication</span></span>](transport-security-with-windows-authentication.md)  
 <span data-ttu-id="96bbb-115">显示由 Windows 安全保护的客户端和服务。</span><span class="sxs-lookup"><span data-stu-id="96bbb-115">Shows a client and service secured by Windows security.</span></span>  
  
 [<span data-ttu-id="96bbb-116">匿名客户端的传输安全性</span><span class="sxs-lookup"><span data-stu-id="96bbb-116">Transport Security with an Anonymous Client</span></span>](transport-security-with-an-anonymous-client.md)  
 <span data-ttu-id="96bbb-117">此方案使用传输安全（如 HTTPS）确保保密性和完整性。</span><span class="sxs-lookup"><span data-stu-id="96bbb-117">This scenario uses transport security (such as HTTPS) to ensure confidentiality and integrity.</span></span>  
  
 [<span data-ttu-id="96bbb-118">利用证书身份验证的传输安全</span><span class="sxs-lookup"><span data-stu-id="96bbb-118">Transport Security with Certificate Authentication</span></span>](transport-security-with-certificate-authentication.md)  
 <span data-ttu-id="96bbb-119">显示由证书保护的客户端和服务。</span><span class="sxs-lookup"><span data-stu-id="96bbb-119">Shows a client and service secured by a certificate.</span></span>  
  
 [<span data-ttu-id="96bbb-120">匿名客户端的消息安全</span><span class="sxs-lookup"><span data-stu-id="96bbb-120">Message Security with an Anonymous Client</span></span>](message-security-with-an-anonymous-client.md)  
 <span data-ttu-id="96bbb-121">显示由 WCF 消息安全保护的客户端和服务。</span><span class="sxs-lookup"><span data-stu-id="96bbb-121">Shows a client and service secured by WCF message security.</span></span>  
  
 [<span data-ttu-id="96bbb-122">用户名客户端的消息安全</span><span class="sxs-lookup"><span data-stu-id="96bbb-122">Message Security with a User Name Client</span></span>](message-security-with-a-user-name-client.md)  
 <span data-ttu-id="96bbb-123">客户端是一个 Windows 窗体应用程序，允许客户端使用域用户名和密码登录。</span><span class="sxs-lookup"><span data-stu-id="96bbb-123">The client is a Windows Forms application that allows clients to log on using a domain user name and password.</span></span>  
  
 [<span data-ttu-id="96bbb-124">使用证书客户端的消息安全</span><span class="sxs-lookup"><span data-stu-id="96bbb-124">Message Security with a Certificate Client</span></span>](message-security-with-a-certificate-client.md)  
 <span data-ttu-id="96bbb-125">服务器有多个证书，每个客户端各有一个证书。</span><span class="sxs-lookup"><span data-stu-id="96bbb-125">Servers have certificates, and each client has a certificate.</span></span> <span data-ttu-id="96bbb-126">通过传输层安全 (TLS) 协商建立安全上下文。</span><span class="sxs-lookup"><span data-stu-id="96bbb-126">A security context is established through Transport Layer Security (TLS) negotiation.</span></span>  
  
 [<span data-ttu-id="96bbb-127">Windows 客户端的消息安全</span><span class="sxs-lookup"><span data-stu-id="96bbb-127">Message Security with a Windows Client</span></span>](message-security-with-a-windows-client.md)  
 <span data-ttu-id="96bbb-128">证书客户端的变体。</span><span class="sxs-lookup"><span data-stu-id="96bbb-128">A variation of the certificate client.</span></span> <span data-ttu-id="96bbb-129">服务器有多个证书，每个客户端各有一个证书。</span><span class="sxs-lookup"><span data-stu-id="96bbb-129">Servers have certificates, and each client has a certificate.</span></span> <span data-ttu-id="96bbb-130">通过 TLS 协商建立安全上下文。</span><span class="sxs-lookup"><span data-stu-id="96bbb-130">A security context is established through TLS negotiation.</span></span>  
  
 [<span data-ttu-id="96bbb-131">没有凭据协商的 Windows 客户端的消息安全</span><span class="sxs-lookup"><span data-stu-id="96bbb-131">Message Security with a Windows Client without Credential Negotiation</span></span>](message-security-with-a-windows-client-without-credential-negotiation.md)  
 <span data-ttu-id="96bbb-132">显示由 Kerberos 域保护的客户端和服务。</span><span class="sxs-lookup"><span data-stu-id="96bbb-132">Shows a client and service secured by a Kerberos domain.</span></span>  
  
 [<span data-ttu-id="96bbb-133">使用相互证书的消息安全</span><span class="sxs-lookup"><span data-stu-id="96bbb-133">Message Security with Mutual Certificates</span></span>](message-security-with-mutual-certificates.md)  
 <span data-ttu-id="96bbb-134">服务器有多个证书，每个客户端各有一个证书。</span><span class="sxs-lookup"><span data-stu-id="96bbb-134">Servers have certificates, and each client has a certificate.</span></span> <span data-ttu-id="96bbb-135">服务器证书随应用程序一起分发，而可在带外使用。</span><span class="sxs-lookup"><span data-stu-id="96bbb-135">The server certificate is distributed with the application and is available out of band.</span></span>  
  
 [<span data-ttu-id="96bbb-136">使用已颁发令牌的消息安全</span><span class="sxs-lookup"><span data-stu-id="96bbb-136">Message Security with Issued Tokens</span></span>](message-security-with-issued-tokens.md)  
 <span data-ttu-id="96bbb-137">允许在独立域间建立信任的联合安全。</span><span class="sxs-lookup"><span data-stu-id="96bbb-137">Federated security that enables the establishment of trust between independent domains.</span></span>  
  
 [<span data-ttu-id="96bbb-138">受信任的子系统</span><span class="sxs-lookup"><span data-stu-id="96bbb-138">Trusted Subsystem</span></span>](trusted-subsystem.md)  
 <span data-ttu-id="96bbb-139">客户端访问分布在网络上的一个或多个 Web 服务。</span><span class="sxs-lookup"><span data-stu-id="96bbb-139">A client accesses one or more Web services that are distributed across a network.</span></span> <span data-ttu-id="96bbb-140">Web 服务访问必须加以保护的其他资源（如数据库或其他 Web 服务）。</span><span class="sxs-lookup"><span data-stu-id="96bbb-140">The Web services access additional resources (such as databases or other Web services) that must be secured.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="96bbb-141">参考</span><span class="sxs-lookup"><span data-stu-id="96bbb-141">Reference</span></span>  

 <xref:System.ServiceModel>  
  
## <a name="related-sections"></a><span data-ttu-id="96bbb-142">相关章节</span><span class="sxs-lookup"><span data-stu-id="96bbb-142">Related Sections</span></span>  

 [<span data-ttu-id="96bbb-143">授权</span><span class="sxs-lookup"><span data-stu-id="96bbb-143">Authorization</span></span>](authorization-in-wcf.md)  
  
 [<span data-ttu-id="96bbb-144">安全性概述</span><span class="sxs-lookup"><span data-stu-id="96bbb-144">Security Overview</span></span>](security-overview.md)  
  
 [<span data-ttu-id="96bbb-145">安全性</span><span class="sxs-lookup"><span data-stu-id="96bbb-145">Security</span></span>](security.md)  
  
 [<span data-ttu-id="96bbb-146">绑定与安全</span><span class="sxs-lookup"><span data-stu-id="96bbb-146">Bindings and Security</span></span>](bindings-and-security.md)  
  
 [<span data-ttu-id="96bbb-147">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="96bbb-147">Securing Services and Clients</span></span>](securing-services-and-clients.md)  
  
 [<span data-ttu-id="96bbb-148">身份验证</span><span class="sxs-lookup"><span data-stu-id="96bbb-148">Authentication</span></span>](authentication-in-wcf.md)  
  
 [<span data-ttu-id="96bbb-149">授权</span><span class="sxs-lookup"><span data-stu-id="96bbb-149">Authorization</span></span>](authorization-in-wcf.md)  
  
 [<span data-ttu-id="96bbb-150">联合令牌与颁发的令牌</span><span class="sxs-lookup"><span data-stu-id="96bbb-150">Federation and Issued Tokens</span></span>](federation-and-issued-tokens.md)  
  
 [<span data-ttu-id="96bbb-151">审核</span><span class="sxs-lookup"><span data-stu-id="96bbb-151">Auditing</span></span>](auditing-security-events.md)  
  
## <a name="see-also"></a><span data-ttu-id="96bbb-152">请参阅</span><span class="sxs-lookup"><span data-stu-id="96bbb-152">See also</span></span>

- [<span data-ttu-id="96bbb-153">安全指导和最佳做法</span><span class="sxs-lookup"><span data-stu-id="96bbb-153">Security Guidance and Best Practices</span></span>](security-guidance-and-best-practices.md)
- <span data-ttu-id="96bbb-154">[Windows Server App Fabric 的安全模型](/previous-versions/appfabric/ee677202(v=azure.10))</span><span class="sxs-lookup"><span data-stu-id="96bbb-154">[Security Model for Windows Server App Fabric](/previous-versions/appfabric/ee677202(v=azure.10))</span></span>
