---
description: 了解详细信息： COINITIEE 枚举
title: COINITIEE 枚举
ms.date: 03/30/2017
api_name:
- COINITIEE
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- COINITIEE
helpviewer_keywords:
- COINITIEE enumeration [.NET Framework metadata]
ms.assetid: 64264238-3b68-4bac-a887-36b552426a6c
topic_type:
- apiref
ms.openlocfilehash: c17980582903a29cdfe33c64200c31f29ddeb17c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678583"
---
# <a name="coinitiee-enumeration"></a>COINITIEE 枚举

指定初始化公共语言运行时 [CoInitializeEE](../hosting/coinitializeee-function.md) 使用的常量。  
  
## <a name="syntax"></a>语法  
  
```cpp  
typedef enum tagCOINITEE {  
   COINITEE_DEFAULT = 0x0,  
   COINITEE_DLL     = 0x1,  
   COINITEE_MAIN    = 0x2  
} COINITIEE;  
```  
  
## <a name="members"></a>成员  
  
|成员|说明|  
|------------|-----------------|  
|`COINITEE_DEFAULT`|默认初始化模式。 这将初始化运行时并创建默认值 <xref:System.AppDomain> 。|  
|`COINITEE_DLL`|初始化以运行托管 DLL。|  
|`COINITEE_MAIN`|初始化以运行托管 EXE。 这将初始化运行时，但不会创建默认值 <xref:System.AppDomain> ，该默认值是在输入 EXE 的主例程之后创建的。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 作为中的资源包含 MsCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [元数据枚举](metadata-enumerations.md)
