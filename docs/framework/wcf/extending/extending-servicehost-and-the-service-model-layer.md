---
description: 了解详细信息：扩展 ServiceHost 和服务模型层
title: 扩展 ServiceHost 和服务模块层
ms.date: 03/30/2017
helpviewer_keywords:
- extending service models [WCF]
ms.assetid: 954c138a-1cd0-45a0-8abe-e4d2b8ff5400
ms.openlocfilehash: 446c02fbbb2391a4cc9c08c9e42f2194dfbcf9b9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99735057"
---
# <a name="extending-servicehost-and-the-service-model-layer"></a><span data-ttu-id="0b68f-103">扩展 ServiceHost 和服务模块层</span><span class="sxs-lookup"><span data-stu-id="0b68f-103">Extending ServiceHost and the Service Model Layer</span></span>

<span data-ttu-id="0b68f-104">服务模型层负责从基础通道提取出传入的消息，将它们翻译成应用程序代码形式的方法调用，并将结果发送回调用方。</span><span class="sxs-lookup"><span data-stu-id="0b68f-104">The service model layer is responsible for pulling incoming messages out of the underlying channels, translating them into method invocations in application code, and sending the results back to the caller.</span></span> <span data-ttu-id="0b68f-105">服务模型扩展将修改或实现执行或通信行为与功能，包括客户端或调度程序功能、自定义行为、消息和参数截获以及其他扩展功能。</span><span class="sxs-lookup"><span data-stu-id="0b68f-105">Service model extensions modify or implement execution or communication behavior and features involving client or dispatcher functionality, custom behaviors, message and parameter interception, and other extensibility functionality.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="0b68f-106">本节内容</span><span class="sxs-lookup"><span data-stu-id="0b68f-106">In This Section</span></span>  

 [<span data-ttu-id="0b68f-107">扩展客户端</span><span class="sxs-lookup"><span data-stu-id="0b68f-107">Extending Clients</span></span>](extending-clients.md)  
 <span data-ttu-id="0b68f-108">描述可以截获和修改客户端运行时的接口以及可以向其中插入客户端应用程序中的自定义扩展的类。</span><span class="sxs-lookup"><span data-stu-id="0b68f-108">Describes the interfaces that can intercept and modify the client runtime, as well as the classes into which you can insert your custom extensions in client applications.</span></span> <span data-ttu-id="0b68f-109">例如，您可以执行自定义客户端消息记录，执行自定义消息序列化，等等。</span><span class="sxs-lookup"><span data-stu-id="0b68f-109">For example, you can perform custom client message logging, perform custom message serialization, and so on.</span></span>  
  
 [<span data-ttu-id="0b68f-110">扩展调度程序</span><span class="sxs-lookup"><span data-stu-id="0b68f-110">Extending Dispatchers</span></span>](extending-dispatchers.md)  
 <span data-ttu-id="0b68f-111">描述可以截获和修改服务运行时的接口以及可以向其中插入服务应用程序中的自定义扩展的类。</span><span class="sxs-lookup"><span data-stu-id="0b68f-111">Describes the interfaces that can intercept and modify the service runtime, as well as the classes into which you can insert your custom extensions in service applications.</span></span> <span data-ttu-id="0b68f-112">例如，您可以执行自定义服务记录、服务侧消息验证、自定义调度，等等。</span><span class="sxs-lookup"><span data-stu-id="0b68f-112">For example, you can perform custom service logging, service-side message validation, custom dispatching, and so on.</span></span>  
  
 [<span data-ttu-id="0b68f-113">可扩展对象</span><span class="sxs-lookup"><span data-stu-id="0b68f-113">Extensible Objects</span></span>](extensible-objects.md)  
 <span data-ttu-id="0b68f-114">描述五个可扩展对象和 <xref:System.ServiceModel.IExtensibleObject%601> 模式。</span><span class="sxs-lookup"><span data-stu-id="0b68f-114">Describes the five extensible objects and the <xref:System.ServiceModel.IExtensibleObject%601> pattern.</span></span> <span data-ttu-id="0b68f-115">可扩展对象模式用于使用新功能扩展现有运行时类，或者向对象中添加新状态。</span><span class="sxs-lookup"><span data-stu-id="0b68f-115">The extensible object pattern is used to either extend existing runtime classes with new functionality or to add new state to an object.</span></span> <span data-ttu-id="0b68f-116">附加到可扩展对象之一的扩展名，在访问附加到公共可扩展对象的共享状态和功能过程的各个不同阶段启用行为，各可扩展对象可以访问该公共扩展对象。</span><span class="sxs-lookup"><span data-stu-id="0b68f-116">Extensions, attached to one of the extensible objects, enable behaviors at very different stages in processing to access shared state and functionality attached to a common extensible object that they can access.</span></span>  
  
 [<span data-ttu-id="0b68f-117">使用行为配置和扩展运行时</span><span class="sxs-lookup"><span data-stu-id="0b68f-117">Configuring and Extending the Runtime with Behaviors</span></span>](configuring-and-extending-the-runtime-with-behaviors.md)  
 <span data-ttu-id="0b68f-118">若要在 WCF 运行时中更改设置或插入扩展，请使用行为。</span><span class="sxs-lookup"><span data-stu-id="0b68f-118">To change settings on or insert extensions in the WCF runtime, you use Behaviors.</span></span> <span data-ttu-id="0b68f-119">WCF 包括系统实现的用于控制遏制、实例化和大量服务及操作的其他方面的行为。</span><span class="sxs-lookup"><span data-stu-id="0b68f-119">WCF includes system-implemented behaviors for controlling throttling, instancing, and many other aspects of services and operations.</span></span> <span data-ttu-id="0b68f-120">本节介绍如何通过编程方式和使用配置文件来创建您自己的自定义行为，以及如何使这些自定义行为变为可用。</span><span class="sxs-lookup"><span data-stu-id="0b68f-120">This section describes how to create your own custom behaviors and how to make them available for use both programmatically and using configuration files.</span></span>  
  
 [<span data-ttu-id="0b68f-121">使用 ServiceHostFactory 扩展宿主</span><span class="sxs-lookup"><span data-stu-id="0b68f-121">Extending Hosting Using ServiceHostFactory</span></span>](extending-hosting-using-servicehostfactory.md)  
 <span data-ttu-id="0b68f-122">描述如何扩展 <xref:System.ServiceModel.ServiceHostBase?displayProperty=nameWithType> 和 <xref:System.ServiceModel.ServiceHost?displayProperty=nameWithType> 以及使用 <xref:System.ServiceModel.Activation.ServiceHostFactory?displayProperty=nameWithType> 类来自定义主机环境。</span><span class="sxs-lookup"><span data-stu-id="0b68f-122">Describes how to extend <xref:System.ServiceModel.ServiceHostBase?displayProperty=nameWithType>, <xref:System.ServiceModel.ServiceHost?displayProperty=nameWithType>, and use the <xref:System.ServiceModel.Activation.ServiceHostFactory?displayProperty=nameWithType> classes to customize the host environment.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="0b68f-123">参考</span><span class="sxs-lookup"><span data-stu-id="0b68f-123">Reference</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="0b68f-124">相关章节</span><span class="sxs-lookup"><span data-stu-id="0b68f-124">Related Sections</span></span>
