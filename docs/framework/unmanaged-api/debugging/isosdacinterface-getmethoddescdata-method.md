---
description: 了解详细信息： ISOSDacInterface：： GetMethodDescData 方法
title: ISOSDacInterface：： GetMethodDescData 方法
ms.date: 01/16/2019
api.name:
- ISOSDacInterface::GetMethodDescData Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- ISOSDacInterface::GetMethodDescData Method
helpviewer.keywords:
- ISOSDacInterface::GetMethodDescData Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: a1284aa4d810ed9d6db7ad3c1b471702b1dad54d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790420"
---
# <a name="isosdacinterfacegetmethoddescdata-method"></a>ISOSDacInterface：： GetMethodDescData 方法

获取给定 MethodDesc 指针的数据。

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>语法

```cpp
HRESULT GetMethodDescData(
    CLRDATA_ADDRESS            methodDesc,
    CLRDATA_ADDRESS            ip,
    DacpMethodDescData *data,
    ULONG                      cRevertedRejitVersions,
    DacpReJitData      *rgRevertedRejitData,
    void                      *pcNeededRevertedRejitData
);
```

## <a name="parameters"></a>参数

`methodDesc`\
中MethodDesc 的地址。

`ip`\
中方法的 IP 地址。

`data`\
弄与 MethodDesc 关联的、从内部 Api 返回的数据。

`cRevertedRejitVersions`\
弄已还原的 rejit 版本数。

`rgRevertedRejitData`\
弄与从内部 Api 返回的已恢复 rejit 版本关联的数据。

`pcNeededRevertedRejitData`\
弄存储与还原的 ReJit 版本关联的数据所需的字节数。

## <a name="remarks"></a>备注

提供的方法是接口的一部分 `ISOSDacInterface` ，并且对应于虚拟方法表的21槽。 若要使用它们， [`CLRDATA_ADDRESS`](../common-data-types-unmanaged-api-reference.md) 必须将定义为64位无符号整数。

## <a name="requirements"></a>要求

**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
**标头：** 内容  
**库：** 内容  
**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]  

## <a name="see-also"></a>请参阅

- [调试](index.md)
- [ISOSDacInterface 接口](isosdacinterface-interface.md)
