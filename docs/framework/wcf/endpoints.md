---
description: 了解详细信息： Windows Communication Foundation 终结点
title: Windows Communication Foundation 终结点
ms.date: 03/30/2017
helpviewer_keywords:
- endpoints [WCF]
ms.assetid: bd0c310f-dd9f-4081-9be2-3db5909850b6
ms.openlocfilehash: caa918f2dd7ca7b0289cc1faf6d189270596808b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99756768"
---
# <a name="windows-communication-foundation-endpoints"></a><span data-ttu-id="b1a01-103">Windows Communication Foundation 终结点</span><span class="sxs-lookup"><span data-stu-id="b1a01-103">Windows Communication Foundation Endpoints</span></span>

<span data-ttu-id="b1a01-104">与 Windows Communication Foundation (WCF) 服务的所有通信都通过服务 *终结点* 进行。</span><span class="sxs-lookup"><span data-stu-id="b1a01-104">All communication with a Windows Communication Foundation (WCF) service occurs through the *endpoints* of the service.</span></span> <span data-ttu-id="b1a01-105">终结点为客户端提供对 WCF 服务所提供的功能的访问权限。</span><span class="sxs-lookup"><span data-stu-id="b1a01-105">Endpoints provide clients access to the functionality that a WCF service offers.</span></span>  
  
 <span data-ttu-id="b1a01-106">有关如何创建终结点的概述，请参阅 [终结点创建概述](endpoint-creation-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="b1a01-106">For an overview about how to create an endpoint, see [Endpoint Creation Overview](endpoint-creation-overview.md).</span></span> <span data-ttu-id="b1a01-107">每个终结点包含：</span><span class="sxs-lookup"><span data-stu-id="b1a01-107">Each endpoint contains:</span></span>  
  
- <span data-ttu-id="b1a01-108">一个指示要查找终结点位置的地址。</span><span class="sxs-lookup"><span data-stu-id="b1a01-108">An address that indicates where to find the endpoint.</span></span>  
  
- <span data-ttu-id="b1a01-109">一个指定客户端如何与终结点进行通信的绑定。</span><span class="sxs-lookup"><span data-stu-id="b1a01-109">A binding that specifies how a client can communicate with the endpoint.</span></span>  
  
- <span data-ttu-id="b1a01-110">一个标识可用方法的协定。</span><span class="sxs-lookup"><span data-stu-id="b1a01-110">A contract that identifies the methods available.</span></span>  
  
 <span data-ttu-id="b1a01-111">有关如何指定终结点的上述各个部分的说明，请参见：</span><span class="sxs-lookup"><span data-stu-id="b1a01-111">For descriptions about how to specify these individual parts of an endpoint, see:</span></span>  
  
- [<span data-ttu-id="b1a01-112">指定终结点地址</span><span class="sxs-lookup"><span data-stu-id="b1a01-112">Specifying an Endpoint Address</span></span>](specifying-an-endpoint-address.md)  
  
- [<span data-ttu-id="b1a01-113">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="b1a01-113">Using Bindings to Configure Services and Clients</span></span>](using-bindings-to-configure-services-and-clients.md)  
  
- [<span data-ttu-id="b1a01-114">设计和实现服务</span><span class="sxs-lookup"><span data-stu-id="b1a01-114">Designing and Implementing Services</span></span>](designing-and-implementing-services.md)  
  
## <a name="in-this-section"></a><span data-ttu-id="b1a01-115">本节内容</span><span class="sxs-lookup"><span data-stu-id="b1a01-115">In This Section</span></span>  

 [<span data-ttu-id="b1a01-116">终结点创建概述</span><span class="sxs-lookup"><span data-stu-id="b1a01-116">Endpoint Creation Overview</span></span>](endpoint-creation-overview.md)  
 <span data-ttu-id="b1a01-117">描述终结点的结构，并概述如何在配置和代码中定义终结点，以及如何使用运行时提供的默认终结点、绑定和行为。</span><span class="sxs-lookup"><span data-stu-id="b1a01-117">Describes the structure of an endpoint and outlines how to define an endpoint in configuration and in code, as well as how to use the default endpoints, bindings, and behaviors provided by the runtime.</span></span>  
  
 [<span data-ttu-id="b1a01-118">指定终结点地址</span><span class="sxs-lookup"><span data-stu-id="b1a01-118">Specifying an Endpoint Address</span></span>](specifying-an-endpoint-address.md)  
 <span data-ttu-id="b1a01-119">介绍如何通过终结点与 WCF 服务进行通信。</span><span class="sxs-lookup"><span data-stu-id="b1a01-119">Describes how communication with a WCF service occurs through endpoints.</span></span>  
  
 [<span data-ttu-id="b1a01-120">如何：在配置中创建服务终结点</span><span class="sxs-lookup"><span data-stu-id="b1a01-120">How to: Create a Service Endpoint in Configuration</span></span>](./feature-details/how-to-create-a-service-endpoint-in-configuration.md)  
 <span data-ttu-id="b1a01-121">演示如何在配置中创建服务终结点。</span><span class="sxs-lookup"><span data-stu-id="b1a01-121">Demonstrates how to create a service endpoint in configuration.</span></span>  
  
 [<span data-ttu-id="b1a01-122">如何：在代码中创建服务终结点</span><span class="sxs-lookup"><span data-stu-id="b1a01-122">How to: Create a Service Endpoint in Code</span></span>](./feature-details/how-to-create-a-service-endpoint-in-code.md)  
 <span data-ttu-id="b1a01-123">演示如何在代码中创建服务终结点。</span><span class="sxs-lookup"><span data-stu-id="b1a01-123">Demonstrates how to create a service endpoint in code.</span></span>  
  
 [<span data-ttu-id="b1a01-124">发布元数据终结点</span><span class="sxs-lookup"><span data-stu-id="b1a01-124">Publishing Metadata Endpoints</span></span>](publishing-metadata-endpoints.md)  
 <span data-ttu-id="b1a01-125">演示如何通过在配置和代码中发布元数据终结点来发布元数据。</span><span class="sxs-lookup"><span data-stu-id="b1a01-125">Demonstrates how to publish metadata by publishing metadata endpoints in configuration and in code.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="b1a01-126">参考</span><span class="sxs-lookup"><span data-stu-id="b1a01-126">Reference</span></span>  

 <xref:System.ServiceModel.EndpointAddress>  
  
## <a name="related-sections"></a><span data-ttu-id="b1a01-127">相关章节</span><span class="sxs-lookup"><span data-stu-id="b1a01-127">Related Sections</span></span>  

 [<span data-ttu-id="b1a01-128">基本编程生命周期</span><span class="sxs-lookup"><span data-stu-id="b1a01-128">Basic Programming Lifecycle</span></span>](basic-programming-lifecycle.md)
