---
description: 了解详细信息： SYMLINEDELTA 结构
title: SYMLINEDELTA 结构
ms.date: 03/30/2017
api_name:
- SYMLINEDELTA
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- SYMLINEDELTA
helpviewer_keywords:
- SYMLINEDELTA structure [.NET Framework debugging]
ms.assetid: 9634e995-d46d-4397-ab66-cc5781d11e4e
topic_type:
- apiref
ms.openlocfilehash: ae00d2be9809b48180d2cd99d05e410624033419
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761442"
---
# <a name="symlinedelta-structure"></a>SYMLINEDELTA 结构

向符号处理程序提供有关因编辑而移动的方法的信息。  
  
## <a name="syntax"></a>语法  
  
```cpp  
typedef struct _SYMLINEDELTA  
    {  
        mdMethodDef  mdMethod;  
        INT32        delta;  
    } SYMLINEDELTA;  
```  
  
## <a name="members"></a>成员  
  
|成员|说明|  
|------------|-----------------|  
|`mdMethod`|方法的元数据标记。|  
|`delta`|此方法已移动的行数。|  
  
## <a name="requirements"></a>要求  

 **标头：** CorSym .idl  
  
## <a name="see-also"></a>请参阅

- [诊断符号存储区结构](diagnostics-symbol-store-structures.md)
