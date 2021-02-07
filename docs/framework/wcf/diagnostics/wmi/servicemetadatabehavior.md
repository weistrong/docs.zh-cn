---
description: 了解详细信息： ServiceMetadataBehavior
title: ServiceMetadataBehavior
ms.date: 03/30/2017
ms.assetid: 0f194476-72f1-467e-bdce-674306316e64
ms.openlocfilehash: 1b1438013ec667b10b300d898687abf6f33f96fb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99715478"
---
# <a name="servicemetadatabehavior"></a>ServiceMetadataBehavior

ServiceMetadataBehavior  
  
## <a name="syntax"></a>语法  
  
```csharp
class ServiceMetadataBehavior : Behavior  
{  
  string ExternalMetadataLocation;  
  boolean HttpGetEnabled;  
  string HttpGetUrl;  
  boolean HttpsGetEnabled;  
  string HttpsGetUrl;  
};  
```  
  
## <a name="methods"></a>方法  

 ServiceMetadataBehavior 类未定义任何方法。  
  
## <a name="properties"></a>属性  

 ServiceMetadataBehavior 类具有以下属性：  
  
### <a name="externalmetadatalocation"></a>ExternalMetadataLocation  

 数据类型：字符串  
  
 访问类型：只读  
  
 设置服务重定向元数据请求的位置。  
  
### <a name="httpgetenabled"></a>HttpGetEnabled  

 数据类型：Boolean  
  
 访问类型：只读  
  
 控制服务是否在 `HttpGetUrl` 属性控制的地址上发布其 WSDL。  
  
### <a name="httpgeturl"></a>HttpGetUrl  

 数据类型：字符串  
  
 访问类型：只读  
  
 设置位置，在该位置发布服务 WSDL 以便使用 HTTP 进行检索。  
  
### <a name="httpsgetenabled"></a>HttpsGetEnabled  

 数据类型：Boolean  
  
 访问类型：只读  
  
 控制服务是否在 `HttpsGetUrl` 属性控制的地址上通过 HTTPS 发布其 WSDL。  
  
### <a name="httpsgeturl"></a>HttpsGetUrl  

 数据类型：字符串  
  
 访问类型：只读  
  
 设置位置，在该位置发布服务 WSDL 以便使用 HTTPS 进行检索。  
  
## <a name="requirements"></a>要求  
  
|MOF|已在 Servicemodel.mof 中声明。|  
|---------|-----------------------------------|  
|命名空间|已在 root\ServiceModel 中定义|  
  
## <a name="see-also"></a>请参阅

- <xref:System.ServiceModel.Description.ServiceMetadataBehavior>
