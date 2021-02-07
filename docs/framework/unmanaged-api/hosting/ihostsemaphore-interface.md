---
description: 了解详细信息： IHostSemaphore 接口
title: IHostSemaphore 接口
ms.date: 03/30/2017
api_name:
- IHostSemaphore
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSemaphore
helpviewer_keywords:
- IHostSemaphore interface [.NET Framework hosting]
ms.assetid: c0765321-656c-441e-bab5-58176292be1e
topic_type:
- apiref
ms.openlocfilehash: 682f1f70925310e93f88f1dc314052e801a5e87b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99671342"
---
# <a name="ihostsemaphore-interface"></a>IHostSemaphore 接口

表示线程的信号量的主机实现。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[ReleaseSemaphore 方法](ihostsemaphore-releasesemaphore-method.md)|`IHostSemaphore`按指定量增加当前实例的计数。|  
|[Wait 方法](ihostsemaphore-wait-method.md)|使当前 `IHostSemaphore` 实例等待，直到其拥有或经过指定的时间量。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICLRSyncManager 接口](iclrsyncmanager-interface.md)
- [IHostAutoEvent 接口](ihostautoevent-interface.md)
- [IHostManualEvent 接口](ihostmanualevent-interface.md)
- [IHostSyncManager 接口](ihostsyncmanager-interface.md)
- [承载接口](hosting-interfaces.md)
