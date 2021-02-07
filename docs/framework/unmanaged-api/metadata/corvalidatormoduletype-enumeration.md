---
description: 了解详细信息： CorValidatorModuleType 枚举
title: CorValidatorModuleType 枚举
ms.date: 03/30/2017
api_name:
- CorValidatorModuleType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorValidatorModuleType
helpviewer_keywords:
- CorValidatorModuleType enumeration [.NET Framework metadata]
ms.assetid: 748f1ab2-fbcb-4f55-89ec-8d23d81ebc80
topic_type:
- apiref
ms.openlocfilehash: 13792c461660ddd8cfd530f5b34d642d806cdea4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707229"
---
# <a name="corvalidatormoduletype-enumeration"></a>CorValidatorModuleType 枚举

指定模块的类型。  
  
## <a name="syntax"></a>语法  
  
```cpp  
typedef enum  
{  
    ValidatorModuleTypeInvalid  = 0x0,  
    ValidatorModuleTypeMin      = 0x00000001,  
    ValidatorModuleTypePE       = 0x00000001,  
    ValidatorModuleTypeObj      = 0x00000002,  
    ValidatorModuleTypeEnc      = 0x00000003,  
    ValidatorModuleTypeIncr     = 0x00000004,  
    ValidatorModuleTypeMax      = 0x00000004  
} CorValidatorModuleType;  
```  
  
## <a name="members"></a>成员  
  
|成员|说明|  
|------------|-----------------|  
|`ValidatorModuleTypeInvalid`|模块是无效类型。|  
|`ValidatorModuleTypeMin`|枚举的最小值 `CorValidatorModuleType` 。|  
|`ValidatorModuleTypePE`|模块是可移植的可执行文件 (PE) 文件。|  
|`ValidatorModuleTypeObj`|模块是 .obj 文件。|  
|`ValidatorModuleTypeEnc`|模块是 "编辑并继续" 调试器会话。|  
|`ValidatorModuleTypeIncr`|模块是增量生成的模块。|  
|`ValidatorModuleTypeMax`|枚举的最大值 `CorValidatorModuleType` 。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 作为中的资源包含 MsCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [元数据枚举](metadata-enumerations.md)
