---
description: 了解详细信息：每秒实例数
title: 每秒实例数
ms.date: 03/30/2017
ms.assetid: 74579397-1058-4278-80cf-2d00854a480f
ms.openlocfilehash: cfcdd85bef8b1873101c1bbb63ce40bd161a97f4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99655300"
---
# <a name="instances-per-second"></a>每秒实例数

计数器名称：Instances Created Per Second（每秒创建的实例数）。  
  
## <a name="description"></a>说明  

 每秒创建的服务实例的总数。  
  
 此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
