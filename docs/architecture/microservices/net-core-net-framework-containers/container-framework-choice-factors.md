---
title: 决策表。 用于 Docker 的 .NET Framework
description: 适用于容器化 .NET 应用程序的 .NET 微服务体系结构 | 决策表，用于 Docker 的 .NET Framework
ms.date: 01/13/2021
ms.openlocfilehash: 35f101b3f4030e081068677b3754363bf6cd8210
ms.sourcegitcommit: a4cecb7389f02c27e412b743f9189bd2a6dea4d6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/14/2021
ms.locfileid: "98188655"
---
# <a name="decision-table-net-frameworks-to-use-for-docker"></a>决策表：用于 Docker 的 .NET Framework

下列决策表汇总了是使用 .NET Framework 还是 .NET 5。 请记住，对于 Linux 容器，你需要基于 Linux 的 Docker 主机（VM 或服务器）；对于 Windows 容器，你需要基于 Windows Server 的 Docker 主机（VM 或服务器）。

> [!IMPORTANT]
> 开发计算机将运行一个 Docker 主机，Linux 或 Windows 均可。 想在一个解决方案中一起运行和测试的相关微服务都需要在同一容器平台上运行。

| 体系结构/应用类型 | Linux 容器 | Windows 容器 |
|-------------------------|------------------|--------------------|
| 容器上的微服务 | .NET 5 | .NET 5 |
| 单一应用程序 | .NET 5 | .NET Framework <br/> .NET 5 |
| 一流性能和可扩展性 | .NET 5 | .NET 5 |
| 到容器的 Windows Server 旧应用程序（“棕色字段”）迁移 | -- | .NET Framework |
| 基于容器的新开发（“绿色字段”） | .NET 5 | .NET 5 |
| ASP.NET Core | .NET 5 | .NET 5（推荐） <br/> .NET Framework |
| ASP.NET 4（MVC 5、Web API 2 和 Web 窗体） | -- | .NET Framework |
| SignalR 服务 | .NET Core 2.1 或更高版本 | .NET Framework <br/> .NET Core 2.1 或更高版本 |
| WCF、WF 和其他旧框架 | .NET Core 中的 WCF（仅客户端库） | .NET Framework <br/> .NET 5 中的 WCF（仅客户端库） |
| Azure 服务的消耗 | .NET 5 <br/> （最终大部分 Azure 服务都将为 .NET 5 提供客户端 SDK） | .NET Framework <br/> .NET 5 <br/> （最终大部分 Azure 服务都将为 .NET 5 提供客户端 SDK） |

>[!div class="step-by-step"]
>[上一页](net-framework-container-scenarios.md)
>[下一页](net-container-os-targets.md)
