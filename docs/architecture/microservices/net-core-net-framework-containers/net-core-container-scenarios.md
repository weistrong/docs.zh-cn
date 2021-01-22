---
title: 何时为 Docker 容器选择 .NET 5
description: 适用于容器化 .NET 应用程序的 .NET 微服务体系结构 | 何时为 Docker 容器选择 .NET
ms.date: 01/13/2021
ms.openlocfilehash: 61909c91d795582af499456c65ae0d7b4f2911e2
ms.sourcegitcommit: a4cecb7389f02c27e412b743f9189bd2a6dea4d6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/14/2021
ms.locfileid: "98189273"
---
# <a name="when-to-choose-net-for-docker-containers"></a>何时为 Docker 容器选择 .NET

.NET 5 的模块化和轻量级特点使其特别适用于容器。 在部署和启动容器时，使用 .NET 5 时容器的映像大小要远小于使用 .NET Framework 时的大小。 与此相反，若要为某个容器使用 .NET Framework，必须以 Windows Server Core 映像作为映像的基础，此映像在体量上远大于用于 .NET 5 的 Windows Nano Server 或 Linux 映像。

此外，.NET 5 可跨平台应用，这样便可使用 Linux 或 Windows 容器映像部署服务器应用。 但如果使用传统的 .NET Framework，只能够基于 Windows Server Core 部署映像。

以下是有关为何要选择 .NET 5 的详尽说明。

## <a name="developing-and-deploying-cross-platform"></a>跨平台开发和部署

显然，如果目标是获得可在 Docker 支持的多个平台（Linux 和 Windows）上运行的应用程序（Web 应用或服务），正确的选择是 .NET 5，因为 .NET Framework 仅支持 Windows。

.NET 5 还支持将 macOS 用作开发平台。 但如果要将容器部署到 Docker 主机，该主机必须（当前）基于 Linux 或 Windows。 例如，在开发环境中，可使用 Mac 上运行的 Linux VM。

[Visual Studio](https://www.visualstudio.com/vs/) 提供用于 Windows 的集成开发环境 (IDE) 并支持 Docker 开发。

[Visual Studio for Mac](https://www.visualstudio.com/vs/visual-studio-mac/) 是一个 IDE，由 Xamarin Studio 演变而来，在 macOS 上运行并支持基于 Docker 的应用程序环境。 对于使用 Mac 计算机工作而又希望使用功能强大的 IDE 的开发者而言，此工具应当是理想之选。

还可在 macOS、Linux 和 Windows 中使用 [Visual Studio Code](https://code.visualstudio.com/)。 Visual Studio 5 完全支持 .NET Core，包括 IntelliSense 和调试。 由于 VS Code 是轻量型编辑器，可以使用它，同时结合使用 Docker CLI 和 [.NET CLI](../../../core/tools/index.md) 在计算机上开发容器化应用。 还可以使用大多数第三方编辑器（如 Sublime、Emacs、VI）和同时提供 IntelliSense 支持的开源 OmniSharp 项目来面向 .NET 5。

除了 IDE 和编辑器，还可为所有支持的平台使用 [.NET CLI](../../../core/tools/index.md)。

## <a name="using-containers-for-new-green-field-projects"></a>为新（“绿地”）项目使用容器

虽然容器通常与微服务体系结构结合使用，但是也可用于对遵循任何体系结构模式的 Web 应用或服务进行容器化。 虽然能够将 .NET Framework 用于 Windows 容器，但 .NET 5 的模块化和轻型特点使之成为容器和微服务体系结构的最佳选择。 在创建和部署容器时，使用 .NET Core 时容器的映像大小要远小于使用 .NET Framework 时的大小。

## <a name="create-and-deploy-microservices-on-containers"></a>在容器上创建和部署微服务

可使用传统 .NET Framework，通过使用普通进程构建基于微服务的应用程序（不含容器）。 通过这种方式，由于已安装 .NET Framework 并在进程之间共享，进程变得轻量，从而可快速启动。 但如果使用容器，传统 .NET Framework 的映像便也基于 Windows Server Core，这样的话，它对于“容器上微服务”方法，就显得体量过于庞大。 但是，团队也一直在寻找机会来改善 .NET Framework 用户体验。 最近，[Windows Server Core 容器映像的大小已减小 40% 以上](https://devblogs.microsoft.com/dotnet/we-made-windows-server-core-container-images-40-smaller)。

另一方面，如果要使用基于容器的面向微服务的系统，.NET 5 是最佳选择，因为它体量轻。 此外，与之相关的容器映像，无论是 Linux 还是 Windows Nano Server，都精简而小巧，让容器变得轻量，从而能够快速启动。

微服务意味着尽可能得小：可轻松访问、占用空间小、小型的界定上下文（检查 DDD、[域驱动设计](https://en.wikipedia.org/wiki/Domain-driven_design)）、较少的关注度、能够快速启动和停止。 为满足这些要求，需要使用可快速实例化的轻量型容器映像，例如 .NET 5 容器映像。

微服务体系结构还允许跨服务边界，组合使用技术。 对于与其他微服务或使用 Node.js、Python、Java、GoLang 或其他技术开发的服务结合使用的新微服务，此方法可以使其逐步迁移到 .NET 5。

## <a name="deploying-high-density-in-scalable-systems"></a>在可缩放的系统中部署高密度

如果基于容器的系统需要实现最佳密度、粒度和性能，.NET 和 ASP.NET Core 是最佳选择。 ASP.NET Core 的运行速度比传统 .NET Framework 中的 ASP.NET 高出 10 倍，领先于其他用于微服务的受欢迎行业技术（例如 Java servlets、Go 和 Node.js）。

此方法特别适用于微服务体系结构，在该体系结构中，可以运行数百个微服务（容器）。 在 Linux 或 Windows Nano 上使用 ASP.NET Core 映像（基于 .NET 运行时），运行系统时所需的服务器或 VM 数量要少得多，最终可以节省基础结构和托管的费用。

>[!div class="step-by-step"]
>[上一页](general-guidance.md)
>[下一页](net-framework-container-scenarios.md)
