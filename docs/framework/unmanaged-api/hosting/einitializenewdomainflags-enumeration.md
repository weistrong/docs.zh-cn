---
description: 了解详细信息： EInitializeNewDomainFlags 枚举
title: EInitializeNewDomainFlags 枚举
ms.date: 03/30/2017
api_name:
- EInitializeNewDomainFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EInitializeNewDomainFlags
helpviewer_keywords:
- EInitializeNewDomainFlags enumeration [.NET Framework hosting]
ms.assetid: 3a120ab2-f5ef-4c9b-8595-d3ed7247c342
ms.openlocfilehash: b856d061e86c0c79b35f842975378307b79a37e7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785459"
---
# <a name="einitializenewdomainflags-enumeration"></a>EInitializeNewDomainFlags 枚举

使宿主能够向运行时提供有关应用程序域初始化的信息。  
  
## <a name="syntax"></a>语法  
  
```cpp  
typedef enum {  
    eInitializeNewDomainFlags_None              = 0x0000,  
    eInitializeNewDomainFlags_NoSecurityChanges = 0x0002  
} EInitializeNewDomainFlags;  
```  
  
## <a name="members"></a>成员  
  
|成员|说明|  
|------------|-----------------|  
|`eInitializeNewDomainFlags_None`|无标志。|  
|`eInitializeNewDomainFlags_NoSecurityChanges`|通知公共语言运行时 (CLR) 宿主不会在方法中更改应用程序域的安全状态 <xref:System.AppDomainManager.InitializeNewDomain%2A> 。|  
  
## <a name="remarks"></a>备注  

 [ICLRDomainManager：： SetAppDomainManagerType](iclrdomainmanager-setappdomainmanagertype-method.md)方法采用类型的参数 `EInitializeNewDomainFlags` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [承载枚举](hosting-enumerations.md)
- [SetAppDomainManagerType 方法](iclrdomainmanager-setappdomainmanagertype-method.md)
