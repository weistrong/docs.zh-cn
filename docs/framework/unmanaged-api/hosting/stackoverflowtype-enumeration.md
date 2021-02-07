---
description: 了解详细信息： StackOverflowType 枚举
title: StackOverflowType 枚举
ms.date: 03/30/2017
api_name:
- StackOverflowType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- StackOverflowType
helpviewer_keywords:
- StackOverflowType enumeration [.NET Framework hosting]
ms.assetid: dab648ad-972b-479c-b129-b4c1dcbd932e
topic_type:
- apiref
ms.openlocfilehash: d39ccd99331a3e839236f1ede21254edb92b2dfb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99679350"
---
# <a name="stackoverflowtype-enumeration"></a>StackOverflowType 枚举

包含指示堆栈溢出事件的根本原因的值。  
  
## <a name="syntax"></a>语法  
  
```cpp  
typedef enum {  
    SO_Managed,  
    SO_ClrEngine,  
    SO_Other  
} StackOverflowType;  
```  
  
## <a name="members"></a>成员  
  
|成员|说明|  
|------------|-----------------|  
|`SO_ClrEngine`|堆栈溢出由执行引擎引起。|  
|`SO_Managed`|堆栈溢出由托管代码引起。|  
|`SO_Other`|堆栈溢出由非托管代码引起。|  
  
## <a name="remarks"></a>备注  

 此信息通过调用 [IActionOnCLREvent：： OnEvent](iactiononclrevent-onevent-method.md) 方法传递到主机。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [承载枚举](hosting-enumerations.md)
