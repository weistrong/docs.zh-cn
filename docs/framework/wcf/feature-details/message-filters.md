---
description: 了解详细信息：消息筛选器
title: 消息筛选器
ms.date: 03/30/2017
helpviewer_keywords:
- routing [WCF], message filters
ms.assetid: cb33ba49-8b1f-4099-8acb-240404a46d9a
ms.openlocfilehash: 1b52b2b50dc94e79ba6960e834f601af18200f52
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99727048"
---
# <a name="message-filters"></a><span data-ttu-id="749a3-103">消息筛选器</span><span class="sxs-lookup"><span data-stu-id="749a3-103">Message Filters</span></span>

<span data-ttu-id="749a3-104">为了实现基于内容的路由，路由服务使用 <xref:System.ServiceModel.Dispatcher.MessageFilter> 实现，这些实现检查消息的特定部分，例如地址、终结点名称或特定 XPath 语句。</span><span class="sxs-lookup"><span data-stu-id="749a3-104">To implement content-based routing, the Routing Service uses <xref:System.ServiceModel.Dispatcher.MessageFilter> implementations that inspect specific sections of a message, such as the address, endpoint name, or a specific XPath statement.</span></span> <span data-ttu-id="749a3-105">如果随 [!INCLUDE[netfx_current_short](../../../../includes/netfx-current-short-md.md)] 一起提供的消息筛选器均无法满足您的需求，则您可以通过创建 <xref:System.ServiceModel.Dispatcher.MessageFilter> 基类的新实现来创建自定义筛选器。</span><span class="sxs-lookup"><span data-stu-id="749a3-105">If none of the message filters provided with [!INCLUDE[netfx_current_short](../../../../includes/netfx-current-short-md.md)] meet your needs, you can create a custom filter by creating a new implementation of the base <xref:System.ServiceModel.Dispatcher.MessageFilter> class.</span></span>  
  
 <span data-ttu-id="749a3-106">配置路由服务时，您必须 (对象定义筛选器元素， <xref:System.ServiceModel.Routing.Configuration.FilterElement>) 描述 **MessageFilter** 的类型以及创建筛选器所需的任何支持数据（例如，要在消息中搜索的特定字符串值）。</span><span class="sxs-lookup"><span data-stu-id="749a3-106">When configuring the Routing Service, you must define filter elements (<xref:System.ServiceModel.Routing.Configuration.FilterElement> objects) that describe the type of **MessageFilter** and any supporting data required to create the filter, such as specific string values to search for within the message.</span></span> <span data-ttu-id="749a3-107">请注意，创建筛选器元素仅定义了单独的消息筛选器；若要使用筛选器计算和路由消息，还必须定义筛选器表 (<xref:System.ServiceModel.Routing.Configuration.FilterTableEntryCollection>)。</span><span class="sxs-lookup"><span data-stu-id="749a3-107">Note that creating the filter elements only defines the individual message filters; to use the filters to evaluate and route messages you must also define a filter table (<xref:System.ServiceModel.Routing.Configuration.FilterTableEntryCollection>).</span></span>  
  
 <span data-ttu-id="749a3-108">筛选器表中的每个条目都引用一个筛选器元素，并指定当消息与筛选器匹配时消息将路由到的客户端终结点。</span><span class="sxs-lookup"><span data-stu-id="749a3-108">Each entry in the filter table references a filter element and specifies the client endpoint that a message will be routed to if the message matches the filter.</span></span> <span data-ttu-id="749a3-109">通过筛选器表条目，您还可以指定一个备份终结点集合 (<xref:System.ServiceModel.Routing.Configuration.BackupEndpointCollection>)，该集合定义在向主终结点发送消息但出现传输故障时，该消息将传输到的目标终结点的列表。</span><span class="sxs-lookup"><span data-stu-id="749a3-109">The filter table entries also allow you to specify a collection of backup endpoints (<xref:System.ServiceModel.Routing.Configuration.BackupEndpointCollection>), which defines a list of endpoints that the message will be transmitted to in the event of a transmission failure when sending to the primary endpoint.</span></span> <span data-ttu-id="749a3-110">将按指定顺序尝试这些终结点，直至某个终结点成功为止。</span><span class="sxs-lookup"><span data-stu-id="749a3-110">These endpoints will be tried in the order specified until one succeeds.</span></span>  
  
## <a name="message-filters"></a><span data-ttu-id="749a3-111">消息筛选器</span><span class="sxs-lookup"><span data-stu-id="749a3-111">Message Filters</span></span>  

 <span data-ttu-id="749a3-112">路由服务使用的消息筛选器提供常用消息选择功能，例如，计算消息已发送到的终结点的名称、SOAP 操作或消息已发送到的地址或地址前缀。</span><span class="sxs-lookup"><span data-stu-id="749a3-112">The message filters used by the Routing Service provide common message selection functionality, such as evaluating the name of the endpoint that a message was sent to, the SOAP action, or the address or address prefix that the message was sent to.</span></span> <span data-ttu-id="749a3-113">也可以使用 `AND` 条件连接筛选器，这样，仅当消息同时与两个筛选器匹配时，才会将消息路由至某个终结点。</span><span class="sxs-lookup"><span data-stu-id="749a3-113">Filters can also be joined with an `AND` condition, so that messages will only be routed to an endpoint if the message matches both filters.</span></span> <span data-ttu-id="749a3-114">此外，还可以通过创建您自己的 <xref:System.ServiceModel.Dispatcher.MessageFilter> 实现来创建自定义筛选器。</span><span class="sxs-lookup"><span data-stu-id="749a3-114">You can also create custom filters by creating your own implementation of <xref:System.ServiceModel.Dispatcher.MessageFilter>.</span></span>  
  
 <span data-ttu-id="749a3-115">下表列出了路由服务使用的 <xref:System.ServiceModel.Routing.Configuration.FilterType>、实现特定消息筛选器的类，以及所需的 <xref:System.ServiceModel.Routing.Configuration.FilterElement.FilterData%2A> 参数。</span><span class="sxs-lookup"><span data-stu-id="749a3-115">The following table lists the <xref:System.ServiceModel.Routing.Configuration.FilterType> used by the Routing Service, the class that implements the specific message filter, and the required <xref:System.ServiceModel.Routing.Configuration.FilterElement.FilterData%2A> parameters.</span></span>  
  
|<span data-ttu-id="749a3-116">筛选器类型</span><span class="sxs-lookup"><span data-stu-id="749a3-116">Filter  Type</span></span>|<span data-ttu-id="749a3-117">说明</span><span class="sxs-lookup"><span data-stu-id="749a3-117">Description</span></span>|<span data-ttu-id="749a3-118">筛选器数据含义</span><span class="sxs-lookup"><span data-stu-id="749a3-118">Filter Data Meaning</span></span>|<span data-ttu-id="749a3-119">示例筛选器</span><span class="sxs-lookup"><span data-stu-id="749a3-119">Example Filter</span></span>|  
|------------------|-----------------|-------------------------|--------------------|  
|<span data-ttu-id="749a3-120">操作</span><span class="sxs-lookup"><span data-stu-id="749a3-120">Action</span></span>|<span data-ttu-id="749a3-121">使用 <xref:System.ServiceModel.Dispatcher.ActionMessageFilter> 类匹配包含特定操作的消息。</span><span class="sxs-lookup"><span data-stu-id="749a3-121">Uses the <xref:System.ServiceModel.Dispatcher.ActionMessageFilter> class to match messages containing a specific action.</span></span>|<span data-ttu-id="749a3-122">筛选器基于的操作。</span><span class="sxs-lookup"><span data-stu-id="749a3-122">The action to filter upon.</span></span>|\<filter name="action1" filterType="Action" filterData="http://namespace/contract/operation" />|  
|<span data-ttu-id="749a3-123">EndpointAddress</span><span class="sxs-lookup"><span data-stu-id="749a3-123">EndpointAddress</span></span>|<span data-ttu-id="749a3-124">使用 <xref:System.ServiceModel.Dispatcher.EndpointAddressMessageFilter> 类 <xref:System.ServiceModel.Dispatcher.EndpointAddressMessageFilter.IncludeHostNameInComparison%2A>  ==  `true` 来匹配包含特定地址的消息。</span><span class="sxs-lookup"><span data-stu-id="749a3-124">Uses the <xref:System.ServiceModel.Dispatcher.EndpointAddressMessageFilter> class, with <xref:System.ServiceModel.Dispatcher.EndpointAddressMessageFilter.IncludeHostNameInComparison%2A> == `true` to match messages containing a specific address.</span></span>|<span data-ttu-id="749a3-125">筛选器基于的地址（在 To 标头中）。</span><span class="sxs-lookup"><span data-stu-id="749a3-125">The address to filter upon (in the To header).</span></span>|\<filter name="address1" filterType="EndpointAddress" filterData="http://host/vdir/s.svc/b"  />|  
|<span data-ttu-id="749a3-126">EndpointAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="749a3-126">EndpointAddressPrefix</span></span>|<span data-ttu-id="749a3-127">使用 <xref:System.ServiceModel.Dispatcher.PrefixEndpointAddressMessageFilter> 类 <xref:System.ServiceModel.Dispatcher.PrefixEndpointAddressMessageFilter.IncludeHostNameInComparison%2A>  ==  `true` 来匹配包含特定地址前缀的消息。</span><span class="sxs-lookup"><span data-stu-id="749a3-127">Uses the <xref:System.ServiceModel.Dispatcher.PrefixEndpointAddressMessageFilter> class, with <xref:System.ServiceModel.Dispatcher.PrefixEndpointAddressMessageFilter.IncludeHostNameInComparison%2A> == `true` to match messages containing a specific address prefix.</span></span>|<span data-ttu-id="749a3-128">筛选器基于的地址（使用最长的前缀匹配项）。</span><span class="sxs-lookup"><span data-stu-id="749a3-128">The address to filter upon using longest prefix matching.</span></span>|\<filter name="prefix1" filterType="EndpointAddressPrefix" filterData="http://host/" />|  
|<span data-ttu-id="749a3-129">And</span><span class="sxs-lookup"><span data-stu-id="749a3-129">And</span></span>|<span data-ttu-id="749a3-130">使用始终在返回前计算两个条件的 <xref:System.ServiceModel.Dispatcher.StrictAndMessageFilter> 类。</span><span class="sxs-lookup"><span data-stu-id="749a3-130">Uses the <xref:System.ServiceModel.Dispatcher.StrictAndMessageFilter> class that always evaluates both conditions before returning.</span></span>|<span data-ttu-id="749a3-131">不使用 filterData;相反，filter1 和 filter2 具有相应的消息筛选器的名称，在表) 中 (也应同时 **存在。**</span><span class="sxs-lookup"><span data-stu-id="749a3-131">filterData is not used; instead filter1 and filter2 have the names of the corresponding message filters (also in the table), which should be **AND** ed together.</span></span>|\<filter name="and1" filterType="And" filter1="address1" filter2="action1" />|  
|<span data-ttu-id="749a3-132">自定义</span><span class="sxs-lookup"><span data-stu-id="749a3-132">Custom</span></span>|<span data-ttu-id="749a3-133">一个用户定义的类型，此类型扩展 <xref:System.ServiceModel.Dispatcher.MessageFilter> 类并具有采用字符串的构造函数。</span><span class="sxs-lookup"><span data-stu-id="749a3-133">A user-defined type that extends the <xref:System.ServiceModel.Dispatcher.MessageFilter> class and has a constructor taking a string.</span></span>|<span data-ttu-id="749a3-134">customType 特性是要创建的类的完全限定类型名称；filterData 是在创建筛选器时要传递给构造函数的字符串。</span><span class="sxs-lookup"><span data-stu-id="749a3-134">The customType attribute is the fully qualified type name of the class to create; filterData is the string to pass to the constructor when creating the filter.</span></span>|\<filter name="custom1" filterType="Custom" customType="CustomAssembly.CustomMsgFilter, CustomAssembly" filterData="Custom Data" />|  
|<span data-ttu-id="749a3-135">EndpointName</span><span class="sxs-lookup"><span data-stu-id="749a3-135">EndpointName</span></span>|<span data-ttu-id="749a3-136">使用 <xref:System.ServiceModel.Dispatcher.EndpointNameMessageFilter> 类根据消息已到达的服务终结点的名称来匹配消息。</span><span class="sxs-lookup"><span data-stu-id="749a3-136">Uses the <xref:System.ServiceModel.Dispatcher.EndpointNameMessageFilter> class to match messages based on the name of the service endpoint they arrived on.</span></span>|<span data-ttu-id="749a3-137">服务终结点的名称，例如： "serviceEndpoint1"。</span><span class="sxs-lookup"><span data-stu-id="749a3-137">The name of the service endpoint, for example: "serviceEndpoint1".</span></span>  <span data-ttu-id="749a3-138">该终结点应为在路由服务上公开的终结点之一。</span><span class="sxs-lookup"><span data-stu-id="749a3-138">This should be one of the endpoints exposed on the Routing Service.</span></span>|\<filter name="stock1" filterType="Endpoint" filterData="SvcEndpoint" />|  
|<span data-ttu-id="749a3-139">MatchAll</span><span class="sxs-lookup"><span data-stu-id="749a3-139">MatchAll</span></span>|<span data-ttu-id="749a3-140">使用 <xref:System.ServiceModel.Dispatcher.MatchAllMessageFilter> 类。</span><span class="sxs-lookup"><span data-stu-id="749a3-140">Uses the <xref:System.ServiceModel.Dispatcher.MatchAllMessageFilter> class.</span></span> <span data-ttu-id="749a3-141">该筛选器匹配所有到达的消息。</span><span class="sxs-lookup"><span data-stu-id="749a3-141">This filter matches all arriving messages.</span></span>|<span data-ttu-id="749a3-142">不使用 filterData。</span><span class="sxs-lookup"><span data-stu-id="749a3-142">filterData is not used.</span></span> <span data-ttu-id="749a3-143">该筛选器将始终匹配所有消息。</span><span class="sxs-lookup"><span data-stu-id="749a3-143">This filter will always match all messages.</span></span>|\<filter name="matchAll1" filterType="MatchAll" />|  
|<span data-ttu-id="749a3-144">XPath</span><span class="sxs-lookup"><span data-stu-id="749a3-144">XPath</span></span>|<span data-ttu-id="749a3-145">使用 <xref:System.ServiceModel.Dispatcher.XPathMessageFilter> 类匹配消息中的特定 XPath 查询。</span><span class="sxs-lookup"><span data-stu-id="749a3-145">Uses the <xref:System.ServiceModel.Dispatcher.XPathMessageFilter> class to match specific XPath queries within the message.</span></span>|<span data-ttu-id="749a3-146">在匹配消息时要使用的 XPath 查询。</span><span class="sxs-lookup"><span data-stu-id="749a3-146">The XPath query to use when matching messages.</span></span>|\<filter name="XPath1" filterType="XPath" filterData="//ns:element" />|  
  
 <span data-ttu-id="749a3-147">下面的示例定义使用 XPath、EndpointName 和 PrefixEndpointAddress 消息筛选器的筛选器条目。</span><span class="sxs-lookup"><span data-stu-id="749a3-147">The following example defines filter entries that use the XPath, EndpointName, and PrefixEndpointAddress message filters.</span></span> <span data-ttu-id="749a3-148">该示例还演示如何对 RoundRobinFilter1 和 RoundRobinFilter2 条目使用自定义筛选器。</span><span class="sxs-lookup"><span data-stu-id="749a3-148">This example also demonstrates using a custom filter for the RoundRobinFilter1 and RoundRobinFilter2 entries.</span></span>  
  
```xml  
<filters>  
     <filter name="XPathFilter" filterType="XPath"
             filterData="/s12:Envelope/s12:Header/custom:RoundingCalculator = 1"/>  
     <filter name="EndpointNameFilter" filterType="EndpointName"
             filterData="calculatorEndpoint"/>  
     <filter name="PrefixAddressFilter" filterType="PrefixEndpointAddress"
             filterData="http://localhost/routingservice/router/rounding/"/>  
     <filter name="RoundRobinFilter1" filterType="Custom"
             customType="RoutingServiceFilters.RoundRobinMessageFilter,
             RoutingService" filterData="group1"/>  
     <filter name="RoundRobinFilter2" filterType="Custom"
             customType="RoutingServiceFilters.RoundRobinMessageFilter,
             RoutingService" filterData="group1"/>  
</filters>  
```  
  
> [!NOTE]
> <span data-ttu-id="749a3-149">仅定义筛选器不会导致根据筛选器计算消息。</span><span class="sxs-lookup"><span data-stu-id="749a3-149">Simply defining a filter does not cause messages to be evaluated against the filter.</span></span> <span data-ttu-id="749a3-150">必须将筛选器添加到筛选器表中，然后会将该筛选器与路由服务公开的服务终结点相关联。</span><span class="sxs-lookup"><span data-stu-id="749a3-150">The filter must be added to a filter table, which is then associated with the service endpoint exposed by the Routing Service.</span></span>  
  
### <a name="namespace-table"></a><span data-ttu-id="749a3-151">命名空间表</span><span class="sxs-lookup"><span data-stu-id="749a3-151">Namespace Table</span></span>  

 <span data-ttu-id="749a3-152">当使用 XPath 筛选器时，包含 XPath 查询的筛选器数据可能会因使用了命名空间而变得非常大。</span><span class="sxs-lookup"><span data-stu-id="749a3-152">When using an XPath filter, the filter data that contains the XPath query can become extremely large due to the use of namespaces.</span></span> <span data-ttu-id="749a3-153">为了解决此问题，路由服务提供使用命名空间表定义您自己的命名空间前缀的功能。</span><span class="sxs-lookup"><span data-stu-id="749a3-153">To alleviate this problem the Routing Service provides the ability to define your own namespace prefixes by using the namespace table.</span></span>  
  
 <span data-ttu-id="749a3-154">命名空间表是 <xref:System.ServiceModel.Routing.Configuration.NamespaceElement> 对象的集合，用于定义可在 XPath 中使用的常用命名空间的命名空间前缀。</span><span class="sxs-lookup"><span data-stu-id="749a3-154">The namespace table is a collection of <xref:System.ServiceModel.Routing.Configuration.NamespaceElement> objects that defines the namespace prefixes for common namespaces that can be used in an XPath.</span></span> <span data-ttu-id="749a3-155">下面列出了命名空间表中包含的默认命名空间和命名空间前缀。</span><span class="sxs-lookup"><span data-stu-id="749a3-155">The following are the default namespaces and namespace prefixes that are contained in the namespace table.</span></span>  
  
|<span data-ttu-id="749a3-156">前缀</span><span class="sxs-lookup"><span data-stu-id="749a3-156">Prefix</span></span>|<span data-ttu-id="749a3-157">命名空间</span><span class="sxs-lookup"><span data-stu-id="749a3-157">Namespace</span></span>|  
|------------|---------------|  
|<span data-ttu-id="749a3-158">s11</span><span class="sxs-lookup"><span data-stu-id="749a3-158">s11</span></span>|`http://schemas.xmlsoap.org/soap/envelope`|  
|<span data-ttu-id="749a3-159">s12</span><span class="sxs-lookup"><span data-stu-id="749a3-159">s12</span></span>|`http://www.w3.org/2003/05/soap-envelope`|  
|<span data-ttu-id="749a3-160">wsaAugust2004</span><span class="sxs-lookup"><span data-stu-id="749a3-160">wsaAugust2004</span></span>|`http://schemas.xmlsoap.org/ws/2004/08/addressing`|  
|<span data-ttu-id="749a3-161">wsa10</span><span class="sxs-lookup"><span data-stu-id="749a3-161">wsa10</span></span>|`http://www.w3.org/2005/08/addressing`|  
|<span data-ttu-id="749a3-162">sm</span><span class="sxs-lookup"><span data-stu-id="749a3-162">sm</span></span>|`http://schemas.microsoft.com/serviceModel/2004/05/xpathfunctions`|  
|<span data-ttu-id="749a3-163">tempuri</span><span class="sxs-lookup"><span data-stu-id="749a3-163">tempuri</span></span>|`http://tempuri.org`|  
|<span data-ttu-id="749a3-164">ser</span><span class="sxs-lookup"><span data-stu-id="749a3-164">ser</span></span>|`http://schemas.microsoft.com/2003/10/Serialization`|  
  
 <span data-ttu-id="749a3-165">如果您确定您将在 XPath 查询中使用特定命名空间，则可以将此命名空间和唯一的命名空间前缀添加到命名空间表中，并在所有 XPath 查询中使用该前缀而不是使用完整命名空间。</span><span class="sxs-lookup"><span data-stu-id="749a3-165">When you know that you will be using a specific namespace in your XPath queries, you can add it to the namespace table along with a unique namespace prefix and use the prefix in any XPath query instead of the full namespace.</span></span> <span data-ttu-id="749a3-166">下面的示例为命名空间定义了一个 "custom" 前缀 `"http://my.custom.namespace"` ，然后在 filterData 中包含的 XPath 查询中使用该前缀。</span><span class="sxs-lookup"><span data-stu-id="749a3-166">The following example defines a prefix of "custom" for the namespace `"http://my.custom.namespace"`, which is then used in the XPath query contained in filterData.</span></span>  
  
```xml  
<namespaceTable>  
     <add prefix="custom" namespace="http://my.custom.namespace/"/>  
</namespaceTable>  
<filters>  
     <filter name="XPathFilter" filterType="XPath" filterData="/s12:Envelope/s12:Header/custom:RoundingCalculator = 1"/>  
</filters>  
```  
  
## <a name="filter-tables"></a><span data-ttu-id="749a3-167">筛选器表</span><span class="sxs-lookup"><span data-stu-id="749a3-167">Filter Tables</span></span>  

 <span data-ttu-id="749a3-168">各筛选器元素定义可应用于消息的逻辑比较，而筛选器表提供筛选器元素和目标客户端终结点之间的关联。</span><span class="sxs-lookup"><span data-stu-id="749a3-168">While each filter element defines a logical comparison that can be applied to a message, the filter table provides the association between the filter element and the destination client endpoint.</span></span> <span data-ttu-id="749a3-169">筛选器表是 <xref:System.ServiceModel.Routing.Configuration.FilterTableEntryElement> 对象的命名集合，用于定义筛选器、主目标终结点和替代备份终结点列表之间的关联。</span><span class="sxs-lookup"><span data-stu-id="749a3-169">A filter table is a named collection of <xref:System.ServiceModel.Routing.Configuration.FilterTableEntryElement> objects that define the association between a filter, a primary destination endpoint, and a list of alternative backup endpoints.</span></span> <span data-ttu-id="749a3-170">筛选器表条目还允许您为每个筛选条件指定可选优先级。</span><span class="sxs-lookup"><span data-stu-id="749a3-170">The filter table entries also allow you to specify an optional priority for each filter condition.</span></span> <span data-ttu-id="749a3-171">下面的示例定义两个筛选器，然后定义一个用于将每个筛选器与目标终结点相关联的筛选器表。</span><span class="sxs-lookup"><span data-stu-id="749a3-171">The following example defines two filters and then defines a filter table that associates each filter with a destination endpoint.</span></span>  
  
```xml  
<routing>  
     <filters>  
       <filter name="AddAction" filterType="Action" filterData="Add" />  
       <filter name="SubtractAction" filterType="Action" filterData="Subtract" />  
     </filters>  
     <filterTables>  
       <table name="routingTable1">  
         <filters>  
           <add filterName="AddAction" endpointName="Addition" />  
           <add filterName="SubtractAction" endpointName="Subtraction" />  
         </filters>  
       </table>  
     </filterTables>
</routing>  
```  
  
### <a name="filter-evaluation-priority"></a><span data-ttu-id="749a3-172">筛选器计算优先级</span><span class="sxs-lookup"><span data-stu-id="749a3-172">Filter Evaluation Priority</span></span>  

 <span data-ttu-id="749a3-173">默认情况下，将同时计算筛选器表中的所有条目，计算的消息将路由至与每个匹配的筛选器条目相关联的终结点。</span><span class="sxs-lookup"><span data-stu-id="749a3-173">By default, all entries in the filter table are evaluated simultaneously, and the message being evaluated is routed to the endpoint(s) associated with each matching filter entry.</span></span> <span data-ttu-id="749a3-174">如果多个筛选器的计算结果均为 `true`，并且消息是单向或双工消息，则会将此消息多播到所有匹配筛选器所对应的终结点。</span><span class="sxs-lookup"><span data-stu-id="749a3-174">If multiple filters evaluate to `true`, and the message is one-way or duplex, the message is multicast to the endpoints for all matching filters.</span></span> <span data-ttu-id="749a3-175">由于只能向客户端返回一个答复，因此无法多播请求-答复消息。</span><span class="sxs-lookup"><span data-stu-id="749a3-175">Request-reply messages cannot be multicast because only one reply can be returned to the client.</span></span>  
  
 <span data-ttu-id="749a3-176">通过为各筛选器指定优先级别，可以实现更复杂的路由逻辑；路由服务将首先计算处于最高优先级别的所有筛选器。</span><span class="sxs-lookup"><span data-stu-id="749a3-176">More complex routing logic can be implemented by specifying priority levels for each filter; the Routing Service evaluates all filters at the highest priority level first.</span></span> <span data-ttu-id="749a3-177">如果某一消息与此级别的筛选器相匹配，则不会处理较低优先级的筛选器。</span><span class="sxs-lookup"><span data-stu-id="749a3-177">If a message matches a filter of this level, no filters of a lower priority are processed.</span></span> <span data-ttu-id="749a3-178">例如，将首先根据优先级为 2 的所有筛选器计算传入的单向消息。</span><span class="sxs-lookup"><span data-stu-id="749a3-178">For example, an incoming one-way message is first evaluated against all filters with a priority of 2.</span></span> <span data-ttu-id="749a3-179">该消息不与此优先级别的任何筛选器匹配，因此，接着将根据优先级为 1 的筛选器比较此消息。</span><span class="sxs-lookup"><span data-stu-id="749a3-179">The message does not match any filter at this priority level, so next the message is compared against filters with a priority of 1.</span></span> <span data-ttu-id="749a3-180">有两个优先级为 1 的筛选器与此消息匹配，并且由于该消息是单向消息，因此将被路由至两个目标终结点。</span><span class="sxs-lookup"><span data-stu-id="749a3-180">Two priority 1 filters match the message, and because it is a one-way message it is routed to both destination endpoints.</span></span>  <span data-ttu-id="749a3-181">由于已在优先级为 1 的筛选器中找到了匹配项，因此不会计算优先级为 0 的筛选器。</span><span class="sxs-lookup"><span data-stu-id="749a3-181">Because a match was found among the priority 1 filters, no filters of priority 0 are evaluated.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="749a3-182">如果未指定优先级，则使用默认优先级 0。</span><span class="sxs-lookup"><span data-stu-id="749a3-182">If no priority is specified, the default priority of 0 is used.</span></span>  
  
 <span data-ttu-id="749a3-183">下面的示例定义一个筛选器表，该筛选器表为其引用的筛选器指定优先级 2、1 和 0。</span><span class="sxs-lookup"><span data-stu-id="749a3-183">The following example defines a filter table that specifies priorities of 2, 1, and 0 for the filters referenced in the table.</span></span>  
  
```xml  
<filterTables>  
     <filterTable name="filterTable1">  
          <add filterName="XPathFilter" endpointName="roundingCalcEndpoint"
               priority="2"/>  
          <add filterName="EndpointNameFilter" endpointName="regularCalcEndpoint"
               priority="1"/>  
          <add filterName="PrefixAddressFilter" endpointName="roundingCalcEndpoint"
               priority="1"/>  
          <add filterName="MatchAllMessageFilter" endpointName="defaultCalcEndpoint"
               priority="0"/>  
     </filterTable>  
</filterTables>  
```  
  
 <span data-ttu-id="749a3-184">在上面的示例中，如果消息与 XPathFilter 匹配，则将该消息路由至 roundingCalcEndpoint，并且不会计算表中的任何其他筛选器，这是因为所有其他筛选器都具有较低的优先级。</span><span class="sxs-lookup"><span data-stu-id="749a3-184">In the preceding example, if a message matches the XPathFilter, it will be routed to the roundingCalcEndpoint and no further filters in the table will be evaluated because all other filters are of a lower priority.</span></span> <span data-ttu-id="749a3-185">但是，如果此消息与 XPathFilter 不匹配，则会根据下一较低优先级的所有筛选器（即 EndpointNameFilter 和 PrefixAddressFilter）计算此消息。</span><span class="sxs-lookup"><span data-stu-id="749a3-185">However, if the message does not match the XPathFilter it will then be evaluated against all filters of the next lower priority, EndpointNameFilter and PrefixAddressFilter.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="749a3-186">如有可能，请使用独占筛选器，而不是指定优先级，因为优先级计算可能会导致性能降级。</span><span class="sxs-lookup"><span data-stu-id="749a3-186">When possible, use exclusive filters instead of specifying a priority because priority evaluation can result in performance degradation.</span></span>  
  
### <a name="backup-lists"></a><span data-ttu-id="749a3-187">备份列表</span><span class="sxs-lookup"><span data-stu-id="749a3-187">Backup Lists</span></span>  

 <span data-ttu-id="749a3-188">筛选器表中的各个筛选器可以选择指定一个备份列表，即终结点的命名集合 (<xref:System.ServiceModel.Routing.Configuration.BackupEndpointCollection>)。</span><span class="sxs-lookup"><span data-stu-id="749a3-188">Each filter in the filter table can optionally specify a backup list, which is a named collection of endpoints (<xref:System.ServiceModel.Routing.Configuration.BackupEndpointCollection>).</span></span> <span data-ttu-id="749a3-189">该集合包含在向主终结点（在 <xref:System.ServiceModel.CommunicationException> 中指定）发送消息期间发生 <xref:System.ServiceModel.Routing.Configuration.FilterTableEntryElement.EndpointName%2A> 时，消息将传输到的终结点的有序列表。</span><span class="sxs-lookup"><span data-stu-id="749a3-189">This collection contains an ordered list of endpoints that the message will be transmitted to in the event of a <xref:System.ServiceModel.CommunicationException> when sending to the primary endpoint specified in <xref:System.ServiceModel.Routing.Configuration.FilterTableEntryElement.EndpointName%2A>.</span></span> <span data-ttu-id="749a3-190">下面的示例定义了一个名为 "backupServiceEndpoints" 的备份列表，其中包含两个终结点。</span><span class="sxs-lookup"><span data-stu-id="749a3-190">The following example defines a backup list named "backupServiceEndpoints" that contains two endpoints.</span></span>  
  
```xml  
<filterTables>  
     <filterTable name="filterTable1">  
          <add filterName="MatchAllFilter1" endpointName="Destination" backupList="backupEndpointList"/>  
     </filterTable>  
</filterTables>  
<backupLists>  
     <backupList name="backupEndpointList">  
          <add endpointName="backupServiceQueue" />  
          <add endpointName="alternateServiceQueue" />  
     </backupList>  
</backupLists>  
```  
  
 <span data-ttu-id="749a3-191">在前面的示例中，如果发送到主终结点 "Destination" 失败，则路由服务将尝试按列出的顺序发送到每个终结点，首先发送到 backupServiceQueue，然后在发送到 backupServiceQueue 失败时发送到 alternateServiceQueue。</span><span class="sxs-lookup"><span data-stu-id="749a3-191">In the preceding example, if a send to the primary endpoint "Destination" fails, the Routing Service will try sending to each endpoint in the sequence they are listed, first sending to backupServiceQueue and subsequently sending to alternateServiceQueue if the send to backupServiceQueue fails.</span></span> <span data-ttu-id="749a3-192">如果所有备份终结点均失败，则会返回错误。</span><span class="sxs-lookup"><span data-stu-id="749a3-192">If all backup endpoints fail, a fault is returned.</span></span>
