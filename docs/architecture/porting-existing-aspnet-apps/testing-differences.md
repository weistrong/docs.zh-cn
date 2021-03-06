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
# <a name="compare-testing-options-between-aspnet-mvc-and-aspnet-core"></a><span data-ttu-id="03eb4-103">在 ASP.NET MVC 和 ASP.NET Core 之间比较测试选项</span><span class="sxs-lookup"><span data-stu-id="03eb4-103">Compare testing options between ASP.NET MVC and ASP.NET Core</span></span>

<span data-ttu-id="03eb4-104">ASP.NET MVC 应用支持控制器的单元测试，但此方法通常省略许多 MVC 功能，如路由、授权、模型绑定、模型验证、筛选器等。</span><span class="sxs-lookup"><span data-stu-id="03eb4-104">ASP.NET MVC apps support unit testing of controllers, but this approach often omits many MVC features like routing, authorization, model binding, model validation, filters, and more.</span></span> <span data-ttu-id="03eb4-105">若要在控制器操作本身的逻辑中测试这些 MVC 功能，通常需要部署应用，然后使用 Selenium 等工具进行测试。</span><span class="sxs-lookup"><span data-stu-id="03eb4-105">To test these MVC features in addition to the logic within the controller action itself, frequently the app would need to be deployed and then tested with a tool like Selenium.</span></span> <span data-ttu-id="03eb4-106">这些测试比不需要托管和运行整个应用的典型单元测试更昂贵、更脆弱且速度更慢。</span><span class="sxs-lookup"><span data-stu-id="03eb4-106">These tests are substantially more expensive, more brittle, and slower than typical unit tests that can be run without the need for hosting and running the entire app.</span></span>

<span data-ttu-id="03eb4-107">[ASP.NET Core 控制器可以进行单元测试](/aspnet/core/mvc/controllers/testing) ，就像 ASP.NET MVC 控制器一样，但有相同的限制。</span><span class="sxs-lookup"><span data-stu-id="03eb4-107">[ASP.NET Core controllers can be unit tested](/aspnet/core/mvc/controllers/testing) just like ASP.NET MVC controllers, but with the same limitations.</span></span> <span data-ttu-id="03eb4-108">不过， [ASP.NET Core 还支持快速、易于创作的集成测试](/aspnet/core/test/integration-tests) 。</span><span class="sxs-lookup"><span data-stu-id="03eb4-108">However, [ASP.NET Core supports fast, easy-to-author integration tests](/aspnet/core/test/integration-tests) as well.</span></span> <span data-ttu-id="03eb4-109">集成测试由 `TestHost` 类承载，通常在 `WebApplicationFactory` 可以重写或替换应用程序依赖项的自定义中进行配置。</span><span class="sxs-lookup"><span data-stu-id="03eb4-109">Integration tests are hosted by a `TestHost` class and are typically configured in a custom `WebApplicationFactory` that can override or replace app dependencies.</span></span> <span data-ttu-id="03eb4-110">例如，在集成测试过程中，应用程序将以不同的数据源为目标，并可能会替换使用虚设或 mock 实现发送电子邮件的服务。</span><span class="sxs-lookup"><span data-stu-id="03eb4-110">For instance, frequently during integration tests the app will target a different data source and may replace services that send emails with fake or mock implementations.</span></span>

<span data-ttu-id="03eb4-111">ASP.NET MVC 和 Web API 不支持 ASP.NET Core 中提供的集成测试方案。</span><span class="sxs-lookup"><span data-stu-id="03eb4-111">ASP.NET MVC and Web API did not support anything like the integration testing scenarios available in ASP.NET Core.</span></span> <span data-ttu-id="03eb4-112">在任何迁移工作中，你都应该为新迁移的系统分配时间来编写一些集成测试，以确保它按预期运行，并继续执行此操作。</span><span class="sxs-lookup"><span data-stu-id="03eb4-112">In any migration effort, you should allocate time to write some integration tests for your newly migrated system to ensure it's working as expected and continues to do so.</span></span> <span data-ttu-id="03eb4-113">即使在迁移之前未编写 web 应用逻辑的测试，也应在移动到 ASP.NET Core 时，强烈考虑这样做。</span><span class="sxs-lookup"><span data-stu-id="03eb4-113">Even if you weren't writing tests of your web app logic before the migration, you should strongly consider doing so as you move to ASP.NET Core.</span></span>

## <a name="references"></a><span data-ttu-id="03eb4-114">参考</span><span class="sxs-lookup"><span data-stu-id="03eb4-114">References</span></span>

- [<span data-ttu-id="03eb4-115">为 ASP.NET MVC 应用程序创建单元测试</span><span class="sxs-lookup"><span data-stu-id="03eb4-115">Creating Unit Tests for ASP.NET MVC Applications</span></span>](/aspnet/mvc/overview/older-versions-1/unit-testing/creating-unit-tests-for-asp-net-mvc-applications-cs)
- [<span data-ttu-id="03eb4-116">ASP.NET Core 中的单元测试控制器逻辑</span><span class="sxs-lookup"><span data-stu-id="03eb4-116">Unit test controller logic in ASP.NET Core</span></span>](/aspnet/core/mvc/controllers/testing)
- <span data-ttu-id="03eb4-117">ASP.NET Core 中的集成测试  </span><span class="sxs-lookup"><span data-stu-id="03eb4-117">[Integration tests in ASP.NET Core](/aspnet/core/test/integration-tests)</span></span>

>[!div class="step-by-step"]
><span data-ttu-id="03eb4-118">[上一页](signalr-differences.md)
>[下一页](migrate-large-solutions.md)</span><span class="sxs-lookup"><span data-stu-id="03eb4-118">[Previous](signalr-differences.md)
[Next](migrate-large-solutions.md)</span></span>
