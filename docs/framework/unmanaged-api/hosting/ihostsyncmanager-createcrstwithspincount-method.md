---
description: 了解详细信息： IHostSyncManager：： CreateCrstWithSpinCount 方法
title: IHostSyncManager::CreateCrstWithSpinCount 方法
ms.date: 03/30/2017
api_name:
- IHostSyncManager.CreateCrstWithSpinCount
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostSyncManager::CreateCrstWithSpinCount
helpviewer_keywords:
- CreateCrstWithSpinCount method [.NET Framework hosting]
- IHostSyncManager::CreateCrstWithSpinCount method [.NET Framework hosting]
ms.assetid: 7280fa8c-3639-4abf-91cb-bc343da742d1
topic_type:
- apiref
ms.openlocfilehash: 3c43f1a3d52eb7174844ecb4079cf54413f20853
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784816"
---
# <a name="ihostsyncmanagercreatecrstwithspincount-method"></a>IHostSyncManager::CreateCrstWithSpinCount 方法

使用自旋计数为同步创建一个临界区对象。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT CreateCrstWithSpinCount (  
    [in]  DWORD dwSpinCount,  
    [out] IHostCrst** ppCrst  
);  
```  
  
## <a name="parameters"></a>参数  

 `dwSpinCount`  
 中为临界区对象指定自旋计数。  
  
 `ppCrst`  
 弄指向 [IHostCrst](ihostcrst-interface.md) 实例的地址的指针; 如果无法创建关键节，则为 null。  
  
## <a name="return-value"></a>返回值  
  
|HRESULT|说明|  
|-------------|-----------------|  
|S_OK|`CreateCrstWithSpinCount` 已成功返回。|  
|HOST_E_CLRNOTAVAILABLE| (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。|  
|HOST_E_TIMEOUT|调用超时。|  
|HOST_E_NOT_OWNER|调用方不拥有该锁。|  
|HOST_E_ABANDONED|已阻止的线程或纤程正在等待某个事件时，该事件被取消。|  
|E_FAIL|发生未知的灾难性故障。 当方法返回 E_FAIL 时，CLR 在该进程内将不再可用。 对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。|  
|E_OUTOFMEMORY|没有足够的内存可用于创建请求的关键部分。|  
  
## <a name="remarks"></a>备注  

 自旋计数仅在多处理器系统上使用。 自旋计数指定调用线程在与不可用关键部分关联的信号量上执行等待操作之前必须旋转的次数。 如果在自旋操作期间关键部分变为免费，则调用线程将避免等待操作。 `CreateCrstWithSpinCount` 对 Win32 函数进行镜像 `InitializeCriticalSectionAndSpinCount` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICLRSyncManager 接口](iclrsyncmanager-interface.md)
- [IHostSemaphore 接口](ihostsemaphore-interface.md)
- [IHostSyncManager 接口](ihostsyncmanager-interface.md)
