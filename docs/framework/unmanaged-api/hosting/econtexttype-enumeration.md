---
description: 了解详细信息： EContextType 枚举
title: EContextType 枚举
ms.date: 03/30/2017
api_name:
- EContextType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EContextType
helpviewer_keywords:
- EContextType enumeration [.NET Framework hosting]
ms.assetid: 92b926a9-b87e-408a-9036-df7b752c9492
topic_type:
- apiref
ms.openlocfilehash: b7d6ddb385386bb0616a01ef6fcc432f2c925d51
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785522"
---
# <a name="econtexttype-enumeration"></a>EContextType 枚举

描述当前正在执行的线程的安全上下文。  
  
## <a name="syntax"></a>语法  
  
```cpp  
typedef enum {  
    eCurrentContext    = 0x00,  
    eRestrictedContext = 0x01  
} EContextType;  
```  
  
## <a name="members"></a>成员  
  
|成员|说明|  
|------------|-----------------|  
|`eCurrentContext`|指示当公共语言运行时 (CLR) 在调用[IHostSecurityManager：： SetSecurityContext](ihostsecuritymanager-setsecuritycontext-method.md)方法的调用中调用[IHostSecurityManager：： GETSECURITYCONTEXT](ihostsecuritymanager-getsecuritycontext-method.md)方法或 CLR 请求的上下文时，当前线程上的上下文。|  
|`eRestrictedContext`|指示宿主具有更低权限的上下文，如垃圾回收器或类或模块构造函数。|  
  
## <a name="remarks"></a>备注  

 `EContextType`在对和方法的调用中，CLR 将值之一作为参数值 `IHostSecurityManager::GetSecurityContext` 提供 `IHostSecurityManager::SetSecurityContext` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IHostSecurityContext 接口](ihostsecuritycontext-interface.md)
- [IHostSecurityManager 接口](ihostsecuritymanager-interface.md)
- [承载枚举](hosting-enumerations.md)
