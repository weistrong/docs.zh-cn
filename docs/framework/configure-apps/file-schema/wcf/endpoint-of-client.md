---
description: 了解详细 <endpoint> 信息： <client>
title: <endpoint> 的 <client>
ms.date: 03/30/2017
ms.assetid: de6238ae-bbf8-48e9-a1b5-e24c0bea8afa
ms.openlocfilehash: 4ace6d49ba18524729925b20cf08e5d57bcc40c5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99725775"
---
# <a name="endpoint-of-client"></a><span data-ttu-id="89b27-103">\<endpoint> 的 \<client></span><span class="sxs-lookup"><span data-stu-id="89b27-103">\<endpoint> of \<client></span></span>

<span data-ttu-id="89b27-104">指定通道终结点的协定、绑定和地址属性，客户端使用通道终结点与服务器上的服务终结点连接。</span><span class="sxs-lookup"><span data-stu-id="89b27-104">Specifies contract, binding, and address properties of the channel endpoint, which is used by clients to connect to service endpoints on the server.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<client>**](client.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<endpoint>**  
  
## <a name="syntax"></a><span data-ttu-id="89b27-105">语法</span><span class="sxs-lookup"><span data-stu-id="89b27-105">Syntax</span></span>  
  
```xml  
<endpoint address="String"
          behaviorConfiguration="String"
          binding="String"
          bindingConfiguration="String"
          contract="String"
          endpointConfiguration="String"
          kind="String"
          name="String">
</endpoint>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="89b27-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="89b27-106">Attributes and Elements</span></span>  

 <span data-ttu-id="89b27-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="89b27-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="89b27-108">特性</span><span class="sxs-lookup"><span data-stu-id="89b27-108">Attributes</span></span>  
  
|<span data-ttu-id="89b27-109">属性</span><span class="sxs-lookup"><span data-stu-id="89b27-109">Attribute</span></span>|<span data-ttu-id="89b27-110">说明</span><span class="sxs-lookup"><span data-stu-id="89b27-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="89b27-111">address</span><span class="sxs-lookup"><span data-stu-id="89b27-111">address</span></span>|<span data-ttu-id="89b27-112">必需的字符串属性。</span><span class="sxs-lookup"><span data-stu-id="89b27-112">Required string attribute.</span></span><br /><br /> <span data-ttu-id="89b27-113">指定终结点的地址。</span><span class="sxs-lookup"><span data-stu-id="89b27-113">Specifies the address of the endpoint.</span></span> <span data-ttu-id="89b27-114">默认值为一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="89b27-114">The default is an empty string.</span></span> <span data-ttu-id="89b27-115">该地址必须为绝对 URI。</span><span class="sxs-lookup"><span data-stu-id="89b27-115">The address must be an absolute URI.</span></span>|  
|<span data-ttu-id="89b27-116">behaviorConfiguration</span><span class="sxs-lookup"><span data-stu-id="89b27-116">behaviorConfiguration</span></span>|<span data-ttu-id="89b27-117">一个字符串，其中包含要用于实例化终结点的行为的行为名。</span><span class="sxs-lookup"><span data-stu-id="89b27-117">A string that contains the behavior name of the behavior to be used to instantiate the endpoint.</span></span> <span data-ttu-id="89b27-118">定义服务时，该行为名必须在作用域内。</span><span class="sxs-lookup"><span data-stu-id="89b27-118">The behavior name must be in scope at the point the service is defined.</span></span> <span data-ttu-id="89b27-119">默认值为一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="89b27-119">The default is an empty string.</span></span>|  
|<span data-ttu-id="89b27-120">binding</span><span class="sxs-lookup"><span data-stu-id="89b27-120">binding</span></span>|<span data-ttu-id="89b27-121">必需的字符串属性。</span><span class="sxs-lookup"><span data-stu-id="89b27-121">Required string attribute.</span></span><br /><br /> <span data-ttu-id="89b27-122">一个字符串，指示要使用的绑定的类型。</span><span class="sxs-lookup"><span data-stu-id="89b27-122">A string that indicates the type of binding to use.</span></span> <span data-ttu-id="89b27-123">该类型必须具有一个已注册的配置节，才能加以引用。</span><span class="sxs-lookup"><span data-stu-id="89b27-123">The type must have a registered configuration section in order to be referenced.</span></span> <span data-ttu-id="89b27-124">该类型是按节名而不是绑定的类型名注册的。</span><span class="sxs-lookup"><span data-stu-id="89b27-124">The type is registered by section name, instead of by the type name of the binding.</span></span>|  
|<span data-ttu-id="89b27-125">bindingConfiguration</span><span class="sxs-lookup"><span data-stu-id="89b27-125">bindingConfiguration</span></span>|<span data-ttu-id="89b27-126">可选。</span><span class="sxs-lookup"><span data-stu-id="89b27-126">Optional.</span></span> <span data-ttu-id="89b27-127">一个字符串，其中包含实例化终结点时要使用的绑定配置的名称。</span><span class="sxs-lookup"><span data-stu-id="89b27-127">A string that contains the name of the binding configuration to be used when the endpoint is instantiated.</span></span> <span data-ttu-id="89b27-128">定义终结点时，绑定配置必须在作用域内。</span><span class="sxs-lookup"><span data-stu-id="89b27-128">The binding configuration must be in scope at the point the endpoint is defined.</span></span> <span data-ttu-id="89b27-129">默认值为一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="89b27-129">The default is an empty string.</span></span><br /><br /> <span data-ttu-id="89b27-130">此属性与 `binding` 结合使用，以引用配置文件中的特定绑定配置。</span><span class="sxs-lookup"><span data-stu-id="89b27-130">This attribute is used in conjunction with `binding` to reference a specific binding configuration in the configuration file.</span></span> <span data-ttu-id="89b27-131">如果尝试使用自定义绑定，请设置此属性。</span><span class="sxs-lookup"><span data-stu-id="89b27-131">Set this attribute if you are attempting to use a custom binding.</span></span> <span data-ttu-id="89b27-132">否则，可能引发异常。</span><span class="sxs-lookup"><span data-stu-id="89b27-132">Otherwise, an exception may be thrown.</span></span>|  
|<span data-ttu-id="89b27-133">contract</span><span class="sxs-lookup"><span data-stu-id="89b27-133">contract</span></span>|<span data-ttu-id="89b27-134">必需的字符串属性。</span><span class="sxs-lookup"><span data-stu-id="89b27-134">Required string attribute.</span></span><br /><br /> <span data-ttu-id="89b27-135">一个字符串，指示此终结点公开了哪个协定。</span><span class="sxs-lookup"><span data-stu-id="89b27-135">A string that indicates which contract this endpoint is exposing.</span></span> <span data-ttu-id="89b27-136">程序集必须实现该协定类型。</span><span class="sxs-lookup"><span data-stu-id="89b27-136">The assembly must implement the contract type.</span></span>|  
|<span data-ttu-id="89b27-137">endpointConfiguration</span><span class="sxs-lookup"><span data-stu-id="89b27-137">endpointConfiguration</span></span>|<span data-ttu-id="89b27-138">一个字符串，指定由 `kind` 特性设置的标准终结点的名称，此名称引用此标准终结点的其他配置信息。</span><span class="sxs-lookup"><span data-stu-id="89b27-138">A string that specifies the name of the standard endpoint that is set by the `kind` attribute, which references to the additional configuration information of this standard endpoint.</span></span> <span data-ttu-id="89b27-139">必须在 `<standardEndpoints>` 节中定义相同的名称。</span><span class="sxs-lookup"><span data-stu-id="89b27-139">The same name must be defined in the `<standardEndpoints>` section.</span></span>|  
|<span data-ttu-id="89b27-140">kind</span><span class="sxs-lookup"><span data-stu-id="89b27-140">kind</span></span>|<span data-ttu-id="89b27-141">一个字符串，指定应用的标准终结点的类型。</span><span class="sxs-lookup"><span data-stu-id="89b27-141">A string that specifies the type of standard endpoint applied.</span></span> <span data-ttu-id="89b27-142">该类型必须在 `<extensions>` 节或 machine.config 中注册。如果未指定任何内容，则会创建一个通用的通道终结点。</span><span class="sxs-lookup"><span data-stu-id="89b27-142">The type must be registered in the `<extensions>` section or in machine.config. If nothing is specified, a common channel endpoint is created.</span></span>|  
|<span data-ttu-id="89b27-143">name</span><span class="sxs-lookup"><span data-stu-id="89b27-143">name</span></span>|<span data-ttu-id="89b27-144">可选的字符串属性。</span><span class="sxs-lookup"><span data-stu-id="89b27-144">Optional string attribute.</span></span> <span data-ttu-id="89b27-145">此属性唯一标识给定协定的终结点。</span><span class="sxs-lookup"><span data-stu-id="89b27-145">This attribute uniquely identifies an endpoint for a given contract.</span></span> <span data-ttu-id="89b27-146">可以为一个给定协定类型定义多个客户端。</span><span class="sxs-lookup"><span data-stu-id="89b27-146">You can define multiple clients for a given Contract type.</span></span> <span data-ttu-id="89b27-147">每个定义都必须用唯一的配置名称加以区分。</span><span class="sxs-lookup"><span data-stu-id="89b27-147">Each definition must be differentiated by a unique configuration name.</span></span> <span data-ttu-id="89b27-148">如果省略此属性，则将对应的终结点用作与指定协定类型相关联的默认终结点。</span><span class="sxs-lookup"><span data-stu-id="89b27-148">If this attribute is omitted, the corresponding endpoint is used as the default endpoint associated with the specified Contract type.</span></span> <span data-ttu-id="89b27-149">默认值为一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="89b27-149">The default is an empty string.</span></span><br /><br /> <span data-ttu-id="89b27-150">绑定的 `name` 属性用于通过 WSDL 进行的定义导出。</span><span class="sxs-lookup"><span data-stu-id="89b27-150">The `name` attribute of a binding is used for definition export through WSDL.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="89b27-151">子元素</span><span class="sxs-lookup"><span data-stu-id="89b27-151">Child Elements</span></span>  
  
|<span data-ttu-id="89b27-152">元素</span><span class="sxs-lookup"><span data-stu-id="89b27-152">Element</span></span>|<span data-ttu-id="89b27-153">说明</span><span class="sxs-lookup"><span data-stu-id="89b27-153">Description</span></span>|  
|-------------|-----------------|  
|[\<headers>](headers.md)|<span data-ttu-id="89b27-154">一个地址标头集合。</span><span class="sxs-lookup"><span data-stu-id="89b27-154">A collection of address headers.</span></span>|  
|[\<identity>](identity.md)|<span data-ttu-id="89b27-155">一个标识，与某个终结点交换消息的其他终结点可以使用该标识对该终结点进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="89b27-155">An identity that enables the authentication of an endpoint by other endpoints exchanging messages with it.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="89b27-156">父元素</span><span class="sxs-lookup"><span data-stu-id="89b27-156">Parent Elements</span></span>  
  
|<span data-ttu-id="89b27-157">元素</span><span class="sxs-lookup"><span data-stu-id="89b27-157">Element</span></span>|<span data-ttu-id="89b27-158">说明</span><span class="sxs-lookup"><span data-stu-id="89b27-158">Description</span></span>|  
|-------------|-----------------|  
|[\<client>](client.md)|<span data-ttu-id="89b27-159">一个配置节，定义客户端可以连接的终结点的列表。</span><span class="sxs-lookup"><span data-stu-id="89b27-159">A configuration section that defines a list of endpoints that a client can connect to.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="89b27-160">示例</span><span class="sxs-lookup"><span data-stu-id="89b27-160">Example</span></span>  

 <span data-ttu-id="89b27-161">这是通道终结点配置的一个示例。</span><span class="sxs-lookup"><span data-stu-id="89b27-161">This is an example of a channel endpoint configuration.</span></span>  
  
```xml  
<endpoint address="/HelloWorld/"
          bindingConfiguration="usingDefaults"
          name="MyBinding"
          binding="customBinding"
          contract="HelloWorld">
</endpoint>
```  
  
## <a name="see-also"></a><span data-ttu-id="89b27-162">请参阅</span><span class="sxs-lookup"><span data-stu-id="89b27-162">See also</span></span>

- <xref:System.ServiceModel.Configuration.ChannelEndpointElement>
- <xref:System.ServiceModel.Configuration.ClientSection>
- <xref:System.ServiceModel.Configuration.ChannelEndpointElementCollection>
- <xref:System.ServiceModel.Configuration.ClientSection.Endpoints%2A>
- <xref:System.ServiceModel.Configuration.ChannelEndpointElement>
- [<span data-ttu-id="89b27-163">WCF 客户端配置</span><span class="sxs-lookup"><span data-stu-id="89b27-163">WCF Client Configuration</span></span>](../../../wcf/feature-details/client-configuration.md)
- [<span data-ttu-id="89b27-164">客户端</span><span class="sxs-lookup"><span data-stu-id="89b27-164">Clients</span></span>](../../../wcf/feature-details/clients.md)
