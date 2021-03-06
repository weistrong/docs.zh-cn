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
# <a name="choose-the-right-net-core-version"></a>选择正确的 .NET Core 版本

选择要作为目标的 .NET Core 版本时，大多数组织的最大考虑因素是支持生命周期。 长期支持 (LTS) 发布的发布频率较低，但支持时间范围比当前 (非 LTS) 版本多。 目前，LTS 版本计划每隔一年交付。 客户可以选择要面向的版本，并可以在同一台计算机上并行安装不同版本的 .NET Core。 LTS 版本将仅在其生命周期内收到关键且兼容的修补程序。 当前版本将接收这些相同的修补程序，还将用兼容的创新和功能进行更新。 首次发布后三年支持 LTS 版本。 当前版本在后续的当前版本或 LTS 版本发布后的三个月内受支持。

目前，希望将大型 .NET Framework 应用迁移到 .NET Core 的大多数客户可能正在寻找稳定的目标，前提是它们尚未迁移到较早版本的 .NET Core。 在这种情况下，迁移目标的最佳 .NET 核心版本是 .NET Core 3.1，这是当前的 LTS 版本。 对 .NET Core 3.1 的支持将于12月2022结束。 下一个计划的 LTS 版本将是 .NET 6.0，预定于 11 2021 月发布。

从 .NET Core 3.1 更新到 .NET 5.0 (下一版本) 所需的工作量要低于从 .NET Framework 移植到 .NET Core 所需的工作量。 出于此原因，大多数客户的建议是先升级到 .NET Core 3.1。 然后，确定下一次更新是否适用于最新的当前版本 ( .NET 5.0) 或等待下一个 LTS 版本 ( .NET 6.0) 再升级。

本书假定 .NET Framework 应用将升级到 .NET Core 3.1。

## <a name="references"></a>参考

[.NET Core 和 .NET 5 支持策略](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)

>[!div class="step-by-step"]
>[上一页](migrate-aspnet-core-2-1.md)
>[下一页](incremental-migration-strategies.md)
