---
title: 迁移指南
description: 了解详细信息：迁移指南
ms.date: 03/30/2017
ms.assetid: cb65c132-58c9-4028-b3d4-1efc71d5e60e
ms.openlocfilehash: 83c6af4d8eed396501aafc568de8e64d30ae7cfe
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102104856"
---
# <a name="migration-guidance"></a>迁移指南

在 .NET Framework 4 中，Microsoft 发布了 Windows Workflow Foundation (WF) 的第二个主要版本。 [!INCLUDE[wf1](../../../includes/wf1-md.md)] 在 WinFX 中发布 (这包括了 System.web 中的类型。 \* 名称现在称为 WF3) 并在 .NET Framework 3.5 中得到增强。 WF3 也是 .NET Framework 4 的一部分，但它存在于新的工作流技术 (系统中的类型。 \* 名称称为 WF4) 。 考虑何时采用 WF4 时，重要的是首先要认识到您来控制时间安排。

- WF3 是 .NET Framework 4 的完全受支持的部分。

- WF3 应用程序无需修改即可在 .NET Framework 4 上运行，并继续完全受支持。

- 可以创建新的 WF3 应用程序，并可在 Visual Studio 2012 中编辑现有应用程序并完全支持这些应用程序。

因此，决定采用 .NET Framework 4 的决定与迁移到 WF4 (的决策是分离的。 \* 从 WF3 (\*) 。) 。 本主题提供 WF 迁移指南的相关链接，涵盖了使用 WF3 和 WF4 的相关信息。

## <a name="wf-migration-white-papers-and-cookbooks"></a>WF 迁移白皮书和指南

 [WF 迁移概述](https://download.microsoft.com/download/5/9/9/599CF8A9-5FE2-426A-A536-A83F84D38BF9/WF%20Migration%20Overview.docx)\
 介绍 WF3 和 WF4 之间的关系，以及在 .NET Framework 4 中作为工作流技术的用户或潜在用户的选择。

 [WF 迁移： WF3 开发的最佳做法](https://download.microsoft.com/download/5/9/9/599CF8A9-5FE2-426A-A536-A83F84D38BF9/WF%20Migration%20Best%20Practices.docx)\
 讨论如何设计 WF3 项目以便可以更轻松地迁移至 WF4。

 [WF 指南：规则](https://download.microsoft.com/download/5/9/9/599CF8A9-5FE2-426A-A536-A83F84D38BF9/WF4%20Rules%20Guidance.docx)\
 介绍如何将规则相关投资引入 .NET Framework 4 解决方案。

 [WF 指南：状态机](https://download.microsoft.com/download/5/9/9/599CF8A9-5FE2-426A-A536-A83F84D38BF9/WF4%20State%20Machine%20Guidance.doc) 讨论缺少 State-Machine 活动时 WF4 控制流建模。 本指南仅适用于面向 .NET Framework 4 的工作流项目。 .NET Framework 4.0.1 中添加了状态机工作流，其中包含平台更新1的发行版，作为 4.5 .NET Framework 的一部分包含在其中。 有关 .NET Framework 4.0.1-4.0.3 和 .NET Framework 4.5 中的状态机工作流的详细信息，请参阅 [Update 4.0.1 for Microsoft .NET Framework 4 功能](/previous-versions/dotnet/netframework-4.0/hh290669(v=vs.100)) 和 [状态机工作流](state-machine-workflows.md)。

 [WF 迁移指南：自定义活动](https://download.microsoft.com/download/5/9/9/599CF8A9-5FE2-426A-A536-A83F84D38BF9/WF%20Migration%20Cookbook%20Custom%20Activities.docx)\
 提供用于在 WF4 上重新设计 WF3 自定义活动的示例和说明。

 [WF 迁移指南：高级自定义活动](https://download.microsoft.com/download/5/9/9/599CF8A9-5FE2-426A-A536-A83F84D38BF9/WF%20Migration%20Cookbook%20Advanced%20Custom%20Activities.docx)\
 提供将使用 WF3 队列和对子活动进行排程的高级 WF3 自定义活动重新设计为 WF4 自定义活动的指南。
%20 [WF 迁移指南：工作流](https://download.microsoft.com/download/5/9/9/599CF8A9-5FE2-426A-A536-A83F84D38BF9/WF%20Migration%20Cookbook%20Workflows.docx)\
 提供用于在 WF4 上重新设计 WF3 工作流的示例和说明。

 [WF 迁移指南：工作流托管](https://download.microsoft.com/download/5/9/9/599CF8A9-5FE2-426A-A536-A83F84D38BF9/WF%20Migration%20Cookbook%20Workflow%20Hosting.docx)\
 提供将 WF3 承载代码重新设计为 WF4 承载代码的指南。 目标是介绍 WF3 和 WF4 在工作流承载上的关键差异。

 [WF 迁移指南：工作流跟踪](https://download.microsoft.com/download/5/9/9/599CF8A9-5FE2-426A-A536-A83F84D38BF9/WF%20Migration%20Cookbook%20Workflow%20Tracking.docx)\
 提供用等价 WF4 跟踪代码和配置来重新设计 WF3 跟踪代码和配置的指南。

 [WF 指南：工作流服务](https://download.microsoft.com/download/5/9/9/599CF8A9-5FE2-426A-A536-A83F84D38BF9/WF4%20Workflow%20Services%20Guidance.docx)\
 提供面向示例的分步说明，针对现成活动的一般方案，将在 WF3 中创建、实现 Windows Communication Foundation (WCF) Web 服务（通常称为工作流服务）的工作流重新设计为使用 WF4。

## <a name="see-also"></a>另请参阅

- <xref:System.Activities.Statements.Interop>
