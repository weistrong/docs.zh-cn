---
description: 了解详细信息： ECustomDumpItemKind 枚举
title: ECustomDumpItemKind 枚举
ms.date: 03/30/2017
api_name:
- ECustomDumpItemKind
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ECustomDumpItemKind
helpviewer_keywords:
- ECustomDumpItemKind enumeration [.NET Framework hosting]
ms.assetid: 7105a6c8-6e4e-48de-ac3d-74ac75e5de2e
topic_type:
- apiref
ms.openlocfilehash: e12bfdc3cd7c38d8fbb2326e05d05b6a7b2daa27
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785494"
---
# <a name="ecustomdumpitemkind-enumeration"></a>ECustomDumpItemKind 枚举

保留以供将来扩展 [CustomDumpItem](customdumpitem-structure.md) 结构。  
  
## <a name="syntax"></a>语法  
  
```cpp  
typedef enum {  
    DUMP_ITEM_None = 0  
} ECustomDumpItemKind;  
```  
  
## <a name="members"></a>成员  
  
|成员|说明|  
|------------|-----------------|  
|`DUMP_ITEM_None`|留待将来使用。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICLRErrorReportingManager 接口](iclrerrorreportingmanager-interface.md)
- [承载枚举](hosting-enumerations.md)
