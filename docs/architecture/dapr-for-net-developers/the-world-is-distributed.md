---
title: 世界 20,000 英尺范围内
description: 分布式应用程序的优点和挑战，同时探讨了单一和 SOA 方法。
author: robvet
ms.date: 02/07/2021
ms.openlocfilehash: b857355880c3942526d751312d98f2b822704759
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102401200"
---
# <a name="the-world-is-distributed"></a>世界 20,000 英尺范围内

只需问 "酷的孩子"： *现代、分布式系统正在进行，而单一应用程序已外出！*

但这并不是 "超酷儿童"。 企业架构师、企业架构师和敏锐开发人员在探索和评估新式分布式应用程序时，会回显这些想法。 许多人都购买了。 他们正在按照分布式微服务应用程序的原理、模式和做法设计新的和 replatforming 的现有企业应用程序。

但这种发展引发了许多问题 .。。

- 什么是分布式应用程序？
- 为什么他们会获得欢迎？
- 成本是多少？
- 重要的是，这是什么折衷因素？

首先，让我们倒带，看看过去15年。 在此期间，我们通常将应用程序构建为单一单一的单位。 图1-1 显示了此体系结构。

![整体体系结构。](./media/the-world-is-distributed/monolithic-design.png)

**图 1-1**。 整体体系结构。

请注意，用于排序、标识和营销的模块在单服务器进程中的执行方式。 应用程序数据存储在共享数据库中。 业务功能通过 HTML 和 RESTful 接口公开。

在许多方面，单一应用程序是 `straightforward` 。 它们非常简单：

- 构建
- 测试
- 部署
- 故障排除
- 垂直缩放 (向上扩展) 

但单一体系结构可能会带来重大挑战。

随着时间的推移，你可能会看到一个开始失去控制的点 .。。

- 单体架构已变得非常复杂，因此不会有任何人理解它。
- 您担心每个更改都会带来意想不到且昂贵的副作用。
- 新功能/修补程序的实现非常耗时且成本高昂。
- 即使是最小的更改，也需要完全部署整个应用程序-成本高昂且风险巨大。
- 一个不稳定的组件可能会损坏整个系统。
- 添加新的技术和框架并不是一个选项。
- 实现敏捷交付方法非常困难。
- 体系结构 erosion 在中将设置为代码库 deteriorates，其中包含永不结束的 "特殊情况"。
- 最终，顾问会提供，并告诉你重写它。

IT 专业人员调用此条件 `the Fear Cycle` 。 如果你已在技术业务中花费了很长时间，则很可能会遇到这种情况。 它很紧张，用完您的 IT 预算。 大多数预算都用来维护旧应用，而不是构建新的创新性解决方案。

企业需要，而不是担心 `speed and agility` 。 他们会寻找一种体系结构样式，使其能够快速响应市场状况。 他们需要即时更新和单独缩放实时应用程序的小区域。

在 [面向服务的体系结构](https://en.wikipedia.org/wiki/Service-oriented_architecture)（或）的基础上，最早尝试获得速度和灵活性 `SOA` 。 在此模型中，服务使用者和服务提供商通过中间件消息传送组件进行协作，通常称为 [企业服务总线](https://en.wikipedia.org/wiki/Enterprise_service_bus)，或 `ESB` 。 图1-2 显示了此体系结构。

![SOA.](./media/the-world-is-distributed/soa-basic.png)

**图 1-2**。 SOA 体系结构。

对于 SOA，已向 ESB 注册的集中式服务提供商。 将业务逻辑内置于 ESB 中以集成提供者和使用者。 然后，服务使用者可以使用 ESB 查找这些提供程序并与其通信。

尽管有 SOA 的承诺，但实现此方法通常会增加复杂性并引入瓶颈。 维护成本变得很高，ESB 中间件成本高昂。 服务倾向大。 它们通常是共享的依赖项和数据存储。 最终，Soa 通常会产生一个带有集中服务的 "分布式单一结构" 结构，这些服务可经受更改。

如今，许多组织通过采用分布式微服务体系结构方法生成系统来实现速度和灵活性。 图1-3 显示了使用分布式技术和实践构建的同一系统。

![分布式体系结构。](./media/the-world-is-distributed/distributed-design.png)

**图 1-3**。 分布式体系结构。

请注意如何在一组分布式服务中分解同一应用程序。 每个都是自包含的，并封装自己的代码、数据和依赖项。 每个部署在软件容器中并由容器 orchestrator 管理。 每个服务都拥有一个专用数据库，而不是由多个服务共享的单个数据库。 其他服务不能直接访问此数据库，只能获取通过拥有它的服务的公共 API 公开的数据。 请注意，某些服务需要完整的关系数据库，而另一些则是 NoSQL 数据存储。 购物篮服务将其状态存储在分布式键/值缓存中。 请注意入站流量如何通过 API 网关服务路由。 它负责将调用定向到服务并强制执行交叉切削问题。 最重要的是，应用程序充分利用了新式云平台中的可伸缩性、可用性和复原功能。

但尽管分布式服务可提供灵活性和速度，但它们却提供了不同的挑战。 请考虑以下事项 .。。

- 分布式服务如何相互发现并进行同步通信？
- 如何实现异步消息传送？
- 如何在事务中维护上下文信息？
- 如何才能灵活应对故障？
- 如何缩放以满足变动需求？
- 如何监视和观察它们？

对于上述每种挑战，都经常提供多种产品。 但会降低应用程序的产品差异，并使代码的可维护性和便携式成为一项挑战。

本书介绍了 Dapr。 Dapr 是分布式应用程序运行时。 它直接解决了分布式应用程序附带的许多挑战。 Dapr，它可能会对分布式应用程序开发产生深远的影响。

## <a name="summary"></a>总结

在本章中，我们讨论了分布式应用程序的采用。 我们与分布式服务的一种单一系统方法相对比。 考虑分布式方法时，我们指出了许多常见的难题。

现在，让我们 Dapr，让我们向你介绍新的。

>[!div class="step-by-step"]
>[上一页](foreword.md)
>[下一页](dapr-at-20000-feet.md)
