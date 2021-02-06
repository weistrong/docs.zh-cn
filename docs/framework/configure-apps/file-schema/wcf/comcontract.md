---
description: 了解详细信息： <comContract>
title: <comContract>
ms.date: 03/30/2017
ms.assetid: 3f8e1c0c-cfdf-4c79-ac65-c64e9323a51c
ms.openlocfilehash: fde1188a087f13da6629460bcebcea16ceefc0e8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638660"
---
# \<comContract>

<span data-ttu-id="79fc8-102">指定 COM+ 集成服务协定。</span><span class="sxs-lookup"><span data-stu-id="79fc8-102">Specifies a COM+ integration service contract.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<comContracts>**](comcontracts.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<comContract>**  
  
## <a name="syntax"></a><span data-ttu-id="79fc8-103">语法</span><span class="sxs-lookup"><span data-stu-id="79fc8-103">Syntax</span></span>  
  
```xml  
<comContracts>
  <comContract contract="String"
               namespace="String"
               name="String"
               requireSession="Boolean">
    <exposedMethods>
      <exposedMethod name="String" />
    </exposedMethods>
    <userDefinedTypes>
      <userDefinedType name="String"
                       typeLibID="String"
                       typeLibVersion="String"
                       typeDefID="String">
      </userDefinedType>
    </userDefinedTypes>
    <persistableTypes>
      <persistableType id="String"
                       name="String">
      </persistableType>
    </persistableTypes>
  </comContract>
</comContracts>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="79fc8-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="79fc8-104">Attributes and Elements</span></span>  

 <span data-ttu-id="79fc8-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="79fc8-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="79fc8-106">特性</span><span class="sxs-lookup"><span data-stu-id="79fc8-106">Attributes</span></span>  
  
|<span data-ttu-id="79fc8-107">属性</span><span class="sxs-lookup"><span data-stu-id="79fc8-107">Attribute</span></span>|<span data-ttu-id="79fc8-108">说明</span><span class="sxs-lookup"><span data-stu-id="79fc8-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="79fc8-109">contract</span><span class="sxs-lookup"><span data-stu-id="79fc8-109">contract</span></span>|<span data-ttu-id="79fc8-110">一个包含协定类型的字符串。</span><span class="sxs-lookup"><span data-stu-id="79fc8-110">A string that contains the contract type.</span></span>|  
|<span data-ttu-id="79fc8-111">name</span><span class="sxs-lookup"><span data-stu-id="79fc8-111">name</span></span>|<span data-ttu-id="79fc8-112">一个包含协定名称的字符串。</span><span class="sxs-lookup"><span data-stu-id="79fc8-112">A string that contains the contract name.</span></span>|  
|<span data-ttu-id="79fc8-113">命名空间</span><span class="sxs-lookup"><span data-stu-id="79fc8-113">namespace</span></span>|<span data-ttu-id="79fc8-114">一个包含协定命名空间的字符串。</span><span class="sxs-lookup"><span data-stu-id="79fc8-114">A string that contains the contract namespace.</span></span>|  
|<span data-ttu-id="79fc8-115">requiresSession</span><span class="sxs-lookup"><span data-stu-id="79fc8-115">requiresSession</span></span>|<span data-ttu-id="79fc8-116">一个布尔值，指定是否只能在会话绑定上使用该协定。</span><span class="sxs-lookup"><span data-stu-id="79fc8-116">A Boolean value that specifies whether the contract can only be used on sessionful bindings.</span></span> <span data-ttu-id="79fc8-117">在初始化服务时，集成运行库可以确保此设置与要使用的绑定的类型一致。</span><span class="sxs-lookup"><span data-stu-id="79fc8-117">When the service is initialized, the integration runtime ensures that this setting is consistent with the type of binding to be used.</span></span> <span data-ttu-id="79fc8-118">如果协定的一个或多个绑定存在冲突，则会生成异常。</span><span class="sxs-lookup"><span data-stu-id="79fc8-118">An exception is generated if one or more of the bindings for the contract are in conflict.</span></span> <span data-ttu-id="79fc8-119">如果此属性为 `false`、使用的是单向通道并且存在任何 [out] 参数，则也会生成异常。</span><span class="sxs-lookup"><span data-stu-id="79fc8-119">If this property is `false`, and a one-way channel is in use and there are any [out] parameters, an exception is also generated.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="79fc8-120">子元素</span><span class="sxs-lookup"><span data-stu-id="79fc8-120">Child Elements</span></span>  
  
|<span data-ttu-id="79fc8-121">元素</span><span class="sxs-lookup"><span data-stu-id="79fc8-121">Element</span></span>|<span data-ttu-id="79fc8-122">说明</span><span class="sxs-lookup"><span data-stu-id="79fc8-122">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="79fc8-123">persistableTypes</span><span class="sxs-lookup"><span data-stu-id="79fc8-123">persistableTypes</span></span>|<span data-ttu-id="79fc8-124">所有持久类型。</span><span class="sxs-lookup"><span data-stu-id="79fc8-124">All the persistable types.</span></span>|  
|<span data-ttu-id="79fc8-125">userDefinedTypes</span><span class="sxs-lookup"><span data-stu-id="79fc8-125">userDefinedTypes</span></span>|<span data-ttu-id="79fc8-126">一个要包括在服务协定中的用户定义的类型 (UDT) 的集合。</span><span class="sxs-lookup"><span data-stu-id="79fc8-126">A collection of User Defined Types (UDT) that is to be included in the service contract.</span></span>|  
|<span data-ttu-id="79fc8-127">exposedMethods</span><span class="sxs-lookup"><span data-stu-id="79fc8-127">exposedMethods</span></span>|<span data-ttu-id="79fc8-128">一个在 COM+ 组件上的接口作为 Web 服务公开时所公开的 COM+ 方法的集合。</span><span class="sxs-lookup"><span data-stu-id="79fc8-128">A collection of COM+ methods that are exposed when the interface on a COM+ component is exposed as a Web service.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="79fc8-129">父元素</span><span class="sxs-lookup"><span data-stu-id="79fc8-129">Parent Elements</span></span>  
  
|<span data-ttu-id="79fc8-130">元素</span><span class="sxs-lookup"><span data-stu-id="79fc8-130">Element</span></span>|<span data-ttu-id="79fc8-131">说明</span><span class="sxs-lookup"><span data-stu-id="79fc8-131">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="79fc8-132">comContracts</span><span class="sxs-lookup"><span data-stu-id="79fc8-132">comContracts</span></span>|<span data-ttu-id="79fc8-133">包含 `comContract` 元素的集合。</span><span class="sxs-lookup"><span data-stu-id="79fc8-133">Contains a collection of `comContract` elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="79fc8-134">备注</span><span class="sxs-lookup"><span data-stu-id="79fc8-134">Remarks</span></span>  

 <span data-ttu-id="79fc8-135">COM + 集成服务协定当前仅限于 `http://tempuri.org` 命名空间，协定名称派生自支持的 COM 接口。</span><span class="sxs-lookup"><span data-stu-id="79fc8-135">COM+ integration service contracts are currently restricted to the `http://tempuri.org` namespace, and contract name is derived from the supporting COM interface.</span></span> <span data-ttu-id="79fc8-136">但是，可以使用配置文件中的 `comContracts` 节以及 `comContract` 元素来指定替代服务协定。</span><span class="sxs-lookup"><span data-stu-id="79fc8-136">You can, however, specify alternatives by using the `comContracts` section, as well as the `comContract` element in the configuration file.</span></span> <span data-ttu-id="79fc8-137">例如，可以使用下面的配置来指定服务协定的命名空间、协定名称、要包含的用户定义类型以及其他设置。</span><span class="sxs-lookup"><span data-stu-id="79fc8-137">For example, you can use the following configuration to specify the namespace, contract name, and user defined types to be included, as well as other settings for a service contract.</span></span>  
  
```xml  
<comContracts>
  <comContract contract="{5163B1E7-F0CF-4B6A-9A02-4AB654F34284}"
               namespace="http://tempuri.org/5163B1E7-F0CF-4B6A-9A02-4AB654F34284"
               name="_Broker"
               requireSession="true">
    <exposedMethods>
      <exposedMethod name="BuyStock" />
      <exposedMethod name="SellStock" />
      <exposedMethod name="ExecuteTransaction" />
    </exposedMethods>
  </comContract>
</comContracts>
```  
  
 <span data-ttu-id="79fc8-138">在初始化服务时，指定的命名空间和协定名称将应用到生成的服务说明。</span><span class="sxs-lookup"><span data-stu-id="79fc8-138">When the service is initialized, the specified namespaces and contract names are applied to the generated service descriptions.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="79fc8-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="79fc8-139">See also</span></span>

- <xref:System.ServiceModel.Configuration.ComContractElementCollection>
- <xref:System.ServiceModel.Configuration.ComContractElement>
- [\<comContracts>](comcontracts.md)
- [<span data-ttu-id="79fc8-140">与 COM + 应用程序集成</span><span class="sxs-lookup"><span data-stu-id="79fc8-140">Integrating with COM+ Applications</span></span>](../../../wcf/feature-details/integrating-with-com-plus-applications.md)
- [<span data-ttu-id="79fc8-141">如何：配置 COM+ 服务设置</span><span class="sxs-lookup"><span data-stu-id="79fc8-141">How to: Configure COM+ Service Settings</span></span>](../../../wcf/feature-details/how-to-configure-com-service-settings.md)
