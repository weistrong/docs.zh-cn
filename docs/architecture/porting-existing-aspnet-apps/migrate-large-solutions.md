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
# <a name="migrate-large-solutions-to-aspnet-core"></a>将大型解决方案迁移到 ASP.NET Core

[!INCLUDE [book-preview](../../../includes/book-preview.md)]

将大型解决方案从 .NET Framework 迁移到 .NET Core 需要进行一些规划。 必须在依赖依赖项的项目之前迁移或更新依赖项。 有一些工具可以识别依赖关系，并帮助你迁移到 .NET Core。 迁移时，可能会采用不同的策略，具体取决于应用及其范围和当前使用模式。 是同时迁移所有项目，还是一段时间与当前系统并行迁移？ 是否在新系统中包装当前系统，并以增量方式替换其功能？

在本章中，你将了解如何为大型解决方案创建迁移计划，如何使用工具来帮助进行迁移，以及要考虑迁移自身的某些策略。

## <a name="references"></a>参考

- [将大型 MVC 和 Web API 应用迁移到 .NET Core 时，哪些主题非常重要？](https://twitter.com/ardalis/status/1313669040859217921)
- [从 .NET Framework 移植到 .NET Core](../../core/porting/index.md)

>[!div class="step-by-step"]
>[上一页](testing-differences.md)
>[下一页](identify-migration-sequence.md)
