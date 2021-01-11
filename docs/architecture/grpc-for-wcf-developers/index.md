---
title: 适用于 WCF 开发人员的 ASP.NET Core gRPC - 适用于 WCF 开发人员的 gRPC
description: 在适用于 WCF 开发人员的 ASP.NET Core 5.0 中构建 gRPC 服务的简介
ms.date: 01/06/2021
ms.openlocfilehash: 26cce6bb784c08a5b59623ff5882fcf2fbb9e9ac
ms.sourcegitcommit: 7ef96827b161ef3fcde75f79d839885632e26ef1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/07/2021
ms.locfileid: "97970188"
---
# <a name="aspnet-core-grpc-for-wcf-developers"></a><span data-ttu-id="83c1b-103">适用于 WCF 开发人员的 ASP.NET Core gRPC</span><span class="sxs-lookup"><span data-stu-id="83c1b-103">ASP.NET Core gRPC for WCF Developers</span></span>

![封面图像](./media/cover.png)

<span data-ttu-id="83c1b-105">EDITION v1.0.1 - 已更新到 ASP.NET Core 5.0</span><span class="sxs-lookup"><span data-stu-id="83c1b-105">EDITION v1.0.1 - Updated to ASP.NET Core 5.0</span></span>

<span data-ttu-id="83c1b-106">请参阅[更改记录](https://aka.ms/grpc-ebook-changelog)了解书籍更新和社区贡献。</span><span class="sxs-lookup"><span data-stu-id="83c1b-106">Refer [changelog](https://aka.ms/grpc-ebook-changelog) for the book updates and community contributions.</span></span>

<span data-ttu-id="83c1b-107">发布者</span><span class="sxs-lookup"><span data-stu-id="83c1b-107">PUBLISHED BY</span></span>

<span data-ttu-id="83c1b-108">Microsoft 开发人员部门、.NET 和 Visual Studio 产品团队</span><span class="sxs-lookup"><span data-stu-id="83c1b-108">Microsoft Developer Division, .NET, and Visual Studio product teams</span></span>

<span data-ttu-id="83c1b-109">Microsoft Corporation 的一个部门</span><span class="sxs-lookup"><span data-stu-id="83c1b-109">A division of Microsoft Corporation</span></span>

<span data-ttu-id="83c1b-110">One Microsoft Way</span><span class="sxs-lookup"><span data-stu-id="83c1b-110">One Microsoft Way</span></span>

<span data-ttu-id="83c1b-111">Redmond, Washington 98052-6399</span><span class="sxs-lookup"><span data-stu-id="83c1b-111">Redmond, Washington 98052-6399</span></span>

<span data-ttu-id="83c1b-112">版权所有 © 2021 Microsoft Corporation</span><span class="sxs-lookup"><span data-stu-id="83c1b-112">Copyright © 2021 by Microsoft Corporation</span></span>

<span data-ttu-id="83c1b-113">保留所有权利。</span><span class="sxs-lookup"><span data-stu-id="83c1b-113">All rights reserved.</span></span> <span data-ttu-id="83c1b-114">未经发布者书面许可，不得以任何形式或任何方式复制或传播本书中的任何内容。</span><span class="sxs-lookup"><span data-stu-id="83c1b-114">No part of the contents of this book may be reproduced or transmitted in any form or by any means without the written permission of the publisher.</span></span>

<span data-ttu-id="83c1b-115">本书“按原样”提供，表达作者的观点和看法。</span><span class="sxs-lookup"><span data-stu-id="83c1b-115">This book is provided "as-is" and expresses the author's views and opinions.</span></span> <span data-ttu-id="83c1b-116">本书中表达的观点、看法和信息（包括 URL 和其他 Internet 网站引用）如有更改，恕不另行通知。</span><span class="sxs-lookup"><span data-stu-id="83c1b-116">The views, opinions and information expressed in this book, including URL and other Internet website references, may change without notice.</span></span>

<span data-ttu-id="83c1b-117">本书中提及的一些示例仅用于说明，纯属虚构。</span><span class="sxs-lookup"><span data-stu-id="83c1b-117">Some examples depicted herein are provided for illustration only and are fictitious.</span></span> <span data-ttu-id="83c1b-118">不存在任何实际关联或联系，请勿妄加推断。</span><span class="sxs-lookup"><span data-stu-id="83c1b-118">No real association or connection is intended or should be inferred.</span></span>

<span data-ttu-id="83c1b-119">Microsoft 和 <https://www.microsoft.com> 上“商标”网页列出的商标是 Microsoft 集团公司的商标。</span><span class="sxs-lookup"><span data-stu-id="83c1b-119">Microsoft and the trademarks listed at <https://www.microsoft.com> on the "Trademarks" webpage are trademarks of the Microsoft group of companies.</span></span>

<span data-ttu-id="83c1b-120">Docker 的鲸鱼徽标是 Docker Inc. 的注册商标经许可方可使用。</span><span class="sxs-lookup"><span data-stu-id="83c1b-120">The Docker whale logo is a registered trademark of Docker, Inc. Used by permission.</span></span>

<span data-ttu-id="83c1b-121">所有其他标记和徽标均为其各自所有者的财产。</span><span class="sxs-lookup"><span data-stu-id="83c1b-121">All other marks and logos are property of their respective owners.</span></span>

<span data-ttu-id="83c1b-122">作者：</span><span class="sxs-lookup"><span data-stu-id="83c1b-122">Authors:</span></span>

> <span data-ttu-id="83c1b-123">**Mark Rendle** -首席技术官 - [视觉对象重新编码](https://visualrecode.com)</span><span class="sxs-lookup"><span data-stu-id="83c1b-123">**Mark Rendle** - Chief Technical Officer - [Visual Recode](https://visualrecode.com)</span></span>
>
> <span data-ttu-id="83c1b-124">**Miranda Steiner** - 技术作者</span><span class="sxs-lookup"><span data-stu-id="83c1b-124">**Miranda Steiner** - Technical Author</span></span>

<span data-ttu-id="83c1b-125">编辑器：</span><span class="sxs-lookup"><span data-stu-id="83c1b-125">Editor:</span></span>

> <span data-ttu-id="83c1b-126">**Maira Wenzel** - 资深内容开发人员 - Microsoft</span><span class="sxs-lookup"><span data-stu-id="83c1b-126">**Maira Wenzel** - Sr. Content Developer - Microsoft</span></span>

## <a name="introduction"></a><span data-ttu-id="83c1b-127">介绍</span><span class="sxs-lookup"><span data-stu-id="83c1b-127">Introduction</span></span>

<span data-ttu-id="83c1b-128">gRPC 是用于构建网络服务和分布式应用程序的新式框架。</span><span class="sxs-lookup"><span data-stu-id="83c1b-128">gRPC is a modern framework for building networked services and distributed applications.</span></span> <span data-ttu-id="83c1b-129">假设结合了 SOAP 跨平台互操作性的 Windows Communication Foundation (WCF) NetTCP 绑定的性能。</span><span class="sxs-lookup"><span data-stu-id="83c1b-129">Imagine the performance of Windows Communication Foundation (WCF) NetTCP bindings, combined with the cross-platform interoperability of SOAP.</span></span> <span data-ttu-id="83c1b-130">gRPC 建立在 HTTP/2 和 Protobuf 消息编码协议的基础上，在应用程序和服务之间提供高性能、低带宽的通信。</span><span class="sxs-lookup"><span data-stu-id="83c1b-130">gRPC builds on HTTP/2 and the Protobuf message-encoding protocol to provide high performance, low-bandwidth communication between applications and services.</span></span> <span data-ttu-id="83c1b-131">它支持跨最常用的编程语言和平台（包括 .NET、Java、Python、Node.js、Go、C++）生成服务器和客户端代码。</span><span class="sxs-lookup"><span data-stu-id="83c1b-131">It supports server and client code generation across most popular programming languages and platforms, including .NET, Java, Python, Node.js, Go, and C++.</span></span> <span data-ttu-id="83c1b-132">凭借对 ASP.NET Core 5.0 中的 gRPC 的卓越支持，外加适用于 .NET Framework 4.x 的现有 gRPC 工具和库，WCF 是希望在组织中采用 .NET 的开发团队的一种很好的替代方法。</span><span class="sxs-lookup"><span data-stu-id="83c1b-132">With the first-class support for gRPC in ASP.NET Core 5.0, alongside the existing gRPC tools and libraries for .NET Framework 4.x, it's an excellent alternative to WCF for development teams looking to adopt .NET in their organizations.</span></span>

## <a name="who-should-use-this-guide"></a><span data-ttu-id="83c1b-133">本指南的目标读者</span><span class="sxs-lookup"><span data-stu-id="83c1b-133">Who should use this guide</span></span>

<span data-ttu-id="83c1b-134">本指南面向正在使用 .NET Framework 或 .NET、以前使用过 WCF 并且正在寻求将应用程序迁移到 .NET Core 3.0 及更高版本的新式 RPC 环境中的开发人员。</span><span class="sxs-lookup"><span data-stu-id="83c1b-134">This guide was written for developers working in .NET Framework or .NET who have previously used WCF, and who are seeking to migrate their applications to a modern RPC environment for .NET Core 3.0 and later versions.</span></span> <span data-ttu-id="83c1b-135">更常见的情况是，如果你要升级或考虑升级到 .NET 5，并且想要使用内置的 gRPC 工具，则本指南非常有用。</span><span class="sxs-lookup"><span data-stu-id="83c1b-135">More generally, if you are upgrading, or considering upgrading, to .NET 5, and you want to use the built-in gRPC tools, this guide is also useful.</span></span>

## <a name="how-you-can-use-this-guide"></a><span data-ttu-id="83c1b-136">如何使用本指南</span><span class="sxs-lookup"><span data-stu-id="83c1b-136">How you can use this guide</span></span>

<span data-ttu-id="83c1b-137">这是在 ASP.NET Core 5.0 中构建 gRPC 服务的简短介绍，还将 WCF 作为类似平台进行了介绍。</span><span class="sxs-lookup"><span data-stu-id="83c1b-137">This is a short introduction to building gRPC Services in ASP.NET Core 5.0, with particular reference to WCF as an analogous platform.</span></span> <span data-ttu-id="83c1b-138">它解释了 gRPC 的原理，将每个概念与 WCF 的等效功能相关联，并提供了有关将现有 WCF 应用程序迁移到 gRPC 的指导。</span><span class="sxs-lookup"><span data-stu-id="83c1b-138">It explains the principles of gRPC, relating each concept to the equivalent features of WCF, and offers guidance for migrating an existing WCF application to gRPC.</span></span> <span data-ttu-id="83c1b-139">对于具有 WCF 经验并想要学习通过 gRPC 构建新服务的开发人员来说，它也很有用。</span><span class="sxs-lookup"><span data-stu-id="83c1b-139">It's also useful for developers who have experience with WCF and are looking to learn gRPC to build new services.</span></span> <span data-ttu-id="83c1b-140">你可使用示例应用程序作为自己项目的模板或参考，并可随意复制和重复使用本书或其示例中的代码。</span><span class="sxs-lookup"><span data-stu-id="83c1b-140">You can use the sample applications as a template or reference for your own projects, and you are free to copy and reuse code from the book or its samples.</span></span>

<span data-ttu-id="83c1b-141">请将本指南转发到团队中，这有助于确保对这些注意事项和机会的共同理解。</span><span class="sxs-lookup"><span data-stu-id="83c1b-141">Feel free to forward this guide to your team to help ensure a common understanding of these considerations and opportunities.</span></span> <span data-ttu-id="83c1b-142">通过让每个人都使用同一组术语和基础原则，帮助确保构建模式和做法的一致应用。</span><span class="sxs-lookup"><span data-stu-id="83c1b-142">Having everybody working from a common set of terms and underlying principles helps ensure consistent application of architectural patterns and practices.</span></span>

## <a name="references"></a><span data-ttu-id="83c1b-143">reference</span><span class="sxs-lookup"><span data-stu-id="83c1b-143">References</span></span>

- <span data-ttu-id="83c1b-144">**gRPC 网站**
  <https://grpc.io></span><span class="sxs-lookup"><span data-stu-id="83c1b-144">**gRPC website**
<https://grpc.io></span></span>
- <span data-ttu-id="83c1b-145">**为服务器应用选择 .NET 5 或 .NET Framework**
  <https://docs.microsoft.com/dotnet/standard/choosing-core-framework-server></span><span class="sxs-lookup"><span data-stu-id="83c1b-145">**Choosing between .NET 5 and .NET Framework for server apps**
<https://docs.microsoft.com/dotnet/standard/choosing-core-framework-server></span></span>

>[!div class="step-by-step"]
>[<span data-ttu-id="83c1b-146">下一页</span><span class="sxs-lookup"><span data-stu-id="83c1b-146">Next</span></span>](introduction.md)
