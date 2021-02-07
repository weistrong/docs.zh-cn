---
description: 了解详细信息：配置 WCF 服务
title: 配置 WCF 服务
ms.date: 03/30/2017
helpviewer_keywords:
- configuration [WCF]
ms.assetid: beac771e-f28e-4f84-9ff1-ad9251c726d3
ms.openlocfilehash: 1c0df8c7d9b4e2b1a032f02e74db2de4a8de020c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99720834"
---
# <a name="configuring-wcf-services"></a><span data-ttu-id="c1d20-103">配置 WCF 服务</span><span class="sxs-lookup"><span data-stu-id="c1d20-103">Configuring WCF services</span></span>

<span data-ttu-id="c1d20-104">在设计和实现服务协定后，即可配置服务。</span><span class="sxs-lookup"><span data-stu-id="c1d20-104">Once you have designed and implemented your service contract, you are ready to configure your service.</span></span> <span data-ttu-id="c1d20-105">在其中可以定义和自定义如何向客户端公开服务，包括指定可以找到服务的地址、服务用于发送和接收消息的传输和消息编码，以及服务需要的安全类型。</span><span class="sxs-lookup"><span data-stu-id="c1d20-105">This is where you define and customize how your service is exposed to clients, including specifying the address where it can be found, the transport and message encoding it uses to send and receive messages, and the type of security it requires.</span></span>  
  
 <span data-ttu-id="c1d20-106">此处使用的配置包括在代码中以强制方式或通过使用配置文件定义和自定义服务的各个方面的所有方法，例如指定其终结点地址、使用的传输及其安全方案。</span><span class="sxs-lookup"><span data-stu-id="c1d20-106">Configuration as used here includes all the ways, imperatively in code or by using a configuration file, in which you can define and customize the various aspects of a service, such as specifying its endpoint addresses, the transports used, and its security schemes.</span></span> <span data-ttu-id="c1d20-107">实际上，编写配置是 WCF 应用程序编程的主要部分。</span><span class="sxs-lookup"><span data-stu-id="c1d20-107">In practice, writing configuration is a major part of programming WCF applications.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="c1d20-108">本节内容</span><span class="sxs-lookup"><span data-stu-id="c1d20-108">In This Section</span></span>  

 [<span data-ttu-id="c1d20-109">简化配置</span><span class="sxs-lookup"><span data-stu-id="c1d20-109">Simplified Configuration</span></span>](simplified-configuration.md)  
 <span data-ttu-id="c1d20-110">从 .NET Framework 4 开始，WCF 附带了新的默认配置模型，该模型可简化 WCF 配置要求。</span><span class="sxs-lookup"><span data-stu-id="c1d20-110">Starting with .NET Framework 4, WCF comes with a new default configuration model that simplifies WCF configuration requirements.</span></span> <span data-ttu-id="c1d20-111">如果没有为特定服务提供任何 WCF 配置，运行时将使用默认终结点、绑定和行为自动配置服务。</span><span class="sxs-lookup"><span data-stu-id="c1d20-111">If you do not provide any WCF configuration for a particular service, the runtime automatically configures your service with default endpoints, bindings, and behaviors.</span></span>  
  
 [<span data-ttu-id="c1d20-112">使用配置文件配置服务</span><span class="sxs-lookup"><span data-stu-id="c1d20-112">Configuring Services Using Configuration Files</span></span>](configuring-services-using-configuration-files.md)  
 <span data-ttu-id="c1d20-113">Windows Communication Foundation (WCF) 服务可使用 .NET Framework 配置技术进行配置。</span><span class="sxs-lookup"><span data-stu-id="c1d20-113">A Windows Communication Foundation (WCF) service is configurable using the .NET Framework configuration technology.</span></span> <span data-ttu-id="c1d20-114">最常见的情况是，XML 元素添加到承载 WCF 服务的 Internet Information Services (IIS) 站点的 Web.config 文件中。</span><span class="sxs-lookup"><span data-stu-id="c1d20-114">Most commonly, XML elements are added to the Web.config file for an Internet Information Services (IIS) site that hosts a WCF service.</span></span> <span data-ttu-id="c1d20-115">这些元素允许您更改详细信息，例如每台计算机上的终结点地址（用于与服务进行通信的实际地址）。</span><span class="sxs-lookup"><span data-stu-id="c1d20-115">The elements allow you to change details, such as the endpoint addresses (the actual addresses used to communicate with the service) on a machine-by-machine basis.</span></span>  
  
 [<span data-ttu-id="c1d20-116">绑定</span><span class="sxs-lookup"><span data-stu-id="c1d20-116">Bindings</span></span>](bindings.md)  
 <span data-ttu-id="c1d20-117">此外，WCF 还包括多个系统提供的常见配置，这些绑定可以让你快速选择有关客户端和服务的通信方式的最基本功能，如使用的传输、安全性和消息编码。</span><span class="sxs-lookup"><span data-stu-id="c1d20-117">In addition, WCF includes several system-provided common configurations in the form of bindings that allow you to quickly select the most basic features for how a client and service communicate, such as the transports, security, and message encodings used.</span></span>  
  
 [<span data-ttu-id="c1d20-118">Endpoints</span><span class="sxs-lookup"><span data-stu-id="c1d20-118">Endpoints</span></span>](endpoints.md)  
 <span data-ttu-id="c1d20-119">与 WCF 服务的所有通信都通过服务 *终结点* 进行。</span><span class="sxs-lookup"><span data-stu-id="c1d20-119">All communication with a WCF service occurs through the *endpoints* of the service.</span></span> <span data-ttu-id="c1d20-120">终结点包含协定、在绑定中指定的配置信息，以及指示查找服务或获取该服务相关信息的位置的地址。</span><span class="sxs-lookup"><span data-stu-id="c1d20-120">Endpoints contain the contract, the configuration information that is specified in the bindings, and the addresses that indicate where to find the service or where to obtain information about the service.</span></span>  
  
 [<span data-ttu-id="c1d20-121">保证服务的安全</span><span class="sxs-lookup"><span data-stu-id="c1d20-121">Securing Services</span></span>](securing-services.md)  
 <span data-ttu-id="c1d20-122">使用 WCF 和现有的安全机制，可以在任何服务中实现保密性、完整性、身份验证和授权。</span><span class="sxs-lookup"><span data-stu-id="c1d20-122">Using WCF and existing security mechanisms, you can implement confidentiality, integrity, authentication, and authorization into any service.</span></span> <span data-ttu-id="c1d20-123">还可以审核安全成功和安全失败。</span><span class="sxs-lookup"><span data-stu-id="c1d20-123">You can also audit for security successes and failures.</span></span>  
  
 [<span data-ttu-id="c1d20-124">创建 WS-I 基本配置文件 1.1 可互操作服务</span><span class="sxs-lookup"><span data-stu-id="c1d20-124">Creating WS-I Basic Profile 1.1 Interoperable Services</span></span>](./creating-ws-i-basic-profile-1-1-interoperable-services.md)  
 <span data-ttu-id="c1d20-125">WS-I 基本配置文件 1.1 规范中概述了部署服务的需求，该服务可与其他任何平台或操作系统上的服务和客户端进行互操作。</span><span class="sxs-lookup"><span data-stu-id="c1d20-125">The requirements for deploying a service that is interoperable with services and clients on any other platform or operating system are outlined in the WS-I Basic Profile 1.1 specification.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="c1d20-126">参考</span><span class="sxs-lookup"><span data-stu-id="c1d20-126">Reference</span></span>  

 <xref:System.ServiceModel>  
  
 <xref:System.ServiceModel.Channels>  
  
 <xref:System.ServiceModel.Description>  
  
## <a name="related-sections"></a><span data-ttu-id="c1d20-127">相关章节</span><span class="sxs-lookup"><span data-stu-id="c1d20-127">Related Sections</span></span>  

 [<span data-ttu-id="c1d20-128">基本编程生命周期</span><span class="sxs-lookup"><span data-stu-id="c1d20-128">Basic Programming Lifecycle</span></span>](basic-programming-lifecycle.md)  
  
 [<span data-ttu-id="c1d20-129">设计和实现服务</span><span class="sxs-lookup"><span data-stu-id="c1d20-129">Designing and Implementing Services</span></span>](designing-and-implementing-services.md)  
  
 [<span data-ttu-id="c1d20-130">承载服务</span><span class="sxs-lookup"><span data-stu-id="c1d20-130">Hosting Services</span></span>](hosting-services.md)  
  
 [<span data-ttu-id="c1d20-131">生成客户端</span><span class="sxs-lookup"><span data-stu-id="c1d20-131">Building Clients</span></span>](building-clients.md)  
  
 [<span data-ttu-id="c1d20-132">扩展性介绍</span><span class="sxs-lookup"><span data-stu-id="c1d20-132">Introduction to Extensibility</span></span>](introduction-to-extensibility.md)  
  
 [<span data-ttu-id="c1d20-133">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="c1d20-133">Administration and Diagnostics</span></span>](./diagnostics/index.md)  
  
## <a name="see-also"></a><span data-ttu-id="c1d20-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="c1d20-134">See also</span></span>

- [<span data-ttu-id="c1d20-135">基本 WCF 编程</span><span class="sxs-lookup"><span data-stu-id="c1d20-135">Basic WCF Programming</span></span>](basic-wcf-programming.md)
- [<span data-ttu-id="c1d20-136">概念性概述</span><span class="sxs-lookup"><span data-stu-id="c1d20-136">Conceptual Overview</span></span>](conceptual-overview.md)
- [<span data-ttu-id="c1d20-137">WCF 功能详细信息</span><span class="sxs-lookup"><span data-stu-id="c1d20-137">WCF Feature Details</span></span>](./feature-details/index.md)
