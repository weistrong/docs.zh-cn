---
title: 选择正确的 .NET Core 版本
description: 如何确定要面向哪个版本的 .NET Core？
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: 401eead986ee8b67ed15be609d0b5d228773312d
ms.sourcegitcommit: 10e719780594efc781b15295e499c66f316068b8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2021
ms.locfileid: "102400996"
---
# <a name="choose-the-right-net-core-version"></a><span data-ttu-id="88b5b-103">选择正确的 .NET Core 版本</span><span class="sxs-lookup"><span data-stu-id="88b5b-103">Choose the right .NET Core version</span></span>

<span data-ttu-id="88b5b-104">选择要作为目标的 .NET Core 版本时，大多数组织的最大考虑因素是支持生命周期。</span><span class="sxs-lookup"><span data-stu-id="88b5b-104">The largest consideration for most organizations when choosing a version of .NET Core to target is the support lifecycle.</span></span> <span data-ttu-id="88b5b-105">长期支持 (LTS) 发布的发布频率较低，但支持时间范围比当前 (非 LTS) 版本多。</span><span class="sxs-lookup"><span data-stu-id="88b5b-105">Long Term Support (LTS) releases ship less frequently but have a longer support window than Current (non-LTS) releases.</span></span> <span data-ttu-id="88b5b-106">目前，LTS 版本计划每隔一年交付。</span><span class="sxs-lookup"><span data-stu-id="88b5b-106">Currently, LTS releases are scheduled to ship every other year.</span></span> <span data-ttu-id="88b5b-107">客户可以选择要面向的版本，并可以在同一台计算机上并行安装不同版本的 .NET Core。</span><span class="sxs-lookup"><span data-stu-id="88b5b-107">Customers can choose which releases to target, and can install different releases of .NET Core side by side on the same machine.</span></span> <span data-ttu-id="88b5b-108">LTS 版本将仅在其生命周期内收到关键且兼容的修补程序。</span><span class="sxs-lookup"><span data-stu-id="88b5b-108">LTS releases will receive only critical and compatible fixes throughout their lifecycle.</span></span> <span data-ttu-id="88b5b-109">当前版本将接收这些相同的修补程序，还将用兼容的创新和功能进行更新。</span><span class="sxs-lookup"><span data-stu-id="88b5b-109">Current releases will receive these same fixes and will also be updated with compatible innovations and features.</span></span> <span data-ttu-id="88b5b-110">首次发布后三年支持 LTS 版本。</span><span class="sxs-lookup"><span data-stu-id="88b5b-110">LTS releases are supported for three years after their initial release.</span></span> <span data-ttu-id="88b5b-111">当前版本在后续的当前版本或 LTS 版本发布后的三个月内受支持。</span><span class="sxs-lookup"><span data-stu-id="88b5b-111">Current releases are supported for three months after a subsequent Current or LTS release.</span></span>

<span data-ttu-id="88b5b-112">目前，希望将大型 .NET Framework 应用迁移到 .NET Core 的大多数客户可能正在寻找稳定的目标，前提是它们尚未迁移到较早版本的 .NET Core。</span><span class="sxs-lookup"><span data-stu-id="88b5b-112">Most customers looking to migrate a large .NET Framework app to .NET Core today are probably looking for a stable destination, given that they haven't already made the move to an earlier version of .NET Core.</span></span> <span data-ttu-id="88b5b-113">在这种情况下，迁移目标的最佳 .NET 核心版本是 .NET Core 3.1，这是当前的 LTS 版本。</span><span class="sxs-lookup"><span data-stu-id="88b5b-113">In this case, the best .NET Core version to target for the migration is .NET Core 3.1, which is the current LTS version.</span></span> <span data-ttu-id="88b5b-114">对 .NET Core 3.1 的支持将于12月2022结束。</span><span class="sxs-lookup"><span data-stu-id="88b5b-114">Support for .NET Core 3.1 ends in December 2022.</span></span> <span data-ttu-id="88b5b-115">下一个计划的 LTS 版本将是 .NET 6.0，预定于 11 2021 月发布。</span><span class="sxs-lookup"><span data-stu-id="88b5b-115">The next planned LTS release will be .NET 6.0, slated to ship in November 2021.</span></span>

<span data-ttu-id="88b5b-116">从 .NET Core 3.1 更新到 .NET 5.0 (下一版本) 所需的工作量要低于从 .NET Framework 移植到 .NET Core 所需的工作量。</span><span class="sxs-lookup"><span data-stu-id="88b5b-116">Updating from .NET Core 3.1 to .NET 5.0 (the next version) requires much less effort than porting from .NET Framework to .NET Core.</span></span> <span data-ttu-id="88b5b-117">出于此原因，大多数客户的建议是先升级到 .NET Core 3.1。</span><span class="sxs-lookup"><span data-stu-id="88b5b-117">For this reason, the recommendation for most customers is to upgrade to .NET Core 3.1 first.</span></span> <span data-ttu-id="88b5b-118">然后，确定下一次更新是否适用于最新的当前版本 ( .NET 5.0) 或等待下一个 LTS 版本 ( .NET 6.0) 再升级。</span><span class="sxs-lookup"><span data-stu-id="88b5b-118">Then decide whether the next update should be to the latest current release (.NET 5.0) or to wait for the next LTS release (.NET 6.0) before upgrading further.</span></span>

<span data-ttu-id="88b5b-119">本书假定 .NET Framework 应用将升级到 .NET Core 3.1。</span><span class="sxs-lookup"><span data-stu-id="88b5b-119">This book assumes .NET Framework apps will be upgraded to .NET Core 3.1.</span></span>

## <a name="references"></a><span data-ttu-id="88b5b-120">参考</span><span class="sxs-lookup"><span data-stu-id="88b5b-120">References</span></span>

[<span data-ttu-id="88b5b-121">.NET Core 和 .NET 5 支持策略</span><span class="sxs-lookup"><span data-stu-id="88b5b-121">.NET Core and .NET 5 Support Policy</span></span>](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)

>[!div class="step-by-step"]
><span data-ttu-id="88b5b-122">[上一页](migrate-aspnet-core-2-1.md)
>[下一页](incremental-migration-strategies.md)</span><span class="sxs-lookup"><span data-stu-id="88b5b-122">[Previous](migrate-aspnet-core-2-1.md)
[Next](incremental-migration-strategies.md)</span></span>
