---
description: 了解详细信息： ICLRPolicyManager 接口
title: ICLRPolicyManager 接口
ms.date: 03/30/2017
api_name:
- ICLRPolicyManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRPolicyManager
helpviewer_keywords:
- ICLRPolicyManager interface [.NET Framework hosting]
ms.assetid: 5c834aa1-f2db-408a-b230-c7bec093d364
topic_type:
- apiref
ms.openlocfilehash: 8823f1db8b15b327306ff3c592b46c94537f4331
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99637373"
---
# <a name="iclrpolicymanager-interface"></a>ICLRPolicyManager 接口

提供允许主机指定在发生故障和超时时要执行的策略操作的方法。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[SetActionOnFailure 方法](iclrpolicymanager-setactiononfailure-method.md)|指定发生指定的故障时公共语言运行时 (CLR) 应执行的策略操作。|  
|[SetActionOnTimeout 方法](iclrpolicymanager-setactionontimeout-method.md)|指定在指定操作超时时 CLR 应执行的策略操作。|  
|[SetDefaultAction 方法](iclrpolicymanager-setdefaultaction-method.md)|指定发生指定操作时 CLR 应执行的策略操作。|  
|[SetTimeout 方法](iclrpolicymanager-settimeout-method.md)|设置指定操作的超时值。|  
|[SetTimeoutAndAction 方法](iclrpolicymanager-settimeoutandaction-method.md)|设置指定操作的超时值，并指定该操作发生时 CLR 应执行的策略操作。|  
|[SetUnhandledExceptionPolicy 方法](iclrpolicymanager-setunhandledexceptionpolicy-method.md)|指定发生未经处理的异常时 CLR 的行为。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [EClrFailure 枚举](eclrfailure-enumeration.md)
- [EClrOperation 枚举](eclroperation-enumeration.md)
- [EPolicyAction 枚举](epolicyaction-enumeration.md)
- [ICLRControl 接口](iclrcontrol-interface.md)
