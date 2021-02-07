---
description: 了解详细信息： <baseAddressPrefixFilters>
title: <baseAddressPrefixFilters>
ms.date: 03/30/2017
ms.assetid: 8cab2a9a-c51f-4283-bb60-2ad0c274fd46
ms.openlocfilehash: 9212838393ead04bdcd475b314bb2707e6f899ce
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99749670"
---
# \<baseAddressPrefixFilters>

<span data-ttu-id="963e1-102">表示配置元素的集合，这些元素指定通过筛选器，这些筛选器提供一种机制，用于在 IIS 中承载 Windows Communication Foundation (WCF) 应用程序时选择适当的 Internet Information Services (IIS) 绑定。</span><span class="sxs-lookup"><span data-stu-id="963e1-102">Represents a collection of configuration elements that specify pass through filters, which provide a mechanism to pick the appropriate Internet Information Services (IIS) bindings when hosting the Windows Communication Foundation (WCF) application in IIS.</span></span>  
  
> [!WARNING]
> <span data-ttu-id="963e1-103">\<baseAddressPrefixFilters> 不识别 "localhost";改为使用完全限定的计算机名称。</span><span class="sxs-lookup"><span data-stu-id="963e1-103">\<baseAddressPrefixFilters> does not recognize "localhost"; use the fully qualified machine name instead.</span></span>  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<serviceHostingEnvironment>**](servicehostingenvironment.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<baseAddressPrefixFilters>**  
  
## <a name="syntax"></a><span data-ttu-id="963e1-104">语法</span><span class="sxs-lookup"><span data-stu-id="963e1-104">Syntax</span></span>  
  
```xml  
<serviceHostingEnvironment>
  <baseAddressPrefixFilters>
    <add prefix="String" />
   </baseAddressPrefixFilters>
</serviceHostingEnvironment>
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="963e1-105">特性和元素</span><span class="sxs-lookup"><span data-stu-id="963e1-105">Attributes and Elements</span></span>  

 <span data-ttu-id="963e1-106">下列各节描述了特性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="963e1-106">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="963e1-107">特性</span><span class="sxs-lookup"><span data-stu-id="963e1-107">Attributes</span></span>  

 <span data-ttu-id="963e1-108">无。</span><span class="sxs-lookup"><span data-stu-id="963e1-108">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="963e1-109">子元素</span><span class="sxs-lookup"><span data-stu-id="963e1-109">Child Elements</span></span>  
  
|<span data-ttu-id="963e1-110">元素</span><span class="sxs-lookup"><span data-stu-id="963e1-110">Element</span></span>|<span data-ttu-id="963e1-111">说明</span><span class="sxs-lookup"><span data-stu-id="963e1-111">Description</span></span>|  
|-------------|-----------------|  
|[\<add>](add-of-baseaddressprefixfilter.md)|<span data-ttu-id="963e1-112">添加一个配置元素，用于指定服务主机所使用的基址的前缀筛选器。</span><span class="sxs-lookup"><span data-stu-id="963e1-112">Adds a configuration element that specifies a prefix filter for the base addresses used by the service host.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="963e1-113">父元素</span><span class="sxs-lookup"><span data-stu-id="963e1-113">Parent Elements</span></span>  
  
|<span data-ttu-id="963e1-114">元素</span><span class="sxs-lookup"><span data-stu-id="963e1-114">Element</span></span>|<span data-ttu-id="963e1-115">说明</span><span class="sxs-lookup"><span data-stu-id="963e1-115">Description</span></span>|  
|-------------|-----------------|  
|[\<serviceHostingEnvironment>](servicehostingenvironment.md)|<span data-ttu-id="963e1-116">定义服务承载环境要为特定传输实例化的类型。</span><span class="sxs-lookup"><span data-stu-id="963e1-116">Defines the type the service hosting environment instantiates for a particular transport.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="963e1-117">备注</span><span class="sxs-lookup"><span data-stu-id="963e1-117">Remarks</span></span>  

 <span data-ttu-id="963e1-118">前缀筛选器为共享的宿主提供程序提供一种指定服务要使用的 URI 的方法。</span><span class="sxs-lookup"><span data-stu-id="963e1-118">A prefix filter provides a way for shared hosting providers to specify which URIs are to be used by the service.</span></span> <span data-ttu-id="963e1-119">它使得共享主机可以在同一站点上通过同一方案的不同基址承载多个应用程序。</span><span class="sxs-lookup"><span data-stu-id="963e1-119">It enables shared hosts to host multiple applications with different base addresses for the same scheme on the same site.</span></span>  
  
 <span data-ttu-id="963e1-120">IIS 网站是包含虚拟目录的虚拟应用程序的容器。</span><span class="sxs-lookup"><span data-stu-id="963e1-120">IIS Web sites are containers for virtual applications which contain virtual directories.</span></span> <span data-ttu-id="963e1-121">可通过一个或多个 IIS 绑定访问站点上的应用程序。</span><span class="sxs-lookup"><span data-stu-id="963e1-121">The application in a site can be accessed through one or more IIS bindings.</span></span> <span data-ttu-id="963e1-122">IIS 绑定提供两条信息：绑定协议和绑定信息。</span><span class="sxs-lookup"><span data-stu-id="963e1-122">IIS bindings provide two pieces of information: binding protocol and binding information.</span></span> <span data-ttu-id="963e1-123">绑定协议（例如 HTTP）定义发生通信所基于的方案，而绑定信息（例如 IP 地址、端口、主机头）包含用于访问站点的数据。</span><span class="sxs-lookup"><span data-stu-id="963e1-123">Binding protocol (for example, HTTP) defines the scheme over which communication occurs, and binding information (for example, IP Address, Port, Hostheader) contains data used to access the site.</span></span>  
  
 <span data-ttu-id="963e1-124">IIS 支持为每个站点指定多个 IIS 绑定，这会导致每个方案有多个基址。</span><span class="sxs-lookup"><span data-stu-id="963e1-124">IIS supports specifying multiple IIS bindings for each site, which results in multiple base addresses for each scheme.</span></span> <span data-ttu-id="963e1-125">因为在站点下承载的 WCF 服务只允许绑定到每个方案的一个基址，所以您可以使用前缀筛选器功能选取所需的承载服务的基址。</span><span class="sxs-lookup"><span data-stu-id="963e1-125">Because a WCF service hosted under a site allows binding to only one base address for each scheme, you can use the prefix filter feature to pick the required base address of the hosted service.</span></span> <span data-ttu-id="963e1-126">根据可选前缀列表筛选器筛选 IIS 提供的传入基址。</span><span class="sxs-lookup"><span data-stu-id="963e1-126">The incoming base addresses, supplied by IIS, are filtered based on the optional prefix list filter.</span></span>  
  
 <span data-ttu-id="963e1-127">例如，你的站点可包含以下基址：</span><span class="sxs-lookup"><span data-stu-id="963e1-127">For example, your site can contain the following base addresses:</span></span>
  
```http
http://testl.fabrikam.com/Service.svc  
http://test2.fabrikam.com/Service.svc  
```  
  
 <span data-ttu-id="963e1-128">可以使用下面的配置文件在 appdomain 级指定前缀筛选器。</span><span class="sxs-lookup"><span data-stu-id="963e1-128">You can use the following configuration file to specify a prefix filter at the appdomain level.</span></span>  
  
```xml  
<system.serviceModel>
  <serviceHostingEnvironment>
    <baseAddressPrefixFilters>
      <add prefix="net.tcp://test1.fabrikam.com:8000" />
      <add prefix="http://test2.fabrikam.com:9000" />
    </baseAddressPrefixFilters>
  </serviceHostingEnvironment>
</system.serviceModel>
```  
  
 <span data-ttu-id="963e1-129">在此示例中，`net.tcp://test1.fabrikam.com:8000` 和 `http://test2.fabrikam.com:9000` 是允许传递的各自方案的唯一基址。</span><span class="sxs-lookup"><span data-stu-id="963e1-129">In this example, `net.tcp://test1.fabrikam.com:8000` and `http://test2.fabrikam.com:9000` are the only base addresses for their respective schemes, which are allowed to be passed through.</span></span>  
  
 <span data-ttu-id="963e1-130">默认情况下，未指定前缀时，将传递所有地址。</span><span class="sxs-lookup"><span data-stu-id="963e1-130">By default, when prefix is not specified, all addresses are passed through.</span></span> <span data-ttu-id="963e1-131">而指定前缀后，将只允许传递该方案的匹配基址。</span><span class="sxs-lookup"><span data-stu-id="963e1-131">Specifying the prefix only allows the matching base address for that scheme to be passed through.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="963e1-132">筛选器不支持任何通配符。</span><span class="sxs-lookup"><span data-stu-id="963e1-132">The filter does not support any wildcards.</span></span> <span data-ttu-id="963e1-133">此外，IIS 提供的基址可能有绑定到在 `baseAddressPrefixFilters` 列表中未列出的其他方案的地址。</span><span class="sxs-lookup"><span data-stu-id="963e1-133">In addition, the baseAddresses supplied by IIS may have addresses bound to other schemes not present in the `baseAddressPrefixFilters` list.</span></span> <span data-ttu-id="963e1-134">不会筛选出这些地址。</span><span class="sxs-lookup"><span data-stu-id="963e1-134">These addresses are not filtered out.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="963e1-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="963e1-135">See also</span></span>

- <xref:System.ServiceModel.Configuration.BaseAddressPrefixFilterElementCollection>
- <xref:System.ServiceModel.Configuration.ServiceHostingEnvironmentSection>
- <xref:System.ServiceModel.ServiceHostingEnvironment>
- [<span data-ttu-id="963e1-136">承载</span><span class="sxs-lookup"><span data-stu-id="963e1-136">Hosting</span></span>](../../../wcf/feature-details/hosting.md)
