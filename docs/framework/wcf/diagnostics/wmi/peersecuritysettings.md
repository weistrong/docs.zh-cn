---
description: 了解详细信息： PeerSecuritySettings
title: PeerSecuritySettings
ms.date: 03/30/2017
ms.assetid: 24ae0d35-f3a3-419b-afd6-686e22aae27b
ms.openlocfilehash: a8b5b8c88e71cb46110fa35186599c0f9c366d17
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803004"
---
# <a name="peersecuritysettings"></a>PeerSecuritySettings

PeerSecuritySettings  
  
## <a name="syntax"></a>语法  
  
```csharp
class PeerSecuritySettings  
{  
  string Mode;  
  PeerTransportSecuritySettings Transport;  
};  
```  
  
## <a name="methods"></a>方法  

 PeerSecuritySettings 类不定义任何方法。  
  
## <a name="properties"></a>属性  

 PeerSecuritySettings 类具有下列属性：  
  
### <a name="mode"></a>模型  

 数据类型：字符串  
  
 访问类型：只读  
  
 配置有绑定的终结点是否使用消息级别和传输级别安全。  
  
### <a name="transport"></a>Transport  

 数据类型：PeerTransportSecuritySettings  
  
 访问类型：只读  
  
 传输安全设置。  
  
## <a name="requirements"></a>要求  
  
|MOF|已在 Servicemodel.mof 中声明。|  
|---------|-----------------------------------|  
|命名空间|已在 root\ServiceModel 中定义|  
  
## <a name="see-also"></a>请参阅

- <xref:System.ServiceModel.PeerSecuritySettings>
