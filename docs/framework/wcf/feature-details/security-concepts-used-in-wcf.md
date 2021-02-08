---
description: 了解详细信息： WCF 中使用的安全概念
title: WCF 中使用的安全概念
ms.date: 03/30/2017
ms.assetid: 3b9dfcf5-4bf1-4f35-9070-723171c823a1
ms.openlocfilehash: 5ad5b80c69e5dec5675879984fbcd2585b295dd4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99779759"
---
# <a name="security-concepts-used-in-wcf"></a><span data-ttu-id="c9452-103">WCF 中使用的安全概念</span><span class="sxs-lookup"><span data-stu-id="c9452-103">Security Concepts Used in WCF</span></span>

<span data-ttu-id="c9452-104">Windows Communication Foundation (WCF) 安全性是根据已在使用中并部署在各种安全基础结构中的概念构建的。</span><span class="sxs-lookup"><span data-stu-id="c9452-104">Windows Communication Foundation (WCF) security is built upon concepts already in use and deployed in various security infrastructures.</span></span>  
  
 <span data-ttu-id="c9452-105">WCF 支持其中一些基础结构，例如安全套接字层通过 HTTP (HTTPS)  (SSL) 。</span><span class="sxs-lookup"><span data-stu-id="c9452-105">WCF supports some of those infrastructures, such as Secure Sockets Layer (SSL) over HTTP (HTTPS).</span></span> <span data-ttu-id="c9452-106">不过，WCF 不支持现有的安全基础结构，方法是通过在 SOAP 编码的消息 (如 WS-MANAGEMENT) 来实现更新的可互操作安全标准。</span><span class="sxs-lookup"><span data-stu-id="c9452-106">However, WCF goes beyond supporting existing security infrastructures by implementing newer interoperable security standards (such as WS-Security) over SOAP-encoded messages.</span></span> <span data-ttu-id="c9452-107">无论是使用现有机制还是新的可互操作标准，其背后的安全概念都是相同的。</span><span class="sxs-lookup"><span data-stu-id="c9452-107">Whether you are using existing mechanisms or new interoperable standards, the security concepts behind both are the same.</span></span> <span data-ttu-id="c9452-108">理解现有基础结构以及较新的标准背后的概念对于为应用程序实现最佳安全模型至关重要。</span><span class="sxs-lookup"><span data-stu-id="c9452-108">Understanding the concepts behind existing infrastructures and the newer standards is central to implementing the best security model for an application.</span></span>  
  
## <a name="introduction-to-security-for-wcf-web-services"></a><span data-ttu-id="c9452-109">WCF Web 服务安全简介</span><span class="sxs-lookup"><span data-stu-id="c9452-109">Introduction to Security for WCF Web Services</span></span>  

<span data-ttu-id="c9452-110">Microsoft 模式和实践组编写了一篇称为 [WCF 安全指南](https://archive.codeplex.com/?p=wcfsecurityguide)的详细白皮书。</span><span class="sxs-lookup"><span data-stu-id="c9452-110">The Microsoft Patterns and Practices group wrote an in-depth white paper called [WCF Security Guide](https://archive.codeplex.com/?p=wcfsecurityguide).</span></span> <span data-ttu-id="c9452-111">本白皮书介绍了与 web 服务、关键的 WCF 安全概念、intranet 应用程序方案和 internet 应用程序方案相关的基本安全概念。</span><span class="sxs-lookup"><span data-stu-id="c9452-111">This white paper describes the fundamental security concepts as they relate to web services, key WCF security concepts, intranet application scenarios, and internet application scenarios.</span></span>  
  
## <a name="industry-wide-security-specifications"></a><span data-ttu-id="c9452-112">业界级安全规范</span><span class="sxs-lookup"><span data-stu-id="c9452-112">Industry-Wide Security Specifications</span></span>  
  
### <a name="public-key-infrastructure"></a><span data-ttu-id="c9452-113">公钥基础结构</span><span class="sxs-lookup"><span data-stu-id="c9452-113">Public Key Infrastructure</span></span>  

<span data-ttu-id="c9452-114">公钥基础结构 (PKI) 是数字证书、证书颁发机构以及其他注册机构的系统，通过使用公钥加密对电子事务中涉及的每个参与方进行验证和身份验证。</span><span class="sxs-lookup"><span data-stu-id="c9452-114">Public Key Infrastructure (PKI) is a system of digital certificates, certification authorities, and other registration authorities that verify and authenticate each party involved in an electronic transaction through the use of public-key cryptography.</span></span>
  
### <a name="kerberos-protocol"></a><span data-ttu-id="c9452-115">Kerberos 协议</span><span class="sxs-lookup"><span data-stu-id="c9452-115">Kerberos Protocol</span></span>  

 <span data-ttu-id="c9452-116">*Kerberos 协议* 是一种用于创建在 Windows 域上对用户进行身份验证的安全机制的规范。</span><span class="sxs-lookup"><span data-stu-id="c9452-116">The *Kerberos protocol* is a specification for creating a security mechanism that authenticates users on a Windows domain.</span></span> <span data-ttu-id="c9452-117">它允许用户建立针对域中的其他实体的安全上下文。</span><span class="sxs-lookup"><span data-stu-id="c9452-117">It allows a user to establish a secure context with other entities within a domain.</span></span> <span data-ttu-id="c9452-118">Windows 2000 及版本更高的平台默认情况下使用 Kerberos 协议。</span><span class="sxs-lookup"><span data-stu-id="c9452-118">Windows 2000 and later platforms use the Kerberos protocol by default.</span></span> <span data-ttu-id="c9452-119">在创建将与 intranet 客户端进行交互的服务时，理解系统的机制非常有用。</span><span class="sxs-lookup"><span data-stu-id="c9452-119">Understanding the mechanisms of the system is useful when creating a service that will interact with intranet clients.</span></span> <span data-ttu-id="c9452-120">此外，由于 *Web Services 安全性 Kerberos 绑定* 已广泛发布，因此可以使用 kerberos 协议与 Internet 客户端通信， (也就是说，kerberos 协议可在) 互操作。</span><span class="sxs-lookup"><span data-stu-id="c9452-120">In addition, since the *Web Services Security Kerberos Binding* is widely published, you can use the Kerberos protocol to communicate with Internet clients (that is, the Kerberos protocol is interoperable).</span></span> <span data-ttu-id="c9452-121">有关如何在 Windows 中实现 Kerberos 协议的详细信息，请参阅  [Microsoft kerberos](/windows/win32/secauthn/microsoft-kerberos)。</span><span class="sxs-lookup"><span data-stu-id="c9452-121">For more information about how the Kerberos protocol is implemented in Windows, see  [Microsoft Kerberos](/windows/win32/secauthn/microsoft-kerberos).</span></span>  
  
### <a name="x509-certificates"></a><span data-ttu-id="c9452-122">X.509 证书</span><span class="sxs-lookup"><span data-stu-id="c9452-122">X.509 Certificates</span></span>  

 <span data-ttu-id="c9452-123">X.509 证书是安全应用程序中使用的主要凭据形式。</span><span class="sxs-lookup"><span data-stu-id="c9452-123">X.509 certificates are a primary credential form used in security applications.</span></span> <span data-ttu-id="c9452-124">有关 x.509 证书的详细信息，请参阅 [X.509 公钥证书](/windows/win32/seccertenroll/about-x-509-public-key-certificates)。</span><span class="sxs-lookup"><span data-stu-id="c9452-124">For more information on X.509 certificates see [X.509 Public Key Certificates](/windows/win32/seccertenroll/about-x-509-public-key-certificates).</span></span> <span data-ttu-id="c9452-125">X.509 证书存储在证书存储区中。</span><span class="sxs-lookup"><span data-stu-id="c9452-125">X.509 certificates are stored within a certificate store.</span></span> <span data-ttu-id="c9452-126">运行 Windows 的计算机有多种证书存储区，每一种都针对不同的用途。</span><span class="sxs-lookup"><span data-stu-id="c9452-126">A computer running Windows has several kinds of certificate stores, each with a different purpose.</span></span> <span data-ttu-id="c9452-127">有关不同存储的详细信息，请参阅 [证书存储](/previous-versions/windows/it-pro/windows-server-2003/cc757138(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="c9452-127">For more information about the different stores, see [Certificate Stores](/previous-versions/windows/it-pro/windows-server-2003/cc757138(v=ws.10)).</span></span>  
  
## <a name="web-services-security-specifications"></a><span data-ttu-id="c9452-128">Web 服务安全规范</span><span class="sxs-lookup"><span data-stu-id="c9452-128">Web Services Security Specifications</span></span>  

 <span data-ttu-id="c9452-129">系统定义的绑定支持许多常用 Web 服务安全规范。</span><span class="sxs-lookup"><span data-stu-id="c9452-129">The system-defined bindings support many commonly used web services security specifications.</span></span> <span data-ttu-id="c9452-130">有关系统提供的绑定和它们支持的 web 服务规范的完整列表，请参阅： [System-Provided 互操作性绑定支持的 Web 服务协议](web-services-protocols-supported-by-system-provided-interoperability-bindings.md)</span><span class="sxs-lookup"><span data-stu-id="c9452-130">For a complete list of system-provided bindings and the web services specifications they support see: [Web Services Protocols Supported by System-Provided Interoperability Bindings](web-services-protocols-supported-by-system-provided-interoperability-bindings.md)</span></span>  
  
## <a name="access-control-mechanisms"></a><span data-ttu-id="c9452-131">访问控制机制</span><span class="sxs-lookup"><span data-stu-id="c9452-131">Access Control Mechanisms</span></span>  

 <span data-ttu-id="c9452-132">WCF 提供了多种服务或操作的访问控制方式。</span><span class="sxs-lookup"><span data-stu-id="c9452-132">WCF provides a number of ways to control access to a service or operation.</span></span> <span data-ttu-id="c9452-133">其中包括：</span><span class="sxs-lookup"><span data-stu-id="c9452-133">Among them are</span></span>  
  
1. <xref:System.Security.Permissions.PrincipalPermissionAttribute>  
  
2. <span data-ttu-id="c9452-134">ASP.NET 成员身份提供程序</span><span class="sxs-lookup"><span data-stu-id="c9452-134">ASP.NET Membership Provider</span></span>  
  
3. <span data-ttu-id="c9452-135">ASP.NET 角色提供程序</span><span class="sxs-lookup"><span data-stu-id="c9452-135">ASP.NET Role Provider</span></span>  
  
4. <span data-ttu-id="c9452-136">授权管理器</span><span class="sxs-lookup"><span data-stu-id="c9452-136">Authorization Manager</span></span>  
  
5. <span data-ttu-id="c9452-137">标识模型</span><span class="sxs-lookup"><span data-stu-id="c9452-137">Identity Model</span></span>  
  
 <span data-ttu-id="c9452-138">有关这些主题的详细信息，请参阅 [访问控制机制](access-control-mechanisms.md)</span><span class="sxs-lookup"><span data-stu-id="c9452-138">For more information on these topics see, [Access Control Mechanisms](access-control-mechanisms.md)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c9452-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="c9452-139">See also</span></span>

- [<span data-ttu-id="c9452-140">安全性概述</span><span class="sxs-lookup"><span data-stu-id="c9452-140">Security Overview</span></span>](security-overview.md)
- <span data-ttu-id="c9452-141">[Windows Server App Fabric 的安全模型](/previous-versions/appfabric/ee677202(v=azure.10))</span><span class="sxs-lookup"><span data-stu-id="c9452-141">[Security Model for Windows Server App Fabric](/previous-versions/appfabric/ee677202(v=azure.10))</span></span>
