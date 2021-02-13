---
title: 中断性变更：Kestrel：日志消息属性已更改
description: 了解 ASP.NET Core 6.0 中的以下中断性变更：Kestrel：日志消息属性已更改
author: scottaddie
ms.author: scaddie
ms.date: 02/01/2021
ms.openlocfilehash: 30b03c22a6c85623fec7db14b58b169f887395a0
ms.sourcegitcommit: 4df8e005c074ceb1f978f007b222fe253be2baf3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2021
ms.locfileid: "99551528"
---
# <a name="kestrel-log-message-attributes-changed"></a>Kestrel：日志消息属性已更改

Kestrel 日志消息具有关联的 ID 和名称。 这些属性唯一地标识了不同类型的日志消息。 其中一些 ID 和名称是错误重复的。 这个重复问题在 ASP.NET Core 6.0 中得到了修复。

## <a name="version-introduced"></a>引入的版本

6.0

## <a name="old-behavior"></a>旧行为

下表显示 ASP.NET Core 6.0 之前受影响的日志消息的状态。

| 消息描述                   | 名称                    | ID |
|---------------------------------------|-------------------------|----|
| HTTP/2 连接关闭日志消息 | `Http2ConnectionClosed` | 36 |
| HTTP/2 帧发送日志消息     | `Http2FrameReceived`    | 37 |

## <a name="new-behavior"></a>新行为

下表显示 ASP.NET Core 6.0 中受影响的日志消息的状态。

| 消息描述                   | 名称                    | ID |
|---------------------------------------|-------------------------|----|
| HTTP/2 连接关闭日志消息 | `Http2ConnectionClosed` | 48 |
| HTTP/2 帧发送日志消息     | `Http2FrameSending`     | 49 |

## <a name="reason-for-change"></a>更改原因

日志 ID 和名称应是唯一的，这样才能识别不同的消息类型。

## <a name="recommended-action"></a>建议的操作

如果你的代码或配置引用了旧的 ID 和名称，请更新这些引用以使用新的 ID 和名称。

<!--

## Category

ASP.NET Core

## Affected APIs

Not detectable via API analysis

-->
