---
description: 了解详细信息：每秒排队拒绝的消息数
title: 每秒拒绝的排队消息数
ms.date: 03/30/2017
ms.assetid: 77ea9aa3-b9e2-4a1d-a65e-5ca115ba0567
ms.openlocfilehash: d0d227a26a49921449786d2c9f885fac13a82bde
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99744066"
---
# <a name="queued-rejected-messages-per-second"></a>每秒拒绝的排队消息数

计数器名称：Queued Messages Rejected Per Second（每秒拒绝的排队消息数）。  
  
## <a name="description"></a>说明  

 此服务中每秒被排队传输拒绝的消息数。  
  
 此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
