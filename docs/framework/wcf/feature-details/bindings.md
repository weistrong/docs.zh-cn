---
description: 了解详细信息： Windows Communication Foundation 绑定
title: Windows Communication Foundation 绑定
ms.date: 03/30/2017
helpviewer_keywords:
- WCF [WCF], bindings
- Windows Communication Foundation [WCF], bindings
- bindings [WCF]
ms.assetid: 83639133-89f7-43f0-b4ef-8d9e57c08d25
ms.openlocfilehash: 0104a33acbef7738607865b135561860f395dd71
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99643626"
---
# <a name="windows-communication-foundation-bindings"></a><span data-ttu-id="36f71-103">Windows Communication Foundation 绑定</span><span class="sxs-lookup"><span data-stu-id="36f71-103">Windows Communication Foundation Bindings</span></span>

<span data-ttu-id="36f71-104">Windows Communication Foundation (WCF) 分隔应用程序的软件如何从它与其他软件通信的方式进行编写。</span><span class="sxs-lookup"><span data-stu-id="36f71-104">Windows Communication Foundation (WCF) separates how the software for an application is written from how it communicates with other software.</span></span> <span data-ttu-id="36f71-105">使用绑定指定客户端与服务彼此通信所需的传输、编码和协议详细信息。</span><span class="sxs-lookup"><span data-stu-id="36f71-105">Bindings are used to specify the transport, encoding, and protocol details required for clients and services to communicate with each other.</span></span> <span data-ttu-id="36f71-106">WCF 使用绑定来生成终结点的基础线路表示形式，因此，通信的各方必须对大多数绑定详细信息达成一致。</span><span class="sxs-lookup"><span data-stu-id="36f71-106">WCF uses bindings to generate the underlying wire representation of the endpoint, so most of the binding details must be agreed upon by the parties that are communicating.</span></span> <span data-ttu-id="36f71-107">完成此任务的最简单方法是让服务的客户端使用该服务的终结点所使用的相同绑定。</span><span class="sxs-lookup"><span data-stu-id="36f71-107">The easiest way to achieve this is for clients of a service to use the same binding that the endpoint for the service uses.</span></span> <span data-ttu-id="36f71-108">有关如何执行此操作的详细信息，请参阅 [使用绑定配置服务和客户端](../using-bindings-to-configure-services-and-clients.md)。</span><span class="sxs-lookup"><span data-stu-id="36f71-108">For more information about how to do this, see [Using Bindings to Configure Services and Clients](../using-bindings-to-configure-services-and-clients.md).</span></span>  
  
 <span data-ttu-id="36f71-109">绑定由绑定元素的集合组成。</span><span class="sxs-lookup"><span data-stu-id="36f71-109">A binding is made up of a collection of binding elements.</span></span> <span data-ttu-id="36f71-110">每个元素描述终结点与客户端的通信方式的某一方面。</span><span class="sxs-lookup"><span data-stu-id="36f71-110">Each element describes some aspect of how the endpoint communicates with clients.</span></span> <span data-ttu-id="36f71-111">一个绑定必须至少包括一个传输绑定元素，至少包括一个消息编码绑定元素（默认情况下，传输绑定元素可能提供该元素）以及包括任意数目的其他协议绑定元素。</span><span class="sxs-lookup"><span data-stu-id="36f71-111">A binding must include at least one transport binding element, at least one message-encoding binding element (which the transport binding element can provide by default), and any number of other protocol binding elements.</span></span> <span data-ttu-id="36f71-112">使用本说明中生成运行时的进程，每个绑定元素均可为该运行时提供代码。</span><span class="sxs-lookup"><span data-stu-id="36f71-112">The process that builds a runtime out of this description allows each binding element to contribute code to that runtime.</span></span>  
  
 <span data-ttu-id="36f71-113">WCF 提供的绑定包含绑定元素的常见选择。</span><span class="sxs-lookup"><span data-stu-id="36f71-113">WCF provides bindings that contain common selections of binding elements.</span></span> <span data-ttu-id="36f71-114">这些绑定可以与其默认设置一起使用，您也可以根据用户需求修改这些默认值。</span><span class="sxs-lookup"><span data-stu-id="36f71-114">These can be used with their default settings or you can modify those default values according to user requirements.</span></span> <span data-ttu-id="36f71-115">这些系统提供的绑定具有一些属性，可以通过这些属性直接控制绑定元素及其设置。</span><span class="sxs-lookup"><span data-stu-id="36f71-115">These system-provided bindings have properties that allow direct control over the binding elements and their settings.</span></span> <span data-ttu-id="36f71-116">通过为绑定的每个版本提供其自己的名称，还可以轻松地并行使用该绑定的多个版本。</span><span class="sxs-lookup"><span data-stu-id="36f71-116">You can also easily work side-by-side with multiple versions of a binding by giving each version of the binding its own name.</span></span> <span data-ttu-id="36f71-117">有关详细信息，请参阅 [配置 System-Provided 绑定](configuring-system-provided-bindings.md)。</span><span class="sxs-lookup"><span data-stu-id="36f71-117">For details, see [Configuring System-Provided Bindings](configuring-system-provided-bindings.md).</span></span>  
  
 <span data-ttu-id="36f71-118">如果需要的绑定元素集合不是由系统提供的这些绑定之一提供，则可以创建由所需绑定元素的集合组成的自定义绑定。</span><span class="sxs-lookup"><span data-stu-id="36f71-118">If you need a collection of binding elements not provided by one of these system-provided bindings, you can create a custom binding that consists of the collection of binding elements required.</span></span> <span data-ttu-id="36f71-119">这些自定义绑定易于创建且不需要新类，但是，它们不提供用于控制绑定元素或其设置的属性。</span><span class="sxs-lookup"><span data-stu-id="36f71-119">These custom bindings are easy to create and do not require a new class, but they do not provide properties for controlling the binding elements or their settings.</span></span> <span data-ttu-id="36f71-120">您可以访问这些绑定元素并通过包含它们的集合修改其设置。</span><span class="sxs-lookup"><span data-stu-id="36f71-120">You can access the binding elements and modify their settings through the collection that contains them.</span></span> <span data-ttu-id="36f71-121">有关详细信息，请参阅 [自定义绑定](../extending/custom-bindings.md)。</span><span class="sxs-lookup"><span data-stu-id="36f71-121">For details, see [Custom Bindings](../extending/custom-bindings.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="36f71-122">本节内容</span><span class="sxs-lookup"><span data-stu-id="36f71-122">In This Section</span></span>  

 [<span data-ttu-id="36f71-123">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="36f71-123">Configuring System-Provided Bindings</span></span>](configuring-system-provided-bindings.md)  
 <span data-ttu-id="36f71-124">描述如何使用和修改 WCF 提供的绑定以支持常见方案。</span><span class="sxs-lookup"><span data-stu-id="36f71-124">Describes how to use and modify the bindings that WCF provides to support common scenarios.</span></span>  
  
 [<span data-ttu-id="36f71-125">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="36f71-125">Using Bindings to Configure Services and Clients</span></span>](../using-bindings-to-configure-services-and-clients.md)  
 <span data-ttu-id="36f71-126">介绍如何在代码中以强制方式为服务和客户端定义 Windows Communication Foundation (WCF) 绑定，并使用配置以声明方式定义。</span><span class="sxs-lookup"><span data-stu-id="36f71-126">Describes how to define Windows Communication Foundation (WCF) bindings for services and clients imperatively in code and declaratively using configuration.</span></span>  
  
 [<span data-ttu-id="36f71-127">自定义绑定</span><span class="sxs-lookup"><span data-stu-id="36f71-127">Custom Bindings</span></span>](../extending/custom-bindings.md)  
 <span data-ttu-id="36f71-128">描述什么是 <xref:System.ServiceModel.Channels.CustomBinding> 以及何时使用它。</span><span class="sxs-lookup"><span data-stu-id="36f71-128">Describes what a <xref:System.ServiceModel.Channels.CustomBinding> is and when it is used.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="36f71-129">参考</span><span class="sxs-lookup"><span data-stu-id="36f71-129">Reference</span></span>  

 <xref:System.ServiceModel.Channels.Binding>  
  
 <xref:System.ServiceModel.Channels.BindingElement>  
  
 <xref:System.ServiceModel.Channels.CustomBinding>  
  
## <a name="related-sections"></a><span data-ttu-id="36f71-130">相关章节</span><span class="sxs-lookup"><span data-stu-id="36f71-130">Related Sections</span></span>  

 [<span data-ttu-id="36f71-131">扩展绑定</span><span class="sxs-lookup"><span data-stu-id="36f71-131">Extending Bindings</span></span>](../extending/extending-bindings.md)
