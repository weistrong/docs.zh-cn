---
description: 了解详细信息： <servicePrincipalName>
title: <servicePrincipalName>
ms.date: 03/30/2017
ms.assetid: 3f3b85d3-20f2-4cd8-8a6a-ee18befbd165
ms.openlocfilehash: 494368f1f47f10aac8009e47a9219966c87e5eda
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786689"
---
# \<servicePrincipalName>

利用对应的服务主体名称 (SPN) 指定服务的标识。  
  
有关设置 SPN 的详细信息，请参阅 [服务标识和身份验证](../../../wcf/feature-details/service-identity-and-authentication.md)。  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<client>**](client.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<endpoint>**](endpoint-of-client.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<identity>**](identity.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<servicePrincipalName>**  
  
## <a name="syntax"></a>语法  
  
```xml  
<servicePrincipalName value="String" />
```  
  
## <a name="attributes-and-elements"></a>特性和元素  

 以下几节描述了特性、子元素和父元素。  
  
### <a name="attributes"></a>特性  
  
|属性|说明|  
|---------------|-----------------|  
|value|客户端用于唯一标识服务实例的名称。 如果在计算机的整个目录林上安装多个服务实例，那么每个实例都必须有自己的 SPN。 如果客户端有多个名称可用于身份验证，则给定的服务实例可以有多个 SPN。|  
  
### <a name="child-elements"></a>子元素  

 无。  
  
### <a name="parent-elements"></a>父元素  
  
|元素|说明|  
|-------------|-----------------|  
|[\<identity>](identity.md)|指定要由客户端进行身份验证的服务的标识。|  
  
## <a name="remarks"></a>备注  

 使用此标识连接到终结点的安全 Windows Communication Foundation (WCF) 客户端在使用终结点进行 SSPI 身份验证时使用 SPN。  
  
## <a name="see-also"></a>请参阅

- <xref:System.ServiceModel.Configuration.IdentityElement>
- <xref:System.ServiceModel.EndpointAddress>
- <xref:System.ServiceModel.EndpointAddress.Identity%2A>
- <xref:System.ServiceModel.SpnEndpointIdentity>
- [服务标识和身份验证](../../../wcf/feature-details/service-identity-and-authentication.md)
- [\<identity>](identity.md)
