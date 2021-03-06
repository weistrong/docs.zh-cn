---
title: 比较 ASP.NET MVC 和 ASP.NET Core 中的 Razor 使用情况
description: Razor 在 ASP.NET MVC 和 ASP.NET Core 之间有何区别？
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: a9f7fa2e6b8c0c6bf61c743cf8c956b1ad09713c
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102401066"
---
# <a name="compare-razor-usage-in-aspnet-mvc-and-aspnet-core"></a>比较 ASP.NET MVC 和 ASP.NET Core 中的 Razor 使用情况

Razor 的基本语法在 ASP.NET MVC 和 ASP.NET Core 之间没有明显变化。 但是，在迁移时，应考虑某些差异，如 [标记帮助](/aspnet/core/mvc/views/tag-helpers/intro) 程序和 Razor Pages 的引入。 如果应用大量使用自定义 Razor 功能，请参阅 [ASP.NET Core 的 Razor 语法参考](/aspnet/core/razor-pages) ，了解迁移到 ASP.NET Core 时可能需要进行哪些更改。

## <a name="tag-helpers"></a>标记帮助程序

标记帮助程序使服务器端代码可以在 Razor 文件中参与创建和呈现 HTML 元素。 与 HTML 帮助程序相比，它们提供了许多优点，应尽可能地用于替代 HTML 帮助器。 它们提供 HTML 友好的开发体验，因为它们看起来像标准 HTML，并且大多数设计用于编辑 HTML 的工具都将忽略这些体验。 在 _Visual Studio_ 中，有丰富的 IntelliSense 支持，可用于创建带有标记帮助程序的 HTML 和 Razor 标记。 标记帮助程序可以从 Razor 文件中的声明性标记提供简单或复杂的行为。

## <a name="razor-pages"></a>Razor 页面

Razor Pages 提供对基于页面和窗体的应用的控制器、操作和视图的替代方法。 [Razor Pages 与本章前面部分的 ASP.NET MVC 进行比较](./comparing-razor-pages-aspnet-mvc.md)。

## <a name="references"></a>参考

- [从 ASP.NET MVC 迁移到 ASP.NET Core MVC：控制器和视图](/aspnet/core/migration/mvc#migrate-controllers-and-views)
- [ASP.NET Core 中的标记帮助程序](/aspnet/core/mvc/views/tag-helpers/intro)
- [ASP.NET Core 中的 Razor 页面介绍](/aspnet/core/razor-pages)
- [ASP.NET Core 的 Razor 语法参考](/aspnet/core/razor-pages)

>[!div class="step-by-step"]
>[上一页](controller-differences.md)
>[下一页](signalr-differences.md)
