---
description: 了解详细信息： BodyToString 方法
title: 'BodyToString 方法 (System.servicemodel) '
ms.date: 11/01/2019
topic_type:
- apiref
api_name:
- System.ServiceModel.Channels.Message.BodyToString
api_location:
- system.servicemodel.dll
api_type:
- Assembly
ms.openlocfilehash: babcd881d191ff46b98e9999c4ff04166479a68d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99699371"
---
# <a name="messagebodytostring-method"></a>BodyToString 方法

通过调用方法将消息正文转换为字符串 <xref:System.ServiceModel.Channels.Message.OnBodyToString%2A?displayProperty=nameWithType> 。

```csharp
internal void BodyToString(XmlDictionaryWriter writer);
```

## <a name="parameters"></a>参数

- `writer` <xref:System.Xml.XmlDictionaryWriter>\
  用于将消息正文转换为字符串的编写器。

## <a name="remarks"></a>备注

> [!WARNING]
> `Message.BodyToString`方法是内部的，不应在代码中直接使用。
>
> 在任何情况下，Microsoft 不支持在生产应用程序中使用此方法。

## <a name="requirements"></a>要求

**命名空间：** <xref:System.ServiceModel.Channels>

**程序集：** System.ServiceModel.dll

**.NET Framework 版本：** 自3.0 起可用。
