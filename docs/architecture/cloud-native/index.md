---
title: 为 Azure 构建云本机 .NET 应用程序
description: 构建利用 Azure 的容器、微服务和无服务器功能的云本机应用程序的指南。
author: ardalis
ms.date: 01/19/2021
ms.openlocfilehash: ad641517f9dc24aed9180cf6a092f4754739bceb
ms.sourcegitcommit: f2ab02d9a780819ca2e5310bbcf5cfe5b7993041
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2021
ms.locfileid: "99506118"
---
# <a name="architecting-cloud-native-net-applications-for-azure"></a><span data-ttu-id="a0355-103">为 Azure 构建云本机 .NET 应用程序</span><span class="sxs-lookup"><span data-stu-id="a0355-103">Architecting Cloud Native .NET Applications for Azure</span></span>

![封面图像](./media/cover.png)

<span data-ttu-id="a0355-105">**版本 v1.0.2**</span><span class="sxs-lookup"><span data-stu-id="a0355-105">**EDITION v1.0.2**</span></span>

<span data-ttu-id="a0355-106">请参阅[更改记录](https://aka.ms/cn-ebook-changelog)了解书籍更新和社区贡献。</span><span class="sxs-lookup"><span data-stu-id="a0355-106">Refer [changelog](https://aka.ms/cn-ebook-changelog) for the book updates and community contributions.</span></span>

<span data-ttu-id="a0355-107">发布者</span><span class="sxs-lookup"><span data-stu-id="a0355-107">PUBLISHED BY</span></span>

<span data-ttu-id="a0355-108">Microsoft 开发人员部门、.NET 和 Visual Studio 产品团队</span><span class="sxs-lookup"><span data-stu-id="a0355-108">Microsoft Developer Division, .NET, and Visual Studio product teams</span></span>

<span data-ttu-id="a0355-109">Microsoft Corporation 的一个部门</span><span class="sxs-lookup"><span data-stu-id="a0355-109">A division of Microsoft Corporation</span></span>

<span data-ttu-id="a0355-110">One Microsoft Way</span><span class="sxs-lookup"><span data-stu-id="a0355-110">One Microsoft Way</span></span>

<span data-ttu-id="a0355-111">Redmond, Washington 98052-6399</span><span class="sxs-lookup"><span data-stu-id="a0355-111">Redmond, Washington 98052-6399</span></span>

<span data-ttu-id="a0355-112">版权所有 &copy; 2021 Microsoft Corporation</span><span class="sxs-lookup"><span data-stu-id="a0355-112">Copyright &copy; 2021 by Microsoft Corporation</span></span>

<span data-ttu-id="a0355-113">保留所有权利。</span><span class="sxs-lookup"><span data-stu-id="a0355-113">All rights reserved.</span></span> <span data-ttu-id="a0355-114">未经发布者书面许可，不得以任何形式或任何方式复制或传播本书中的任何内容。</span><span class="sxs-lookup"><span data-stu-id="a0355-114">No part of the contents of this book may be reproduced or transmitted in any form or by any means without the written permission of the publisher.</span></span>

<span data-ttu-id="a0355-115">本书“按原样”提供，表达作者的观点和看法。</span><span class="sxs-lookup"><span data-stu-id="a0355-115">This book is provided "as-is" and expresses the author's views and opinions.</span></span> <span data-ttu-id="a0355-116">本书中表达的观点、看法和信息（包括 URL 和其他 Internet 网站引用）如有更改，恕不另行通知。</span><span class="sxs-lookup"><span data-stu-id="a0355-116">The views, opinions, and information expressed in this book, including URL and other Internet website references, may change without notice.</span></span>

<span data-ttu-id="a0355-117">本书中提及的一些示例仅用于说明，纯属虚构。</span><span class="sxs-lookup"><span data-stu-id="a0355-117">Some examples depicted herein are provided for illustration only and are fictitious.</span></span> <span data-ttu-id="a0355-118">不存在任何实际关联或联系，请勿妄加推断。</span><span class="sxs-lookup"><span data-stu-id="a0355-118">No real association or connection is intended or should be inferred.</span></span>

<span data-ttu-id="a0355-119">Microsoft 和 <https://www.microsoft.com> 上“商标”网页列出的商标是 Microsoft 集团公司的商标。</span><span class="sxs-lookup"><span data-stu-id="a0355-119">Microsoft and the trademarks listed at <https://www.microsoft.com> on the "Trademarks" webpage are trademarks of the Microsoft group of companies.</span></span>

<span data-ttu-id="a0355-120">Mac 和 macOS 是 Apple Inc. 的商标</span><span class="sxs-lookup"><span data-stu-id="a0355-120">Mac and macOS are trademarks of Apple Inc.</span></span>

<span data-ttu-id="a0355-121">Docker 的鲸鱼徽标是 Docker Inc. 的注册商标经许可方可使用。</span><span class="sxs-lookup"><span data-stu-id="a0355-121">The Docker whale logo is a registered trademark of Docker, Inc. Used by permission.</span></span>

<span data-ttu-id="a0355-122">所有其他标记和徽标均为其各自所有者的财产。</span><span class="sxs-lookup"><span data-stu-id="a0355-122">All other marks and logos are property of their respective owners.</span></span>

<span data-ttu-id="a0355-123">作者：</span><span class="sxs-lookup"><span data-stu-id="a0355-123">Authors:</span></span>

> <span data-ttu-id="a0355-124">Rob Vettor，Microsoft 首席云系统架构师/IP 架构师 ([thinkingincloudnative.com](https://thinkingincloudnative.com/about/))</span><span class="sxs-lookup"><span data-stu-id="a0355-124">**Rob Vettor**, Principal Cloud System Architect/IP Architect - [thinkingincloudnative.com](https://thinkingincloudnative.com/about/), Microsoft</span></span>
>
> <span data-ttu-id="a0355-125">Steve "ardalis" Smith，[Ardalis.com](https://ardalis.com) 软件设计师及培训师</span><span class="sxs-lookup"><span data-stu-id="a0355-125">**Steve "ardalis" Smith**, Software Architect and Trainer - [Ardalis.com](https://ardalis.com)</span></span>

<span data-ttu-id="a0355-126">参与者和审阅者：</span><span class="sxs-lookup"><span data-stu-id="a0355-126">Participants and Reviewers:</span></span>

> <span data-ttu-id="a0355-127">**Cesar De Torre**，Microsoft .NET 团队首席项目经理</span><span class="sxs-lookup"><span data-stu-id="a0355-127">**Cesar De la Torre**, Principal Program Manager, .NET team, Microsoft</span></span>
>
> <span data-ttu-id="a0355-128">Nish Anil，Microsoft .NET 团队高级项目经理 </span><span class="sxs-lookup"><span data-stu-id="a0355-128">**Nish Anil**, Senior Program Manager, .NET team, Microsoft</span></span>
>
> <span data-ttu-id="a0355-129">Jeremy Likness，Microsoft .NET 团队高级项目经理</span><span class="sxs-lookup"><span data-stu-id="a0355-129">**Jeremy Likness**, Senior Program Manager, .NET team, Microsoft</span></span>
>
> <span data-ttu-id="a0355-130">Cecil Phillip，Microsoft 高级云大使</span><span class="sxs-lookup"><span data-stu-id="a0355-130">**Cecil Phillip**, Senior Cloud Advocate, Microsoft</span></span>
>
> <span data-ttu-id="a0355-131">Sumit Ghosh，Neudesic 的首席顾问</span><span class="sxs-lookup"><span data-stu-id="a0355-131">**Sumit Ghosh**, Principal Consultant at Neudesic</span></span>

<span data-ttu-id="a0355-132">编辑：</span><span class="sxs-lookup"><span data-stu-id="a0355-132">Editors:</span></span>

> <span data-ttu-id="a0355-133">Maira Wenzel，Microsoft .NET 团队高级项目经理</span><span class="sxs-lookup"><span data-stu-id="a0355-133">**Maira Wenzel**, Program Manager, .NET team, Microsoft</span></span>

> <span data-ttu-id="a0355-134">Microsoft .NET 文档资深内容开发人员 David Pine</span><span class="sxs-lookup"><span data-stu-id="a0355-134">**David Pine**, Senior Content Developer, .NET docs, Microsoft</span></span>

## <a name="version"></a><span data-ttu-id="a0355-135">版本</span><span class="sxs-lookup"><span data-stu-id="a0355-135">Version</span></span>

<span data-ttu-id="a0355-136">本指南涵盖了 .NET 5 版本，以及与 .NET 5 发布时间同步的同一波技术（即 Azure 和额外第三方技术）相关的许多额外更新。</span><span class="sxs-lookup"><span data-stu-id="a0355-136">This guide has been written to cover **.NET 5** version along with many additional updates related to the same “wave” of technologies (that is, Azure and additional third-party technologies) coinciding in time with the .NET 5 release.</span></span>

## <a name="who-should-use-this-guide"></a><span data-ttu-id="a0355-137">本指南的目标读者</span><span class="sxs-lookup"><span data-stu-id="a0355-137">Who should use this guide</span></span>

<span data-ttu-id="a0355-138">本指南的受众主要是对学习如何构建为云设计的应用程序感兴趣的开发人员、开发主管和架构师。</span><span class="sxs-lookup"><span data-stu-id="a0355-138">The audience for this guide is mainly developers, development leads, and architects who are interested in learning how to build applications designed for the cloud.</span></span>

<span data-ttu-id="a0355-139">次级受众是计划选择是否使用云本机方法构建其应用程序的技术决策者。</span><span class="sxs-lookup"><span data-stu-id="a0355-139">A secondary audience is technical decision-makers who plan to choose whether to build their applications using a cloud-native approach.</span></span>

## <a name="how-you-can-use-this-guide"></a><span data-ttu-id="a0355-140">如何使用本指南</span><span class="sxs-lookup"><span data-stu-id="a0355-140">How you can use this guide</span></span>

<span data-ttu-id="a0355-141">本指南首先定义云本机，并介绍使用云本机原则和技术构建的参考应用程序。</span><span class="sxs-lookup"><span data-stu-id="a0355-141">This guide begins by defining cloud native and introducing a reference application built using cloud-native principles and technologies.</span></span> <span data-ttu-id="a0355-142">除了前两章，本书内容分成特定章节，集中讨论大多数云本机应用程序的共通主题。</span><span class="sxs-lookup"><span data-stu-id="a0355-142">Beyond these first two chapters, the rest of the book is broken up into specific chapters focused on topics common to most cloud-native applications.</span></span> <span data-ttu-id="a0355-143">可以跳转到以下任何章节，了解相关云本机方法：</span><span class="sxs-lookup"><span data-stu-id="a0355-143">You can jump to any of these chapters to learn about cloud-native approaches to:</span></span>

- <span data-ttu-id="a0355-144">数据和数据访问</span><span class="sxs-lookup"><span data-stu-id="a0355-144">Data and data access</span></span>
- <span data-ttu-id="a0355-145">通信模式</span><span class="sxs-lookup"><span data-stu-id="a0355-145">Communication patterns</span></span>
- <span data-ttu-id="a0355-146">缩放和可伸缩性</span><span class="sxs-lookup"><span data-stu-id="a0355-146">Scaling and scalability</span></span>
- <span data-ttu-id="a0355-147">应用程序复原能力</span><span class="sxs-lookup"><span data-stu-id="a0355-147">Application resiliency</span></span>
- <span data-ttu-id="a0355-148">监视和运行状况</span><span class="sxs-lookup"><span data-stu-id="a0355-148">Monitoring and health</span></span>
- <span data-ttu-id="a0355-149">标识和安全性</span><span class="sxs-lookup"><span data-stu-id="a0355-149">Identity and security</span></span>
- <span data-ttu-id="a0355-150">DevOps</span><span class="sxs-lookup"><span data-stu-id="a0355-150">DevOps</span></span>

<span data-ttu-id="a0355-151">本指南有 [PDF](https://dotnet.microsoft.com/download/e-book/cloud-native-azure/pdf) 格式和在线版本。</span><span class="sxs-lookup"><span data-stu-id="a0355-151">This guide is available both in [PDF](https://dotnet.microsoft.com/download/e-book/cloud-native-azure/pdf) form and online.</span></span> <span data-ttu-id="a0355-152">欢迎随时将此文档或其在线版本的链接转发给你的团队，以确保对这些主题有共同的理解。</span><span class="sxs-lookup"><span data-stu-id="a0355-152">Feel free to forward this document or links to its online version to your team to help ensure common understanding of these topics.</span></span> <span data-ttu-id="a0355-153">这些主题中的大多数都得益于对基本原则和模式的一致理解，以及与这些主题相关的决策所涉及的权衡。</span><span class="sxs-lookup"><span data-stu-id="a0355-153">Most of these topics benefit from a consistent understanding of the underlying principles and patterns, as well as the trade-offs involved in decisions related to these topics.</span></span> <span data-ttu-id="a0355-154">本文档的目标是为团队及其领导提供所需的信息，使其能够为应用程序的体系结构、开发和托管作出明智的决策。</span><span class="sxs-lookup"><span data-stu-id="a0355-154">Our goal with this document is to equip teams and their leaders with the information they need to make well-informed decisions for their applications' architecture, development, and hosting.</span></span>

## <a name="send-your-feedback"></a><span data-ttu-id="a0355-155">提供你的反馈</span><span class="sxs-lookup"><span data-stu-id="a0355-155">Send your feedback</span></span>

<span data-ttu-id="a0355-156">我们正在不断完善本书和相关示例，欢迎你提供反馈！</span><span class="sxs-lookup"><span data-stu-id="a0355-156">This book and related samples are constantly evolving, so your feedback is welcomed!</span></span> <span data-ttu-id="a0355-157">如果对如何改进本书有任何建议，请使用 [GitHub 问题](https://github.com/dotnet/docs/issues)上任何页面底部的反馈部分进行反馈。</span><span class="sxs-lookup"><span data-stu-id="a0355-157">If you have comments about how this book can be improved, use the feedback section at the bottom of any page built on [GitHub issues](https://github.com/dotnet/docs/issues).</span></span>

>[!div class="step-by-step"]
>[<span data-ttu-id="a0355-158">下一页</span><span class="sxs-lookup"><span data-stu-id="a0355-158">Next</span></span>](introduction.md)
