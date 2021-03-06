---
title: 比较 ASP.NET SignalR 和 ASP.NET Core SignalR
description: ASP.NET Core SignalR 的不同之处在于 ASP.NET SignalR？
author: ardalis
ms.date: 11/13/2020
ms.openlocfilehash: 89236bd0272c8f20cf9838dddefeb9afee1f3d93
ms.sourcegitcommit: 42d436ebc2a7ee02fc1848c7742bc7d80e13fc2f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "102401058"
---
# <a name="compare-aspnet-signalr-and-aspnet-core-signalr"></a>比较 ASP.NET SignalR 和 ASP.NET Core SignalR

ASP.NET Core SignalR 与使用 ASP.NET SignalR 的客户端或服务器不兼容。 需要更新客户端和服务器以使用 ASP.NET Core SignalR。 此部分中介绍了一些差异，而 [文档](/aspnet/core/signalr/version-differences)中提供了完整列表。ASP.NET Core SignalR 需要 .NET Core 2.1 或更高版本。

## <a name="feature-differences"></a>功能差异

- ASP.NET SignalR 自动尝试重新连接已断开的连接;此行为适用于 ASP.NET Core SignalR 客户端
- 这两个框架都支持 JSON;ASP.NET Core SignalR 还支持基于 MessagePack 的二进制协议，并可创建自定义协议。
- ASP.NET Core SignalR 不支持 ASP.NET SignalR 支持的永久帧传输。
- ASP.NET Core SignalR 必须通过 `services.AddSignalR()` `app.UseEndpoints` 分别在和中添加和进行配置 `Startup.ConfigureServices` `Startup.Configure` 。
- ASP.NET Core SignalR 需要粘滞会话;ASP.NET SignalR。
- ASP.NET Core 简化了连接模型;仅连接到单个集线器。
- ASP.NET Core SignalR 支持从集线器向客户端流式传输数据。
- ASP.NET Core SignalR 不支持在客户端和中心之间传递状态。
- `PersistentConnection`类在 ASP.NET Core SignalR 中不存在。
- ASP.NET SignalR 支持 SQL Server 和 Redis。 ASP.NET Core SignalR 支持 [Azure SignalR](/azure/azure-signalr/) 和 Redis。

## <a name="references"></a>参考

- [ASP.NET SignalR 和 ASP.NET Core SignalR 之间的差异](/aspnet/core/signalr/version-differences)
- [Azure SignalR 服务](/azure/azure-signalr/)

>[!div class="step-by-step"]
>[上一页](razor-differences.md)
>[下一页](testing-differences.md)
