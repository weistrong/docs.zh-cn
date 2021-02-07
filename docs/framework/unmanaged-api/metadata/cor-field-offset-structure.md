---
description: 了解详细信息： COR_FIELD_OFFSET 结构
title: COR_FIELD_OFFSET 结构
ms.date: 03/30/2017
api_name:
- COR_FIELD_OFFSET
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- COR_FIELD_OFFSET
helpviewer_keywords:
- COR_FIELD_OFFSET structure [.NET Framework metadata]
ms.assetid: cced5298-277f-4a5a-8ecf-a0050c1096ea
topic_type:
- apiref
ms.openlocfilehash: 7976e79a5484fa467d7ac887a4e1a7fa324abf69
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678622"
---
# <a name="cor_field_offset-structure"></a>COR_FIELD_OFFSET 结构

存储一个类中的指定字段的偏移量。  
  
## <a name="syntax"></a>语法  
  
```cpp  
typedef struct COR_FIELD_OFFSET {  
    mdFieldDef  ridOfField;  
    ULONG       ulOffset;  
} COR_FIELD_OFFSET;  
```  
  
## <a name="members"></a>成员  
  
|成员|说明|  
|------------|-----------------|  
|`ridOfField`|`mdFieldDef`表示字段的元数据标记。|  
|`ulOffset`|字段在其类中的偏移量。|  
  
## <a name="remarks"></a>备注  

 [IMetaDataImport：： GetClassLayout](imetadataimport-getclasslayout-method.md) 和 [IMetaDataEmit：： SetClassLayout](imetadataemit-setclasslayout-method.md) 方法采用类型的参数 `COR_FIELD_OFFSET` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Corhdr.h，Corprof.idl  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [元数据结构](metadata-structures.md)
- [IMetaDataEmit 接口](imetadataemit-interface.md)
- [IMetaDataImport 接口](imetadataimport-interface.md)
