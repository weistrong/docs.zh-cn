---
description: 了解详细信息： CorLocalRefPreservation 枚举
title: CorLocalRefPreservation 枚举
ms.date: 03/30/2017
api_name:
- CorLocalRefPreservation
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorLocalRefPreservation
helpviewer_keywords:
- CorLocalRefPreservation enumeration [.NET Framework metadata]
ms.assetid: 44757163-1228-4213-a4c4-d4de503cc75d
topic_type:
- apiref
ms.openlocfilehash: afcdf6ce22c5f786e8f728cc1e45ad3ca44e7ef5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784413"
---
# <a name="corlocalrefpreservation-enumeration"></a>CorLocalRefPreservation 枚举

包含用于处理本地引用的标志值。  
  
## <a name="syntax"></a>语法  
  
```cpp  
typedef enum CorLocalRefPreservation  
{  
    MDPreserveLocalRefsNone     =   0x00000000,  
    MDPreserveLocalTypeRef      =   0x00000001,  
    MDPreserveLocalMemberRef    =   0x00000002  
} CorLocalRefPreservation;  
```  
  
## <a name="members"></a>成员  
  
|成员|说明|  
|------------|-----------------|  
|`MDPreserveLocalRefsNone`|不保留本地引用。|  
|`MDPreserveLocalTypeRef`|保留本地类型引用。|  
|`MDPreserveLocalMemberRef`|保留局部成员引用。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Corhdr。h  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [元数据枚举](metadata-enumerations.md)
