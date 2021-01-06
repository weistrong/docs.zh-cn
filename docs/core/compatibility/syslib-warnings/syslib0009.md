---
title: SYSLIB0009 警告
description: 了解有关生成编译时警告 SYSLIB0009 的过时信息。
ms.topic: reference
ms.date: 10/20/2020
ms.openlocfilehash: 922fcc30b2b1577976e4e88e3f7631e19d4b2cce
ms.sourcegitcommit: e301979e3049ce412d19b094c60ed95b316a8f8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/16/2020
ms.locfileid: "97596282"
---
# <a name="syslib0009-the-authenticationmanager-authenticate-and-preauthenticate-methods-are-not-supported"></a><span data-ttu-id="d7444-103">SYSLIB0009：AuthenticationManager 身份验证和预身份验证方法不受支持</span><span class="sxs-lookup"><span data-stu-id="d7444-103">SYSLIB0009: The AuthenticationManager Authenticate and PreAuthenticate methods are not supported</span></span>

<span data-ttu-id="d7444-104">从 .NET 5.0 开始，以下 API 标记为已过时。</span><span class="sxs-lookup"><span data-stu-id="d7444-104">The following APIs are marked obsolete, starting in .NET 5.0.</span></span> <span data-ttu-id="d7444-105">使用这些 API 会在编译时生成警告 `SYSLIB0009`。</span><span class="sxs-lookup"><span data-stu-id="d7444-105">Use of these APIs generates warning `SYSLIB0009` at compile time.</span></span>

- <xref:System.Net.AuthenticationManager.Authenticate%2A?displayProperty=nameWithType>
- <xref:System.Net.AuthenticationManager.PreAuthenticate%2A?displayProperty=nameWithType>

## <a name="suppress-the-warning"></a><span data-ttu-id="d7444-106">禁止显示警告</span><span class="sxs-lookup"><span data-stu-id="d7444-106">Suppress the warning</span></span>

<span data-ttu-id="d7444-107">如果无法更改代码，可以通过 `#pragma` 指令或 `<NoWarn>` 项目设置来禁止显示警告。</span><span class="sxs-lookup"><span data-stu-id="d7444-107">If you cannot change your code, you can suppress the warning through a `#pragma` directive or a `<NoWarn>` project setting.</span></span> <span data-ttu-id="d7444-108">有关示例，请参阅[禁止显示警告](../syslib-obsoletions.md#suppress-warnings)。</span><span class="sxs-lookup"><span data-stu-id="d7444-108">For examples, see [Suppress warnings](../syslib-obsoletions.md#suppress-warnings).</span></span>
