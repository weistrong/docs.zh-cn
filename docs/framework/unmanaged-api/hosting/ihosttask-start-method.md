---
description: 了解详细信息： IHostTask：： Start 方法
title: IHostTask::Start 方法
ms.date: 03/30/2017
api_name:
- IHostTask.Start
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTask::Start
helpviewer_keywords:
- IHostTask::Start method [.NET Framework hosting]
- Start method, IHostTask interface [.NET Framework hosting]
ms.assetid: b18742b0-d8c4-401c-ae89-e6eccdaa81d0
topic_type:
- apiref
ms.openlocfilehash: 48352a3df49ba2ef3e008ed211da19f54deb82f6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784621"
---
# <a name="ihosttaskstart-method"></a>IHostTask::Start 方法

请求宿主将当前 [IHostTask](ihosttask-interface.md) 实例表示的任务从挂起状态移动到实时状态，在此状态下可以执行代码。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT Start ();  
```  
  
## <a name="return-value"></a>返回值  
  
|HRESULT|说明|  
|-------------|-----------------|  
|S_OK|已成功启动。|  
|E_FAIL|发生未知的灾难性故障。 当方法返回 E_FAIL 时，公共语言运行时 (CLR) 在该进程内不再可用。 对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。|  
  
## <a name="remarks"></a>备注  

 `Start` 始终返回 S_OK 的 HRESULT 值，但发生灾难性故障的情况除外。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICLRTask 接口](iclrtask-interface.md)
- [ICLRTaskManager 接口](iclrtaskmanager-interface.md)
- [IHostTask 接口](ihosttask-interface.md)
- [IHostTaskManager 接口](ihosttaskmanager-interface.md)
