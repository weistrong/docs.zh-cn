---
title: SYSLIB0010 警告
description: 了解有关生成编译时警告 SYSLIB0010 的过时信息。
ms.topic: reference
ms.date: 10/20/2020
ms.openlocfilehash: 289fb3f766a6e1d37bea8faec1896d20442f43f9
ms.sourcegitcommit: e301979e3049ce412d19b094c60ed95b316a8f8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/16/2020
ms.locfileid: "97596272"
---
# <a name="syslib0010-unsupported-remoting-apis"></a><span data-ttu-id="7fa31-103">SYSLIB0010：不支持的远程处理 API</span><span class="sxs-lookup"><span data-stu-id="7fa31-103">SYSLIB0010: Unsupported remoting APIs</span></span>

<span data-ttu-id="7fa31-104">[.NET 远程处理](/previous-versions/dotnet/netframework-1.1/kwdt6w2k(v=vs.71))是一项传统技术，基础结构仅存在于 .NET Framework 中。</span><span class="sxs-lookup"><span data-stu-id="7fa31-104">[.NET remoting](/previous-versions/dotnet/netframework-1.1/kwdt6w2k(v=vs.71)) is a legacy technology, and the infrastructure exists only in .NET Framework.</span></span> <span data-ttu-id="7fa31-105">从 .NET 5.0 开始，以下与远程处理相关的 API 标记为已过时。</span><span class="sxs-lookup"><span data-stu-id="7fa31-105">The following remoting-related APIs are marked as obsolete, starting in .NET 5.0.</span></span> <span data-ttu-id="7fa31-106">在代码中使用这些 API 会在编译时生成警告 `SYSLIB0010`。</span><span class="sxs-lookup"><span data-stu-id="7fa31-106">Using them in code generates warning `SYSLIB0010` at compile time.</span></span>

- <xref:System.MarshalByRefObject.GetLifetimeService?displayProperty=nameWithType>
- <xref:System.MarshalByRefObject.InitializeLifetimeService?displayProperty=nameWithType>

## <a name="workarounds"></a><span data-ttu-id="7fa31-107">工作区</span><span class="sxs-lookup"><span data-stu-id="7fa31-107">Workarounds</span></span>

<span data-ttu-id="7fa31-108">请考虑使用 WCF 或基于 HTTP 的 REST 服务与其他应用程序的对象或跨计算机进行通信。</span><span class="sxs-lookup"><span data-stu-id="7fa31-108">Consider using WCF or HTTP-based REST services to communicate with objects in other applications or across machines.</span></span> <span data-ttu-id="7fa31-109">有关详细信息，请参阅 [.NET Framework 技术在 .NET Core 上不可用](../../porting/net-framework-tech-unavailable.md)。</span><span class="sxs-lookup"><span data-stu-id="7fa31-109">For more information, see [.NET Framework technologies unavailable on .NET Core](../../porting/net-framework-tech-unavailable.md).</span></span>

[!INCLUDE [suppress-syslib-warning](../../../../includes/suppress-syslib-warning.md)]

## <a name="see-also"></a><span data-ttu-id="7fa31-110">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7fa31-110">See also</span></span>

- <span data-ttu-id="7fa31-111">[.NET 远程处理](/previous-versions/dotnet/netframework-1.1/kwdt6w2k(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="7fa31-111">[.NET remoting](/previous-versions/dotnet/netframework-1.1/kwdt6w2k(v=vs.71))</span></span>
