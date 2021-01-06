---
title: SYSLIB0008 警告
description: 了解有关生成编译时警告 SYSLIB0008 的过时信息。
ms.topic: reference
ms.date: 10/20/2020
ms.openlocfilehash: 2b573f4b28cdf79107395f5cb38a4226d0ccc11e
ms.sourcegitcommit: e301979e3049ce412d19b094c60ed95b316a8f8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/16/2020
ms.locfileid: "97596271"
---
# <a name="syslib0008-createpdbgenerator-is-not-supported"></a><span data-ttu-id="4bdf8-103">SYSLIB0008：不支持 CreatePdbGenerator</span><span class="sxs-lookup"><span data-stu-id="4bdf8-103">SYSLIB0008: CreatePdbGenerator is not supported</span></span>

<span data-ttu-id="4bdf8-104">从 .NET 5.0 开始，<xref:System.Runtime.CompilerServices.DebugInfoGenerator.CreatePdbGenerator?displayProperty=nameWithType> API 标记为已过时。</span><span class="sxs-lookup"><span data-stu-id="4bdf8-104">The <xref:System.Runtime.CompilerServices.DebugInfoGenerator.CreatePdbGenerator?displayProperty=nameWithType> API is marked obsolete, starting in .NET 5.0.</span></span> <span data-ttu-id="4bdf8-105">使用此 API 会在编译时生成警告 `SYSLIB0008`。</span><span class="sxs-lookup"><span data-stu-id="4bdf8-105">Using this API generates warning `SYSLIB0008` at compile time.</span></span>

## <a name="suppress-the-warning"></a><span data-ttu-id="4bdf8-106">禁止显示警告</span><span class="sxs-lookup"><span data-stu-id="4bdf8-106">Suppress the warning</span></span>

<span data-ttu-id="4bdf8-107">如果无法更改代码，可以通过 `#pragma` 指令或 `<NoWarn>` 项目设置来禁止显示警告。</span><span class="sxs-lookup"><span data-stu-id="4bdf8-107">If you cannot change your code, you can suppress the warning through a `#pragma` directive or a `<NoWarn>` project setting.</span></span> <span data-ttu-id="4bdf8-108">有关示例，请参阅[禁止显示警告](../syslib-obsoletions.md#suppress-warnings)。</span><span class="sxs-lookup"><span data-stu-id="4bdf8-108">For examples, see [Suppress warnings](../syslib-obsoletions.md#suppress-warnings).</span></span>
