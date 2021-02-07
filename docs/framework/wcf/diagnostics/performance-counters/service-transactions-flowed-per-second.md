---
description: 了解详细信息：服务：每秒流动的事务数
title: 服务：Transactions Flowed Per Second（每秒流动的事务数）
ms.date: 03/30/2017
ms.assetid: ec72eb49-2942-4811-91df-d6e5dad81fd8
ms.openlocfilehash: aae78853272b46a97ce25a710039661f36bf7079
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99759492"
---
# <a name="service-transactions-flowed-per-second"></a>服务：Transactions Flowed Per Second（每秒流动的事务数）

计数器名称：Transactions Flowed Per Second（每秒流动的事务数）。  
  
## <a name="description"></a>说明  

 一秒内流向此服务中操作的事务数。  
  
 此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
