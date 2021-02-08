---
description: 了解详细信息： <service>
title: <service>
ms.date: 03/30/2017
ms.assetid: 13123dd6-c4a9-4a04-a984-df184b851788
ms.openlocfilehash: c3870a170847d773996625235c75591ced75e315
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99786780"
---
# \<service>

<span data-ttu-id="7048c-102">`service` 元素包含 Windows Communication Foundation (WCF) 服务的设置。</span><span class="sxs-lookup"><span data-stu-id="7048c-102">The `service` element contains the settings for a Windows Communication Foundation (WCF) service.</span></span> <span data-ttu-id="7048c-103">它还包含公开此服务的终结点。</span><span class="sxs-lookup"><span data-stu-id="7048c-103">It also contains endpoints that expose the service.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<services>**](services.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<service>**  
  
## <a name="syntax"></a><span data-ttu-id="7048c-104">语法</span><span class="sxs-lookup"><span data-stu-id="7048c-104">Syntax</span></span>  
  
```xml  
<service behaviorConfiguration="String"
         name="String">
</service>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="7048c-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="7048c-105">Attributes and Elements</span></span>  

 <span data-ttu-id="7048c-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7048c-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="7048c-107">特性</span><span class="sxs-lookup"><span data-stu-id="7048c-107">Attributes</span></span>  
  
|<span data-ttu-id="7048c-108">属性</span><span class="sxs-lookup"><span data-stu-id="7048c-108">Attribute</span></span>|<span data-ttu-id="7048c-109">说明</span><span class="sxs-lookup"><span data-stu-id="7048c-109">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="7048c-110">behaviorConfiguration</span><span class="sxs-lookup"><span data-stu-id="7048c-110">behaviorConfiguration</span></span>|<span data-ttu-id="7048c-111">一个字符串，其中包含要用于实例化服务的行为的行为名。</span><span class="sxs-lookup"><span data-stu-id="7048c-111">A string that contains the behavior name of the behavior to be used to instantiate the service.</span></span> <span data-ttu-id="7048c-112">定义服务时，该行为名必须在作用域内。</span><span class="sxs-lookup"><span data-stu-id="7048c-112">The behavior name must be in scope at the point the service is defined.</span></span> <span data-ttu-id="7048c-113">默认值为一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="7048c-113">The default value is an empty string.</span></span>|  
|<span data-ttu-id="7048c-114">name</span><span class="sxs-lookup"><span data-stu-id="7048c-114">name</span></span>|<span data-ttu-id="7048c-115">必需的字符串属性，此属性指定要进行实例化的服务的类型。</span><span class="sxs-lookup"><span data-stu-id="7048c-115">Required String attribute that specifies the type of the service to be instantiated.</span></span> <span data-ttu-id="7048c-116">此设置必须等同于一个有效类型。</span><span class="sxs-lookup"><span data-stu-id="7048c-116">This setting must equate to a valid type.</span></span> <span data-ttu-id="7048c-117">格式应为 `Namespace.Class.`</span><span class="sxs-lookup"><span data-stu-id="7048c-117">The format should be `Namespace.Class.`</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="7048c-118">子元素</span><span class="sxs-lookup"><span data-stu-id="7048c-118">Child Elements</span></span>  
  
|<span data-ttu-id="7048c-119">元素</span><span class="sxs-lookup"><span data-stu-id="7048c-119">Element</span></span>|<span data-ttu-id="7048c-120">说明</span><span class="sxs-lookup"><span data-stu-id="7048c-120">Description</span></span>|  
|-------------|-----------------|  
|[\<endpoint>](endpoint-element.md)|<span data-ttu-id="7048c-121">公开此服务的 `endpoint` 元素的集合。</span><span class="sxs-lookup"><span data-stu-id="7048c-121">A collection of `endpoint` elements that expose this service.</span></span>|  
|[\<host>](host.md)|<span data-ttu-id="7048c-122">指定此服务实例的主机。</span><span class="sxs-lookup"><span data-stu-id="7048c-122">Specifies the host of this service instance.</span></span> <span data-ttu-id="7048c-123">此元素的类型为 <xref:System.ServiceModel.Configuration.HostElement>。</span><span class="sxs-lookup"><span data-stu-id="7048c-123">This element is of type <xref:System.ServiceModel.Configuration.HostElement>.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="7048c-124">父元素</span><span class="sxs-lookup"><span data-stu-id="7048c-124">Parent Elements</span></span>  
  
|<span data-ttu-id="7048c-125">元素</span><span class="sxs-lookup"><span data-stu-id="7048c-125">Element</span></span>|<span data-ttu-id="7048c-126">说明</span><span class="sxs-lookup"><span data-stu-id="7048c-126">Description</span></span>|  
|-------------|-----------------|  
|[\<services>](services.md)|<span data-ttu-id="7048c-127">所有 WCF 配置元素的根元素。</span><span class="sxs-lookup"><span data-stu-id="7048c-127">The root element of all WCF configuration elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7048c-128">备注</span><span class="sxs-lookup"><span data-stu-id="7048c-128">Remarks</span></span>  

 <span data-ttu-id="7048c-129">服务是在配置文件的 `services` 节中定义的。</span><span class="sxs-lookup"><span data-stu-id="7048c-129">Services are defined in the `services` section of the configuration file.</span></span> <span data-ttu-id="7048c-130">程序集可以包含任意多个服务。</span><span class="sxs-lookup"><span data-stu-id="7048c-130">An assembly can contain any number of services.</span></span> <span data-ttu-id="7048c-131">每个服务都有自己的 `service` 配置节。</span><span class="sxs-lookup"><span data-stu-id="7048c-131">Each service has its own `service` configuration section.</span></span> <span data-ttu-id="7048c-132">本节及其内容定义特定服务的服务协定、行为和终结点。</span><span class="sxs-lookup"><span data-stu-id="7048c-132">This section and its content define the service contract, behavior, and endpoints of the particular service.</span></span>  
  
 <span data-ttu-id="7048c-133">`behaviorConfiguration` 元素也是可选的。</span><span class="sxs-lookup"><span data-stu-id="7048c-133">The `behaviorConfiguration` element is also optional.</span></span> <span data-ttu-id="7048c-134">它标识服务使用的行为。</span><span class="sxs-lookup"><span data-stu-id="7048c-134">It identifies the behavior the service uses.</span></span> <span data-ttu-id="7048c-135">在此属性中指定的行为必须链接到同一配置文件中的作用域内的行为。</span><span class="sxs-lookup"><span data-stu-id="7048c-135">The behavior specified in this attribute must link to a behavior in scope in the same configuration file.</span></span>  
  
 <span data-ttu-id="7048c-136">每个服务都将公开一个或多个终结点，每个终结点具有自己的地址和绑定。</span><span class="sxs-lookup"><span data-stu-id="7048c-136">Each service exposes one or more endpoints, which has its own address and binding.</span></span> <span data-ttu-id="7048c-137">配置文件中使用的所有绑定都必须在该文件的范围内定义。</span><span class="sxs-lookup"><span data-stu-id="7048c-137">All bindings used within the configuration file must be defined in the scope of the file.</span></span> <span data-ttu-id="7048c-138">绑定通过 `name` 和 `bindingConfiguration` 属性的组合链接到终结点。</span><span class="sxs-lookup"><span data-stu-id="7048c-138">Binding are linked to endpoints through the combination of the attributes `name` and `bindingConfiguration`.</span></span> <span data-ttu-id="7048c-139">`name` 特性说明在哪个节中定义绑定。</span><span class="sxs-lookup"><span data-stu-id="7048c-139">The `name` attribute describes the section the binding is defined in.</span></span> <span data-ttu-id="7048c-140">`bindingConfiguration` 特性定义使用绑定节中的哪个配置。</span><span class="sxs-lookup"><span data-stu-id="7048c-140">The `bindingConfiguration` attribute defines which configuration within the binding section is used.</span></span> <span data-ttu-id="7048c-141">绑定节可以定义若干个配置。</span><span class="sxs-lookup"><span data-stu-id="7048c-141">A binding section can define several configurations.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7048c-142">示例</span><span class="sxs-lookup"><span data-stu-id="7048c-142">Example</span></span>  

 <span data-ttu-id="7048c-143">这是服务配置的一个示例。</span><span class="sxs-lookup"><span data-stu-id="7048c-143">This is an example of a service configuration.</span></span>  
  
```xml  
<service behaviorConfiguration="testChannelBehavior"
         name="HelloWorld">
  <endpoint address="/HelloWorld2/"
            name="test"
            bindingNamespace="http://www.cohowinery.com/"
            binding="basicHttpBinding"
            contract="IHelloWorld" />
</service>
```  
  
## <a name="see-also"></a><span data-ttu-id="7048c-144">请参阅</span><span class="sxs-lookup"><span data-stu-id="7048c-144">See also</span></span>

- <xref:System.ServiceModel.Configuration.ServiceElement>
- [<span data-ttu-id="7048c-145">正在配置服务</span><span class="sxs-lookup"><span data-stu-id="7048c-145">Configuring Services</span></span>](../../../wcf/configuring-services.md)
