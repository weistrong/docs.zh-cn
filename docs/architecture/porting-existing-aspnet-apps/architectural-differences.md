---
title: ASP.NET MVC 和 ASP.NET Core 之间的体系结构差异
description: 查看 ASP.NET 与 ASP.NET Core 之间的体系结构差异。
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: 96477f2393482380eee9891e9b2dbbb6445e15bd
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102401100"
---
# <a name="architectural-differences-between-aspnet-mvc-and-aspnet-core"></a>ASP.NET MVC 和 ASP.NET Core 之间的体系结构差异

[!INCLUDE [book-preview](../../../includes/book-preview.md)]

.NET Framework 和 ASP.NET Core 上的 ASP.NET MVC 之间存在许多不同的体系结构差异。 当团队评估将 ASP.NET MVC 应用程序迁移到 ASP.NET Core 所涉及的工作时，必须广泛地了解这些差异。 本章介绍 ASP.NET Core 与 ASP.NET MVC 明显不同的各种方式。

## <a name="breaking-changes"></a>中断性变更

.NET Core 是一种跨平台的 .NET Framework 重写。 [这两个框架之间](../../core/compatibility/fx-core.md)存在很多重大更改。 以下各节介绍了如何设计和开发 ASP.NET MVC 和 ASP.NET Core 应用程序之间的具体差异。 请注意，还应查看相关文档，确定所使用的框架库可能需要更改。 在许多情况下，可以使用替代 NuGet 包来填充 .NET Framework 与 .NET Core 之间留下的任何空白。 在极少数情况下，可能需要找到第三方解决方案或实现新的自定义代码来解决不兼容问题。

>[!div class="step-by-step"]
>[上一页](additional-migration-resources.md)
>[下一页](app-startup-differences.md)
