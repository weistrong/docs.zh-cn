---
description: 了解详细信息： MemoryStream. InternalGetOriginAndLength 方法
title: 'MemoryStream. InternalGetOriginAndLength 方法 (System.IO) '
ms.date: 11/19/2019
topic_type:
- apiref
api_name:
- System.IO.MemoryStream.InternalGetOriginAndLength
api_location:
- mscorlib.dll
api_type:
- Assembly
ms.openlocfilehash: 4232852c0835a43454f36271a43062e1240297a5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99802536"
---
# <a name="memorystreaminternalgetoriginandlength-method"></a>MemoryStream.InternalGetOriginAndLength 方法

获取内存流的源的内部值和长度。

```csharp
internal void InternalGetOriginAndLength(out int origin, out int length)
```

## <a name="parameters"></a>参数

- `origin` <xref:System.Int32>\
  此方法返回时，创建新对象时指定的字节数组的偏移量 <xref:System.IO.MemoryStream> 。 如果创建字节数组，则包含 0 <xref:System.IO.MemoryStream> 。

- `length` <xref:System.Int32>\
  此方法返回时，为内存流中的字节数。

## <a name="remarks"></a>备注

> [!WARNING]
> `MemoryStream.InternalGetOriginAndLength`方法是内部的，不应在代码中直接使用。
>
> 在任何情况下，Microsoft 不支持在生产应用程序中使用此方法。

## <a name="requirements"></a>要求

**命名空间：** <xref:System.IO>

**程序集：** mscorlib.dll (mscorlib.dll 中) 

**.NET Framework 版本：** 自2.0 起可用。
