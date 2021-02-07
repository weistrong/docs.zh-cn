---
description: 了解详细 <security> 信息： <wsDualHttpBinding>
title: <security> 的 <wsDualHttpBinding>
ms.date: 03/30/2017
ms.assetid: 869c05e7-4ebe-467d-95ab-c8f8de4e6b9e
ms.openlocfilehash: 6d2e87912aef6114d7dcb99b82e4a7804317b28a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683029"
---
# <a name="security-of-wsdualhttpbinding"></a><span data-ttu-id="2c71a-103">\<security> 的 \<wsDualHttpBinding></span><span class="sxs-lookup"><span data-stu-id="2c71a-103">\<security> of \<wsDualHttpBinding></span></span>

<span data-ttu-id="2c71a-104">定义的安全功能 [\<wsDualHttpBinding>](wsdualhttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="2c71a-104">Defines the security capabilities of the [\<wsDualHttpBinding>](wsdualhttpbinding.md).</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<wsDualHttpBinding>**](wsdualhttpbinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<security>**  
  
## <a name="syntax"></a><span data-ttu-id="2c71a-105">语法</span><span class="sxs-lookup"><span data-stu-id="2c71a-105">Syntax</span></span>  
  
```xml  
<security mode="Message/None">
  <message algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"
           clientCredentialType="Certificate/IssuedToken/None/UserName/Windows"
           negotiateServiceCredential="Boolean"/>
</security>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2c71a-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="2c71a-106">Attributes and Elements</span></span>  

 <span data-ttu-id="2c71a-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2c71a-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2c71a-108">特性</span><span class="sxs-lookup"><span data-stu-id="2c71a-108">Attributes</span></span>  
  
|<span data-ttu-id="2c71a-109">属性</span><span class="sxs-lookup"><span data-stu-id="2c71a-109">Attribute</span></span>|<span data-ttu-id="2c71a-110">说明</span><span class="sxs-lookup"><span data-stu-id="2c71a-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="2c71a-111">mode</span><span class="sxs-lookup"><span data-stu-id="2c71a-111">mode</span></span>|<span data-ttu-id="2c71a-112">可有可无.</span><span class="sxs-lookup"><span data-stu-id="2c71a-112">-   Optional.</span></span> <span data-ttu-id="2c71a-113">指定所应用的安全类型。</span><span class="sxs-lookup"><span data-stu-id="2c71a-113">Specifies the type of security that is applied.</span></span> <span data-ttu-id="2c71a-114">默认值是 `Message`。</span><span class="sxs-lookup"><span data-stu-id="2c71a-114">The default value is `Message`.</span></span> <span data-ttu-id="2c71a-115">此属性的类型为 <xref:System.ServiceModel.WSDualHttpSecurityMode>。</span><span class="sxs-lookup"><span data-stu-id="2c71a-115">This attribute is of type <xref:System.ServiceModel.WSDualHttpSecurityMode>.</span></span>|  
  
## <a name="mode-attribute"></a><span data-ttu-id="2c71a-116">Mode 属性</span><span class="sxs-lookup"><span data-stu-id="2c71a-116">Mode Attribute</span></span>  
  
|<span data-ttu-id="2c71a-117">值</span><span class="sxs-lookup"><span data-stu-id="2c71a-117">Value</span></span>|<span data-ttu-id="2c71a-118">说明</span><span class="sxs-lookup"><span data-stu-id="2c71a-118">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="2c71a-119">无</span><span class="sxs-lookup"><span data-stu-id="2c71a-119">None</span></span>|<span data-ttu-id="2c71a-120">禁用安全性。</span><span class="sxs-lookup"><span data-stu-id="2c71a-120">Security is disabled.</span></span>|  
|<span data-ttu-id="2c71a-121">消息</span><span class="sxs-lookup"><span data-stu-id="2c71a-121">Message</span></span>|<span data-ttu-id="2c71a-122">使用 SOAP 消息安全提供安全性。</span><span class="sxs-lookup"><span data-stu-id="2c71a-122">Security is provided using SOAP message security.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="2c71a-123">子元素</span><span class="sxs-lookup"><span data-stu-id="2c71a-123">Child Elements</span></span>  
  
|<span data-ttu-id="2c71a-124">元素</span><span class="sxs-lookup"><span data-stu-id="2c71a-124">Element</span></span>|<span data-ttu-id="2c71a-125">说明</span><span class="sxs-lookup"><span data-stu-id="2c71a-125">Description</span></span>|  
|-------------|-----------------|  
|[\<message>](message-of-wsdualhttpbinding.md)|<span data-ttu-id="2c71a-126">定义消息级安全性设置。</span><span class="sxs-lookup"><span data-stu-id="2c71a-126">Defines the settings for the message-level security.</span></span> <span data-ttu-id="2c71a-127">此元素的类型为 <xref:System.ServiceModel.MessageSecurityOverHttp>。</span><span class="sxs-lookup"><span data-stu-id="2c71a-127">This element is of type <xref:System.ServiceModel.MessageSecurityOverHttp>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="2c71a-128">父元素</span><span class="sxs-lookup"><span data-stu-id="2c71a-128">Parent Elements</span></span>  
  
|<span data-ttu-id="2c71a-129">元素</span><span class="sxs-lookup"><span data-stu-id="2c71a-129">Element</span></span>|<span data-ttu-id="2c71a-130">说明</span><span class="sxs-lookup"><span data-stu-id="2c71a-130">Description</span></span>|  
|-------------|-----------------|  
|[\<binding>](bindings.md)|<span data-ttu-id="2c71a-131">定义的所有绑定功能 [\<wsDualHttpBinding>](wsdualhttpbinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="2c71a-131">Defines all binding capabilities of the [\<wsDualHttpBinding>](wsdualhttpbinding.md).</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="2c71a-132">备注</span><span class="sxs-lookup"><span data-stu-id="2c71a-132">Remarks</span></span>  

 <span data-ttu-id="2c71a-133">双向绑定向服务公开客户端的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="2c71a-133">A dual binding exposes the IP address of the client to the service.</span></span> <span data-ttu-id="2c71a-134">客户端应使用安全来确保仅连接到自己信任的服务。</span><span class="sxs-lookup"><span data-stu-id="2c71a-134">The client should use security to ensure that it only connects to services it trusts.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2c71a-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="2c71a-135">See also</span></span>

- <xref:System.ServiceModel.WSDualHttpSecurity>
- <xref:System.ServiceModel.BasicHttpSecurity>
- [<span data-ttu-id="2c71a-136">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="2c71a-136">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="2c71a-137">绑定</span><span class="sxs-lookup"><span data-stu-id="2c71a-137">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="2c71a-138">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="2c71a-138">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="2c71a-139">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="2c71a-139">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)
