---
title: 将现有 ASP.NET 应用移植到 .NET Core
description: 该免费指南指导你将 ASP.NET MVC 和 Web API 应用转换为 ASP.NET Core。
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: 36c0cdbe03fb97ae82336d53e15be2108e9c6367
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "100488161"
---
# <a name="porting-existing-aspnet-apps-to-net-core"></a><span data-ttu-id="ddcc7-103">将现有 ASP.NET 应用移植到 .NET Core</span><span class="sxs-lookup"><span data-stu-id="ddcc7-103">Porting Existing ASP.NET Apps to .NET Core</span></span>

![封面图像](./media/index/porting-existing-aspnet-apps.png)

[!INCLUDE [book-preview](../../../includes/book-preview.md)]

<span data-ttu-id="ddcc7-105">发布者</span><span class="sxs-lookup"><span data-stu-id="ddcc7-105">PUBLISHED BY</span></span>

<span data-ttu-id="ddcc7-106">Microsoft 开发人员部门、.NET 和 Visual Studio 产品团队</span><span class="sxs-lookup"><span data-stu-id="ddcc7-106">Microsoft Developer Division, .NET, and Visual Studio product teams</span></span>

<span data-ttu-id="ddcc7-107">Microsoft Corporation 的一个部门</span><span class="sxs-lookup"><span data-stu-id="ddcc7-107">A division of Microsoft Corporation</span></span>

<span data-ttu-id="ddcc7-108">One Microsoft Way</span><span class="sxs-lookup"><span data-stu-id="ddcc7-108">One Microsoft Way</span></span>

<span data-ttu-id="ddcc7-109">Redmond, Washington 98052-6399</span><span class="sxs-lookup"><span data-stu-id="ddcc7-109">Redmond, Washington 98052-6399</span></span>

<span data-ttu-id="ddcc7-110">版权所有 &copy; 2020 Microsoft Corporation</span><span class="sxs-lookup"><span data-stu-id="ddcc7-110">Copyright &copy; 2020 by Microsoft Corporation</span></span>

<span data-ttu-id="ddcc7-111">保留所有权利。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-111">All rights reserved.</span></span> <span data-ttu-id="ddcc7-112">未经发布者书面许可，不得以任何形式或任何方式复制或传播本书中的任何内容。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-112">No part of this book's contents may be reproduced or transmitted in any form or by any means without the written permission of the publisher.</span></span>

<span data-ttu-id="ddcc7-113">本书“按原样”提供，表达作者的观点和看法。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-113">This book is provided "as-is" and expresses the author's views and opinions.</span></span> <span data-ttu-id="ddcc7-114">本书中表达的观点、看法和信息（包括 URL 和其他 Internet 网站引用）如有更改，恕不另行通知。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-114">The views, opinions, and information expressed in this book, including URL and other Internet website references, may change without notice.</span></span>

<span data-ttu-id="ddcc7-115">本书中提及的一些示例仅用于说明，纯属虚构。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-115">Some examples depicted herein are provided for illustration only and are fictitious.</span></span> <span data-ttu-id="ddcc7-116">不存在任何实际关联或联系，请勿妄加推断。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-116">No real association or connection is intended or should be inferred.</span></span>

<span data-ttu-id="ddcc7-117">Microsoft 和 <https://www.microsoft.com> 上“商标”网页列出的商标是 Microsoft 集团公司的商标。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-117">Microsoft and the trademarks listed at <https://www.microsoft.com> on the "Trademarks" webpage are trademarks of the Microsoft group of companies.</span></span>

<span data-ttu-id="ddcc7-118">Mac 和 macOS 是 Apple Inc. 的商标</span><span class="sxs-lookup"><span data-stu-id="ddcc7-118">Mac and macOS are trademarks of Apple Inc.</span></span>

<span data-ttu-id="ddcc7-119">Docker 的鲸鱼徽标是 Docker Inc. 的注册商标经许可方可使用。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-119">The Docker whale logo is a registered trademark of Docker, Inc. Used by permission.</span></span>

<span data-ttu-id="ddcc7-120">所有其他标记和徽标均为其各自所有者的财产。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-120">All other marks and logos are property of their respective owners.</span></span>

<span data-ttu-id="ddcc7-121">作者：</span><span class="sxs-lookup"><span data-stu-id="ddcc7-121">Authors:</span></span>

> <span data-ttu-id="ddcc7-122">Steve "ardalis" Smith，[Ardalis.com](https://ardalis.com) 软件设计师及培训师</span><span class="sxs-lookup"><span data-stu-id="ddcc7-122">**Steve "ardalis" Smith**, Software Architect and Trainer - [Ardalis.com](https://ardalis.com)</span></span>

<span data-ttu-id="ddcc7-123">参与者和审阅者：</span><span class="sxs-lookup"><span data-stu-id="ddcc7-123">Participants and Reviewers:</span></span>

> <span data-ttu-id="ddcc7-124">Nish Anil，Microsoft .NET 团队高级项目经理 </span><span class="sxs-lookup"><span data-stu-id="ddcc7-124">**Nish Anil**, Senior Program Manager, .NET team, Microsoft</span></span>

> <span data-ttu-id="ddcc7-125">Mike Rousos，Microsoft .NET 团队的首席软件工程师</span><span class="sxs-lookup"><span data-stu-id="ddcc7-125">**Mike Rousos**, Principal Software Engineer, .NET team, Microsoft</span></span>

> <span data-ttu-id="ddcc7-126">Scott Addie，Microsoft .NET 团队资深内容开发人员</span><span class="sxs-lookup"><span data-stu-id="ddcc7-126">**Scott Addie**, Senior Content Developer, .NET team, Microsoft</span></span>

> <span data-ttu-id="ddcc7-127">David Pine，Microsoft .NET 团队资深内容开发人员</span><span class="sxs-lookup"><span data-stu-id="ddcc7-127">**David Pine**, Senior Content Developer, .NET team, Microsoft</span></span>

## <a name="version"></a><span data-ttu-id="ddcc7-128">Version</span><span class="sxs-lookup"><span data-stu-id="ddcc7-128">Version</span></span>

<span data-ttu-id="ddcc7-129">本指南包含 .NET Core 3.1 和与 .NET Core 3.1 版本同步发布的相同技术“wave”（即 Azure 和其他第三方技术）相关的更新。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-129">This guide covers **.NET Core 3.1** and updates related to the same technology "wave" (that is, Azure and other third-party technologies) coinciding in time with the .NET Core 3.1 release.</span></span> <span data-ttu-id="ddcc7-130">从 .NET Core 3.1 更新到 .NET 5.0（下一版本）的过程相对简单，所需工作量要比从 .NET Framework 移植到 .NET Core 的工作量少得多。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-130">Updating from .NET Core 3.1 to .NET 5.0 (the next version) is relatively straightforward and certainly will require substantially less effort than porting from .NET Framework to .NET Core.</span></span> <span data-ttu-id="ddcc7-131">从 .NET Framework 4.x 迁移到 .NET 5.0 将类似于迁移到 .NET Core 3.1。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-131">Migrating from .NET Framework 4.x to .NET 5.0 will be similar to migrating to .NET Core 3.1.</span></span> <span data-ttu-id="ddcc7-132">有关详细信息，请参阅[选择正确的 .NET Core 版本](choose-net-core-version.md)。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-132">For more information, see [choosing the right .NET Core version](choose-net-core-version.md).</span></span>

## <a name="who-should-use-this-guide"></a><span data-ttu-id="ddcc7-133">本指南的目标读者</span><span class="sxs-lookup"><span data-stu-id="ddcc7-133">Who should use this guide</span></span>

<span data-ttu-id="ddcc7-134">本指南的受众是有意将为 ASP.NET MVC 和 Web API (.NET Framework 4.x) 编写的现有应用迁移到 .NET Core 的开发人员、开发组长和架构师。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-134">This guide's audience is developers, development leads, and architects who are interested in migrating their existing apps written for ASP.NET MVC and Web API (.NET Framework 4.x) to .NET Core.</span></span> <span data-ttu-id="ddcc7-135">ASP.NET Web Forms 开发人员将从本指南中受益，但还应参阅[面向 ASP.NET Web Forms 开发人员的 Blazor](https://docs.microsoft.com/dotnet/architecture/blazor-for-web-forms-developers/) 电子书。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-135">ASP.NET Web Forms developers will benefit from this guide but should also read the [Blazor for ASP.NET Web Forms Developers](https://docs.microsoft.com/dotnet/architecture/blazor-for-web-forms-developers/) e-book.</span></span>

<span data-ttu-id="ddcc7-136">第二受众是计划何时将应用迁移到 .NET Core 的技术决策者。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-136">A secondary audience is technical decision-makers planning when to move their apps to .NET Core.</span></span>

<span data-ttu-id="ddcc7-137">本书的目标受众是拥有在 ASP.NET MVC 和 Web API 上运行的现行大型应用的 .NET 开发人员。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-137">The target audience for this book is .NET developers with large, existing apps that run on ASP.NET MVC and Web API.</span></span> <span data-ttu-id="ddcc7-138">基于 ASP.NET Web Forms 构建的应用不在本书的关注范围之内，尽管很多对照 .NET Framework 和 .NET Core 的信息仍然相关。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-138">Apps built on ASP.NET Web Forms are outside of the focus of this book, though much of the information comparing .NET Framework and .NET Core may still be relevant.</span></span>

## <a name="how-you-can-use-this-guide"></a><span data-ttu-id="ddcc7-139">如何使用本指南</span><span class="sxs-lookup"><span data-stu-id="ddcc7-139">How you can use this guide</span></span>

<span data-ttu-id="ddcc7-140">你可以通读本书籍，因为我们希望很多读者都可以这样做。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-140">You can read this book straight through, as we expect many readers to do.</span></span> <span data-ttu-id="ddcc7-141">本书首先提供有关是否应移植应用的相关考量。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-141">This book will provide you first with considerations for whether you should port your app at all.</span></span> <span data-ttu-id="ddcc7-142">然后介绍 .NET Framework 与 .NET Core 之间的体系结构差异。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-142">That content is followed by architectural differences between .NET Framework and .NET Core.</span></span> <span data-ttu-id="ddcc7-143">之后将介绍随时间推移迁移大型解决方案的策略，以及如何移植实际应用。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-143">From there, you'll learn strategies for migrating a large solution over time and how to port a real app.</span></span> <span data-ttu-id="ddcc7-144">接下来，本书包含了一些部署方案，这些方案可满足运行不同应用时向用户显示为单个应用的需要。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-144">Next, the book includes deployment scenarios that address the need to run different apps while appearing as a single app to users.</span></span> <span data-ttu-id="ddcc7-145">最后给出了两个案例研究，其中介绍了从 ASP.NET MVC 迁移到 ASP.NET Core 的实际应用。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-145">The book concludes with two case studies describing real apps that have migrated from ASP.NET MVC to ASP.NET Core.</span></span>

<span data-ttu-id="ddcc7-146">无论是否选择从第一章开始，都可以参考这些章节来了解具体概念：</span><span class="sxs-lookup"><span data-stu-id="ddcc7-146">Whether or not you choose to start from the first chapter, you can reference any of these chapters to learn about specific concepts:</span></span>

- [<span data-ttu-id="ddcc7-147">体系结构差异</span><span class="sxs-lookup"><span data-stu-id="ddcc7-147">Architectural differences</span></span>](architectural-differences.md)
- [<span data-ttu-id="ddcc7-148">迁移大型解决方案</span><span class="sxs-lookup"><span data-stu-id="ddcc7-148">Migrate large solutions</span></span>](migrate-large-solutions.md)
- [<span data-ttu-id="ddcc7-149">示例迁移</span><span class="sxs-lookup"><span data-stu-id="ddcc7-149">Sample migration</span></span>](example-migration-eshop.md)
- [<span data-ttu-id="ddcc7-150">部署方案</span><span class="sxs-lookup"><span data-stu-id="ddcc7-150">Deployment scenarios</span></span>](deployment-scenarios.md)

<span data-ttu-id="ddcc7-151">本指南有 [PDF 格式](https://aka.ms/aspnet-porting-ebook)和在线版本。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-151">This guide is available both in [PDF form](https://aka.ms/aspnet-porting-ebook) and online.</span></span> <span data-ttu-id="ddcc7-152">欢迎随时将此文档或其在线版本的链接转发给你的团队，以确保对这些概念有共同的理解。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-152">Feel free to forward this document or links to its online version to your team to ensure a common understanding of these concepts.</span></span>

## <a name="send-your-feedback"></a><span data-ttu-id="ddcc7-153">提供你的反馈</span><span class="sxs-lookup"><span data-stu-id="ddcc7-153">Send your feedback</span></span>

<span data-ttu-id="ddcc7-154">我们正在不断完善本书和相关示例，欢迎你提供反馈！</span><span class="sxs-lookup"><span data-stu-id="ddcc7-154">This book and related samples are constantly evolving, so your feedback is welcomed!</span></span> <span data-ttu-id="ddcc7-155">如果对如何改进本书有任何建议，请使用 [GitHub 问题](https://github.com/dotnet/docs/issues)上任何页面底部的反馈部分进行反馈。</span><span class="sxs-lookup"><span data-stu-id="ddcc7-155">If you have comments about how this book can be improved, use the feedback section at the bottom of any page built on [GitHub issues](https://github.com/dotnet/docs/issues).</span></span>

>[!div class="step-by-step"]
>[<span data-ttu-id="ddcc7-156">下一页</span><span class="sxs-lookup"><span data-stu-id="ddcc7-156">Next</span></span>](introduction.md)
