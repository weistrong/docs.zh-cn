---
description: 了解详细信息： DacpGetModuleAddress：： Request 方法
title: DacpGetModuleAddress::Request 方法
ms.date: 01/16/2019
api.name:
- DacpGetModuleAddress::Request Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- DacpGetModuleAddress::Request Method
helpviewer.keywords:
- DacpGetModuleAddress::Request Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 4cdec9cf6b9bd818ce1137fb5b2c691532fab94e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801496"
---
# <a name="dacpgetmoduleaddressrequest-method"></a>DacpGetModuleAddress::Request 方法

执行从给定的运行时结构填充结构的请求。

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a>语法

```cpp
HRESULT Request(
    [in] IXCLRDataModule* pDataModule
);
```

## <a name="parameters"></a>参数

`pDataModule`\
中指向种子数据模块的指针。

## <a name="remarks"></a>备注

此结构存在于运行时中，并且不会通过任何标头或库文件公开。 若要使用它，最简单的方法是模拟实现：

- 返回通过在参数上调用方法获取的值 `Request` ，该方法 `IXCLRDataModule*` 具有以下参数： `((uint32) 0xf0000000, 0, 0, (uint32) sizeof(*this), (uint8*) this)`

## <a name="requirements"></a>要求

**平台：** 查看 [系统要求](../../get-started/system-requirements.md)\
**标头：** 内容
**库：** 内容
**.NET Framework 版本：**[!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]

## <a name="see-also"></a>请参阅

- [调试](index.md)
- [DacpGetModuleAddress 结构](dacpgetmoduleaddress-structure.md)
