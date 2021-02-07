---
description: 了解详细信息： ServiceToEndpointAssociation
title: ServiceToEndpointAssociation
ms.date: 03/30/2017
ms.assetid: 03c3cd15-e1b2-4dc2-bdc2-59fdccdae110
ms.openlocfilehash: 1ae2ce2bcc0b3494b00fffa750f3ca46d26fe08f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99715335"
---
# <a name="servicetoendpointassociation"></a>ServiceToEndpointAssociation

将服务映射到终结点。  
  
## <a name="syntax"></a>语法  
  
```csharp
class ServiceToEndpointAssociation  
{  
  Service ref;  
  Endpoint ref;  
};  
```  
  
## <a name="methods"></a>方法  

 ServiceToEndpointAssociation 类不定义任何方法。  
  
## <a name="properties"></a>属性  

 ServiceToEndpointAssociation 类有以下属性：  
  
### <a name="ref"></a>ref  

 数据类型：Service  
  
 访问类型：只读  
限定符：键  
  
 与终结点关联的服务。  
  
### <a name="ref"></a>ref  

 数据类型：Endpoint  
  
 访问类型：只读  
限定符：键  
  
 与服务关联的终结点。  
  
## <a name="requirements"></a>要求  
  
|MOF|已在 Servicemodel.mof 中声明。|  
|---------|-----------------------------------|  
|命名空间|已在 root\ServiceModel 中定义|
