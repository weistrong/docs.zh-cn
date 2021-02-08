---
description: 了解详细信息： PeerCustomResolverBindingElement
title: PeerCustomResolverBindingElement
ms.date: 03/30/2017
ms.assetid: 9ccc2770-a20e-4dff-9970-f56ad8aec2b5
ms.openlocfilehash: f4277c04818eec69c1041eee30282d3111421eaa
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803043"
---
# <a name="peercustomresolverbindingelement"></a>PeerCustomResolverBindingElement

PeerCustomResolverBindingElement

## <a name="syntax"></a>语法

```csharp
class PeerCustomResolverBindingElement : PeerResolverBindingElement
{
    string Address;
    string Binding;
};
```

## <a name="methods"></a>方法

PeerCustomResolverBindingElement 类不定义任何方法。

## <a name="properties"></a>属性

 PeerCustomResolverBindingElement 类具有下列属性：

### <a name="address"></a>地址

数据类型：字符串

访问类型：只读

对等自定义解析程序的地址。

### <a name="binding"></a>绑定

数据类型：字符串

访问类型：只读

绑定的配置名称。

## <a name="requirements"></a>要求

|MOF|已在 Servicemodel.mof 中声明。|
|---------|-----------------------------------|
|命名空间|已在 root\ServiceModel 中定义|

## <a name="see-also"></a>请参阅

- <xref:System.ServiceModel.Channels.PeerCustomResolverBindingElement>
