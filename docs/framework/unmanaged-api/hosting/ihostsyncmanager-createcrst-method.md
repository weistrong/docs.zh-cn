---
description: 了解详细信息： IHostSyncManager：： CreateCrst 方法
title: IHostSyncManager::CreateCrst 方法
ms.date: 03/30/2017
api_name:
- IHostSyncManager.CreateCrst
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSyncManager::CreateCrst
helpviewer_keywords:
- CreateCrst method [.NET Framework hosting]
- IHostSyncManager::CreateCrst method [.NET Framework hosting]
ms.assetid: ac278cc8-2540-4a6c-b5c6-b90c3970b4f4
topic_type:
- apiref
ms.openlocfilehash: 7d1880f1553d159f62efe65afe8368a60b5bf9cc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784803"
---
# <a name="ihostsyncmanagercreatecrst-method"></a>IHostSyncManager::CreateCrst 方法

创建用于同步的临界区对象。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT CreateCrst (  
    [out] IHostCrst** ppCrst  
);  
```  
  
## <a name="parameters"></a>参数  

 `ppCrst`  
 弄指向主机实现的 [IHostCrst](ihostcrst-interface.md) 实例的地址的指针; 如果无法创建关键节，则为 null。  
  
## <a name="return-value"></a>返回值  
  
|HRESULT|说明|  
|-------------|-----------------|  
|S_OK|`CreateCrst` 已成功返回。|  
|HOST_E_CLRNOTAVAILABLE| (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。|  
|HOST_E_TIMEOUT|调用超时。|  
|HOST_E_NOT_OWNER|调用方不拥有该锁。|  
|HOST_E_ABANDONED|已阻止的线程或纤程正在等待某个事件时，该事件被取消。|  
|E_FAIL|发生未知的灾难性故障。 当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。 对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。|  
|E_OUTOFMEMORY|没有足够的内存可用于创建请求的关键部分。|  
  
## <a name="remarks"></a>备注  

 临界区对象提供与 mutex 对象提供的同步，只不过临界区只能由单个进程的线程使用。 `CreateCrst` 对 Win32 函数进行镜像 `InitializeCriticalSection` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICLRSyncManager 接口](iclrsyncmanager-interface.md)
- [IHostCrst 接口](ihostcrst-interface.md)
- [IHostSyncManager 接口](ihostsyncmanager-interface.md)
- [IHostSemaphore 接口](ihostsemaphore-interface.md)
- [Mutex](../../../standard/threading/mutexes.md)
- [Semaphore 和 SemaphoreSlim](../../../standard/threading/semaphore-and-semaphoreslim.md)
