---
title: 使用 .NET 5 在 Windows 10 上对桌面应用进行现代化改造
description: 了解如何使用 .NET 5 对现有桌面应用进行现代化改造
ms.date: 01/06/2021
ms.openlocfilehash: de8a451b0598b5eabd99028d377c161dace61623
ms.sourcegitcommit: 632818f4b527e5bf3c48fc04e0c7f3b4bdb8a248
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/20/2021
ms.locfileid: "98615694"
---
# <a name="modernizing-desktop-apps-on-windows-10-with-net-5"></a><span data-ttu-id="a2022-103">使用 .NET 5 在 Windows 10 上对桌面应用进行现代化改造</span><span class="sxs-lookup"><span data-stu-id="a2022-103">Modernizing Desktop Apps on Windows 10 with .NET 5</span></span>

![显示“对桌面应用进行现代化改造”电子书封面的屏幕截图。](./media/modernizing-existing-desktop-apps-ebook-cover.png)

<span data-ttu-id="a2022-105">**版本 v1.0.1** - 已更新到 .NET 5</span><span class="sxs-lookup"><span data-stu-id="a2022-105">**EDITION v1.0.1** - Updated to .NET 5</span></span>

<span data-ttu-id="a2022-106">请参阅[更改记录](https://aka.ms/desktop-ebook-changelog)了解书籍更新和社区贡献。</span><span class="sxs-lookup"><span data-stu-id="a2022-106">Refer [changelog](https://aka.ms/desktop-ebook-changelog) for the book updates and community contributions.</span></span>

<span data-ttu-id="a2022-107">发布者</span><span class="sxs-lookup"><span data-stu-id="a2022-107">PUBLISHED BY</span></span>

<span data-ttu-id="a2022-108">Microsoft 开发人员部门、.NET 和 Visual Studio 产品团队</span><span class="sxs-lookup"><span data-stu-id="a2022-108">Microsoft Developer Division, .NET, and Visual Studio product teams</span></span>

<span data-ttu-id="a2022-109">Microsoft Corporation 的一个部门</span><span class="sxs-lookup"><span data-stu-id="a2022-109">A division of Microsoft Corporation</span></span>

<span data-ttu-id="a2022-110">One Microsoft Way</span><span class="sxs-lookup"><span data-stu-id="a2022-110">One Microsoft Way</span></span>

<span data-ttu-id="a2022-111">Redmond, Washington 98052-6399</span><span class="sxs-lookup"><span data-stu-id="a2022-111">Redmond, Washington 98052-6399</span></span>

<span data-ttu-id="a2022-112">版权所有 © 2021 Microsoft Corporation</span><span class="sxs-lookup"><span data-stu-id="a2022-112">Copyright © 2021 by Microsoft Corporation</span></span>

<span data-ttu-id="a2022-113">保留所有权利。</span><span class="sxs-lookup"><span data-stu-id="a2022-113">All rights reserved.</span></span> <span data-ttu-id="a2022-114">未经发布者书面许可，不得以任何形式或任何方式复制或传播本书中的任何内容。</span><span class="sxs-lookup"><span data-stu-id="a2022-114">No part of the contents of this book may be reproduced or transmitted in any form or by any means without the written permission of the publisher.</span></span>

<span data-ttu-id="a2022-115">本书“按原样”提供，表达作者的观点和看法。</span><span class="sxs-lookup"><span data-stu-id="a2022-115">This book is provided "as-is" and expresses the author's views and opinions.</span></span> <span data-ttu-id="a2022-116">本书中表达的观点、看法和信息（包括 URL 和其他 Internet 网站引用）如有更改，恕不另行通知。</span><span class="sxs-lookup"><span data-stu-id="a2022-116">The views, opinions, and information expressed in this book, including URL and other Internet website references, may change without notice.</span></span>

<span data-ttu-id="a2022-117">本书中提及的一些示例仅用于说明，纯属虚构。</span><span class="sxs-lookup"><span data-stu-id="a2022-117">Some examples depicted herein are provided for illustration only and are fictitious.</span></span> <span data-ttu-id="a2022-118">不存在任何实际关联或联系，请勿妄加推断。</span><span class="sxs-lookup"><span data-stu-id="a2022-118">No real association or connection is intended or should be inferred.</span></span>

<span data-ttu-id="a2022-119">Microsoft 和 <https://www.microsoft.com> 上“商标”网页列出的商标是 Microsoft 集团公司的商标。</span><span class="sxs-lookup"><span data-stu-id="a2022-119">Microsoft and the trademarks listed at <https://www.microsoft.com> on the "Trademarks" webpage are trademarks of the Microsoft group of companies.</span></span>

<span data-ttu-id="a2022-120">Mac 和 macOS 是 Apple Inc. 的商标</span><span class="sxs-lookup"><span data-stu-id="a2022-120">Mac and macOS are trademarks of Apple Inc.</span></span>

<span data-ttu-id="a2022-121">所有其他标记和徽标均为其各自所有者的财产。</span><span class="sxs-lookup"><span data-stu-id="a2022-121">All other marks and logos are property of their respective owners.</span></span>

<span data-ttu-id="a2022-122">合著者：</span><span class="sxs-lookup"><span data-stu-id="a2022-122">Co-Authors:</span></span>

> <span data-ttu-id="a2022-123">Microsoft .NET 团队项目经理 Olia Gavrysh </span><span class="sxs-lookup"><span data-stu-id="a2022-123">**Olia Gavrysh**, Program Manager, .NET team, Microsoft</span></span>

> <span data-ttu-id="a2022-124">Kabel 创新架构师 Miguel Angel Castejón Dominguez </span><span class="sxs-lookup"><span data-stu-id="a2022-124">**Miguel Angel Castejón Dominguez**, Innovation Architect, Kabel</span></span>

<span data-ttu-id="a2022-125">参与者和审阅者：</span><span class="sxs-lookup"><span data-stu-id="a2022-125">Participants and reviewers:</span></span>

> <span data-ttu-id="a2022-126">Microsoft .NET 团队高级项目经理 Maira Wenzel </span><span class="sxs-lookup"><span data-stu-id="a2022-126">**Maira Wenzel**, Senior Program Manager, .NET team, Microsoft</span></span>

> <span data-ttu-id="a2022-127">Microsoft .NET 文档团队高级内容开发人员 Andy De Gorge </span><span class="sxs-lookup"><span data-stu-id="a2022-127">**Andy De Gorge**, Senior Content Developer, .NET docs team, Microsoft</span></span>

> <span data-ttu-id="a2022-128">Microsoft Windows 开发人员平台团队高级项目经理 Miguel Ramos </span><span class="sxs-lookup"><span data-stu-id="a2022-128">**Miguel Ramos**, Senior Program Manager, Windows Developer Platform team, Microsoft</span></span>

> <span data-ttu-id="a2022-129">Microsoft Windows 开发人员平台团队首席项目经理 Adam Braden </span><span class="sxs-lookup"><span data-stu-id="a2022-129">**Adam Braden**, Principal Program Manager, Windows Developer Platform team, Microsoft</span></span>

> <span data-ttu-id="a2022-130">Microsoft Azure IoT 团队高级项目经理 Ricardo Minguez Pablos </span><span class="sxs-lookup"><span data-stu-id="a2022-130">**Ricardo Minguez Pablos**, Senior Program Manager, Azure IoT team, Microsoft</span></span>

> <span data-ttu-id="a2022-131">Nish Anil，Microsoft .NET 团队高级项目经理 </span><span class="sxs-lookup"><span data-stu-id="a2022-131">**Nish Anil**, Senior Program Manager, .NET team, Microsoft</span></span>

> <span data-ttu-id="a2022-132">Microsoft 高级产品营销经理 Beth Massi </span><span class="sxs-lookup"><span data-stu-id="a2022-132">**Beth Massi**, Senior Product Marketing Manager, Microsoft</span></span>

> <span data-ttu-id="a2022-133">Microsoft .NET 团队合作伙伴总监项目经理 Scott Hunter </span><span class="sxs-lookup"><span data-stu-id="a2022-133">**Scott Hunter**, Partner Director Program Manager, .NET team, Microsoft</span></span>

> <span data-ttu-id="a2022-134">Marta Fuentes Lara，Kabel </span><span class="sxs-lookup"><span data-stu-id="a2022-134">**Marta Fuentes Lara**, Kabel</span></span>

> <span data-ttu-id="a2022-135">Raúl Fernández de Córdoba，Kabel </span><span class="sxs-lookup"><span data-stu-id="a2022-135">**Raúl Fernández de Córdoba**, Kabel</span></span>

> <span data-ttu-id="a2022-136">Antonio Manuel Fernández Cantos，Kabel </span><span class="sxs-lookup"><span data-stu-id="a2022-136">**Antonio Manuel Fernández Cantos**, Kabel</span></span>

## <a name="introduction"></a><span data-ttu-id="a2022-137">介绍</span><span class="sxs-lookup"><span data-stu-id="a2022-137">Introduction</span></span>

<span data-ttu-id="a2022-138">本书介绍了可用于通过现代化路径移动现有桌面应用程序并合并最新的运行时、语言和平台功能的策略。</span><span class="sxs-lookup"><span data-stu-id="a2022-138">This book is about strategies you can adopt to move your existing desktop applications through the path of modernization and incorporate the latest runtime, language, and platform features.</span></span> <span data-ttu-id="a2022-139">你会发现，由于每个应用程序不同，并且你的要求和偏好也不同，因此没有独特的方法。</span><span class="sxs-lookup"><span data-stu-id="a2022-139">You'll discover that there's no unique recipe as each application is different, and so are your requirements and preferences.</span></span> <span data-ttu-id="a2022-140">好消息是有一些常用的方法可用于向应用程序添加新特性和功能。</span><span class="sxs-lookup"><span data-stu-id="a2022-140">The good news is that there are common approaches you can apply to add new features and capabilities to your applications.</span></span> <span data-ttu-id="a2022-141">其中一些方法甚至不需要对代码进行重大修改。</span><span class="sxs-lookup"><span data-stu-id="a2022-141">Some of them won't even require major modifications of your code.</span></span> <span data-ttu-id="a2022-142">本书介绍了所有这些功能在后台的工作原理，并说明了其实现机制。</span><span class="sxs-lookup"><span data-stu-id="a2022-142">In this book, we'll reveal how all those features work behind the scenes and explain the mechanics of their implementations.</span></span> <span data-ttu-id="a2022-143">此外，本书还详细介绍了一些对现有桌面应用程序进行现代化改造的常见场景，以便你可以找到发展项目的灵感。</span><span class="sxs-lookup"><span data-stu-id="a2022-143">Moreover, you'll find some common scenarios for modernizing existing desktop applications shown in detail so you can find inspiration for evolving your projects.</span></span>

<span data-ttu-id="a2022-144">Microsoft 对现有应用程序进行现代化改造的方法是让你能够灵活地创建自己的自定义路径。</span><span class="sxs-lookup"><span data-stu-id="a2022-144">Microsoft's approach to modernizing existing applications is to give you the flexibility to create your own customized path.</span></span> <span data-ttu-id="a2022-145">本书中所述的所有现代化策略多是独立的。</span><span class="sxs-lookup"><span data-stu-id="a2022-145">All the modernization strategies described in this book are mostly independent.</span></span> <span data-ttu-id="a2022-146">你可以选择与你的应用程序相关的策略，跳过对你不重要的其他策略。</span><span class="sxs-lookup"><span data-stu-id="a2022-146">You can choose ones that are relevant for your application and skip others that aren't important for you.</span></span> <span data-ttu-id="a2022-147">换句话说，你可以混合搭配策略以最好地满足你的应用程序需求。</span><span class="sxs-lookup"><span data-stu-id="a2022-147">In other words, you can mix and match the strategies to best address your application needs.</span></span>

## <a name="who-should-use-the-book"></a><span data-ttu-id="a2022-148">本书的目标读者</span><span class="sxs-lookup"><span data-stu-id="a2022-148">Who should use the book</span></span>

<span data-ttu-id="a2022-149">本书面向希望通过对现有 Windows 窗体和 WPF 桌面应用程序进行现代化改造以利用 .NET 和 Windows 10 好处的开发人员和解决方案架构师。</span><span class="sxs-lookup"><span data-stu-id="a2022-149">This book for developers and solution architects who want to modernize existing Windows Forms and WPF desktop applications to leverage the benefits of .NET and Windows 10.</span></span>

<span data-ttu-id="a2022-150">如果你是一位技术决策制定者（例如需要大致了解更新现有桌面应用程序的好处的企业架构师、开发主管或主管），你也可能会发现本书非常有用。</span><span class="sxs-lookup"><span data-stu-id="a2022-150">You might also find this book useful if you're a technical decision maker, such as an enterprise architect or a development lead or director who wants an overview of the benefits of updating existing desktop applications.</span></span>

## <a name="how-to-use-the-book"></a><span data-ttu-id="a2022-151">如何使用本书</span><span class="sxs-lookup"><span data-stu-id="a2022-151">How to use the book</span></span>

<span data-ttu-id="a2022-152">本书介绍了需要对现有应用程序进行现代化改造的原因，以及使用 NET 和 MSIX 对桌面应用进行现代化改造的具体好处。</span><span class="sxs-lookup"><span data-stu-id="a2022-152">This book addresses the "why"—why you might want to modernize your existing applications, and the specific benefits you get from using NET and MSIX to modernize your desktop apps.</span></span> <span data-ttu-id="a2022-153">本书的内容适用于架构师和技术决策者，他们只需大概了解，不需要实现和技术分步细节。</span><span class="sxs-lookup"><span data-stu-id="a2022-153">The content of the book is designed for architects and technical decision makers who want an overview, but who don't need to focus on implementation and technical, step-by-step details.</span></span>

<span data-ttu-id="a2022-154">不同的章节还提供了示例实现代码片段和屏幕截图，第 5 章专门介绍了示例应用程序的完整迁移过程。</span><span class="sxs-lookup"><span data-stu-id="a2022-154">Along the different chapters, sample implementation code snippets and screenshots are provided, with chapter 5 devoted to showcase a complete migration process for sample applications.</span></span>

## <a name="what-this-book-doesnt-cover"></a><span data-ttu-id="a2022-155">本书未涵盖的内容</span><span class="sxs-lookup"><span data-stu-id="a2022-155">What this book doesn't cover</span></span>

<span data-ttu-id="a2022-156">本书介绍了一些特定的场景（侧重于直接迁移场景），其中概述了利用现代化改造的好处且不需要重写代码的方法。</span><span class="sxs-lookup"><span data-stu-id="a2022-156">This book covers a specific subset of scenarios that are focused on lift-and-shift scenarios, outlining the way to gain the benefits of modernizing without the effort of rewriting code.</span></span>

<span data-ttu-id="a2022-157">本书并未介绍如何使用 .NET 从头开始开发新式应用程序，也未介绍 Windows 窗体和 WPF 使用入门。</span><span class="sxs-lookup"><span data-stu-id="a2022-157">This book isn't about developing modern applications with .NET from scratch or about getting started with Windows Forms and WPF.</span></span> <span data-ttu-id="a2022-158">它重点介绍如何通过最新的桌面开发技术来更新现有桌面应用程序。</span><span class="sxs-lookup"><span data-stu-id="a2022-158">It focuses on how you can update existing desktop applications with the latest technologies for desktop development.</span></span>

## <a name="samples-used-in-this-book"></a><span data-ttu-id="a2022-159">本书中使用的示例</span><span class="sxs-lookup"><span data-stu-id="a2022-159">Samples used in this book</span></span>

<span data-ttu-id="a2022-160">为了强调执行现代化改造所需的步骤，我们将使用名为 `eShopModernizing` 的示例应用程序。</span><span class="sxs-lookup"><span data-stu-id="a2022-160">To highlight the necessary steps to perform a modernization, we'll be using a sample application called `eShopModernizing`.</span></span> <span data-ttu-id="a2022-161">此应用程序有两种样式（Windows 窗体和 WPF），我们将分步介绍如何使用 .NET 针对这两种风格进行现代化改造。</span><span class="sxs-lookup"><span data-stu-id="a2022-161">This application has two flavors, Windows Forms and WPF, and we'll show a step-by-step process on how to perform the modernization on both of them to .NET.</span></span>

<span data-ttu-id="a2022-162">此外，在本书的 GitHub 存储库中，你会发现该过程的结果，如果你决定按照分步教程操作，则可以将其用作参考。</span><span class="sxs-lookup"><span data-stu-id="a2022-162">Also, on the GitHub repository for this book, you'll find the results of the process, which you can consult with if you decide to follow the step-by-step tutorial.</span></span>

## <a name="send-your-feedback"></a><span data-ttu-id="a2022-163">提供你的反馈</span><span class="sxs-lookup"><span data-stu-id="a2022-163">Send your feedback</span></span>

<span data-ttu-id="a2022-164">我们正在不断完善本书和相关示例，欢迎你提供反馈！</span><span class="sxs-lookup"><span data-stu-id="a2022-164">This book and related samples are constantly evolving, so your feedback is welcomed!</span></span> <span data-ttu-id="a2022-165">如果对如何改进本书有任何建议，请使用 [GitHub 问题](https://github.com/dotnet/docs/issues)上任何页面底部的反馈部分进行反馈。</span><span class="sxs-lookup"><span data-stu-id="a2022-165">If you have comments about how this book can be improved, use the feedback section at the bottom of any page built on [GitHub issues](https://github.com/dotnet/docs/issues).</span></span>

>[!div class="step-by-step"]
>[<span data-ttu-id="a2022-166">下一页</span><span class="sxs-lookup"><span data-stu-id="a2022-166">Next</span></span>](why-modern-applications.md)
