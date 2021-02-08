---
description: 了解详细信息： MessageEncodingBindingElement
title: MessageEncodingBindingElement
ms.date: 03/30/2017
ms.assetid: 7f750742-b96b-498f-bf5e-05933a1a5961
ms.openlocfilehash: 7c6660245165acb67db8af9043d956e8a82d9a03
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803186"
---
# <a name="messageencodingbindingelement"></a>MessageEncodingBindingElement

MessageEncodingBindingElement

## <a name="syntax"></a>语法

```csharp
class MessageEncodingBindingElement : BindingElement
{
    string MessageVersion;
};
```

## <a name="methods"></a>方法

MessageEncodingBindingElement 类不定义任何方法。

## <a name="properties"></a>属性

MessageEncodingBindingElement 类具有以下属性：

### <a name="messageversion"></a>MessageVersion

数据类型：字符串

访问类型：只读

使用绑定发送的 SOAP 版本的消息。

## <a name="requirements"></a>要求

|MOF|已在 Servicemodel.mof 中声明。|
|---------|-----------------------------------|
|命名空间|已在 root\ServiceModel 中定义|

## <a name="see-also"></a>请参阅

- <xref:System.ServiceModel.Channels.MessageEncodingBindingElement>
