---
description: 了解详细信息： Endpoint：每秒调用数
title: 终结点：Calls Per Second（每秒调用次数）
ms.date: 03/30/2017
ms.assetid: ca0fc06d-d68f-4236-bd5f-c7ff6214acdd
ms.openlocfilehash: 10e3cb892119999225abaa8b85ea59065650795d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99759570"
---
# <a name="endpoint-calls-per-second"></a>终结点：Calls Per Second（每秒调用次数）

计数器名称：Calls Per Second（每秒调用次数）  
  
## <a name="description"></a>说明  

 一秒内对此终结点的调用次数。  
  
 此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
