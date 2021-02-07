---
description: 了解详细信息： ICLRErrorReportingManager：： BeginCustomDump 方法
title: ICLRErrorReportingManager::BeginCustomDump 方法
ms.date: 03/30/2017
api_name:
- ICLRErrorReportingManager.BeginCustomDump
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRErrorReportingManager::BeginCustomDump
helpviewer_keywords:
- ICLRErrorReportingManager::BeginCustomDump method [.NET Framework hosting]
- BeginCustomDump method
ms.assetid: 93424a87-ba13-4fa1-b4dc-69d44437b7ae
topic_type:
- apiref
ms.openlocfilehash: 3f8498068d50ffc6ea00cf4f08f969c92f010d6c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689477"
---
# <a name="iclrerrorreportingmanagerbegincustomdump-method"></a>ICLRErrorReportingManager::BeginCustomDump 方法

指定用于错误报告的自定义堆转储配置。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT BeginCustomDump (  
    [in] ECustomDumpFlavor dwFlavor,  
    [in] DWORD dwNumItems,  
    [in, size_is(dwNumItems), length_is(dwNumItems)] CustomDumpItem items[],  
    DWORD dwReserved  
);  
```  
  
## <a name="parameters"></a>参数  

 `dwFlavor`  
 中一个 [ECustomDumpFlavor](ecustomdumpflavor-enumeration.md) 值，指示用于生成自定义堆转储的堆转储的种类。  
  
 `dwNumItems`  
 中数组的长度 `items` 。 如果 `dwFlavor` 不是 DUMP_FLAVOR_Mini，则 `dwNumItems` 应为零。  
  
 `items`  
 中 [CustomDumpItem](customdumpitem-structure.md) 实例的数组，指定要添加到小型转储中的项。 如果 `dwFlavor` 不 DUMP_FLAVOR_Mini，则 `items` 应为 null。  
  
 `dwReserved`  
 中保留供将来使用。  
  
## <a name="return-value"></a>返回值  
  
|HRESULT|说明|  
|-------------|-----------------|  
|S_OK|该方法已成功返回。|  
|HOST_E_CLRNOTAVAILABLE| (CLR) 的公共语言运行时未加载到进程中，或 CLR 处于无法运行托管代码或成功处理调用的状态。|  
|HOST_E_TIMEOUT|调用超时。|  
|HOST_E_NOT_OWNER|调用方不拥有该锁。|  
|HOST_E_ABANDONED|已阻止的线程或纤程正在等待某个事件时，该事件被取消。|  
|E_FAIL|发生未知的灾难性故障。 方法返回 E_FAIL 后，CLR 在该进程内将不再可用。 对宿主方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。|  
  
## <a name="remarks"></a>备注  

 `BeginCustomDump`方法设置自定义堆转储配置。 [EndCustomDump](iclrerrorreportingmanager-endcustomdump-method.md)方法清除自定义堆转储配置并释放任何关联的状态。 应在自定义堆转储完成后调用它。  
  
> [!IMPORTANT]
> 调用失败 `EndCustomDump` 会导致内存泄露。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [CustomDumpItem 结构](customdumpitem-structure.md)
- [ECustomDumpFlavor 枚举](ecustomdumpflavor-enumeration.md)
- [ICLRErrorReportingManager 接口](iclrerrorreportingmanager-interface.md)
