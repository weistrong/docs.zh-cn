---
title: 在 ASP.NET MVC 和 ASP.NET Core 之间比较测试选项
description: ASP.NET MVC 应用和 ASP.NET Core 应用之间的测试有什么不同？
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: f0907d09df058c07ed993c251868f00bc28b0736
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102401056"
---
# <a name="compare-testing-options-between-aspnet-mvc-and-aspnet-core"></a>在 ASP.NET MVC 和 ASP.NET Core 之间比较测试选项

ASP.NET MVC 应用支持控制器的单元测试，但此方法通常省略许多 MVC 功能，如路由、授权、模型绑定、模型验证、筛选器等。 若要在控制器操作本身的逻辑中测试这些 MVC 功能，通常需要部署应用，然后使用 Selenium 等工具进行测试。 这些测试比不需要托管和运行整个应用的典型单元测试更昂贵、更脆弱且速度更慢。

[ASP.NET Core 控制器可以进行单元测试](/aspnet/core/mvc/controllers/testing) ，就像 ASP.NET MVC 控制器一样，但有相同的限制。 不过， [ASP.NET Core 还支持快速、易于创作的集成测试](/aspnet/core/test/integration-tests) 。 集成测试由 `TestHost` 类承载，通常在 `WebApplicationFactory` 可以重写或替换应用程序依赖项的自定义中进行配置。 例如，在集成测试过程中，应用程序将以不同的数据源为目标，并可能会替换使用虚设或 mock 实现发送电子邮件的服务。

ASP.NET MVC 和 Web API 不支持 ASP.NET Core 中提供的集成测试方案。 在任何迁移工作中，你都应该为新迁移的系统分配时间来编写一些集成测试，以确保它按预期运行，并继续执行此操作。 即使在迁移之前未编写 web 应用逻辑的测试，也应在移动到 ASP.NET Core 时，强烈考虑这样做。

## <a name="references"></a>参考

- [为 ASP.NET MVC 应用程序创建单元测试](/aspnet/mvc/overview/older-versions-1/unit-testing/creating-unit-tests-for-asp-net-mvc-applications-cs)
- [ASP.NET Core 中的单元测试控制器逻辑](/aspnet/core/mvc/controllers/testing)
- ASP.NET Core 中的集成测试  

>[!div class="step-by-step"]
>[上一页](signalr-differences.md)
>[下一页](migrate-large-solutions.md)
