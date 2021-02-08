---
description: 了解详细 <security> 信息： <netMsmqBinding>
title: <security> 的 <netMsmqBinding>
ms.date: 03/30/2017
ms.assetid: 001d11a9-7439-498c-b09d-fca20eaf8cd3
ms.openlocfilehash: 1b60d9e390e371555f4c3abf4988e79bb0f04fe8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786845"
---
# <a name="security-of-netmsmqbinding"></a>\<security> 的 \<netMsmqBinding>

定义 MSMQ 绑定的安全设置。 它指定是否启用传输或 SOAP 安全；如果启用，还指定所使用的身份验证模式和保护级别。  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<netMsmqBinding>**](netmsmqbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<security>**  
  
## <a name="syntax"></a>语法  
  
```xml  
<security mode="None/Transport/Message/Both">
  <transport msmqAuthenticationMode="None/WindowsDomain/Certificate"
             msmqEncryptionAlgorithm="RC4Stream/AES"
             msmqProtectionLevel="None/Sign/EncryptAndSign"
             msmqSecureHashAlgorithm="MD5/SHA1/SHA256/SHA512" />
    <message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
             clientCredentialType="None/Windows/UserName/Certificate/CardSpace" />
</security>
```  
  
## <a name="attributes-and-elements"></a>特性和元素  

 下列各节描述了特性、子元素和父元素。  
  
### <a name="attributes"></a>特性  
  
|属性|说明|  
|---------------|-----------------|  
|mode|指定用于控制完整性、保密性和身份验证的安全类型。 有效值包括以下值：<br /><br /> -None：这将禁用安全性。<br />-Transport：传输提供保护和身份验证。 这适用于两个队列管理器之间的消息安全性。 未在应用程序和队列管理器之间提供安全性。 现有的 Msmq 应用程序与此类型的安全模式功能等效。<br />-Message：指定端应用程序安全性。 未在传输层提供安全性。 这类似于其他标准绑定提供的安全性。<br />-Both：同时在传输和 SOAP 消息传送层上提供安全性。 在这两个层上需要相同的凭据。<br /><br /> 默认值为 Transport。 此属性的类型为 <xref:System.ServiceModel.NetMsmqSecurityMode>。|  
  
### <a name="child-elements"></a>子元素  
  
|元素|说明|  
|-------------|-----------------|  
|[\<message>](message-of-netmsmqbinding.md)|定义 SOAP 消息安全设置。 此元素的类型为 <xref:System.ServiceModel.Configuration.MessageSecurityOverMsmqElement>。|  
|[\<transport>](transport-of-netmsmqbinding.md)|定义 MSMQ 传输的安全设置。 此元素的类型为 <xref:System.ServiceModel.Configuration.MsmqTransportSecurityElement>。|  
  
### <a name="parent-elements"></a>父元素  
  
|元素|说明|  
|-------------|-----------------|  
|binding|的绑定元素 [\<netMsmqBinding>](netmsmqbinding.md)|  
  
## <a name="see-also"></a>请参阅

- <xref:System.ServiceModel.Configuration.NetMsmqSecurityElement>
- <xref:System.ServiceModel.NetMsmqBinding.Security%2A>
- <xref:System.ServiceModel.Configuration.NetMsmqBindingElement.Security%2A>
- <xref:System.ServiceModel.NetMsmqSecurity>
- [保护服务和客户端的安全](../../../wcf/feature-details/securing-services-and-clients.md)
- [绑定](../../../wcf/bindings.md)
- [配置系统提供的绑定](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [使用绑定配置服务和客户端](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)
- [WCF 中的队列](../../../wcf/feature-details/queues-in-wcf.md)
