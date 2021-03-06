---
title: 将大型解决方案迁移到 ASP.NET Core
description: 介绍如何将大型 ASP.NET MVC 应用迁移到 ASP.NET Core。
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: d3ebd71213e074ce80dc83fc3230c4e365275ad3
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102401069"
---
# <a name="migrate-large-solutions-to-aspnet-core"></a><span data-ttu-id="a3c08-103">将大型解决方案迁移到 ASP.NET Core</span><span class="sxs-lookup"><span data-stu-id="a3c08-103">Migrate large solutions to ASP.NET Core</span></span>

[!INCLUDE [book-preview](../../../includes/book-preview.md)]

<span data-ttu-id="a3c08-104">将大型解决方案从 .NET Framework 迁移到 .NET Core 需要进行一些规划。</span><span class="sxs-lookup"><span data-stu-id="a3c08-104">Migrating large solutions from .NET Framework to .NET Core requires some planning.</span></span> <span data-ttu-id="a3c08-105">必须在依赖依赖项的项目之前迁移或更新依赖项。</span><span class="sxs-lookup"><span data-stu-id="a3c08-105">Dependencies must be migrated or updated before the projects that depend on them.</span></span> <span data-ttu-id="a3c08-106">有一些工具可以识别依赖关系，并帮助你迁移到 .NET Core。</span><span class="sxs-lookup"><span data-stu-id="a3c08-106">There are tools that can identify dependencies and offer help with migrating to .NET Core.</span></span> <span data-ttu-id="a3c08-107">迁移时，可能会采用不同的策略，具体取决于应用及其范围和当前使用模式。</span><span class="sxs-lookup"><span data-stu-id="a3c08-107">Depending on the app, its scope, and current usage patterns, different strategies may be employed when migrating.</span></span> <span data-ttu-id="a3c08-108">是同时迁移所有项目，还是一段时间与当前系统并行迁移？</span><span class="sxs-lookup"><span data-stu-id="a3c08-108">Do you migrate it all at once, or over time, side-by-side with the current system?</span></span> <span data-ttu-id="a3c08-109">是否在新系统中包装当前系统，并以增量方式替换其功能？</span><span class="sxs-lookup"><span data-stu-id="a3c08-109">Do you wrap the current system in the new one, and incrementally replace its functionality?</span></span>

<span data-ttu-id="a3c08-110">在本章中，你将了解如何为大型解决方案创建迁移计划，如何使用工具来帮助进行迁移，以及要考虑迁移自身的某些策略。</span><span class="sxs-lookup"><span data-stu-id="a3c08-110">In this chapter, you'll learn how create a migration plan for a large solution, how to use tools to help with the migration, and some strategies to consider for the migration itself.</span></span>

## <a name="references"></a><span data-ttu-id="a3c08-111">参考</span><span class="sxs-lookup"><span data-stu-id="a3c08-111">References</span></span>

- [<span data-ttu-id="a3c08-112">将大型 MVC 和 Web API 应用迁移到 .NET Core 时，哪些主题非常重要？</span><span class="sxs-lookup"><span data-stu-id="a3c08-112">What topics are important to migrating large MVC and Web API apps to .NET Core?</span></span>](https://twitter.com/ardalis/status/1313669040859217921)
- [<span data-ttu-id="a3c08-113">从 .NET Framework 移植到 .NET Core</span><span class="sxs-lookup"><span data-stu-id="a3c08-113">Porting from .NET Framework to .NET Core</span></span>](../../core/porting/index.md)

>[!div class="step-by-step"]
><span data-ttu-id="a3c08-114">[上一页](testing-differences.md)
>[下一页](identify-migration-sequence.md)</span><span class="sxs-lookup"><span data-stu-id="a3c08-114">[Previous](testing-differences.md)
[Next](identify-migration-sequence.md)</span></span>
