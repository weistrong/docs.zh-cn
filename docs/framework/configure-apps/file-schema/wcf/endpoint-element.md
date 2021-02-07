---
description: 了解详细信息： <endpoint> 元素
title: <endpoint> 元素
ms.date: 03/30/2017
ms.assetid: 2fc8fedc-78d0-4e87-8142-fbfd26c15a4e
ms.openlocfilehash: d5555ae895e6655d1ce6e3dcb026ddec3ff8cf44
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99725800"
---
# <a name="endpoint-element"></a><span data-ttu-id="9a316-103">\<endpoint> 元素</span><span class="sxs-lookup"><span data-stu-id="9a316-103">\<endpoint> element</span></span>

<span data-ttu-id="9a316-104">指定用于公开服务的服务终结点的绑定、协定和地址属性。</span><span class="sxs-lookup"><span data-stu-id="9a316-104">Specifies binding, contract, and address properties for a service endpoint, which is used to expose services.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<services>**](services.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<service>**](service.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<endpoint>**  
  
## <a name="syntax"></a><span data-ttu-id="9a316-105">语法</span><span class="sxs-lookup"><span data-stu-id="9a316-105">Syntax</span></span>  
  
```xml  
<endpoint address="String"
          behaviorConfiguration="String"
          binding="String"
          bindingConfiguration="String"
          bindingName="String"
          bindingNamespace="String"
          contract="String"
          endpointConfiguration="String"
          isSystemEndpoint="Boolean"
          kind="String"
          listenUriMode="Explicit/Unique"
          listenUri="Uri">
</endpoint>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="9a316-106">特性和元素</span><span class="sxs-lookup"><span data-stu-id="9a316-106">Attributes and Elements</span></span>  

 <span data-ttu-id="9a316-107">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9a316-107">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="9a316-108">特性</span><span class="sxs-lookup"><span data-stu-id="9a316-108">Attributes</span></span>  
  
|<span data-ttu-id="9a316-109">属性</span><span class="sxs-lookup"><span data-stu-id="9a316-109">Attribute</span></span>|<span data-ttu-id="9a316-110">说明</span><span class="sxs-lookup"><span data-stu-id="9a316-110">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="9a316-111">address</span><span class="sxs-lookup"><span data-stu-id="9a316-111">address</span></span>|<span data-ttu-id="9a316-112">一个包含终结点地址的字符串。</span><span class="sxs-lookup"><span data-stu-id="9a316-112">A string that contains the address of the endpoint.</span></span> <span data-ttu-id="9a316-113">可以将地址指定为绝对地址或相对地址。</span><span class="sxs-lookup"><span data-stu-id="9a316-113">The address can be specified as an absolute or relative address.</span></span> <span data-ttu-id="9a316-114">如果提供的是相对地址，则需要主机提供适合于绑定中所使用的传输方案的基址。</span><span class="sxs-lookup"><span data-stu-id="9a316-114">If a relative address is provided, the host is expected to provide a base address appropriate for the transport scheme used in the binding.</span></span> <span data-ttu-id="9a316-115">如果未配置地址，则假定基址为该终结点的地址。</span><span class="sxs-lookup"><span data-stu-id="9a316-115">If an address is not configured, the base address is assumed to be the address for that endpoint.</span></span><br /><br /> <span data-ttu-id="9a316-116">默认值为一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="9a316-116">The default is an empty string.</span></span>|  
|<span data-ttu-id="9a316-117">behaviorConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a316-117">behaviorConfiguration</span></span>|<span data-ttu-id="9a316-118">一个字符串，其中包含要在终结点中使用的行为的名称。</span><span class="sxs-lookup"><span data-stu-id="9a316-118">A string that contains the name of the behavior to be used in the endpoint.</span></span>|  
|<span data-ttu-id="9a316-119">binding</span><span class="sxs-lookup"><span data-stu-id="9a316-119">binding</span></span>|<span data-ttu-id="9a316-120">必需的字符串属性，此属性指定要使用的绑定类型。</span><span class="sxs-lookup"><span data-stu-id="9a316-120">Required string attribute that specifies the type of binding to use.</span></span> <span data-ttu-id="9a316-121">该类型必须具有一个已注册的配置节，才能加以引用。</span><span class="sxs-lookup"><span data-stu-id="9a316-121">The type must have a registered configuration section in order to be referenced.</span></span> <span data-ttu-id="9a316-122">该类型是按节名而不是绑定的类型名注册的。</span><span class="sxs-lookup"><span data-stu-id="9a316-122">The type is the registered by section name, rather than by the type name of the binding.</span></span>|  
|<span data-ttu-id="9a316-123">bindingConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a316-123">bindingConfiguration</span></span>|<span data-ttu-id="9a316-124">一个字符串，指定实例化终结点时所使用的绑定的绑定名称。</span><span class="sxs-lookup"><span data-stu-id="9a316-124">A string that specifies the binding name of the binding to use when the endpoint is instantiated.</span></span> <span data-ttu-id="9a316-125">定义终结点时，绑定名称必须在作用域内。</span><span class="sxs-lookup"><span data-stu-id="9a316-125">The binding name must be in scope at the point the endpoint is defined.</span></span> <span data-ttu-id="9a316-126">默认值为一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="9a316-126">The default is an empty string.</span></span><br /><br /> <span data-ttu-id="9a316-127">此属性与 `binding` 结合使用，以引用配置文件中的特定绑定配置。</span><span class="sxs-lookup"><span data-stu-id="9a316-127">This attribute is used in conjunction with `binding` to reference a specific binding configuration in the configuration file.</span></span> <span data-ttu-id="9a316-128">如果尝试使用自定义绑定，请设置此属性。</span><span class="sxs-lookup"><span data-stu-id="9a316-128">Set this attribute if you are attempting to use a custom binding.</span></span> <span data-ttu-id="9a316-129">否则，可能引发异常。</span><span class="sxs-lookup"><span data-stu-id="9a316-129">Otherwise, an exception may be thrown.</span></span>|  
|<span data-ttu-id="9a316-130">bindingName</span><span class="sxs-lookup"><span data-stu-id="9a316-130">bindingName</span></span>|<span data-ttu-id="9a316-131">一个字符串，指定绑定的唯一限定名称，用于通过 WSDL 进行的定义导出。</span><span class="sxs-lookup"><span data-stu-id="9a316-131">A string that specifies the unique qualified name of the binding for definition export through WSDL.</span></span> <span data-ttu-id="9a316-132">默认值为一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="9a316-132">The default is an empty string.</span></span>|  
|<span data-ttu-id="9a316-133">bindingNamespace</span><span class="sxs-lookup"><span data-stu-id="9a316-133">bindingNamespace</span></span>|<span data-ttu-id="9a316-134">一个字符串，指定绑定的命名空间的限定名称，用于通过 WSDL 进行的定义导出。</span><span class="sxs-lookup"><span data-stu-id="9a316-134">A string that specifies the qualified name of the namespace of the binding for definition export through WSDL.</span></span> <span data-ttu-id="9a316-135">默认值为一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="9a316-135">The default is an empty string.</span></span>|  
|<span data-ttu-id="9a316-136">contract</span><span class="sxs-lookup"><span data-stu-id="9a316-136">contract</span></span>|<span data-ttu-id="9a316-137">一个字符串，指示此终结点公开了哪个协定。</span><span class="sxs-lookup"><span data-stu-id="9a316-137">A string that indicates which contract this endpoint is exposing.</span></span> <span data-ttu-id="9a316-138">程序集必须实现该协定类型。</span><span class="sxs-lookup"><span data-stu-id="9a316-138">The assembly must implement the contract type.</span></span> <span data-ttu-id="9a316-139">如果服务实现所实现的是单个协定类型，则可以省略此属性。</span><span class="sxs-lookup"><span data-stu-id="9a316-139">If a service implementation implements a single contract type, then this property can be omitted.</span></span> <span data-ttu-id="9a316-140">默认值为一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="9a316-140">The default is an empty string.</span></span>|  
|<span data-ttu-id="9a316-141">endpointConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a316-141">endpointConfiguration</span></span>|<span data-ttu-id="9a316-142">一个字符串，指定由 `kind` 特性设置的标准终结点的名称，此名称引用此标准终结点的其他配置信息。</span><span class="sxs-lookup"><span data-stu-id="9a316-142">A string that specifies the name of the standard endpoint that is set by the `kind` attribute, which references to the additional configuration information of this standard endpoint.</span></span> <span data-ttu-id="9a316-143">必须在 `<standardEndpoints>` 节中定义相同的名称。</span><span class="sxs-lookup"><span data-stu-id="9a316-143">The same name must be defined in the `<standardEndpoints>` section.</span></span>|  
|<span data-ttu-id="9a316-144">isSystemEndpoint</span><span class="sxs-lookup"><span data-stu-id="9a316-144">isSystemEndpoint</span></span>|<span data-ttu-id="9a316-145">一个布尔值，指定终结点是否是基础结构终结点。</span><span class="sxs-lookup"><span data-stu-id="9a316-145">A Boolean value that specifies whether an endpoint is an infrastructure endpoint.</span></span>|  
|<span data-ttu-id="9a316-146">kind</span><span class="sxs-lookup"><span data-stu-id="9a316-146">kind</span></span>|<span data-ttu-id="9a316-147">一个字符串，指定应用的标准终结点的类型。</span><span class="sxs-lookup"><span data-stu-id="9a316-147">A string that specifies the type of standard endpoint applied.</span></span> <span data-ttu-id="9a316-148">该类型必须在 `<extensions>` 节或 machine.config 中注册。如果未指定任何内容，则会创建一个通用的服务终结点。</span><span class="sxs-lookup"><span data-stu-id="9a316-148">The type must be registered in the `<extensions>` section or in machine.config. If nothing is specified, a common service endpoint is created.</span></span>|  
|<span data-ttu-id="9a316-149">listenUriMode</span><span class="sxs-lookup"><span data-stu-id="9a316-149">listenUriMode</span></span>|<span data-ttu-id="9a316-150">指定传输如何处理供服务侦听的 `ListenUri`。</span><span class="sxs-lookup"><span data-stu-id="9a316-150">Specifies how the transport treats the `ListenUri` provided for the service to listen on.</span></span> <span data-ttu-id="9a316-151">有效值为</span><span class="sxs-lookup"><span data-stu-id="9a316-151">Valid values are</span></span><br /><br /> <span data-ttu-id="9a316-152">-Explicit</span><span class="sxs-lookup"><span data-stu-id="9a316-152">-   Explicit</span></span><br /><span data-ttu-id="9a316-153">-唯一</span><span class="sxs-lookup"><span data-stu-id="9a316-153">-   Unique</span></span><br /><br /> <span data-ttu-id="9a316-154">默认值为 Explicit。</span><span class="sxs-lookup"><span data-stu-id="9a316-154">The default value is Explicit.</span></span>|  
|<span data-ttu-id="9a316-155">listenUri</span><span class="sxs-lookup"><span data-stu-id="9a316-155">listenUri</span></span>|<span data-ttu-id="9a316-156">一个字符串，指定服务终结点侦听的 URI。</span><span class="sxs-lookup"><span data-stu-id="9a316-156">A string that specifies the URI at which the service endpoint listens.</span></span> <span data-ttu-id="9a316-157">默认值为一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="9a316-157">The default is an empty string.</span></span>|  
|<span data-ttu-id="9a316-158">name</span><span class="sxs-lookup"><span data-stu-id="9a316-158">name</span></span>|<span data-ttu-id="9a316-159">可选特性。</span><span class="sxs-lookup"><span data-stu-id="9a316-159">Optional attribute.</span></span> <span data-ttu-id="9a316-160">一个指定服务终结点名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="9a316-160">A string that specifies the name the service endpoint.</span></span> <span data-ttu-id="9a316-161">默认值为绑定名称和协定说明名称的串联。</span><span class="sxs-lookup"><span data-stu-id="9a316-161">The default value is the concatenation of the binding name and the contract description name.</span></span> <span data-ttu-id="9a316-162">服务可能有多个终结点，因此终结点的 `name` 特性是通过服务名称区分的。</span><span class="sxs-lookup"><span data-stu-id="9a316-162">Services may have multiple endpoints, so the endpoint’s `name` attribute is distinct from the name of the service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="9a316-163">子元素</span><span class="sxs-lookup"><span data-stu-id="9a316-163">Child Elements</span></span>  
  
|<span data-ttu-id="9a316-164">元素</span><span class="sxs-lookup"><span data-stu-id="9a316-164">Element</span></span>|<span data-ttu-id="9a316-165">说明</span><span class="sxs-lookup"><span data-stu-id="9a316-165">Description</span></span>|  
|-------------|-----------------|  
|[\<headers>](headers.md)|<span data-ttu-id="9a316-166">一个地址标头集合。</span><span class="sxs-lookup"><span data-stu-id="9a316-166">A collection of address headers.</span></span>|  
|[\<identity>](identity.md)|<span data-ttu-id="9a316-167">一个标识，与某个终结点交换消息的其他终结点可以使用该标识对该终结点进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="9a316-167">An identity that enables the authentication of an endpoint by other endpoints exchanging messages with it.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="9a316-168">父元素</span><span class="sxs-lookup"><span data-stu-id="9a316-168">Parent Elements</span></span>  
  
|<span data-ttu-id="9a316-169">元素</span><span class="sxs-lookup"><span data-stu-id="9a316-169">Element</span></span>|<span data-ttu-id="9a316-170">说明</span><span class="sxs-lookup"><span data-stu-id="9a316-170">Description</span></span>|  
|-------------|-----------------|  
|[\<service>](service.md)|<span data-ttu-id="9a316-171">一个配置节，定义客户端可以连接的终结点的列表。</span><span class="sxs-lookup"><span data-stu-id="9a316-171">A configuration section that defines a list of endpoints that a client can connect to.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="9a316-172">示例</span><span class="sxs-lookup"><span data-stu-id="9a316-172">Example</span></span>  

 <span data-ttu-id="9a316-173">这是服务终结点配置的一个示例。</span><span class="sxs-lookup"><span data-stu-id="9a316-173">This is an example of a service endpoint configuration.</span></span>  
  
```xml  
<endpoint address="/HelloWorld/"
          bindingConfiguration="usingDefaults"
          bindingName="MyBinding"
          binding="customBinding"
          contract="HelloWorld">
  <headers>
    <region xmlns="http://tempuri.org/">EastCoast</region>
    <member xmlns="http://tempuri.org/">Gold</member>
  </headers>
</endpoint>
```  
  
## <a name="see-also"></a><span data-ttu-id="9a316-174">请参阅</span><span class="sxs-lookup"><span data-stu-id="9a316-174">See also</span></span>

- <xref:System.ServiceModel.Configuration.ServiceEndpointElement>
- <xref:System.ServiceModel.EndpointAddress>
- <xref:System.ServiceModel.Description.ServiceEndpoint>
- [<span data-ttu-id="9a316-175">终结点：地址、绑定和协定</span><span class="sxs-lookup"><span data-stu-id="9a316-175">Endpoints: Addresses, Bindings, and Contracts</span></span>](../../../wcf/feature-details/endpoints-addresses-bindings-and-contracts.md)
- [<span data-ttu-id="9a316-176">如何：在配置中创建服务终结点</span><span class="sxs-lookup"><span data-stu-id="9a316-176">How to: Create a Service Endpoint in Configuration</span></span>](../../../wcf/feature-details/how-to-create-a-service-endpoint-in-configuration.md)
