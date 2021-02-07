---
description: 了解详细信息：每秒队列丢弃的消息数
title: 每秒丢弃的排队消息数
ms.date: 03/30/2017
ms.assetid: 74540f52-8762-4147-b5ba-e171180515a3
ms.openlocfilehash: e5959b76795514dec03d6ae4d08ac248994777fa
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99759544"
---
# <a name="queue-dropped-messages-per-second"></a>每秒丢弃的排队消息数

计数器名称：Queued Messages Dropped Per Second（每秒丢弃的排队消息数）。  
  
## <a name="description"></a>说明  

 此服务处的排队传输机制每秒丢弃的消息数。  
  
 此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
