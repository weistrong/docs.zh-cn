---
title: 面向 .NET 开发人员的 Dapr
description: 可帮助 .NET 开发人员了解并充分利用 Microsoft 开源分散式应用程序运行时的全部功能的指南。
author: robvet
ms.date: 02/07/2021
ms.openlocfilehash: a9f1362d8e588790151f9b828f53de90565cacbb
ms.sourcegitcommit: f0fc5db7bcbf212e46933e9cf2d555bb82666141
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "100626006"
---
# <a name="dapr-for-net-developers"></a><span data-ttu-id="b4984-103">面向 .NET 开发人员的 Dapr</span><span class="sxs-lookup"><span data-stu-id="b4984-103">Dapr for .NET Developers</span></span>

![封面图像](./media/cover.png)

<span data-ttu-id="b4984-105">**预览版**</span><span class="sxs-lookup"><span data-stu-id="b4984-105">**PREVIEW EDITION**</span></span>

<span data-ttu-id="b4984-106">发布者</span><span class="sxs-lookup"><span data-stu-id="b4984-106">PUBLISHED BY</span></span>

<span data-ttu-id="b4984-107">Microsoft 开发人员部门、.NET 和 Azure Incubations 团队</span><span class="sxs-lookup"><span data-stu-id="b4984-107">Microsoft Developer Division, .NET, and Azure Incubations teams</span></span>

<span data-ttu-id="b4984-108">Microsoft Corporation 的一个部门</span><span class="sxs-lookup"><span data-stu-id="b4984-108">A division of Microsoft Corporation</span></span>

<span data-ttu-id="b4984-109">One Microsoft Way</span><span class="sxs-lookup"><span data-stu-id="b4984-109">One Microsoft Way</span></span>

<span data-ttu-id="b4984-110">Redmond, Washington 98052-6399</span><span class="sxs-lookup"><span data-stu-id="b4984-110">Redmond, Washington 98052-6399</span></span>

<span data-ttu-id="b4984-111">版权所有 &copy; 2021 Microsoft Corporation</span><span class="sxs-lookup"><span data-stu-id="b4984-111">Copyright &copy; 2021 by Microsoft Corporation</span></span>

<span data-ttu-id="b4984-112">保留所有权利。</span><span class="sxs-lookup"><span data-stu-id="b4984-112">All rights reserved.</span></span> <span data-ttu-id="b4984-113">未经发布者书面许可，不得以任何形式或任何方式复制或传播本书中的任何内容。</span><span class="sxs-lookup"><span data-stu-id="b4984-113">No part of the contents of this book may be reproduced or transmitted in any form or by any means without the written permission of the publisher.</span></span>

<span data-ttu-id="b4984-114">本书“按原样”提供，表达作者的观点和看法。</span><span class="sxs-lookup"><span data-stu-id="b4984-114">This book is provided "as-is" and expresses the author's views and opinions.</span></span> <span data-ttu-id="b4984-115">本书中表达的观点、看法和信息（包括 URL 和其他 Internet 网站引用）如有更改，恕不另行通知。</span><span class="sxs-lookup"><span data-stu-id="b4984-115">The views, opinions, and information expressed in this book, including URL and other Internet website references, may change without notice.</span></span>

<span data-ttu-id="b4984-116">本书中提及的一些示例仅用于说明，纯属虚构。</span><span class="sxs-lookup"><span data-stu-id="b4984-116">Some examples depicted herein are provided for illustration only and are fictitious.</span></span> <span data-ttu-id="b4984-117">不存在任何实际关联或联系，请勿妄加推断。</span><span class="sxs-lookup"><span data-stu-id="b4984-117">No real association or connection is intended or should be inferred.</span></span>

<span data-ttu-id="b4984-118">Microsoft 和 <https://www.microsoft.com> 上“商标”网页列出的商标是 Microsoft 集团公司的商标。</span><span class="sxs-lookup"><span data-stu-id="b4984-118">Microsoft and the trademarks listed at <https://www.microsoft.com> on the "Trademarks" webpage are trademarks of the Microsoft group of companies.</span></span>

<span data-ttu-id="b4984-119">Mac 和 macOS 是 Apple Inc. 的商标</span><span class="sxs-lookup"><span data-stu-id="b4984-119">Mac and macOS are trademarks of Apple Inc.</span></span>

<span data-ttu-id="b4984-120">Docker 的鲸鱼徽标是 Docker Inc. 的注册商标经许可方可使用。</span><span class="sxs-lookup"><span data-stu-id="b4984-120">The Docker whale logo is a registered trademark of Docker, Inc. Used by permission.</span></span>

<span data-ttu-id="b4984-121">所有其他标记和徽标均为其各自所有者的财产。</span><span class="sxs-lookup"><span data-stu-id="b4984-121">All other marks and logos are property of their respective owners.</span></span>

<span data-ttu-id="b4984-122">作者：</span><span class="sxs-lookup"><span data-stu-id="b4984-122">Authors:</span></span>

> <span data-ttu-id="b4984-123">Rob Vettor，Microsoft 首席云解决方案架构师 - [thinkingincloudnative.com](https://thinkingincloudnative.com/about/)</span><span class="sxs-lookup"><span data-stu-id="b4984-123">**Rob Vettor**, Principal Cloud Solution Architect - [thinkingincloudnative.com](https://thinkingincloudnative.com/about/), Microsoft</span></span>
>
> <span data-ttu-id="b4984-124">Sander Molenkamp，[Info Support](https://www.infosupport.com/en/) 首席云架构师/Microsoft MVP - [sandermolenkamp.com](https://www.sandermolenkamp.com)</span><span class="sxs-lookup"><span data-stu-id="b4984-124">**Sander Molenkamp**, Principal Cloud Architect/Microsoft MVP - [sandermolenkamp.com](https://www.sandermolenkamp.com), [Info Support](https://www.infosupport.com/en/)</span></span>
>
> <span data-ttu-id="b4984-125">Edwin van Wijk，[Info Support](https://www.infosupport.com/en/) 首席解决方案架构师/Microsoft MVP - [defaultconstructor.com](https://defaultconstructor.com)</span><span class="sxs-lookup"><span data-stu-id="b4984-125">**Edwin van Wijk**, Principal Solution Architect/Microsoft MVP - [defaultconstructor.com](https://defaultconstructor.com), [Info Support](https://www.infosupport.com/en/)</span></span>

<span data-ttu-id="b4984-126">参与者和审阅者：</span><span class="sxs-lookup"><span data-stu-id="b4984-126">Participants and Reviewers:</span></span>

> <span data-ttu-id="b4984-127">Mark Russinovich，Microsoft Azure Office of CTO 的 Azure CTO 兼技术研究员</span><span class="sxs-lookup"><span data-stu-id="b4984-127">**Mark Russinovich**, Azure CTO and Technical Fellow, Azure Office of CTO, Microsoft</span></span>
>
> <span data-ttu-id="b4984-128">Nish Anil，Microsoft .NET 团队高级项目经理 </span><span class="sxs-lookup"><span data-stu-id="b4984-128">**Nish Anil**, Senior Program Manager, .NET team, Microsoft</span></span>
>
> <span data-ttu-id="b4984-129">Mark Fussell，Microsoft Azure Incubations 首席项目经理</span><span class="sxs-lookup"><span data-stu-id="b4984-129">**Mark Fussell**, Principal Program Manager, Azure Incubations, Microsoft</span></span>
>
> <span data-ttu-id="b4984-130">Yaron Schneider，Microsoft Azure Incubations 首席软件工程师</span><span class="sxs-lookup"><span data-stu-id="b4984-130">**Yaron Schneider**, Principal Software Engineer, Azure Incubations, Microsoft</span></span>
>
> <span data-ttu-id="b4984-131">Ori Zohar，Microsoft Azure Incubations 高级项目经理</span><span class="sxs-lookup"><span data-stu-id="b4984-131">**Ori Zohar**, Senior Program Manager, Azure Incubations, Microsoft</span></span>

<span data-ttu-id="b4984-132">编辑：</span><span class="sxs-lookup"><span data-stu-id="b4984-132">Editors:</span></span>

> <span data-ttu-id="b4984-133">David Pine，Microsoft .NET 团队资深内容开发人员</span><span class="sxs-lookup"><span data-stu-id="b4984-133">**David Pine**, Senior Content Developer, .NET team, Microsoft</span></span>

> <span data-ttu-id="b4984-134">Maira Wenzel，Microsoft .NET 团队高级项目经理</span><span class="sxs-lookup"><span data-stu-id="b4984-134">**Maira Wenzel**, Program Manager, .NET team, Microsoft</span></span>

## <a name="version"></a><span data-ttu-id="b4984-135">Version</span><span class="sxs-lookup"><span data-stu-id="b4984-135">Version</span></span>

<span data-ttu-id="b4984-136">本指南已编写为涵盖 Dapr 1.0 版本。</span><span class="sxs-lookup"><span data-stu-id="b4984-136">This guide has been written to cover the **Dapr 1.0** version.</span></span> <span data-ttu-id="b4984-137">.NET Core 示例基于 .NET Core 3.1。</span><span class="sxs-lookup"><span data-stu-id="b4984-137">.NET Core samples are based on **.NET Core 3.1**.</span></span>

## <a name="who-should-use-this-guide"></a><span data-ttu-id="b4984-138">本指南的目标读者</span><span class="sxs-lookup"><span data-stu-id="b4984-138">Who should use this guide</span></span>

<span data-ttu-id="b4984-139">本指南的受众主要是对学习如何构建为云设计的应用程序感兴趣的开发人员、开发主管和架构师。</span><span class="sxs-lookup"><span data-stu-id="b4984-139">The audience for this guide is mainly developers, development leads, and architects who are interested in learning how to build applications designed for the cloud.</span></span>

<span data-ttu-id="b4984-140">次级受众是计划选择是否使用云本机方法构建其应用程序的技术决策者。</span><span class="sxs-lookup"><span data-stu-id="b4984-140">A secondary audience is technical decision-makers who plan to choose whether to build their applications using a cloud-native approach.</span></span>

## <a name="how-you-can-use-this-guide"></a><span data-ttu-id="b4984-141">如何使用本指南</span><span class="sxs-lookup"><span data-stu-id="b4984-141">How you can use this guide</span></span>

<span data-ttu-id="b4984-142">本指南有 [PDF](https://aka.ms/dapr-ebook) 格式和在线版本。</span><span class="sxs-lookup"><span data-stu-id="b4984-142">This guide is available both in [PDF](https://aka.ms/dapr-ebook) form and online.</span></span> <span data-ttu-id="b4984-143">欢迎随时将此文档或其在线版本的链接转发给你的团队，以确保对这些主题有共同的理解。</span><span class="sxs-lookup"><span data-stu-id="b4984-143">Feel free to forward this document or links to its online version to your team to help ensure common understanding of these topics.</span></span> <span data-ttu-id="b4984-144">这些主题中的大多数都得益于对基本原则和模式的一致理解，以及与这些主题相关的决策所涉及的权衡。</span><span class="sxs-lookup"><span data-stu-id="b4984-144">Most of these topics benefit from a consistent understanding of the underlying principles and patterns, as well as the trade-offs involved in decisions related to these topics.</span></span> <span data-ttu-id="b4984-145">本文档的目标是为团队及其领导提供所需的信息，使其能够为应用程序的体系结构、开发和托管作出明智的决策。</span><span class="sxs-lookup"><span data-stu-id="b4984-145">Our goal with this document is to equip teams and their leaders with the information they need to make well-informed decisions for their applications' architecture, development, and hosting.</span></span>

## <a name="send-your-feedback"></a><span data-ttu-id="b4984-146">提供你的反馈</span><span class="sxs-lookup"><span data-stu-id="b4984-146">Send your feedback</span></span>

<span data-ttu-id="b4984-147">我们正在不断完善本书和相关示例，欢迎你提供反馈！</span><span class="sxs-lookup"><span data-stu-id="b4984-147">This book and related samples are constantly evolving, so your feedback is welcomed!</span></span> <span data-ttu-id="b4984-148">如果对如何改进本书有任何建议，请使用 [GitHub 问题](https://github.com/dotnet/docs/issues)上任何页面底部的反馈部分进行反馈。</span><span class="sxs-lookup"><span data-stu-id="b4984-148">If you have comments about how this book can be improved, use the feedback section at the bottom of any page built on [GitHub issues](https://github.com/dotnet/docs/issues).</span></span>

>[!div class="step-by-step"]
>[<span data-ttu-id="b4984-149">下一页</span><span class="sxs-lookup"><span data-stu-id="b4984-149">Next</span></span>](foreword.md)
