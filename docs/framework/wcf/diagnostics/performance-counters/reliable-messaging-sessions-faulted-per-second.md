---
description: 了解详细信息：每秒出错的可靠消息会话数
title: Reliable Messaging Sessions Faulted Per Second（每秒出错的可靠消息会话数）
ms.date: 03/30/2017
ms.assetid: 8f8ca2eb-1be4-4b6a-aa78-fcd3ee145fe8
ms.openlocfilehash: 11759ad659d9e860c94b4428091fc0852ebf038c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99716284"
---
# <a name="reliable-messaging-sessions-faulted-per-second"></a>Reliable Messaging Sessions Faulted Per Second（每秒出错的可靠消息会话数）

计数器名称：Reliable Messaging Sessions Faulted Per Second（每秒出错的可靠消息会话数）。  
  
## <a name="description"></a>说明  

 此服务每秒出错的可靠消息会话的数目。  
  
 此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
