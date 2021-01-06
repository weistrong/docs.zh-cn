---
title: SYSLIB0012 警告
description: 了解有关生成编译时警告 SYSLIB0012 的过时信息。
ms.topic: reference
ms.date: 10/20/2020
ms.openlocfilehash: 9b3fa94029efb2343e6dbbeb3ae36195f0956523
ms.sourcegitcommit: e301979e3049ce412d19b094c60ed95b316a8f8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/16/2020
ms.locfileid: "97596270"
---
# <a name="syslib0012-assemblycodebase-and-assemblyescapedcodebase-are-obsolete"></a><span data-ttu-id="9c588-103">SYSLIB0012：Assembly.CodeBase 和 Assembly.EscapedCodeBase 已过时</span><span class="sxs-lookup"><span data-stu-id="9c588-103">SYSLIB0012: Assembly.CodeBase and Assembly.EscapedCodeBase are obsolete</span></span>

<span data-ttu-id="9c588-104">从 .NET 5.0 开始，以下 API 标记为已过时。</span><span class="sxs-lookup"><span data-stu-id="9c588-104">The following APIs are marked as obsolete, starting in .NET 5.0.</span></span> <span data-ttu-id="9c588-105">在代码中使用这些 API 会在编译时生成警告 `SYSLIB0012`。</span><span class="sxs-lookup"><span data-stu-id="9c588-105">Using them in code generates warning `SYSLIB0012` at compile time.</span></span>

- <xref:System.Reflection.Assembly.CodeBase?displayProperty=nameWithType>
- <xref:System.Reflection.Assembly.EscapedCodeBase?displayProperty=nameWithType>

## <a name="workarounds"></a><span data-ttu-id="9c588-106">工作区</span><span class="sxs-lookup"><span data-stu-id="9c588-106">Workarounds</span></span>

<span data-ttu-id="9c588-107">请改用 <xref:System.Reflection.Assembly.Location?displayProperty=nameWithType>。</span><span class="sxs-lookup"><span data-stu-id="9c588-107">Use <xref:System.Reflection.Assembly.Location?displayProperty=nameWithType> instead.</span></span>

[!INCLUDE [suppress-syslib-warning](../../../../includes/suppress-syslib-warning.md)]
