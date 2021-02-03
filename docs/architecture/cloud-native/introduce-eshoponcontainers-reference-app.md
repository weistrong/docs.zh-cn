---
title: EShopOnContainers 参考应用简介
description: 介绍适用于 ASP.NET Core 和 Azure 的 eShopOnContainers Cloud 本机微服务 Reference 应用。
ms.date: 01/19/2021
ms.openlocfilehash: 35aa92794d8488c3de60f42af52654c4c26aad82
ms.sourcegitcommit: f2ab02d9a780819ca2e5310bbcf5cfe5b7993041
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2021
ms.locfileid: "99505669"
---
# <a name="introducing-eshoponcontainers-reference-app"></a>EShopOnContainers 参考应用简介

Microsoft 与领先社区专家合作，已生成了一个功能完备的云本机微服务参考应用程序 eShopOnContainers。 构建此应用程序时，可以使用 .NET 和 Docker，还可以选择使用 Azure、Kubernetes 和 Visual Studio 来构建在线店面。

![eShopOnContainers 示例应用屏幕快照。](./media/eshoponcontainers-sample-app-screenshot.png)

**图 2-1**. eShopOnContainers 示例应用屏幕快照。

在开始本章之前，我们建议下载 [eShopOnContainers 引用应用程序](https://github.com/dotnet-architecture/eShopOnContainers)。 如果执行此操作，则应更轻松地遵循所显示的信息。

## <a name="features-and-requirements"></a>功能和要求

让我们先来回顾一下应用程序的功能和要求。 EShopOnContainers 应用程序代表了一款在线商店，其中销售各种实物产品，如 t 恤衫和咖啡杯子。 如果你之前已购买过任何内容，则使用该商店的体验应该比较熟悉。 下面是应用商店实现的一些基本功能：

- 列出目录项
- 按类型筛选项目
- 按品牌筛选项目
- 将商品添加到购物篮
- 编辑或删除购物篮中的项
- 签出
- 注册帐户
- 登录
- 注销
- 查看订单

该应用程序还具有以下非功能性要求：

- 它必须具有高可用性，并且必须自动缩放以满足增加的流量 (并在流量下降) 后向下缩放。
- 它应该为其运行状况和诊断日志提供易于使用的监视，以帮助解决所遇到的任何问题。
- 它应支持 agile 开发过程，其中包括支持持续集成和部署 (CI/CD) 。
- 除两个 web 前端外 (传统的单页应用程序) ，应用程序还必须支持运行不同种类的操作系统的移动客户端应用程序。
- 它应该支持跨平台托管和跨平台开发。

![eShopOnContainers 参考应用程序开发体系结构。](./media/eshoponcontainers-development-architecture.png)

**图 2-2**。 eShopOnContainers 参考应用程序开发体系结构。

可以从通过 HTTPS 访问应用程序的 web 或移动客户端访问 eShopOnContainers 应用程序，该应用程序针对的是 ASP.NET Core MVC 服务器应用程序或相应的 API 网关。 API 网关提供多种优势，例如将后端服务与单个前端客户端分离并提供更好的安全性。 应用程序还使用称为后端的相关模式 (BFF) ，这建议为每个前端客户端创建单独的 API 网关。 参考体系结构演示了如何根据请求是来自 web 客户端还是移动客户端来细分 API 网关。

应用程序的功能分为多个不同的微服务。 有一些服务负责身份验证和标识、列出产品目录中的项目、管理用户的购物篮和订购订单。 每个单独的服务都有自己的持久存储。 不存在所有服务都与之进行交互的单个主数据存储。 相反，服务之间的协调和通信是按需执行的，而是通过使用消息总线来完成的。

每个不同的微服务根据其各自的需求进行了不同的设计。 此方面意味着它们的技术堆栈可能会有所不同，不过它们都是使用 .NET 构建的，并且是针对云设计的。 更简单的服务提供基本的创建-读取-更新-删除 (CRUD) 对基础数据存储区的访问，而更高级的服务则使用 Domain-Driven 设计方法和模式来管理业务复杂性。

![不同类型的微服务](./media/different-kinds-of-microservices.png)

**图 2-3**。 不同类型的微服务。

## <a name="overview-of-the-code"></a>代码概述

由于它使用微服务，eShopOnContainers 应用在其 GitHub 存储库中包含非常多的单独项目和解决方案。 除了单独的解决方案和可执行文件，各种服务还设计为在本地开发期间和在生产环境中运行时，在其自己的容器中运行。 图2-4 显示了完整的 Visual Studio 解决方案，其中组织了各种不同的项目。

![Visual Studio 解决方案中的项目。](./media/projects-in-visual-studio-solution.png)

**图 2-4**。 Visual Studio 解决方案中的项目。

对代码进行组织以支持不同的微服务，并在每个微服务中将代码分解为域逻辑、基础结构问题、用户界面或服务终结点。 在许多情况下，每个服务的依赖项可由 Azure 服务在生产环境中实现，而备用选项用于本地开发。 让我们看看应用程序的需求如何映射到 Azure 服务。

## <a name="understanding-microservices"></a>了解微服务

本书重点介绍使用 Azure 技术构建的云本机应用程序。 若要详细了解微服务最佳实践和如何构建基于微服务的应用程序，请阅读 [适用于容器化 .Net 应用程序的 .Net 微服务：架构](https://dotnet.microsoft.com/download/thank-you/microservices-architecture-ebook)。

>[!div class="step-by-step"]
>[上一页](candidate-apps.md)
>[下一页](map-eshoponcontainers-azure-services.md)
