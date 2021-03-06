---
title: 将应用移植到 .NET Core 简介
description: 本章介绍了考虑将现有 ASP.NET 应用迁移到 .NET Core 的团队的注意事项列表。
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: a346d1c693389cc4ca682b41a3b7fc094cfa5482
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "102400977"
---
# <a name="introduction-to-porting-apps-to-net-core"></a><span data-ttu-id="406ea-103">将应用移植到 .NET Core 简介</span><span class="sxs-lookup"><span data-stu-id="406ea-103">Introduction to porting apps to .NET Core</span></span>

[!INCLUDE [book-preview](../../../includes/book-preview.md)]

<span data-ttu-id="406ea-104">.NET Core 是 .NET Framework 的一种革新性步骤。</span><span class="sxs-lookup"><span data-stu-id="406ea-104">.NET Core is a revolutionary step forward from .NET Framework.</span></span> <span data-ttu-id="406ea-105">由于跨平台的支持与开发人员满意度相比，它提供了一种与从工作效率到性能之间的 .NET Framework 优势的主机。</span><span class="sxs-lookup"><span data-stu-id="406ea-105">It offers a host of advantages over .NET Framework across the board from productivity to performance, from cross-platform support to developer satisfaction.</span></span> <span data-ttu-id="406ea-106">ASP.NET Core 甚至还投票了 [2020 Stack Overflow 开发人员调查](https://insights.stackoverflow.com/survey/2020#technology-most-loved-dreaded-and-wanted-web-frameworks)中最喜欢的 web 框架。</span><span class="sxs-lookup"><span data-stu-id="406ea-106">ASP.NET Core was even voted the most-loved web framework in the [2020 Stack Overflow developer survey](https://insights.stackoverflow.com/survey/2020#technology-most-loved-dreaded-and-wanted-web-frameworks).</span></span> <span data-ttu-id="406ea-107">很明显，需要考虑迁移。</span><span class="sxs-lookup"><span data-stu-id="406ea-107">Clearly there are strong reasons to consider migrating.</span></span>

<span data-ttu-id="406ea-108">请记住， [.Net Core 是 .net 的未来](https://devblogs.microsoft.com/dotnet/net-core-is-the-future-of-net/)，这一点很重要。</span><span class="sxs-lookup"><span data-stu-id="406ea-108">It's important to keep in mind that [.NET Core is the Future of .NET](https://devblogs.microsoft.com/dotnet/net-core-is-the-future-of-net/).</span></span> <span data-ttu-id="406ea-109">若要引言本文：</span><span class="sxs-lookup"><span data-stu-id="406ea-109">To quote this article:</span></span>

> <span data-ttu-id="406ea-110">新应用程序应基于 .NET Core 构建。</span><span class="sxs-lookup"><span data-stu-id="406ea-110">New apps should be built on .NET Core.</span></span> <span data-ttu-id="406ea-111">.NET Core 是 .NET 的未来投资。</span><span class="sxs-lookup"><span data-stu-id="406ea-111">.NET Core is where future investments in .NET will happen.</span></span> <span data-ttu-id="406ea-112">现有的应用程序可以安全地保留在 .NET Framework 上。</span><span class="sxs-lookup"><span data-stu-id="406ea-112">Existing apps are safe to remain on .NET Framework which will be supported.</span></span> <span data-ttu-id="406ea-113">希望利用 .NET 中的新功能的现有应用应考虑迁移到 .NET Core。</span><span class="sxs-lookup"><span data-stu-id="406ea-113">Existing apps that want to take advantage of the new features in .NET should consider moving to .NET Core.</span></span> <span data-ttu-id="406ea-114">随着我们计划未来的发展，我们将进一步为平台带来更多的功能。</span><span class="sxs-lookup"><span data-stu-id="406ea-114">As we plan into the future, we will be bringing in even more capabilities to the platform.</span></span>

<span data-ttu-id="406ea-115">但是，将应用程序升级到 ASP.NET Core 需要一些精力。</span><span class="sxs-lookup"><span data-stu-id="406ea-115">However, upgrading your app to ASP.NET Core will require some effort.</span></span> <span data-ttu-id="406ea-116">应根据业务价值和目标来权衡这一工作。</span><span class="sxs-lookup"><span data-stu-id="406ea-116">That effort should be balanced against business value and goals.</span></span> <span data-ttu-id="406ea-117">.NET Framework 的应用程序的生存期很长，而且可预见的未来，Windows 内置了支持。</span><span class="sxs-lookup"><span data-stu-id="406ea-117">.NET Framework apps have a long life ahead of them, with support built into Windows for the foreseeable future.</span></span> <span data-ttu-id="406ea-118">确定迁移到 .NET Core 之前应考虑的一些问题是合适的吗？</span><span class="sxs-lookup"><span data-stu-id="406ea-118">What are some of the questions you should consider before deciding migration to .NET Core is appropriate?</span></span> <span data-ttu-id="406ea-119">预期的优点是什么？</span><span class="sxs-lookup"><span data-stu-id="406ea-119">What are the expected advantages?</span></span> <span data-ttu-id="406ea-120">权衡有哪些？</span><span class="sxs-lookup"><span data-stu-id="406ea-120">What are the tradeoffs?</span></span> <span data-ttu-id="406ea-121">涉及了多少工作量？</span><span class="sxs-lookup"><span data-stu-id="406ea-121">How much effort is involved?</span></span> <span data-ttu-id="406ea-122">这些明显的问题只是开始，但由于团队考虑到了如何使用目前和未来的应用程序来支持其客户需求，因此提供了一个很好的起点。</span><span class="sxs-lookup"><span data-stu-id="406ea-122">These obvious questions are just the beginning, but make for a great starting point as teams consider how to support their customers' needs with apps today and tomorrow.</span></span>

- <span data-ttu-id="406ea-123">是否适合迁移到 .NET Core？</span><span class="sxs-lookup"><span data-stu-id="406ea-123">Is migration to .NET Core appropriate?</span></span>
- <span data-ttu-id="406ea-124">何时保持 .NET Framework？</span><span class="sxs-lookup"><span data-stu-id="406ea-124">When does it make sense to remain on .NET Framework?</span></span>
- <span data-ttu-id="406ea-125">应用程序的目标是否应作为步进石头 ASP.NET Core 2.1？</span><span class="sxs-lookup"><span data-stu-id="406ea-125">Should apps target ASP.NET Core 2.1 as a stepping stone?</span></span>
- <span data-ttu-id="406ea-126">团队应如何选择合适的 .NET Core 版本作为目标？</span><span class="sxs-lookup"><span data-stu-id="406ea-126">How should teams choose the right .NET Core version to target?</span></span>
- <span data-ttu-id="406ea-127">对于大型应用的增量迁移，建议使用哪些策略？</span><span class="sxs-lookup"><span data-stu-id="406ea-127">What strategies are recommended for incremental migration of large apps?</span></span>
- <span data-ttu-id="406ea-128">移植到 .NET Core 时应考虑的部署策略是什么？</span><span class="sxs-lookup"><span data-stu-id="406ea-128">What deployment strategies should be considered when porting to .NET Core?</span></span>
- <span data-ttu-id="406ea-129">在哪里可以找到其他资源？</span><span class="sxs-lookup"><span data-stu-id="406ea-129">Where can we find additional resources?</span></span>

<span data-ttu-id="406ea-130">本介绍章节介绍了所有这些问题，并详细介绍了以后几章中更具体的技术注意事项。</span><span class="sxs-lookup"><span data-stu-id="406ea-130">This introductory chapter addresses all of these questions and more before moving on to more specific and technical considerations in future chapters.</span></span>

## <a name="references"></a><span data-ttu-id="406ea-131">参考</span><span class="sxs-lookup"><span data-stu-id="406ea-131">References</span></span>

- [<span data-ttu-id="406ea-132">2020 Stack Overflow 开发人员调查最喜欢的 web 框架</span><span class="sxs-lookup"><span data-stu-id="406ea-132">2020 Stack Overflow developer survey most loved web frameworks</span></span>](https://insights.stackoverflow.com/survey/2020#technology-most-loved-dreaded-and-wanted-web-frameworks)
- [<span data-ttu-id="406ea-133">.Net Core 是 .NET 的未来</span><span class="sxs-lookup"><span data-stu-id="406ea-133">.NET Core is the Future of .NET</span></span>](https://devblogs.microsoft.com/dotnet/net-core-is-the-future-of-net/)

>[!div class="step-by-step"]
><span data-ttu-id="406ea-134">[上一页](index.md)
>[下一页](migration-considerations.md)</span><span class="sxs-lookup"><span data-stu-id="406ea-134">[Previous](index.md)
[Next](migration-considerations.md)</span></span>
