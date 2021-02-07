---
description: 了解详细信息： COR_NATIVE_LINK 结构
title: COR_NATIVE_LINK 结构
ms.date: 03/30/2017
api_name:
- COR_NATIVE_LINK
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- COR_NATIVE_LINK
helpviewer_keywords:
- COR_NATIVE_LINK structure [.NET Framework metadata]
ms.assetid: 6ef78d3c-1c69-4141-b687-dcb065b7a74d
topic_type:
- apiref
ms.openlocfilehash: 09c715af698a0614fd4a9a17679df6908a1497a6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678570"
---
# <a name="cor_native_link-structure"></a>COR_NATIVE_LINK 结构

包含用于链接本机代码的信息。  
  
## <a name="syntax"></a>语法  
  
```cpp  
typedef struct
{  
    BYTE        m_linkType;  
    BYTE        m_flags;  
    mdMemberRef m_entryPoint;  
} COR_NATIVE_LINK;  
```  
  
## <a name="members"></a>成员  
  
|成员|说明|  
|------------|-----------------|  
|`m_linkType`|要在本机代码中链接的类型。 此值为 [CorNativeLinkType](cornativelinktype-enumeration.md) 值之一。|  
|`m_flags`|链接本机代码时链接器使用的标志。 此值为 [CorNativeLinkFlags](cornativelinkflags-enumeration.md) 值之一。|  
|`m_entryPoint`|表示入口点的 MemberRef 元数据标记。 格式为 `lib:entrypoint`。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cor  
  
 **库：** 用作 MsCorEE.dll 中的资源  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [元数据结构](metadata-structures.md)
- [CorNativeLinkType 枚举](cornativelinktype-enumeration.md)
- [CorNativeLinkFlags 枚举](cornativelinkflags-enumeration.md)
