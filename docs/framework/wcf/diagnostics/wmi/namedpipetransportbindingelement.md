---
description: 了解详细信息： NamedPipeTransportBindingElement
title: NamedPipeTransportBindingElement
ms.date: 03/30/2017
ms.assetid: c201309c-c528-4b92-a53c-4d48151c5749
ms.openlocfilehash: 7e76b51fdcc64256427141dcae1d980a9fb2db7e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803095"
---
# <a name="namedpipetransportbindingelement"></a>NamedPipeTransportBindingElement

NamedPipeTransportBindingElement  
  
## <a name="syntax"></a>语法  
  
```csharp
class NamedPipeTransportBindingElement : ConnectionOrientedTransportBindingElement  
{  
  NamedPipeConnectionPoolSettings ConnectionPoolSettings;  
};  
```  
  
## <a name="methods"></a>方法  

 NamedPipeTransportBindingElement 类不定义任何方法。  
  
## <a name="properties"></a>属性  

 NamedPipeTransportBindingElement 类具有以下属性：  
  
### <a name="connectionpoolsettings"></a>ConnectionPoolSettings  

 数据类型：NamedPipeConnectionPoolSettings  
  
 访问类型：只读  
  
 连接池设置。  
  
## <a name="requirements"></a>要求  
  
|MOF|已在 Servicemodel.mof 中声明。|  
|---------|-----------------------------------|  
|命名空间|已在 root\ServiceModel 中定义|  
  
## <a name="see-also"></a>请参阅

- <xref:System.ServiceModel.Channels.NamedPipeTransportBindingElement>
