---
title: 将 Razor Pages 与 ASP.NET MVC 进行比较
description: Razor Pages 提供了一种更好的方式来组织责任，而不是将传统 MVC 视图用于基于页面的应用。 了解如何与本部分中的传统 ASP.NET MVC 方法进行比较。
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: c188e7336e129fa710002081f1bef1f635cbe1fd
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102401091"
---
# <a name="compare-razor-pages-to-aspnet-mvc"></a>将 Razor Pages 与 ASP.NET MVC 进行比较

Razor Pages 是在 ASP.NET Core 中创建基于页面或基于窗体的应用程序的首选方法。 从这些 [文档](/aspnet/core/razor-pages/)开始，"Razor Pages 可以使编码的以页面为中心的方案更简单、更高效，而不是使用控制器和视图。" 如果 ASP.NET MVC 应用大量使用视图，则可能需要考虑从操作和视图迁移到 Razor Pages。

典型的基于强类型化视图的 MVC 应用将使用控制器来包含一个或多个操作。 控制器将与域或数据模型交互，并创建 viewmodel 类的实例。 然后，此 viewmodel 类将传递到与该操作关联的视图。 使用此方法与 MVC 应用的默认文件夹结构结合，若要向应用程序添加新页面，需要修改一个文件夹中的控制器、另一个文件夹中嵌套子文件夹中的视图，以及另一个文件夹中的 viewmodel。

Razor Pages 将 (的操作组合在一起，此时将 *处理程序*) ，并在一个类中调用一个名为 *PageModel* 的 viewmodel (，并将此类链接到名为 Razor 页面) 的视图。 所有 Razor Pages 进入 ASP.NET Core 项目根目录中的 " *页面* " 文件夹。 Razor Pages 在此文件夹中根据其名称和位置使用路由约定。 处理程序的行为与操作方法完全相同，但其名称中处理的 HTTP 谓词 (例如 `OnGet`) 。 它们也不一定需要返回，因为在默认情况下，它们会返回与其关联的页面。 这往往会使 Razor Pages 及其处理程序更小、更集中，同时可以更轻松地查找和处理添加或修改应用程序的特定部分所需的所有文件。

作为从 ASP.NET MVC 迁移到 ASP.NET Core 的一部分，团队应考虑是否要将控制器和视图迁移到 ASP.NET Core 控制器和视图，或者 Razor Pages。 前者极有可能需要稍微不太重要的工作，但不允许团队利用通过传统的基于视图的文件组织 Razor Pages 的好处。

## <a name="references"></a>参考

- [ASP.NET Core 中的 Razor 页面介绍](/aspnet/core/razor-pages/)
- [更简单 ASP.NET Core 应用 Razor Pages](/archive/msdn-magazine/2017/september/asp-net-core-simpler-asp-net-mvc-apps-with-razor-pages)

>[!div class="step-by-step"]
>[上一页](routing-differences.md)
>[下一页](webapi-differences.md)
