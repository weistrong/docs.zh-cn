---
description: 了解详细信息：每秒排队的病毒消息数
title: 每秒排队病毒消息数
ms.date: 03/30/2017
ms.assetid: d193fdd1-02f1-44a0-906e-f632a8f574c3
ms.openlocfilehash: 3240974445debf86ff17187e4c6762b39610bd46
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99744079"
---
# <a name="queued-poison-messages-per-second"></a>每秒排队病毒消息数

计数器名称：Queued Poison Messages Per Second（每秒排队病毒消息数）。  
  
## <a name="description"></a>说明  

 此服务中每秒由排队传输标记为病毒消息的消息数。  
  
 此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
