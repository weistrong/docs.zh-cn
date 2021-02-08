---
description: 了解详细信息： ISOSDacInterface：： GetMethodDescPtrFromIP 方法
title: ISOSDacInterface：： GetMethodDescPtrFromIP 方法
ms.date: 02/01/2019
api.name:
- ISOSDacInterface::GetMethodDescPtrFromIP Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- ISOSDacInterface::GetMethodDescPtrFromIP Method
helpviewer.keywords:
- ISOSDacInterface::GetMethodDescPtrFromIP Method [.NET Framework debugging]
topic_type:
- apiref
author: hoyosjs
ms.author: juhoyosa
ms.openlocfilehash: 8d7c7071b7b3fc520faea71c8d7792317745cfde
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790407"
---
# <a name="isosdacinterfacegetmethoddescptrfromip-method"></a>ISOSDacInterface：： GetMethodDescPtrFromIP 方法

检索与包含给定本机指令地址的方法相对应的 MethodDesc 的指针。

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>语法

```cpp
HRESULT GetMethodDescPtrFromIP(
    CLRDATA_ADDRESS ip,
    CLRDATA_ADDRESS * ppMD
);
```

## <a name="parameters"></a>参数

`ip`\
中运行时方法中的地址。

`ppMD`\
弄特定方法的地址 `MethodDesc` 。

## <a name="remarks"></a>备注

提供的方法是[ `ISOSDacInterface` 接口](isosdacinterface-interface.md)的一部分，并且对应于虚拟方法表的22日槽。

## <a name="requirements"></a>要求

**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
**标头：** 内容  
**库：** 内容  
**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>请参阅

- [调试](index.md)
- [ISOSDacInterface 接口](isosdacinterface-interface.md)
