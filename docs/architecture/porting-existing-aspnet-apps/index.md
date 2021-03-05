---
title: 将现有 ASP.NET 应用移植到 .NET Core
description: 该免费指南指导你将 ASP.NET MVC 和 Web API 应用转换为 ASP.NET Core。
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: 848f0e9533a65b59055853f1d502307abb69118c
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102105940"
---
# <a name="porting-existing-aspnet-apps-to-net-core"></a>将现有 ASP.NET 应用移植到 .NET Core

![封面图像](./media/index/porting-existing-aspnet-apps.png)

[!INCLUDE [book-preview](../../../includes/book-preview.md)]

发布者

Microsoft 开发人员部门、.NET 和 Visual Studio 产品团队

Microsoft Corporation 的一个部门

One Microsoft Way

Redmond, Washington 98052-6399

版权所有 &copy; 2020 Microsoft Corporation

保留所有权利。 未经发布者书面许可，不得以任何形式或任何方式复制或传播本书中的任何内容。

本书“按原样”提供，表达作者的观点和看法。 本书中表达的观点、看法和信息（包括 URL 和其他 Internet 网站引用）如有更改，恕不另行通知。

本书中提及的一些示例仅用于说明，纯属虚构。 不存在任何实际关联或联系，请勿妄加推断。

Microsoft 和 <https://www.microsoft.com> 上“商标”网页列出的商标是 Microsoft 集团公司的商标。

Mac 和 macOS 是 Apple Inc. 的商标

Docker 的鲸鱼徽标是 Docker Inc. 的注册商标经许可方可使用。

所有其他标记和徽标均为其各自所有者的财产。

作者：

> Steve "ardalis" Smith，[Ardalis.com](https://ardalis.com) 软件设计师及培训师

参与者和审阅者：

> Nish Anil，Microsoft .NET 团队高级项目经理 

> Mike Rousos，Microsoft .NET 团队的首席软件工程师

> Scott Addie，Microsoft .NET 团队资深内容开发人员

> David Pine，Microsoft .NET 团队资深内容开发人员

## <a name="version"></a>Version

本指南包含 .NET Core 3.1 和与 .NET Core 3.1 版本同步发布的相同技术“wave”（即 Azure 和其他第三方技术）相关的更新。 从 .NET Core 3.1 更新到 .NET 5.0（下一版本）的过程相对简单，所需工作量要比从 .NET Framework 移植到 .NET Core 的工作量少得多。 从 .NET Framework 4.x 迁移到 .NET 5.0 将类似于迁移到 .NET Core 3.1。 有关详细信息，请参阅[选择正确的 .NET Core 版本](choose-net-core-version.md)。

## <a name="who-should-use-this-guide"></a>本指南的目标读者

本指南的受众是有意将为 ASP.NET MVC 和 Web API (.NET Framework 4.x) 编写的现有应用迁移到 .NET Core 的开发人员、开发组长和架构师。 ASP.NET Web Forms 开发人员将从本指南中受益，但还应参阅[面向 ASP.NET Web Forms 开发人员的 Blazor](../blazor-for-web-forms-developers/index.md) 电子书。

第二受众是计划何时将应用迁移到 .NET Core 的技术决策者。

本书的目标受众是拥有在 ASP.NET MVC 和 Web API 上运行的现行大型应用的 .NET 开发人员。 基于 ASP.NET Web Forms 构建的应用不在本书的关注范围之内，尽管很多对照 .NET Framework 和 .NET Core 的信息仍然相关。

## <a name="how-you-can-use-this-guide"></a>如何使用本指南

你可以通读本书籍，因为我们希望很多读者都可以这样做。 本书首先提供有关是否应移植应用的相关考量。 然后介绍 .NET Framework 与 .NET Core 之间的体系结构差异。 之后将介绍随时间推移迁移大型解决方案的策略，以及如何移植实际应用。 接下来，本书包含了一些部署方案，这些方案可满足运行不同应用时向用户显示为单个应用的需要。 最后给出了两个案例研究，其中介绍了从 ASP.NET MVC 迁移到 ASP.NET Core 的实际应用。

无论是否选择从第一章开始，都可以参考这些章节来了解具体概念：

- [体系结构差异](architectural-differences.md)
- [迁移大型解决方案](migrate-large-solutions.md)
- [示例迁移](example-migration-eshop.md)
- [部署方案](deployment-scenarios.md)

本指南有 [PDF 格式](https://aka.ms/aspnet-porting-ebook)和在线版本。 欢迎随时将此文档或其在线版本的链接转发给你的团队，以确保对这些概念有共同的理解。

## <a name="send-your-feedback"></a>提供你的反馈

我们正在不断完善本书和相关示例，欢迎你提供反馈！ 如果对如何改进本书有任何建议，请使用 [GitHub 问题](https://github.com/dotnet/docs/issues)上任何页面底部的反馈部分进行反馈。

>[!div class="step-by-step"]
>[下一页](introduction.md)
