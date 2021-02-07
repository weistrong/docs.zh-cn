---
description: 了解详细信息：每秒调用失败数
title: Calls Failed Per Second（每秒失败的调用次数）
ms.date: 03/30/2017
ms.assetid: e4ef3773-f650-4876-99cf-4d0c02aa03d4
ms.openlocfilehash: 3961754eb73743a1213922f7c9e1bd164334cd6e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99759713"
---
# <a name="calls-failed-per-second"></a>Calls Failed Per Second（每秒失败的调用次数）

计数器名称：Calls Failed Per Second（每秒失败的调用次数）  
  
## <a name="description"></a>说明  

 该操作中每秒钟出现未处理异常的调用数目。  
  
 此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)  
  
 此操作中每次出现未处理的异常时，此计数器都会递增。  
  
## <a name="see-also"></a>请参阅

- [在协定和服务中指定和处理错误](../../specifying-and-handling-faults-in-contracts-and-services.md)
