---
description: 了解详细信息： StackOverflowInfo 结构
title: StackOverflowInfo 结构
ms.date: 03/30/2017
api_name:
- StackOverflowInfo
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- StackOverflowInfo
helpviewer_keywords:
- StackOverflowInfo structure [.NET Framework hosting]
ms.assetid: 519389f2-0217-436c-99d4-93a76ebce5b5
topic_type:
- apiref
ms.openlocfilehash: cca65e4293c05b89ebefc3c6dd36a6b8898eb15f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99679389"
---
# <a name="stackoverflowinfo-structure"></a>StackOverflowInfo 结构

存储发生的溢出的类型以及因溢出而引发的异常的信息。  
  
## <a name="syntax"></a>语法  
  
```cpp  
typedef struct _StackOverflowInfo {  
    StackOverflowType   soType;  
    EXCEPTION_POINTERS  *pExceptionInfo;  
} StackOverflowInfo;  
```  
  
## <a name="members"></a>成员  
  
|成员|说明|  
|------------|-----------------|  
|`soType`|指定溢出类型的 [StackOverflowType](stackoverflowtype-enumeration.md) 枚举的值。|  
|`pExceptionInfo`|一个指向 Win32 对象的指针 `EXCEPTION_POINTERS` ，该对象包含一个异常记录，其中包含与计算机无关的异常说明和一个上下文记录，其中包含发生异常时的处理器上下文的依赖于计算机的说明。|  
  
## <a name="remarks"></a>备注  

 `StackOverflowInfo`对象将传递到事件的[IActionOnCLREvent：： OnEvent](iactiononclrevent-onevent-method.md)方法 `Event_StackOverflow` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [承载结构](hosting-structures.md)
