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
# <a name="compare-aspnet-identity-and-aspnet-core-identity"></a>比较 ASP.NET Identity 和 ASP.NET Core 标识

在 ASP.NET MVC 中，标识功能通常在 *App_Start* 文件夹的 *IdentityConfig.cs* 中进行配置。 查看现有应用程序中的配置方式，并将其与 *Startup.cs* 中 [ASP.NET Core 标识所需的配置](/aspnet/core/security/authentication/identity-configuration)进行比较。

ASP.NET Identity 是一种 API，它支持用户界面登录功能并管理用户、密码、配置文件数据、角色、声明、令牌、电子邮件确认等。 它支持 Facebook、Google、Microsoft 和 Twitter 等外部登录提供程序。

如果你的 ASP.NET MVC 应用正在使用 ASP.NET 成员身份，你会发现 [从 ASP.NET 成员身份验证迁移到 ASP.NET Core 2.0 标识](/aspnet/core/migration/proper-to-2x/membership-to-core-identity)的指南。 这主要是一种数据迁移练习，在这种情况下，您应该能够将 ASP.NET Core 标识与已迁移的用户记录一起使用。

如果你将 ASP.NET Identity 用户迁移到 ASP.NET Core 标识，你可能需要更新其密码哈希，或跟踪哪些密码是用新的 ASP.NET Core 标识方法或旧的 ASP.NET Identity 方法进行哈希处理的。 [Stack Overflow 上所述的这种方法](https://stackoverflow.com/a/57074910/13729) 提供了一些选项，用于在一段时间内迁移用户密码哈希，而不是一次迁移所有

与 ASP.NET Identity 相比，ASP.NET Core 标识的最大差异之一是需要在项目中包含的代码。 ASP.NET Core 标识现在作为 Razor 类库提供，这意味着其 UI 和逻辑均可从 NuGet 包获得。 可以通过 [将 ASP.NET Core 标识文件的基架](/aspnet/core/security/authentication/scaffold-identity) 来覆盖现有的 UI 和逻辑，但是，在这种情况下，只需基架要修改的页面，而不是每个页面都存在。

## <a name="migrate-from-owin--katana"></a>从 OWIN/Katana 迁移

以下资源提供了有关从 OWIN/Katana 迁移的一些指南：

- [迁移](/aspnet/core/migration/proper-to-2x/#globalasax-file-replacement)
- [Katana 到 ASPNET 5](https://devblogs.microsoft.com/aspnet/katana-asp-net-5-and-bridging-the-gap/)

## <a name="references"></a>参考

- [将身份验证和标识迁移到 ASP.NET Core](/aspnet/core/migration/identity)
- [ASP.NET Core 上的标识简介](/aspnet/core/security/authorization/introduction)
- [配置 ASP.NET Core 标识](/aspnet/core/security/authentication/identity-configuration)
- [ASP.NET Core 项目中的基架标识](/aspnet/core/security/authentication/scaffold-identity)

>[!div class="step-by-step"]
>[上一页](authentication-differences.md)
>[下一页](controller-differences.md)
