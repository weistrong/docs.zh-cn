---
description: 了解详细信息： SymmetricSecurityBindingElement
title: SymmetricSecurityBindingElement
ms.date: 03/30/2017
ms.assetid: b2e182b6-c041-4d80-a926-6058068d9f79
ms.openlocfilehash: c158f0bedec91a74b305f359889dd307cff48079
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99715296"
---
# <a name="symmetricsecuritybindingelement"></a>SymmetricSecurityBindingElement

SymmetricSecurityBindingElement  
  
## <a name="syntax"></a>语法  
  
```csharp
class SymmetricSecurityBindingElement : SecurityBindingElement  
{  
  string MessageProtectionOrder;  
  boolean RequireSignatureConfirmation;  
};  
```  
  
## <a name="methods"></a>方法  

 SymmetricSecurityBindingElement 类不定义任何方法。  
  
## <a name="properties"></a>属性  

 SymmetricSecurityBindingElement 类具有下列属性：  
  
### <a name="messageprotectionorder"></a>MessageProtectionOrder  

 数据类型：字符串  
  
 访问类型：只读  
  
 此绑定的消息加密和签名的顺序。  
  
### <a name="requiresignatureconfirmation"></a>RequireSignatureConfirmation  

 数据类型：Boolean  
  
 访问类型：只读  
  
 此绑定是否需要签名确认。  
  
## <a name="requirements"></a>要求  
  
|MOF|已在 Servicemodel.mof 中声明。|  
|---------|-----------------------------------|  
|命名空间|已在 root\ServiceModel 中定义|  
  
## <a name="see-also"></a>请参阅

- <xref:System.ServiceModel.Channels.SymmetricSecurityBindingElement>
