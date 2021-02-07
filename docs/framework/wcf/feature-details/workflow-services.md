---
description: 了解详细信息：工作流服务
title: 工作流服务
ms.date: 03/30/2017
ms.assetid: 7b05c766-f181-425d-9a3d-2a5e150c85f7
ms.openlocfilehash: 195ecf0322146a8735362dfbb82dc19bf1c04312
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99704467"
---
# <a name="workflow-services"></a><span data-ttu-id="7ed25-103">工作流服务</span><span class="sxs-lookup"><span data-stu-id="7ed25-103">Workflow Services</span></span>

<span data-ttu-id="7ed25-104">使用 [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)]，您可以在 XAML 中以声明方式充分描述基于工作流的服务。</span><span class="sxs-lookup"><span data-stu-id="7ed25-104">[!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)] allows you to fully describe a workflow-based service declaratively in XAML.</span></span> <span data-ttu-id="7ed25-105">您完全可以在 XAML 中定义实现服务的工作流并描述服务所公开的终结点。</span><span class="sxs-lookup"><span data-stu-id="7ed25-105">You can define a workflow that implements your service and describe endpoints the service exposes, all entirely in XAML.</span></span> <span data-ttu-id="7ed25-106">本节中的主题详细描述支持以声明方式编写服务的编程模型。</span><span class="sxs-lookup"><span data-stu-id="7ed25-106">The topics in this section describe, in detail, the programming model that supports writing services declaratively.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="7ed25-107">本节内容</span><span class="sxs-lookup"><span data-stu-id="7ed25-107">In This Section</span></span>  

 [<span data-ttu-id="7ed25-108">工作流服务概述</span><span class="sxs-lookup"><span data-stu-id="7ed25-108">Workflow Services Overview</span></span>](workflow-services-overview.md)  
 <span data-ttu-id="7ed25-109">描述创建和承载工作流服务所涉及的组件。</span><span class="sxs-lookup"><span data-stu-id="7ed25-109">Describes the components involved in creating and hosting a workflow service.</span></span>  
  
 [<span data-ttu-id="7ed25-110">消息传递活动</span><span class="sxs-lookup"><span data-stu-id="7ed25-110">Messaging Activities</span></span>](messaging-activities.md)  
 <span data-ttu-id="7ed25-111">讨论允许工作流发送和接收消息的活动。</span><span class="sxs-lookup"><span data-stu-id="7ed25-111">Discusses activities that allow workflows to send and receive messages.</span></span>  
  
 [<span data-ttu-id="7ed25-112">如何：使用消息传递活动创建工作流服务</span><span class="sxs-lookup"><span data-stu-id="7ed25-112">How to: Create a Workflow Service with Messaging Activities</span></span>](how-to-create-a-workflow-service-with-messaging-activities.md)  
 <span data-ttu-id="7ed25-113">说明如何使用消息传递活动创建工作流服务。</span><span class="sxs-lookup"><span data-stu-id="7ed25-113">Describes how to use messaging activities to create a workflow service.</span></span>  
  
 [<span data-ttu-id="7ed25-114">如何：从工作流应用程序访问服务</span><span class="sxs-lookup"><span data-stu-id="7ed25-114">How To: Access a Service From a Workflow Application</span></span>](how-to-access-a-service-from-a-workflow-application.md)  
 <span data-ttu-id="7ed25-115">讨论如何从工作流应用程序调用服务。</span><span class="sxs-lookup"><span data-stu-id="7ed25-115">Discusses how to call a service from a workflow application.</span></span>  
  
 [<span data-ttu-id="7ed25-116">相关性</span><span class="sxs-lookup"><span data-stu-id="7ed25-116">Correlation</span></span>](correlation.md)  
 <span data-ttu-id="7ed25-117">讨论相关性对象如何在彼此之间映射消息以及将消息映射到实例。</span><span class="sxs-lookup"><span data-stu-id="7ed25-117">Discusses how correlation maps messages to each other and to instances.</span></span>  
  
 [<span data-ttu-id="7ed25-118">无序消息处理</span><span class="sxs-lookup"><span data-stu-id="7ed25-118">Out-of-Order Message Processing</span></span>](out-of-order-message-processing.md)  
 <span data-ttu-id="7ed25-119">说明如何将服务配置为接受无序消息。</span><span class="sxs-lookup"><span data-stu-id="7ed25-119">Describes configuring a service to accept out of order messages.</span></span>  
  
 [<span data-ttu-id="7ed25-120">协定优先的工作流服务开发</span><span class="sxs-lookup"><span data-stu-id="7ed25-120">Contract First Workflow Service Development</span></span>](../../windows-workflow-foundation/contract-first-workflow-service-development.md)  
 <span data-ttu-id="7ed25-121">说明如何基于现有服务协定创建工作流服务。</span><span class="sxs-lookup"><span data-stu-id="7ed25-121">Describes creating a workflow service based on an existing service contract.</span></span>  
  
 [<span data-ttu-id="7ed25-122">如何：创建使用现有服务协定的工作流服务</span><span class="sxs-lookup"><span data-stu-id="7ed25-122">How to: Create a workflow service that consumes an existing service contract</span></span>](../../windows-workflow-foundation/how-to-create-a-workflow-service-that-consumes-an-existing-service-contract.md)  
 <span data-ttu-id="7ed25-123">提供了一个对使用现有服务协定创建工作流服务的分步说明示例。</span><span class="sxs-lookup"><span data-stu-id="7ed25-123">Provides a step-by-step example of creating a workflow service using an existing service contract.</span></span>  
  
 [<span data-ttu-id="7ed25-124">承载工作流服务概述</span><span class="sxs-lookup"><span data-stu-id="7ed25-124">Hosting Workflow Services Overview</span></span>](hosting-workflow-services-overview.md)  
 <span data-ttu-id="7ed25-125">描述承载工作流服务的不同方面。</span><span class="sxs-lookup"><span data-stu-id="7ed25-125">Describes the different aspects of hosting a workflow service.</span></span>  
  
 [<span data-ttu-id="7ed25-126">在工作流中使用协定</span><span class="sxs-lookup"><span data-stu-id="7ed25-126">Using Contracts in Workflow</span></span>](using-contracts-in-workflow.md)  
 <span data-ttu-id="7ed25-127">描述不同类型的协定和协定接口。</span><span class="sxs-lookup"><span data-stu-id="7ed25-127">Describes the different types of contracts and contract inference.</span></span>
