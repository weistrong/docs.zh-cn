---
description: 了解详细信息：每秒提交的事务处理操作
title: Transacted Operations Committed Per Second（每秒提交的事务处理操作次数）
ms.date: 03/30/2017
ms.assetid: 7318921b-47c4-4c8c-9fdd-41a92061c53f
ms.openlocfilehash: 019906cccc527a032d91eb20328eddbb6d9aada8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99655079"
---
# <a name="transacted-operations-committed-per-second"></a>Transacted Operations Committed Per Second（每秒提交的事务处理操作次数）

计数器名称：Transacted Operations Committed Per Second（每秒提交的事务处理操作次数）。  
  
## <a name="description"></a>说明  

 此服务中每秒提交的事务处理操作的数量。  
  
 此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
