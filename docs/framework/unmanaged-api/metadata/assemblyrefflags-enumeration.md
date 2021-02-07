---
description: 了解详细信息： AssemblyRefFlags 枚举
title: AssemblyRefFlags 枚举
ms.date: 03/30/2017
api_name:
- AssemblyRefFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- AssemblyRefFlags
helpviewer_keywords:
- AssemblyRefFlags enumeration [.NET Framework metadata]
ms.assetid: decd4f46-f3b2-466f-9501-e74f2b86b846
topic_type:
- apiref
ms.openlocfilehash: 1b33faf816194c8b386f34a63d885ba37c4329a4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678895"
---
# <a name="assemblyrefflags-enumeration"></a>AssemblyRefFlags 枚举

包含用于描述程序集引用的功能的值。  
  
## <a name="syntax"></a>语法  
  
```cpp  
typedef enum {  
    arfFullOriginator = 0x0001  
} AssemblyRefFlags;  
```  
  
## <a name="members"></a>成员  
  
|成员|说明|  
|------------|-----------------|  
|`arfFullOriginator`|指定程序集引用包含有关程序集的发布服务器的完整的未哈哈希信息。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [元数据枚举](metadata-enumerations.md)
- [IMetaDataAssemblyEmit 接口](imetadataassemblyemit-interface.md)
- [DefineAssemblyRef 方法](imetadataassemblyemit-defineassemblyref-method.md)
