---
description: 了解详细信息：迁移指南
title: 迁移指南
ms.date: 03/30/2017
ms.assetid: cb65c132-58c9-4028-b3d4-1efc71d5e60e
ms.openlocfilehash: 05aede02d7ad615ddeeceab6d71a545db9bcf5ba
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755346"
---
# <a name="migration-guidance"></a><span data-ttu-id="c692d-103">迁移指南</span><span class="sxs-lookup"><span data-stu-id="c692d-103">Migration Guidance</span></span>

<span data-ttu-id="c692d-104">在 .NET Framework 4 中，Microsoft 发布了 Windows Workflow Foundation (WF) 的第二个主要版本。</span><span class="sxs-lookup"><span data-stu-id="c692d-104">In the .NET Framework 4, Microsoft is releasing the second major version of Windows Workflow Foundation (WF).</span></span> [!INCLUDE[wf1](../../../includes/wf1-md.md)] <span data-ttu-id="c692d-105">在 WinFX 中发布 (这包括了 System.web 中的类型。 \* 名称现在称为 WF3) 并在 .NET Framework 3.5 中得到增强。</span><span class="sxs-lookup"><span data-stu-id="c692d-105">was released in WinFX (this included the types in the System.Workflow.\* namespaces; now referred to as WF3) and enhanced in .NET Framework 3.5.</span></span> <span data-ttu-id="c692d-106">WF3 也是 .NET Framework 4 的一部分，但它存在于新的工作流技术 (系统中的类型。 \* 名称称为 WF4) 。</span><span class="sxs-lookup"><span data-stu-id="c692d-106">WF3 is also part of the .NET Framework 4, but it exists there alongside new workflow technology (the types in the System.Activities.\* namespaces; referred to as WF4).</span></span> <span data-ttu-id="c692d-107">考虑何时采用 WF4 时，重要的是首先要认识到您来控制时间安排。</span><span class="sxs-lookup"><span data-stu-id="c692d-107">When considering when to adopt WF4, it is important to first recognize that you control the timing.</span></span>

- <span data-ttu-id="c692d-108">WF3 是 .NET Framework 4 的完全受支持的部分。</span><span class="sxs-lookup"><span data-stu-id="c692d-108">WF3 is a fully supported part of the .NET Framework 4.</span></span>

- <span data-ttu-id="c692d-109">WF3 应用程序无需修改即可在 .NET Framework 4 上运行，并继续完全受支持。</span><span class="sxs-lookup"><span data-stu-id="c692d-109">WF3 applications run on the .NET Framework 4 without modification and continue to be fully supported.</span></span>

- <span data-ttu-id="c692d-110">可以创建新的 WF3 应用程序，并可在 Visual Studio 2012 中编辑现有应用程序并完全支持这些应用程序。</span><span class="sxs-lookup"><span data-stu-id="c692d-110">New WF3 applications can be created and your existing applications can be edited in Visual Studio 2012 and are fully supported.</span></span>

 <span data-ttu-id="c692d-111">因此，决定采用 .NET Framework 4 的决定与迁移到 WF4 (的决策是分离的。 \* 从 WF3 (\*) 。) 。</span><span class="sxs-lookup"><span data-stu-id="c692d-111">Thus, the decision to adopt the .NET Framework 4 is decoupled from your decision to move to WF4 (System.Activities.\*) from WF3 (System.Workflow.\*).</span></span> <span data-ttu-id="c692d-112">本主题提供 WF 迁移指南的相关链接，涵盖了使用 WF3 和 WF4 的相关信息。</span><span class="sxs-lookup"><span data-stu-id="c692d-112">This topic provides links to WF migration guidance that provides information about working with WF3 and WF4.</span></span>

## <a name="wf-migration-white-papers-and-cookbooks"></a><span data-ttu-id="c692d-113">WF 迁移白皮书和指南</span><span class="sxs-lookup"><span data-stu-id="c692d-113">WF migration white papers and cookbooks</span></span>

 <span data-ttu-id="c692d-114">[WF 迁移概述](/previous-versions/appfabric/ff383417(v=azure.10))主题提供了 WF3 和 WF4 之间的关系以及迁移策略的全面概述。</span><span class="sxs-lookup"><span data-stu-id="c692d-114">The [WF Migration Overview](/previous-versions/appfabric/ff383417(v=azure.10)) topic provides a broad overview of the relationship between WF3 and WF4 and migration strategies.</span></span> <span data-ttu-id="c692d-115">关联的主题深入探讨特定主题。</span><span class="sxs-lookup"><span data-stu-id="c692d-115">Companion topics drill into specific topics.</span></span>

 <span data-ttu-id="c692d-116">[WF 迁移概述](/previous-versions/appfabric/ff383417(v=azure.10)) 介绍 WF3 和 WF4 之间的关系，以及在 .NET Framework 4 中作为工作流技术的用户或潜在用户的选择。</span><span class="sxs-lookup"><span data-stu-id="c692d-116">[WF Migration Overview](/previous-versions/appfabric/ff383417(v=azure.10)) Describes the relationship between WF3 and WF4, and the choices you have as a user or a potential user of workflow technology in .NET Framework 4.</span></span>

 <span data-ttu-id="c692d-117">[WF 迁移： WF3 开发的最佳做法](/previous-versions/appfabric/ff383417(v=azure.10)) 讨论如何设计 WF3 项目，以便可以更轻松地将其迁移到 WF4。</span><span class="sxs-lookup"><span data-stu-id="c692d-117">[WF Migration: Best Practices for WF3 Development](/previous-versions/appfabric/ff383417(v=azure.10)) Discusses how to design WF3 artifacts so they can be more easily migrated to WF4.</span></span>

 <span data-ttu-id="c692d-118">[WF 指南：规则](/previous-versions/appfabric/ff383417(v=azure.10)) 介绍如何将规则相关投资引入 .NET Framework 4 解决方案。</span><span class="sxs-lookup"><span data-stu-id="c692d-118">[WF Guidance: Rules](/previous-versions/appfabric/ff383417(v=azure.10)) Discusses how to bring rules-related investments forward into .NET Framework 4 solutions.</span></span>

 <span data-ttu-id="c692d-119">[WF 指南：状态机](/previous-versions/appfabric/ff383417(v=azure.10)) 讨论缺少 State-Machine 活动时 WF4 控制流建模。</span><span class="sxs-lookup"><span data-stu-id="c692d-119">[WF Guidance: State Machine](/previous-versions/appfabric/ff383417(v=azure.10)) Discusses WF4 control flow modeling in the absence of a State-Machine activity.</span></span>

 <span data-ttu-id="c692d-120">请注意，本指南仅适用于面向 .NET Framework 4 的工作流项目。</span><span class="sxs-lookup"><span data-stu-id="c692d-120">Note that this guidance only applies to workflow projects that target .NET Framework 4.</span></span> <span data-ttu-id="c692d-121">.NET Framework 4.0.1 中添加了状态机工作流，其中包含平台更新1的发行版，作为 4.5 .NET Framework 的一部分包含在其中。</span><span class="sxs-lookup"><span data-stu-id="c692d-121">State Machine workflows were added in .NET Framework 4.0.1 with the release of Platform Update 1, and were included as part of .NET Framework 4.5.</span></span> <span data-ttu-id="c692d-122">有关 .NET Framework 4.0.1-4.0.3 和 .NET Framework 4.5 中的状态机工作流的详细信息，请参阅 [Update 4.0.1 for Microsoft .NET Framework 4 功能](/previous-versions/dotnet/netframework-4.0/hh290669(v=vs.100)) 和 [状态机工作流](state-machine-workflows.md)。</span><span class="sxs-lookup"><span data-stu-id="c692d-122">For more information about state machine workflows in .NET Framework 4.0.1 - 4.0.3 and .NET Framework 4.5, see [Update 4.0.1 for Microsoft .NET Framework 4 Features](/previous-versions/dotnet/netframework-4.0/hh290669(v=vs.100)) and [State Machine Workflows](state-machine-workflows.md).</span></span>

 <span data-ttu-id="c692d-123">[WF 迁移指南：自定义活动](/previous-versions/appfabric/ff383417(v=azure.10)) 提供用于在 WF4 上重新设计 WF3 自定义活动的示例和说明。</span><span class="sxs-lookup"><span data-stu-id="c692d-123">[WF Migration Cookbook: Custom Activities](/previous-versions/appfabric/ff383417(v=azure.10)) Provides examples and instructions for redesigning WF3 custom activities on WF4.</span></span>

 <span data-ttu-id="c692d-124">[WF 迁移指南：高级自定义活动](/previous-versions/appfabric/ff383417(v=azure.10)) 提供用于重新设计高级 WF3 自定义活动的指南，这些活动使用 WF3 队列并将子活动安排为 WF4 自定义活动。</span><span class="sxs-lookup"><span data-stu-id="c692d-124">[WF Migration Cookbook: Advanced Custom Activities](/previous-versions/appfabric/ff383417(v=azure.10)) Provides guidance for redesigning advanced WF3 custom activities that use WF3 queues and schedule child activities as WF4 custom activities.</span></span>

 <span data-ttu-id="c692d-125">[WF 迁移指南：工作流](/previous-versions/appfabric/ff383417(v=azure.10)) 提供有关在 WF4 上重新设计 WF3 工作流的示例和说明。</span><span class="sxs-lookup"><span data-stu-id="c692d-125">[WF Migration Cookbook: Workflows](/previous-versions/appfabric/ff383417(v=azure.10)) Provides examples and instructions for redesigning WF3 workflows on WF4.</span></span>

 <span data-ttu-id="c692d-126">[WF 迁移指南：工作流托管](/previous-versions/appfabric/ff383417(v=azure.10)) 提供有关将 WF3 托管代码重新设计为 WF4 托管代码的指南。</span><span class="sxs-lookup"><span data-stu-id="c692d-126">[WF Migration Cookbook: Workflow Hosting](/previous-versions/appfabric/ff383417(v=azure.10)) Provides guidance for redesigning WF3 hosting code as WF4 hosting code.</span></span> <span data-ttu-id="c692d-127">目标是介绍 WF3 和 WF4 在工作流承载上的关键差异。</span><span class="sxs-lookup"><span data-stu-id="c692d-127">The goal is to cover the key differences in workflow hosting between WF3 and WF4.</span></span>

 <span data-ttu-id="c692d-128">[WF 迁移指南：工作流跟踪](/previous-versions/appfabric/ff383417(v=azure.10)) 提供使用等效的 WF4 跟踪代码和配置重新设计 WF3 跟踪代码和配置的指导。</span><span class="sxs-lookup"><span data-stu-id="c692d-128">[WF Migration Cookbook: Workflow Tracking](/previous-versions/appfabric/ff383417(v=azure.10)) Provides guidance for redesigning WF3 tracking code and configuration using equivalent WF4 tracking code and configuration.</span></span>

 <span data-ttu-id="c692d-129">[WF 指南：工作流服务](/previous-versions/appfabric/ff383417(v=azure.10)) 提供面向示例的分步说明，介绍如何将实现 Windows Communication Foundation (WCF) web 服务的工作流 (通常称为工作流服务) 在 WF3 中创建为使用 WF4，适用于全新活动方案。</span><span class="sxs-lookup"><span data-stu-id="c692d-129">[WF Guidance: Workflow Services](/previous-versions/appfabric/ff383417(v=azure.10)) Provides example-oriented step-by-step instructions for redesigning workflows that implement Windows Communication Foundation (WCF) web services (commonly referred to as workflow services) created in WF3 to use WF4, for common scenarios for out-of-box activities.</span></span>

## <a name="see-also"></a><span data-ttu-id="c692d-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="c692d-130">See also</span></span>

- <xref:System.Activities.Statements.Interop>
