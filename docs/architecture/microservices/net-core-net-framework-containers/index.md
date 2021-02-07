---
title: 为 Docker 容器选择 .NET 5 或 .NET Framework
description: 适用于容器化 .NET 应用程序的 .NET 微服务体系结构 | 为 Docker 容器选择 .NET 5 还是 .NET Framework
ms.date: 02/02/2021
ms.openlocfilehash: 5c3d4eff00399c8a6a041daaa71cf9fe5c9d854f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99665154"
---
# <a name="choosing-between-net-5-and-net-framework-for-docker-containers"></a><span data-ttu-id="43bc2-103">为 Docker 容器选择 .NET 5 或 .NET Framework</span><span class="sxs-lookup"><span data-stu-id="43bc2-103">Choosing Between .NET 5 and .NET Framework for Docker Containers</span></span>

<span data-ttu-id="43bc2-104">通过 .NET 生成服务器端容器化 Docker 应用程序时，有两种支持的框架：[.NET Framework 和 .NET 5](https://dotnet.microsoft.com/download)。</span><span class="sxs-lookup"><span data-stu-id="43bc2-104">There are two supported frameworks for building server-side containerized Docker applications with .NET: [.NET Framework and .NET 5](https://dotnet.microsoft.com/download).</span></span> <span data-ttu-id="43bc2-105">这两者共享许多 .NET 平台组件，可在它们之间共享代码。</span><span class="sxs-lookup"><span data-stu-id="43bc2-105">They share many .NET platform components, and you can share code across the two.</span></span> <span data-ttu-id="43bc2-106">但两者之间存在根本差异，可根据需要实现的目标选择框架。</span><span class="sxs-lookup"><span data-stu-id="43bc2-106">However, there are fundamental differences between them, and which framework you use will depend on what you want to accomplish.</span></span> <span data-ttu-id="43bc2-107">本节提供有关何时选择各框架的指南。</span><span class="sxs-lookup"><span data-stu-id="43bc2-107">This section provides guidance on when to choose each framework.</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="43bc2-108">[上一页](../container-docker-introduction/docker-containers-images-registries.md)
>[下一页](general-guidance.md)</span><span class="sxs-lookup"><span data-stu-id="43bc2-108">[Previous](../container-docker-introduction/docker-containers-images-registries.md)
[Next](general-guidance.md)</span></span>
