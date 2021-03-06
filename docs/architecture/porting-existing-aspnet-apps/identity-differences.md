---
title: 比较 ASP.NET Identity 和 ASP.NET Core 标识
description: 本部分介绍 ASP.NET Identity 和 ASP.NET Core 标识之间的差异，这在规划从 .NET Framework 迁移到 .NET Core 时尤为重要。
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: 184c0e7c872b7676530b917727f380d6735ba10a
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102401080"
---
# <a name="compare-aspnet-identity-and-aspnet-core-identity"></a><span data-ttu-id="db345-103">比较 ASP.NET Identity 和 ASP.NET Core 标识</span><span class="sxs-lookup"><span data-stu-id="db345-103">Compare ASP.NET Identity and ASP.NET Core Identity</span></span>

<span data-ttu-id="db345-104">在 ASP.NET MVC 中，标识功能通常在 *App_Start* 文件夹的 *IdentityConfig.cs* 中进行配置。</span><span class="sxs-lookup"><span data-stu-id="db345-104">In ASP.NET MVC, identity features are typically configured in *IdentityConfig.cs* in the *App_Start* folder.</span></span> <span data-ttu-id="db345-105">查看现有应用程序中的配置方式，并将其与 *Startup.cs* 中 [ASP.NET Core 标识所需的配置](/aspnet/core/security/authentication/identity-configuration)进行比较。</span><span class="sxs-lookup"><span data-stu-id="db345-105">Review how this is configured in the existing app, and compare it to the [configuration required for ASP.NET Core Identity](/aspnet/core/security/authentication/identity-configuration) in *Startup.cs*.</span></span>

<span data-ttu-id="db345-106">ASP.NET Identity 是一种 API，它支持用户界面登录功能并管理用户、密码、配置文件数据、角色、声明、令牌、电子邮件确认等。</span><span class="sxs-lookup"><span data-stu-id="db345-106">ASP.NET Identity is an API that supports user interface login functionality and manages users, passwords, profile data, roles, claims, tokens, email confirmations, and more.</span></span> <span data-ttu-id="db345-107">它支持 Facebook、Google、Microsoft 和 Twitter 等外部登录提供程序。</span><span class="sxs-lookup"><span data-stu-id="db345-107">It supports external login providers like Facebook, Google, Microsoft, and Twitter.</span></span>

<span data-ttu-id="db345-108">如果你的 ASP.NET MVC 应用正在使用 ASP.NET 成员身份，你会发现 [从 ASP.NET 成员身份验证迁移到 ASP.NET Core 2.0 标识](/aspnet/core/migration/proper-to-2x/membership-to-core-identity)的指南。</span><span class="sxs-lookup"><span data-stu-id="db345-108">If your ASP.NET MVC app is using ASP.NET Membership, you'll find a guide to [migrate from ASP.NET Membership authentication to ASP.NET Core 2.0 Identity](/aspnet/core/migration/proper-to-2x/membership-to-core-identity).</span></span> <span data-ttu-id="db345-109">这主要是一种数据迁移练习，在这种情况下，您应该能够将 ASP.NET Core 标识与已迁移的用户记录一起使用。</span><span class="sxs-lookup"><span data-stu-id="db345-109">This is mainly a data migration exercise, at the completion of which you should be able to use ASP.NET Core Identity with your migrated user records.</span></span>

<span data-ttu-id="db345-110">如果你将 ASP.NET Identity 用户迁移到 ASP.NET Core 标识，你可能需要更新其密码哈希，或跟踪哪些密码是用新的 ASP.NET Core 标识方法或旧的 ASP.NET Identity 方法进行哈希处理的。</span><span class="sxs-lookup"><span data-stu-id="db345-110">If you migrate your ASP.NET Identity users to ASP.NET Core Identity, you may need to update their password hashes, or track which passwords are hashed with the new ASP.NET Core Identity approach or the older ASP.NET Identity approach.</span></span> <span data-ttu-id="db345-111">[Stack Overflow 上所述的这种方法](https://stackoverflow.com/a/57074910/13729) 提供了一些选项，用于在一段时间内迁移用户密码哈希，而不是一次迁移所有</span><span class="sxs-lookup"><span data-stu-id="db345-111">[This approach described on Stack Overflow](https://stackoverflow.com/a/57074910/13729) provides some options for migrating user password hashes over time, rather than all at once.</span></span>

<span data-ttu-id="db345-112">与 ASP.NET Identity 相比，ASP.NET Core 标识的最大差异之一是需要在项目中包含的代码。</span><span class="sxs-lookup"><span data-stu-id="db345-112">One of the biggest differences when it comes to ASP.NET Core Identity compared to ASP.NET Identity is how little code you need to include in your project.</span></span> <span data-ttu-id="db345-113">ASP.NET Core 标识现在作为 Razor 类库提供，这意味着其 UI 和逻辑均可从 NuGet 包获得。</span><span class="sxs-lookup"><span data-stu-id="db345-113">ASP.NET Core Identity now ships as a Razor Class Library, meaning its UI and logic are all available from a NuGet package.</span></span> <span data-ttu-id="db345-114">可以通过 [将 ASP.NET Core 标识文件的基架](/aspnet/core/security/authentication/scaffold-identity) 来覆盖现有的 UI 和逻辑，但是，在这种情况下，只需基架要修改的页面，而不是每个页面都存在。</span><span class="sxs-lookup"><span data-stu-id="db345-114">You can override the existing UI and logic by [scaffolding the ASP.NET Core Identity files](/aspnet/core/security/authentication/scaffold-identity) but even in this case you need only scaffold the pages you want to modify, not every one that exists.</span></span>

## <a name="migrate-from-owin--katana"></a><span data-ttu-id="db345-115">从 OWIN/Katana 迁移</span><span class="sxs-lookup"><span data-stu-id="db345-115">Migrate from OWIN / Katana</span></span>

<span data-ttu-id="db345-116">以下资源提供了有关从 OWIN/Katana 迁移的一些指南：</span><span class="sxs-lookup"><span data-stu-id="db345-116">The following resources offer some guidance for migrating from OWIN / Katana:</span></span>

- [<span data-ttu-id="db345-117">迁移</span><span class="sxs-lookup"><span data-stu-id="db345-117">Migration</span></span>](/aspnet/core/migration/proper-to-2x/#globalasax-file-replacement)
- [<span data-ttu-id="db345-118">Katana 到 ASPNET 5</span><span class="sxs-lookup"><span data-stu-id="db345-118">Katana to ASPNET 5</span></span>](https://devblogs.microsoft.com/aspnet/katana-asp-net-5-and-bridging-the-gap/)

## <a name="references"></a><span data-ttu-id="db345-119">参考</span><span class="sxs-lookup"><span data-stu-id="db345-119">References</span></span>

- [<span data-ttu-id="db345-120">将身份验证和标识迁移到 ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="db345-120">Migrate Authentication and Identity to ASP.NET Core</span></span>](/aspnet/core/migration/identity)
- [<span data-ttu-id="db345-121">ASP.NET Core 上的标识简介</span><span class="sxs-lookup"><span data-stu-id="db345-121">Introduction to Identity on ASP.NET Core</span></span>](/aspnet/core/security/authorization/introduction)
- [<span data-ttu-id="db345-122">配置 ASP.NET Core 标识</span><span class="sxs-lookup"><span data-stu-id="db345-122">Configure ASP.NET Core Identity</span></span>](/aspnet/core/security/authentication/identity-configuration)
- [<span data-ttu-id="db345-123">ASP.NET Core 项目中的基架标识</span><span class="sxs-lookup"><span data-stu-id="db345-123">Scaffold Identity in ASP.NET Core projects</span></span>](/aspnet/core/security/authentication/scaffold-identity)

>[!div class="step-by-step"]
><span data-ttu-id="db345-124">[上一页](authentication-differences.md)
>[下一页](controller-differences.md)</span><span class="sxs-lookup"><span data-stu-id="db345-124">[Previous](authentication-differences.md)
[Next](controller-differences.md)</span></span>
