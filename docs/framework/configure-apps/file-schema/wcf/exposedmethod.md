---
description: 了解详细信息： <exposedMethod>
title: <exposedMethod>
ms.date: 03/30/2017
ms.assetid: 61c938cd-4ee9-4b06-ab28-922ef491ab11
ms.openlocfilehash: 7bf271ba03ee16c6a45726e2bcb522bf6f55d441
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99664725"
---
# \<exposedMethod>

<span data-ttu-id="3e063-102">表示一个在 COM+ 组件上的接口作为 Web 服务公开时公开的 COM+ 方法。</span><span class="sxs-lookup"><span data-stu-id="3e063-102">Represents a COM+ method that is exposed when the interface on a COM+ component is exposed as a Web service.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<comContracts>**](comcontracts.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<comContract>**](comcontract.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<exposedMethods>**](exposedmethods.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<exposedMethod>**  
  
## <a name="syntax"></a><span data-ttu-id="3e063-103">语法</span><span class="sxs-lookup"><span data-stu-id="3e063-103">Syntax</span></span>  
  
```xml  
<comContracts>
  <comContract>
    <exposedMethods>
      <exposedMethod name="String" />
    </exposedMethods>
  </comContract>
</comContracts>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="3e063-104">特性和元素</span><span class="sxs-lookup"><span data-stu-id="3e063-104">Attributes and Elements</span></span>  

 <span data-ttu-id="3e063-105">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3e063-105">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="3e063-106">特性</span><span class="sxs-lookup"><span data-stu-id="3e063-106">Attributes</span></span>  
  
|<span data-ttu-id="3e063-107">属性</span><span class="sxs-lookup"><span data-stu-id="3e063-107">Attribute</span></span>|<span data-ttu-id="3e063-108">说明</span><span class="sxs-lookup"><span data-stu-id="3e063-108">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="3e063-109">name</span><span class="sxs-lookup"><span data-stu-id="3e063-109">name</span></span>|<span data-ttu-id="3e063-110">一个字符串，包含在 COM+ 组件上的接口作为 Web 服务公开时公开的 COM+ 方法。</span><span class="sxs-lookup"><span data-stu-id="3e063-110">A string that contains the COM+ method that is exposed when the interface on a COM+ component is exposed as a Web service.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="3e063-111">子元素</span><span class="sxs-lookup"><span data-stu-id="3e063-111">Child Elements</span></span>  

 <span data-ttu-id="3e063-112">无。</span><span class="sxs-lookup"><span data-stu-id="3e063-112">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="3e063-113">父元素</span><span class="sxs-lookup"><span data-stu-id="3e063-113">Parent Elements</span></span>  
  
|<span data-ttu-id="3e063-114">元素</span><span class="sxs-lookup"><span data-stu-id="3e063-114">Element</span></span>|<span data-ttu-id="3e063-115">说明</span><span class="sxs-lookup"><span data-stu-id="3e063-115">Description</span></span>|  
|-------------|-----------------|  
|[\<exposedMethods>](exposedmethods.md)|<span data-ttu-id="3e063-116">元素的集合 [\<exposedMethod>](exposedmethod.md) 。</span><span class="sxs-lookup"><span data-stu-id="3e063-116">A collection of [\<exposedMethod>](exposedmethod.md) elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3e063-117">备注</span><span class="sxs-lookup"><span data-stu-id="3e063-117">Remarks</span></span>  

 <span data-ttu-id="3e063-118">可以使用 COM+ 集成配置工具 (ComSvcConfig.exe) 来添加 COM 接口中的特定方法，使其出现在生成的服务协定中。</span><span class="sxs-lookup"><span data-stu-id="3e063-118">The COM+ integration configuration tool (ComSvcConfig.exe) can be used to add specific methods from a COM interface to appear on the generated service contract.</span></span>  
  
 <span data-ttu-id="3e063-119">例如，可以使用以下命令将 `IFinances`.Financial 组件上的 `ItemOrders` COM 接口中的三个命名方法添加到生成的服务协定中。</span><span class="sxs-lookup"><span data-stu-id="3e063-119">For example, you can use the following command to add the three named methods from the `IFinances` COM interface on the `ItemOrders`.Financial component, to the generated service contract.</span></span>  
  
 `ComSvcConfig.exe /i /application:OnlineStore /contract:ItemOrders.Financial,IFinances.{TransferFunds,AddFunds,RemoveFunds} /hosting:complus`  
  
 <span data-ttu-id="3e063-120">当你同时运行 ComSvcConfig.exe 时，它会生成以下服务协定，将前面提到的方法作为 [\<exposedMethod>](exposedmethod.md) 元素列出。</span><span class="sxs-lookup"><span data-stu-id="3e063-120">When you also run the ComSvcConfig.exe, it then generates the following service contract listing the previously mentioned methods as [\<exposedMethod>](exposedmethod.md) elements.</span></span>  
  
```xml  
<comContract contractType="{C551FBA9-E3AA-4272-8C2A-84BD8D290AC7}"
             name="IFinances"
             namespace="http://contoso.com/services/financial">
  <exposedMethod name="TransferFunds"/>
  <exposedMethod name="AddFunds"/>
  <exposedMethod name="RemoveFunds"/>
</comContract>
```  
  
 <span data-ttu-id="3e063-121">在服务初始化时，运行时将尝试通过反射并仅添加元素列表中包含的方法来生成服务协定 [\<exposedMethod>](exposedmethod.md) 。</span><span class="sxs-lookup"><span data-stu-id="3e063-121">At service initialization time, the runtime attempts to generate a service contract by reflecting over and adding only the methods included in the list of [\<exposedMethod>](exposedmethod.md) elements.</span></span> <span data-ttu-id="3e063-122">对于该服务协定中未包括的每个接口方法，都会产生一个跟踪。</span><span class="sxs-lookup"><span data-stu-id="3e063-122">A trace is produced for every interface method that is not included on the service contract.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3e063-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="3e063-123">See also</span></span>

- <xref:System.ServiceModel.Configuration.ComMethodElementCollection>
- <xref:System.ServiceModel.Configuration.ComMethodElement>
- [\<comContracts>](comcontracts.md)
- [<span data-ttu-id="3e063-124">与 COM + 应用程序集成</span><span class="sxs-lookup"><span data-stu-id="3e063-124">Integrating with COM+ Applications</span></span>](../../../wcf/feature-details/integrating-with-com-plus-applications.md)
- [<span data-ttu-id="3e063-125">如何：配置 COM+ 服务设置</span><span class="sxs-lookup"><span data-stu-id="3e063-125">How to: Configure COM+ Service Settings</span></span>](../../../wcf/feature-details/how-to-configure-com-service-settings.md)
