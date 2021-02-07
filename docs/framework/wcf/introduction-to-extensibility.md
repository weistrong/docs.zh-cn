---
description: 了解详细信息：扩展性简介
title: 扩展性介绍
ms.date: 03/30/2017
helpviewer_keywords:
- WCF [WCF], extensibility
- Windows Communication Foundation [WCF], extensibility
- extensibility [WCF]
ms.assetid: ef56c251-d63c-4b3f-944f-b0c67bfb0f68
ms.openlocfilehash: a3e614d107d2371076358f8e7786c1bb246e36eb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99732834"
---
# <a name="introduction-to-extensibility"></a><span data-ttu-id="f3870-103">扩展性介绍</span><span class="sxs-lookup"><span data-stu-id="f3870-103">Introduction to Extensibility</span></span>

<span data-ttu-id="f3870-104">Windows Communication Foundation (WCF) 应用程序模型设计用于解决任何分布式应用程序的通信要求的更大一部分。</span><span class="sxs-lookup"><span data-stu-id="f3870-104">The Windows Communication Foundation (WCF) application model is designed to solve the greater part of the communication requirements of any distributed application.</span></span> <span data-ttu-id="f3870-105">但是，总是会存在一些默认应用程序模型和系统提供的实现不支持的情况。</span><span class="sxs-lookup"><span data-stu-id="f3870-105">But there are always scenarios that the default application model and system-provided implementations do not support.</span></span> <span data-ttu-id="f3870-106">WCF 扩展性模型旨在支持自定义方案，使您可以在每个级别修改系统行为，甚至替换整个应用程序模型。</span><span class="sxs-lookup"><span data-stu-id="f3870-106">The WCF extensibility model is intended to support custom scenarios by enabling you to modify system behavior at every level, even to the point of replacing the entire application model.</span></span> <span data-ttu-id="f3870-107">本主题概述各个扩展范围并指出关于每个范围的更多信息。</span><span class="sxs-lookup"><span data-stu-id="f3870-107">This topic outlines the various areas of extension and points to more information about each.</span></span>  
  
## <a name="areas-to-extend"></a><span data-ttu-id="f3870-108">要扩展的范围</span><span class="sxs-lookup"><span data-stu-id="f3870-108">Areas to Extend</span></span>  

 <span data-ttu-id="f3870-109">可以扩展：</span><span class="sxs-lookup"><span data-stu-id="f3870-109">You can extend:</span></span>  
  
- <span data-ttu-id="f3870-110">应用程序运行库。</span><span class="sxs-lookup"><span data-stu-id="f3870-110">The application runtime.</span></span> <span data-ttu-id="f3870-111">这将扩展应用程序消息的调度和处理。</span><span class="sxs-lookup"><span data-stu-id="f3870-111">This extends the dispatching and the processing of messages for the application.</span></span> <span data-ttu-id="f3870-112">此范围还包括扩展安全系统、元数据系统、序列化系统以及将应用程序与基础通道系统相连的绑定和绑定元素。</span><span class="sxs-lookup"><span data-stu-id="f3870-112">This area also includes extending the security system, the metadata system, the serialization system, and the bindings and binding elements that connect the application with the underlying channel system.</span></span>  
  
- <span data-ttu-id="f3870-113">通道和通道运行库。</span><span class="sxs-lookup"><span data-stu-id="f3870-113">The channel and channel runtime.</span></span> <span data-ttu-id="f3870-114">这将扩展在消息级别运行的系统，用于提供协议、传输和编码支持。</span><span class="sxs-lookup"><span data-stu-id="f3870-114">This extends the system that functions at the message level, providing protocol, transport, and encoding support.</span></span>  
  
- <span data-ttu-id="f3870-115">主机运行库。</span><span class="sxs-lookup"><span data-stu-id="f3870-115">The host runtime.</span></span> <span data-ttu-id="f3870-116">此范围将主机应用程序域的关系扩展到通道和应用程序运行库。</span><span class="sxs-lookup"><span data-stu-id="f3870-116">This extends the relationship of the hosting application domain to the channel and application runtime.</span></span>  
  
### <a name="extending-the-application-runtime"></a><span data-ttu-id="f3870-117">扩展应用程序运行库</span><span class="sxs-lookup"><span data-stu-id="f3870-117">Extending the Application Runtime</span></span>  

 <span data-ttu-id="f3870-118">在 WCF 应用程序中，对于发送到相应通道的消息和发往应用程序本身的消息，会有区别。</span><span class="sxs-lookup"><span data-stu-id="f3870-118">In WCF applications, there is a distinction between messages that are destined for a corresponding channel and messages that are destined for the application itself.</span></span> <span data-ttu-id="f3870-119">通道消息支持某些与通道相关的功能，如建立安全对话或可靠会话。</span><span class="sxs-lookup"><span data-stu-id="f3870-119">Channel messages support some channel-related functionality, such as establishing a secure conversation or establishing a reliable session.</span></span> <span data-ttu-id="f3870-120">这些消息对于应用程序运行库不可用；涉及应用程序层之前，将处理这些消息。</span><span class="sxs-lookup"><span data-stu-id="f3870-120">These messages are not available to the application runtime; they are processed before the application layer is involved.</span></span>  
  
 <span data-ttu-id="f3870-121">应用程序消息中包含发往客户端或发往您或您的客户创建的服务操作的数据。</span><span class="sxs-lookup"><span data-stu-id="f3870-121">Application messages contain data that is destined for a client or service operation that you or your customer has created.</span></span> <span data-ttu-id="f3870-122">这些消息可用于采用消息或对象形式的应用程序级扩展系统，具体取决于您的需要。</span><span class="sxs-lookup"><span data-stu-id="f3870-122">These messages are available to the application-level extension system in message or object form, depending upon your needs.</span></span>  
  
 <span data-ttu-id="f3870-123">所有消息都通过通道系统传递；只有应用程序消息是从通道系统传入应用程序的。</span><span class="sxs-lookup"><span data-stu-id="f3870-123">All messages pass through the channel system; only application messages are passed from the channel system into the application.</span></span> <span data-ttu-id="f3870-124">若要创建新的通道级功能，必须扩展通道系统。</span><span class="sxs-lookup"><span data-stu-id="f3870-124">To create new channel-level functionality, you must extend the channel system.</span></span> <span data-ttu-id="f3870-125">若要创建新的应用程序级功能，必须扩展服务或客户端运行库（分别为调度程序和通道工厂）。</span><span class="sxs-lookup"><span data-stu-id="f3870-125">To create new application-level functionality, you must extend the service or client runtime (dispatchers and channel factories, respectively).</span></span> <span data-ttu-id="f3870-126">有关扩展应用程序运行时的详细信息，请参阅 [扩展 ServiceHost 和服务模型层](./extending/extending-servicehost-and-the-service-model-layer.md)。</span><span class="sxs-lookup"><span data-stu-id="f3870-126">For more information about extending the application runtime, see [Extending ServiceHost and the Service Model Layer](./extending/extending-servicehost-and-the-service-model-layer.md).</span></span>  
  
#### <a name="extending-security"></a><span data-ttu-id="f3870-127">扩展安全性</span><span class="sxs-lookup"><span data-stu-id="f3870-127">Extending Security</span></span>  

 <span data-ttu-id="f3870-128">若要生成自定义安全机制（如令牌和凭据），必须扩展安全系统。</span><span class="sxs-lookup"><span data-stu-id="f3870-128">To build custom security mechanisms such as tokens and credentials, you must extend the security system.</span></span> <span data-ttu-id="f3870-129">有关详细信息，请参阅 [扩展安全性](./extending/extending-security.md)。</span><span class="sxs-lookup"><span data-stu-id="f3870-129">For more information, see [Extending Security](./extending/extending-security.md).</span></span>  
  
#### <a name="extending-metadata"></a><span data-ttu-id="f3870-130">扩展元数据</span><span class="sxs-lookup"><span data-stu-id="f3870-130">Extending Metadata</span></span>  

 <span data-ttu-id="f3870-131">若要以非默认方式公开元数据，必须扩展元数据系统。</span><span class="sxs-lookup"><span data-stu-id="f3870-131">To expose your metadata in differently than the default, you must extend the metadata system.</span></span> <span data-ttu-id="f3870-132">有关详细信息，请参阅 [扩展元数据系统](./extending/extending-the-metadata-system.md)。</span><span class="sxs-lookup"><span data-stu-id="f3870-132">For more information, see [Extending the Metadata System](./extending/extending-the-metadata-system.md).</span></span>  
  
#### <a name="extending-serialization"></a><span data-ttu-id="f3870-133">扩展序列化</span><span class="sxs-lookup"><span data-stu-id="f3870-133">Extending Serialization</span></span>  

 <span data-ttu-id="f3870-134">若要生成自定义编码器、提供数据代理项或涉及自定义传输数据的其他工作，必须扩展序列化系统。</span><span class="sxs-lookup"><span data-stu-id="f3870-134">To build custom encoders, provide data surrogates, or other work involving the customization of transferred data, you must extend the serialization system.</span></span> <span data-ttu-id="f3870-135">有关详细信息，请参阅 [扩展编码器和序列化](./extending/extending-encoders-and-serializers.md)程序。</span><span class="sxs-lookup"><span data-stu-id="f3870-135">For more information, see [Extending Encoders and Serializers](./extending/extending-encoders-and-serializers.md).</span></span>  
  
#### <a name="extending-bindings"></a><span data-ttu-id="f3870-136">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="f3870-136">Extending Bindings</span></span>  

 <span data-ttu-id="f3870-137">若要将传输通道或协议通道与应用程序层关联，必须扩展绑定系统。</span><span class="sxs-lookup"><span data-stu-id="f3870-137">To associate transport or protocol channels with the application layer, you must extend the binding system.</span></span> <span data-ttu-id="f3870-138">有关详细信息，请参阅 [扩展绑定](./extending/extending-bindings.md)。</span><span class="sxs-lookup"><span data-stu-id="f3870-138">For more information, see [Extending Bindings](./extending/extending-bindings.md).</span></span>  
  
### <a name="extending-the-channel-system"></a><span data-ttu-id="f3870-139">扩展通道系统</span><span class="sxs-lookup"><span data-stu-id="f3870-139">Extending the Channel System</span></span>  

 <span data-ttu-id="f3870-140">若要创建支持自定义传输或协议功能的通道，请参阅 [扩展通道层](./extending/extending-the-channel-layer.md)。</span><span class="sxs-lookup"><span data-stu-id="f3870-140">To create channels that support custom transports or protocol functionality, see [Extending the Channel Layer](./extending/extending-the-channel-layer.md).</span></span>  
  
### <a name="extending-the-service-hosting-system"></a><span data-ttu-id="f3870-141">扩展服务主机系统</span><span class="sxs-lookup"><span data-stu-id="f3870-141">Extending the Service Hosting System</span></span>  

 <span data-ttu-id="f3870-142">若要修改服务范围的应用程序模型，必须扩展 <xref:System.ServiceModel.ServiceHostBase?displayProperty=nameWithType> 类。</span><span class="sxs-lookup"><span data-stu-id="f3870-142">To modify the service-wide application model, you must extend <xref:System.ServiceModel.ServiceHostBase?displayProperty=nameWithType> class.</span></span> <span data-ttu-id="f3870-143">有关详细信息，请参阅 [扩展 ServiceHost 和服务模型层](./extending/extending-servicehost-and-the-service-model-layer.md)。</span><span class="sxs-lookup"><span data-stu-id="f3870-143">For more information, see [Extending ServiceHost and the Service Model Layer](./extending/extending-servicehost-and-the-service-model-layer.md).</span></span>  
  
 <span data-ttu-id="f3870-144">若要修改主机应用程序域和服务主机之间的关系，必须扩展 <xref:System.ServiceModel.Activation.ServiceHostFactory?displayProperty=nameWithType> 类。</span><span class="sxs-lookup"><span data-stu-id="f3870-144">To modify the relationship between the hosting application domain and the service host, you must extend the <xref:System.ServiceModel.Activation.ServiceHostFactory?displayProperty=nameWithType> class.</span></span> <span data-ttu-id="f3870-145">有关详细信息，请参阅 [使用 ServiceHostFactory 扩展托管](./extending/extending-hosting-using-servicehostfactory.md)。</span><span class="sxs-lookup"><span data-stu-id="f3870-145">For more information, see [Extending Hosting Using ServiceHostFactory](./extending/extending-hosting-using-servicehostfactory.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f3870-146">请参阅</span><span class="sxs-lookup"><span data-stu-id="f3870-146">See also</span></span>

- [<span data-ttu-id="f3870-147">扩展 WCF</span><span class="sxs-lookup"><span data-stu-id="f3870-147">Extending WCF</span></span>](./extending/index.md)
