---
description: 了解详细信息： IHostPolicyManager 接口
title: IHostPolicyManager 接口
ms.date: 03/30/2017
api_name:
- IHostPolicyManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostPolicyManager
helpviewer_keywords:
- IHostPolicyManager interface [.NET Framework hosting]
ms.assetid: 8c4aa124-5e00-46d9-b1e8-57ba6574bb0d
topic_type:
- apiref
ms.openlocfilehash: d823ee2526019188afd17df903b61a720e18207f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99671907"
---
# <a name="ihostpolicymanager-interface"></a>IHostPolicyManager 接口

提供一些方法，这些方法可通知宿主公共语言运行时 (CLR) 在发生中止、超时或失败时执行的操作。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[OnDefaultAction 方法](ihostpolicymanager-ondefaultaction-method.md)|向宿主通知 CLR 将使用对 [ICLRPolicyManager：： SetDefaultAction](iclrpolicymanager-setdefaultaction-method.md) 的调用指定的默认操作来响应线程中止或 <xref:System.AppDomain> 卸载。|  
|[OnFailure 方法](ihostpolicymanager-onfailure-method.md)|向宿主通知 CLR 即将获取调用 [ICLRPolicyManager：： SetActionOnFailure](iclrpolicymanager-setactiononfailure-method.md) 所指定的操作，以响应资源分配或回收失败。|  
|[OnTimeout 方法](ihostpolicymanager-ontimeout-method.md)|向宿主通知 CLR 即将使用对 [ICLRPolicyManager：： SetActionOnTimeout](iclrpolicymanager-setactionontimeout-method.md) 的调用指定的操作来响应超时。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [EClrFailure 枚举](eclrfailure-enumeration.md)
- [EClrOperation 枚举](eclroperation-enumeration.md)
- [EPolicyAction 枚举](epolicyaction-enumeration.md)
- [ICLRPolicyManager 接口](iclrpolicymanager-interface.md)
- [承载接口](hosting-interfaces.md)
