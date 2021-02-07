---
description: 了解详细 <security> 信息： <netNamedPipeBinding>
title: <security> 的 <netNamedPipeBinding>
ms.date: 03/30/2017
ms.assetid: bb3cb022-637e-49fd-92e8-6766038affa7
ms.openlocfilehash: d64917c53390cade00d9e104c8581ce45355ac34
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99683094"
---
# <a name="security-of-netnamedpipebinding"></a><span data-ttu-id="f5f80-103">\<security> 的 \<netNamedPipeBinding></span><span class="sxs-lookup"><span data-stu-id="f5f80-103">\<security> of \<netNamedPipeBinding></span></span>

<span data-ttu-id="f5f80-104">定义绑定的安全设置。</span><span class="sxs-lookup"><span data-stu-id="f5f80-104">Defines the security settings for a binding.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<netNamedPipeBinding>**](netnamedpipebinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<security>**  
  
## <a name="syntax"></a><span data-ttu-id="f5f80-105">语法</span><span class="sxs-lookup"><span data-stu-id="f5f80-105">Syntax</span></span>  
  
```xml  
<netNamedPipeBinding>
  <binding>
    <security mode="None/Transport">
      <transport protectionLevel="None/Sign/EncryptAndSign" />
    </security>
  </binding>
</netNamedPipeBinding>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="f5f80-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="f5f80-106">Attributes and Elements</span></span>  

 <span data-ttu-id="f5f80-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f5f80-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="f5f80-108">特性</span><span class="sxs-lookup"><span data-stu-id="f5f80-108">Attributes</span></span>  
  
|<span data-ttu-id="f5f80-109">属性</span><span class="sxs-lookup"><span data-stu-id="f5f80-109">Attribute</span></span>|<span data-ttu-id="f5f80-110">说明</span><span class="sxs-lookup"><span data-stu-id="f5f80-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="f5f80-111">mode</span><span class="sxs-lookup"><span data-stu-id="f5f80-111">mode</span></span>|<span data-ttu-id="f5f80-112">指定应用于此绑定的安全类型。</span><span class="sxs-lookup"><span data-stu-id="f5f80-112">Specifies the type of security that is applied to this binding.</span></span> <span data-ttu-id="f5f80-113">有效值包括以下值：</span><span class="sxs-lookup"><span data-stu-id="f5f80-113">Valid values include the following:</span></span><br /><br /> <span data-ttu-id="f5f80-114">-None：这将禁用安全性。</span><span class="sxs-lookup"><span data-stu-id="f5f80-114">-   None: This disables security.</span></span><br /><span data-ttu-id="f5f80-115">-Transport：使用基于传输的基础安全性提供安全性。</span><span class="sxs-lookup"><span data-stu-id="f5f80-115">-   Transport: Security is provided using underlying transport based security.</span></span> <span data-ttu-id="f5f80-116">可以使用此模式控制保护级别。</span><span class="sxs-lookup"><span data-stu-id="f5f80-116">It is possible to control the protection level with this mode.</span></span><br /><span data-ttu-id="f5f80-117">-默认值为 Transport。</span><span class="sxs-lookup"><span data-stu-id="f5f80-117">-   The default value is Transport.</span></span> <span data-ttu-id="f5f80-118">此属性的类型为 <xref:System.ServiceModel.NetNamedPipeSecurityMode>。</span><span class="sxs-lookup"><span data-stu-id="f5f80-118">This attribute is of type <xref:System.ServiceModel.NetNamedPipeSecurityMode>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="f5f80-119">子元素</span><span class="sxs-lookup"><span data-stu-id="f5f80-119">Child Elements</span></span>  
  
|<span data-ttu-id="f5f80-120">元素</span><span class="sxs-lookup"><span data-stu-id="f5f80-120">Element</span></span>|<span data-ttu-id="f5f80-121">说明</span><span class="sxs-lookup"><span data-stu-id="f5f80-121">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f5f80-122">运输</span><span class="sxs-lookup"><span data-stu-id="f5f80-122">transport</span></span>|<span data-ttu-id="f5f80-123">定义传输的安全设置。</span><span class="sxs-lookup"><span data-stu-id="f5f80-123">Defines the security settings for the transport.</span></span> <span data-ttu-id="f5f80-124">此元素的类型为 <xref:System.ServiceModel.Configuration.NamedPipeTransportSecurityElement>。</span><span class="sxs-lookup"><span data-stu-id="f5f80-124">This element is of type <xref:System.ServiceModel.Configuration.NamedPipeTransportSecurityElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="f5f80-125">父元素</span><span class="sxs-lookup"><span data-stu-id="f5f80-125">Parent Elements</span></span>  
  
|<span data-ttu-id="f5f80-126">元素</span><span class="sxs-lookup"><span data-stu-id="f5f80-126">Element</span></span>|<span data-ttu-id="f5f80-127">说明</span><span class="sxs-lookup"><span data-stu-id="f5f80-127">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f5f80-128">binding</span><span class="sxs-lookup"><span data-stu-id="f5f80-128">binding</span></span>|<span data-ttu-id="f5f80-129">的绑定元素 [\<netNamedPipeBinding>](netnamedpipebinding.md) 。</span><span class="sxs-lookup"><span data-stu-id="f5f80-129">The binding element of the [\<netNamedPipeBinding>](netnamedpipebinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="f5f80-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="f5f80-130">See also</span></span>

- <xref:System.ServiceModel.NetNamedPipeSecurity>
- <xref:System.ServiceModel.NetNamedPipeBinding.Security%2A>
- <xref:System.ServiceModel.Configuration.NetNamedPipeBindingElement.Security%2A>
- <xref:System.ServiceModel.Configuration.NetNamedPipeSecurityElement>
- [<span data-ttu-id="f5f80-131">保护服务和客户端的安全</span><span class="sxs-lookup"><span data-stu-id="f5f80-131">Securing Services and Clients</span></span>](../../../wcf/feature-details/securing-services-and-clients.md)
- [<span data-ttu-id="f5f80-132">选择凭据类型</span><span class="sxs-lookup"><span data-stu-id="f5f80-132">Selecting a Credential Type</span></span>](../../../wcf/feature-details/selecting-a-credential-type.md)
- [<span data-ttu-id="f5f80-133">绑定</span><span class="sxs-lookup"><span data-stu-id="f5f80-133">Bindings</span></span>](../../../wcf/bindings.md)
- [<span data-ttu-id="f5f80-134">配置系统提供的绑定</span><span class="sxs-lookup"><span data-stu-id="f5f80-134">Configuring System-Provided Bindings</span></span>](../../../wcf/feature-details/configuring-system-provided-bindings.md)
- [<span data-ttu-id="f5f80-135">使用绑定配置服务和客户端</span><span class="sxs-lookup"><span data-stu-id="f5f80-135">Using Bindings to Configure Services and Clients</span></span>](../../../wcf/using-bindings-to-configure-services-and-clients.md)
- [\<binding>](bindings.md)
