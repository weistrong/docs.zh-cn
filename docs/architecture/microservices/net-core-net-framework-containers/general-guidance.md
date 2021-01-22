---
title: 通用指南
description: 适用于容器化 .NET 应用程序的 .NET 微服务体系结构 | 通用指南
ms.date: 01/13/2021
ms.openlocfilehash: 4fd2d936c524cb3e5ae463038eaffe88b459d2bd
ms.sourcegitcommit: a4cecb7389f02c27e412b743f9189bd2a6dea4d6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/14/2021
ms.locfileid: "98187946"
---
# <a name="general-guidance"></a>通用指南

本部分提供有关何时选择 .NET 5 或 .NET Framework 的总结。 后面各部分将提供对上述选择的详细介绍。

在以下情况下，将 .NET 5 与 Linux 或 Windows 容器结合使用并用于容器化 Docker 服务器应用程序：

- 用户有跨平台需求。 例如，想同时使用 Linux 和 Windows 容器。

- 应用程序体系结构基于微服务。

- 需快速启动容器且每个容器内存占用较小，以实现更好的密度，或每个硬件单位中的容器较多，以降低成本。

简单地说，在创建新的容器化 .NET 应用程序时，应考虑将 .NET 5 作为默认选择。 它具有许多好处，并最匹配容器的基本原理和运行方式。

使用 .NET 5 的另一个好处是可在同一台计算机中并行运行 .NET 版本的应用程序。 这一优势对于不使用容器的服务器或虚拟机而言更为重要，因为容器会隔离应用所需的 .NET 版本。 （只要它们与基础操作系统兼容。）

在以下情况下，应将 .NET Framework 用于容器化 Docker 服务器应用程序：

- 应用程序当前使用 .NET Framework 并在 Windows 上具有强依赖关系。

- 需要使用 .NET 5 不支持的 Windows API。

- 用户需要使用不可用于 .NET 5 的第三方 .NET 库或 NuGet 包。

在 Docker 上使用.NET Framework 可通过最大限度地减少部署问题来提升部署体验。 此[“提升和移动”方案](https://aka.ms/liftandshiftwithcontainersebook)对于针对最初使用传统 .NET Framework（如 ASP.NET WebForms、MVC Web 应用或 WCF (Windows Communication Foundation) 服务）开发的旧应用程序实施容器化而言很重要。

### <a name="additional-resources"></a>其他资源

- 电子书：**Modernize existing .NET Framework applications with Azure and Windows Containers**（使用 Azure 和 Windows 容器更新现有 .NET Framework 应用程序）  
    <https://aka.ms/liftandshiftwithcontainersebook>

- **示例应用：Modernization of legacy ASP.NET web apps by using Windows Containers**（使用 Windows 容器更新旧的 ASP.NET Web 应用）  
    <https://aka.ms/eshopmodernizing>

>[!div class="step-by-step"]
>[上一页](index.md)
>[下一页](net-core-container-scenarios.md)
