---
description: 了解详细信息：调用持续时间
title: 调用持续时间
ms.date: 03/30/2017
ms.assetid: e4973ec3-3c66-4c0b-b5d0-294b62c83f7d
ms.openlocfilehash: 334ab1e6ef0b3b5abc2c58876e018c1a8499cb6c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99759726"
---
# <a name="calls-duration"></a>调用持续时间

计数器名称：调用持续时间  
  
## <a name="description"></a>说明  

 调用该操作的平均持续时间。 平均持续时间根据此公式计算：(N1-N0)/(D1-D0)。  
  
> [!WARNING]
> 在异步 WCF 服务上使用时，调用 Duration 计数器将始终返回-1。  
  
## <a name="see-also"></a>请参阅

- [PERF_AVERAGE_TIMER](/previous-versions/windows/embedded/ms938538(v=msdn.10))
