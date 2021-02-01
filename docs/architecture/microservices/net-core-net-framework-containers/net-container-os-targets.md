---
title: 使用 .NET 容器时定位的操作系统
description: 适用于容器化 .NET 应用程序的 .NET 微服务体系结构 | 使用 .NET 容器时定位的操作系统
ms.date: 01/13/2021
ms.openlocfilehash: b128a7b98d7f46034a56314bd8cc6b4f5731f121
ms.sourcegitcommit: 7e42488c2f8f63f6d499b5f8fb1dec5bac9ad254
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2021
ms.locfileid: "98957905"
---
# <a name="what-os-to-target-with-net-containers"></a><span data-ttu-id="b5806-103">使用 .NET 容器时定位的操作系统</span><span class="sxs-lookup"><span data-stu-id="b5806-103">What OS to target with .NET containers</span></span>

<span data-ttu-id="b5806-104">由于 Docker 支持多种操作系统，且鉴于 .NET Framework 和 .NET 5 之间的差异，应根据所使用的框架，面向特定操作系统和特定版本。</span><span class="sxs-lookup"><span data-stu-id="b5806-104">Given the diversity of operating systems supported by Docker and the differences between .NET Framework and .NET 5, you should target a specific OS and specific versions depending on the framework you are using.</span></span>

<span data-ttu-id="b5806-105">对于 Windows，可使用 Windows Server Core 或 Windows Nano Server。</span><span class="sxs-lookup"><span data-stu-id="b5806-105">For Windows, you can use Windows Server Core or Windows Nano Server.</span></span> <span data-ttu-id="b5806-106">这两种 Windows 版本分别提供 .NET Framework 和 .NET 5 各自所需的特征（Windows Server Core 中的 IIS 与 Nano Server 中自承载的 Web 服务器，如 Kestrel）。</span><span class="sxs-lookup"><span data-stu-id="b5806-106">These Windows versions provide different characteristics (IIS in Windows Server Core versus a self-hosted web server like Kestrel in Nano Server) that might be needed by .NET Framework or .NET 5, respectively.</span></span>

<span data-ttu-id="b5806-107">对于 Linux，正式的 .NET Docker 映像（如 Debian）中提供并支持多个发行版本。</span><span class="sxs-lookup"><span data-stu-id="b5806-107">For Linux, multiple distros are available and supported in official .NET Docker images (like Debian).</span></span>

<span data-ttu-id="b5806-108">图 3-1 显示基于所使用的 .NET framework，可使用的操作系统版本。</span><span class="sxs-lookup"><span data-stu-id="b5806-108">In Figure 3-1, you can see the possible OS version depending on the .NET framework used.</span></span>

![显示要与哪些 .NET 容器一起使用的操作系统的关系图。](./media/net-container-os-targets/targeting-operating-systems.png)

<span data-ttu-id="b5806-110">**图 3-1。**</span><span class="sxs-lookup"><span data-stu-id="b5806-110">**Figure 3-1.**</span></span> <span data-ttu-id="b5806-111">根据 .NET framework 确定要面向的操作系统</span><span class="sxs-lookup"><span data-stu-id="b5806-111">Operating systems to target depending on versions of the .NET framework</span></span>

<span data-ttu-id="b5806-112">部署旧的 .NET Framework 应用程序时，必须以与旧应用程序和 IIS 兼容但具有更大映像的 Windows Server Core 为目标。</span><span class="sxs-lookup"><span data-stu-id="b5806-112">When deploying legacy .NET Framework applications you have to target Windows Server Core, compatible with legacy apps and IIS, but it has a larger image.</span></span> <span data-ttu-id="b5806-113">部署 .NET 5 应用程序时，可以针对已经过云优化、使用 Kestrel、更小且启动速度更快的 Windows Nano Server。</span><span class="sxs-lookup"><span data-stu-id="b5806-113">When deploying .NET 5 applications, you can target Windows Nano Server, which is cloud optimized, uses Kestrel and is smaller and starts faster.</span></span> <span data-ttu-id="b5806-114">还可以面向 Linux，支持 Debian、Alpine 和其他操作系统。</span><span class="sxs-lookup"><span data-stu-id="b5806-114">You can also target Linux, supporting Debian, Alpine, and others.</span></span> <span data-ttu-id="b5806-115">也使用 Kestrel、更小且启动速度更快。</span><span class="sxs-lookup"><span data-stu-id="b5806-115">Also uses Kestrel, is smaller, and starts faster.</span></span>

<span data-ttu-id="b5806-116">如果想使用不同的 Linux 发行版本或要使用 Microsoft 不支持的映像版本，还可以创建自己的 Docker 映像。</span><span class="sxs-lookup"><span data-stu-id="b5806-116">You can also create your own Docker image in cases where you want to use a different Linux distro or where you want an image with versions not provided by Microsoft.</span></span> <span data-ttu-id="b5806-117">例如，可以使用 ASP.NET Core 创建一个在传统 .NET Framework 和 Windows Server Core 上运行的映像，但这不是常见的 Docker 方案。</span><span class="sxs-lookup"><span data-stu-id="b5806-117">For example, you might create an image with ASP.NET Core running on the traditional .NET Framework and Windows Server Core, which is a not-so-common scenario for Docker.</span></span>

<span data-ttu-id="b5806-118">将映像名称添加到 Dockerfile 文件后，可根据所使用的标记选择操作系统和版本，如下例所示：</span><span class="sxs-lookup"><span data-stu-id="b5806-118">When you add the image name to your Dockerfile file, you can select the operating system and version depending on the tag you use, as in the following examples:</span></span>

| <span data-ttu-id="b5806-119">图像</span><span class="sxs-lookup"><span data-stu-id="b5806-119">Image</span></span> | <span data-ttu-id="b5806-120">注释</span><span class="sxs-lookup"><span data-stu-id="b5806-120">Comments</span></span> |
|-------|----------|
| <span data-ttu-id="b5806-121">mcr.microsoft.com/dotnet/runtime:5.0</span><span class="sxs-lookup"><span data-stu-id="b5806-121">mcr.microsoft.com/dotnet/runtime:5.0</span></span> | <span data-ttu-id="b5806-122">.NET 5 多体系结构：支持 Linux 和 Windows Nano Server，具体取决于 Docker 主机。</span><span class="sxs-lookup"><span data-stu-id="b5806-122">.NET 5 multi-architecture: Supports Linux and Windows Nano Server depending on the Docker host.</span></span> |
| <span data-ttu-id="b5806-123">mcr.microsoft.com/dotnet/aspnet:5.0</span><span class="sxs-lookup"><span data-stu-id="b5806-123">mcr.microsoft.com/dotnet/aspnet:5.0</span></span> | <span data-ttu-id="b5806-124">ASP.NET Core 5.0 多体系结构：支持 Linux 和 Windows Nano Server，具体取决于 Docker 主机。</span><span class="sxs-lookup"><span data-stu-id="b5806-124">ASP.NET Core 5.0 multi-architecture: Supports Linux and Windows Nano Server depending on the Docker host.</span></span> <br/> <span data-ttu-id="b5806-125">ASP.NET Core 的 aspnetcore 映像具有多个优化。</span><span class="sxs-lookup"><span data-stu-id="b5806-125">The aspnetcore image has a few optimizations for ASP.NET Core.</span></span> |
| <span data-ttu-id="b5806-126">mcr.microsoft.com/dotnet/aspnet:5.0-buster-slim</span><span class="sxs-lookup"><span data-stu-id="b5806-126">mcr.microsoft.com/dotnet/aspnet:5.0-buster-slim</span></span> | <span data-ttu-id="b5806-127">Linux Debian 发行版上的 .NET 5 仅运行时</span><span class="sxs-lookup"><span data-stu-id="b5806-127">.NET 5 runtime-only on Linux Debian distro</span></span> |
| <span data-ttu-id="b5806-128">mcr.microsoft.com/dotnet/aspnet:5.0-nanoserver-1809</span><span class="sxs-lookup"><span data-stu-id="b5806-128">mcr.microsoft.com/dotnet/aspnet:5.0-nanoserver-1809</span></span> | <span data-ttu-id="b5806-129">Windows Nano Server（Windows Server 版本 1809）上的 .NET 5 仅运行时</span><span class="sxs-lookup"><span data-stu-id="b5806-129">.NET 5 runtime-only on Windows Nano Server (Windows Server version 1809)</span></span> |

> [!div class="step-by-step"]
> <span data-ttu-id="b5806-130">[上一页](container-framework-choice-factors.md)
> [下一页](official-net-docker-images.md)</span><span class="sxs-lookup"><span data-stu-id="b5806-130">[Previous](container-framework-choice-factors.md)
[Next](official-net-docker-images.md)</span></span>
