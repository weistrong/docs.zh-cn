---
description: 了解详细信息：承载工作流服务概述
title: 承载工作流服务概述
ms.date: 03/30/2017
ms.assetid: 19f3704f-06bf-4eeb-8724-5224e02d7ead
ms.openlocfilehash: e183dfd7428c11cf20e731ab4a9975a7388b6f98
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99743078"
---
# <a name="hosting-workflow-services-overview"></a><span data-ttu-id="b07a3-103">承载工作流服务概述</span><span class="sxs-lookup"><span data-stu-id="b07a3-103">Hosting Workflow Services Overview</span></span>

<span data-ttu-id="b07a3-104">工作流服务必须进行承载才能执行。</span><span class="sxs-lookup"><span data-stu-id="b07a3-104">Workflow services must be hosted to execute.</span></span> <span data-ttu-id="b07a3-105"><xref:System.ServiceModel.WorkflowServiceHost> 是现成的工作流主机，可支持多个实例、配置和 WCF 消息传递（虽然工作流无需使用消息传递即可进行承载）。</span><span class="sxs-lookup"><span data-stu-id="b07a3-105">The <xref:System.ServiceModel.WorkflowServiceHost> is the out-of-the-box workflow host that supports multiple instances, configuration, and WCF messaging (although the workflows aren’t required to use messaging in order to be hosted).</span></span>  <span data-ttu-id="b07a3-106">它还通过一组服务行为集成了持久性、跟踪和实例控件。</span><span class="sxs-lookup"><span data-stu-id="b07a3-106">It also integrates with persistence, tracking, and instance control through a set of service behaviors.</span></span>  <span data-ttu-id="b07a3-107">正如 WCF 的 <xref:System.ServiceModel.ServiceHost> 一样，<xref:System.ServiceModel.WorkflowServiceHost> 可以在任何托管 .NET 应用程序中自承载，或是在 IIS/WAS 中进行 Web 承载（作为 .xamlx 文件）。</span><span class="sxs-lookup"><span data-stu-id="b07a3-107">Just like WCF’s <xref:System.ServiceModel.ServiceHost>, the <xref:System.ServiceModel.WorkflowServiceHost> can be self-hosted in any managed .NET application, or web-hosted (as a .xamlx file) in IIS / WAS.</span></span>  <span data-ttu-id="b07a3-108">本节中的主题描述如何承载工作流服务。</span><span class="sxs-lookup"><span data-stu-id="b07a3-108">Topics in this section describe how to host a workflow service.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="b07a3-109">本节内容</span><span class="sxs-lookup"><span data-stu-id="b07a3-109">In This Section</span></span>  

 [<span data-ttu-id="b07a3-110">承载工作流服务</span><span class="sxs-lookup"><span data-stu-id="b07a3-110">Hosting Workflow Services</span></span>](hosting-workflow-services.md)  
 <span data-ttu-id="b07a3-111">描述承载工作流服务。</span><span class="sxs-lookup"><span data-stu-id="b07a3-111">Describes hosting workflow services.</span></span>  
  
 [<span data-ttu-id="b07a3-112">工作流服务主机内部机制</span><span class="sxs-lookup"><span data-stu-id="b07a3-112">Workflow Service Host Internals</span></span>](workflow-service-host-internals.md)  
 <span data-ttu-id="b07a3-113">描述 <xref:System.ServiceModel.WorkflowServiceHost> 如何处理传入消息。</span><span class="sxs-lookup"><span data-stu-id="b07a3-113">Describes how <xref:System.ServiceModel.WorkflowServiceHost> processes incoming messages.</span></span>  
  
 [<span data-ttu-id="b07a3-114">工作流服务主机可扩展性</span><span class="sxs-lookup"><span data-stu-id="b07a3-114">Workflow Service Host Extensibility</span></span>](workflow-service-host-extensibility.md)  
 <span data-ttu-id="b07a3-115">描述如何扩展工作流服务主机的功能。</span><span class="sxs-lookup"><span data-stu-id="b07a3-115">Describes how to extend the functionality of the workflow service host.</span></span>  
  
 [<span data-ttu-id="b07a3-116">工作流控制终结点</span><span class="sxs-lookup"><span data-stu-id="b07a3-116">Workflow Control Endpoint</span></span>](workflow-control-endpoint.md)  
 <span data-ttu-id="b07a3-117">描述如何定义使您可以创建工作流实例的终结点。</span><span class="sxs-lookup"><span data-stu-id="b07a3-117">Describes how to define an endpoint that allows you to create workflow instances.</span></span>
  
 [<span data-ttu-id="b07a3-118">如何：使用 Windows Server App Fabric 承载工作流服务</span><span class="sxs-lookup"><span data-stu-id="b07a3-118">How to: Host a Workflow Service with Windows Server App Fabric</span></span>](how-to-host-a-workflow-service-with-windows-server-app-fabric.md)  
 <span data-ttu-id="b07a3-119">演示如何在 Windows Server App Fabric 中承载现有工作流服务。</span><span class="sxs-lookup"><span data-stu-id="b07a3-119">Demonstrates how to host an existing workflow service in Windows Server App Fabric.</span></span>  
  
 [<span data-ttu-id="b07a3-120">配置 WorkflowServiceHost</span><span class="sxs-lookup"><span data-stu-id="b07a3-120">Configuring WorkflowServiceHost</span></span>](configuring-workflowservicehost.md)  
 <span data-ttu-id="b07a3-121">描述如何控制持久性、跟踪、空闲和未经处理的异常行为。</span><span class="sxs-lookup"><span data-stu-id="b07a3-121">Describes how to control persistence, tracking, idle, and unhandled exception behavior.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="b07a3-122">参考</span><span class="sxs-lookup"><span data-stu-id="b07a3-122">Reference</span></span>  

 <xref:System.ServiceModel.Activities.WorkflowServiceHost>  
  
 <xref:System.ServiceModel.Activities.WorkflowService>  
  
 <xref:System.ServiceModel.Activation.ServiceHostFactory>  
  
 <xref:System.ServiceModel.Activation.ServiceHostFactoryBase>  
  
 <xref:System.ServiceModel.Activation.WorkflowServiceHostFactory>  
  
## <a name="related-sections"></a><span data-ttu-id="b07a3-123">相关章节</span><span class="sxs-lookup"><span data-stu-id="b07a3-123">Related Sections</span></span>  

 [<span data-ttu-id="b07a3-124">工作流服务</span><span class="sxs-lookup"><span data-stu-id="b07a3-124">Workflow Services</span></span>](workflow-services.md)
