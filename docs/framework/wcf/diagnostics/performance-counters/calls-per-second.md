---
description: 了解详细信息：每秒调用数
title: Calls Per Second（每秒调用次数）
ms.date: 03/30/2017
ms.assetid: 0efb5a94-d83b-4793-b529-6fcbedb65c43
ms.openlocfilehash: 1d204e4c88d9f9ab113e59c76f1eaecc280e552e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99759648"
---
# <a name="calls-per-second"></a>Calls Per Second（每秒调用次数）

计数器名称：Calls Per Second（每秒调用次数）  
  
## <a name="description"></a>说明  

 一秒内对此操作调用的次数。  
  
 此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
