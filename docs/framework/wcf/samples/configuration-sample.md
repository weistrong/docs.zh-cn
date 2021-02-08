---
description: 了解详细信息：配置示例
title: 配置示例
ms.date: 03/30/2017
ms.assetid: 75515b4a-8d70-44c8-99e0-7423df41380e
ms.openlocfilehash: e11237fbc32b203c9b661288dbccab01745928d0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99778381"
---
# <a name="configuration-sample"></a><span data-ttu-id="24a91-103">配置示例</span><span class="sxs-lookup"><span data-stu-id="24a91-103">Configuration Sample</span></span>

<span data-ttu-id="24a91-104">此示例演示如何使用配置文件使服务成为可发现的服务。</span><span class="sxs-lookup"><span data-stu-id="24a91-104">This sample demonstrates the use of a configuration file to make a service discoverable.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="24a91-105">此示例将在配置中实现发现。</span><span class="sxs-lookup"><span data-stu-id="24a91-105">This sample implements discovery in configuration.</span></span> <span data-ttu-id="24a91-106">有关在代码中实现发现的示例，请参阅 " [基本](basic-sample.md)"。</span><span class="sxs-lookup"><span data-stu-id="24a91-106">For a sample that implements discovery in code, see [Basic](basic-sample.md).</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="24a91-107">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="24a91-107">The samples may already be installed on your computer.</span></span> <span data-ttu-id="24a91-108">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="24a91-108">Check for the following (default) directory before continuing.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples`  
>
> <span data-ttu-id="24a91-109">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="24a91-109">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="24a91-110">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="24a91-110">This sample is located in the following directory.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Discovery\Configuration`  
  
## <a name="service-configuration"></a><span data-ttu-id="24a91-111">服务配置</span><span class="sxs-lookup"><span data-stu-id="24a91-111">Service Configuration</span></span>  

 <span data-ttu-id="24a91-112">此示例中的配置文件演示两个功能：</span><span class="sxs-lookup"><span data-stu-id="24a91-112">The configuration file in this sample demonstrates two features:</span></span>  
  
- <span data-ttu-id="24a91-113">使服务在标准 <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint> 上成为可发现的服务。</span><span class="sxs-lookup"><span data-stu-id="24a91-113">Making the service discoverable over a standard <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint>.</span></span>  
  
- <span data-ttu-id="24a91-114">调整该服务的应用程序终结点的发现相关信息，并在标准终结点上调整某些与发现相关的设置。</span><span class="sxs-lookup"><span data-stu-id="24a91-114">Adjusting discovery-related information for the service’s application endpoint and adjusting some of the discovery-related settings on the standard endpoint.</span></span>  
  
 <span data-ttu-id="24a91-115">若要启用发现，必须在该服务的应用程序配置文件中进行几个更改：</span><span class="sxs-lookup"><span data-stu-id="24a91-115">To enable discovery, a few changes must be made in the application configuration file for the service:</span></span>  
  
- <span data-ttu-id="24a91-116">必须将一个发现终结点添加到 `<service>` 元素。</span><span class="sxs-lookup"><span data-stu-id="24a91-116">A discovery endpoint must be added to the `<service>` element.</span></span> <span data-ttu-id="24a91-117">这是一个标准 <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint> 终结点，</span><span class="sxs-lookup"><span data-stu-id="24a91-117">This is a standard <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint> endpoint.</span></span> <span data-ttu-id="24a91-118">这是一个运行时与发现服务相关联的系统终结点。</span><span class="sxs-lookup"><span data-stu-id="24a91-118">This is a system endpoint that the runtime associates with the discovery service.</span></span> <span data-ttu-id="24a91-119">发现服务侦听此终结点上的消息。</span><span class="sxs-lookup"><span data-stu-id="24a91-119">The discovery service listens for messages on this endpoint.</span></span>  
  
- <span data-ttu-id="24a91-120">`<serviceDiscovery>` 行为将添加到 `<serviceBehaviors>` 节。</span><span class="sxs-lookup"><span data-stu-id="24a91-120">A `<serviceDiscovery>` behavior is added to the `<serviceBehaviors>` section.</span></span> <span data-ttu-id="24a91-121">这使该服务在运行时可被发现，并使用前面提到的发现终结点来侦听发现 `Probe` 和 `Resolve` 消息。</span><span class="sxs-lookup"><span data-stu-id="24a91-121">This enables the service to be discovered at runtime and uses the discovery endpoint mentioned previously to listen for discovery `Probe` and `Resolve` messages.</span></span> <span data-ttu-id="24a91-122">通过这两个添加操作，可在指定的发现终结点处发现服务。</span><span class="sxs-lookup"><span data-stu-id="24a91-122">With these two additions, the service is discoverable at the discovery endpoint specified.</span></span>  
  
 <span data-ttu-id="24a91-123">下面的配置代码段演示定义了一个应用程序终结点和一个发现终结点的服务：</span><span class="sxs-lookup"><span data-stu-id="24a91-123">The following config snippet shows a service with an application endpoint and a discovery endpoint defined:</span></span>  
  
```xml
<services>  
        <service name="Microsoft.Samples.Discovery.CalculatorService"  
                 behaviorConfiguration="calculatorServiceBehavior">  
          <endpoint address=""  
                    binding="wsHttpBinding"  
                    contract="Microsoft.Samples.Discovery.ICalculatorService"  
                    behaviorConfiguration="endpointBehaviorConfiguration" />  
          <endpoint name="udpDiscovery"
                    kind="udpDiscoveryEndpoint"
                endpointConfiguration="adhocDiscoveryEndpointConfiguration"/>        </service>  
      </services>  
```  
  
 <span data-ttu-id="24a91-124">若要利用公告，需要添加公告终结点。</span><span class="sxs-lookup"><span data-stu-id="24a91-124">To take advantage of announcements, you will need to add an announcement endpoint.</span></span> <span data-ttu-id="24a91-125">为此，请修改配置文件，如下面的代码所示。</span><span class="sxs-lookup"><span data-stu-id="24a91-125">To do this, modify the configuration file as shown in the following code.</span></span>  
  
```xml  
<serviceDiscovery>  
            <announcementEndpoints>  
              <endpoint kind="udpAnnouncementEndpoint"/>  
            </announcementEndpoints>  
          </serviceDiscovery>  
```  
  
 <span data-ttu-id="24a91-126">向发现服务行为添加公告终结点会为服务创建默认公告客户端。</span><span class="sxs-lookup"><span data-stu-id="24a91-126">Adding an announcement endpoint to the discovery service behavior creates a default announcement client for the service.</span></span> <span data-ttu-id="24a91-127">这可保证在打开和关闭服务时，服务会分别发送联机和脱机公告。</span><span class="sxs-lookup"><span data-stu-id="24a91-127">This guarantees that the service will send an online and offline announcement when the service is opened and closed respectively.</span></span>  
  
 <span data-ttu-id="24a91-128">通过修改其他行为，此配置文件还可以执行这些简单步骤之外的步骤。</span><span class="sxs-lookup"><span data-stu-id="24a91-128">This configuration file goes beyond just those simple steps by modifying additional behaviors.</span></span> <span data-ttu-id="24a91-129">通过使用特定终结点，可以控制与发现相关的信息。</span><span class="sxs-lookup"><span data-stu-id="24a91-129">It is possible to control discovery-related information by using specific endpoints.</span></span> <span data-ttu-id="24a91-130">也就是说，用户可以控制一个终结点是否可被发现，还可以使用 <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior.Scopes%2A> 和自定义 XML 元数据来标记该终结点。</span><span class="sxs-lookup"><span data-stu-id="24a91-130">That is, a user can control whether an endpoint can be discovered and the user can also mark that endpoint with <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior.Scopes%2A> and custom XML metadata.</span></span> <span data-ttu-id="24a91-131">为此，用户必须将一个 `behaviorConfiguration` 属性添加到应用程序终结点。</span><span class="sxs-lookup"><span data-stu-id="24a91-131">To do this, the user must add a `behaviorConfiguration` property to the application endpoint.</span></span> <span data-ttu-id="24a91-132">在这种情况下，以下属性将添加到该应用程序终结点。</span><span class="sxs-lookup"><span data-stu-id="24a91-132">In this case, the following property is added to the application endpoint.</span></span>  
  
`behaviorConfiguration="endpointBehaviorConfiguration"`  
  
 <span data-ttu-id="24a91-133">现在，通过该行为配置元素，可以控制与发现相关的特性。</span><span class="sxs-lookup"><span data-stu-id="24a91-133">Now, through the behavior configuration element, you can control discovery-related attributes.</span></span> <span data-ttu-id="24a91-134">在这种情况下，两个范围将添加到该应用程序终结点。</span><span class="sxs-lookup"><span data-stu-id="24a91-134">In this case, two scopes are added to the application endpoint.</span></span>  
  
```xml  
<endpointBehaviors>  
          <behavior name="endpointBehaviorConfiguration">  
            <endpointDiscovery>  
              <scopes>  
                <add scope="http://www.example.com/calculator"/>  
                <add scope="ldap:///ou=engineering,o=examplecom,c=us"/>  
              </scopes>  
            </endpointDiscovery>  
  
          </behavior>
        </endpointBehaviors>  
```  
  
 <span data-ttu-id="24a91-135">有关范围的详细信息，请参阅 [发现 Find 和 s](../feature-details/discovery-find-and-findcriteria.md)。</span><span class="sxs-lookup"><span data-stu-id="24a91-135">For more information about scopes, see [Discovery Find and FindCriteria](../feature-details/discovery-find-and-findcriteria.md).</span></span>  
  
 <span data-ttu-id="24a91-136">还可以控制发现终结点的特定详细信息。</span><span class="sxs-lookup"><span data-stu-id="24a91-136">You can also control specific details of the discovery endpoint.</span></span> <span data-ttu-id="24a91-137">这是通过 <xref:System.ServiceModel.Configuration.StandardEndpointsSection> 完成的。</span><span class="sxs-lookup"><span data-stu-id="24a91-137">This is done through the <xref:System.ServiceModel.Configuration.StandardEndpointsSection>.</span></span> <span data-ttu-id="24a91-138">在此示例中，将修改所用协议的版本并添加一个 `maxResponseDelay` 特性，如以下代码示例所示。</span><span class="sxs-lookup"><span data-stu-id="24a91-138">In this sample, the version of the protocol used is modified as well as adding a `maxResponseDelay` attribute as shown in the following code example.</span></span>  
  
```xml  
<standardEndpoints>  
   <udpDiscoveryEndpoint>  
      <standardEndpoint name="adhocDiscoveryEndpointConfiguration" discoveryVersion="WSDiscovery11" maxResponseDelay="00:00:00.600" />
   </udpDiscoveryEndpoint>  
</standardEndpoints>  
```  
  
 <span data-ttu-id="24a91-139">下面是此示例中使用的完整配置文件：</span><span class="sxs-lookup"><span data-stu-id="24a91-139">The following is the complete configuration file used in this example:</span></span>  
  
```xml  
<configuration>  
    <system.serviceModel>  
  
      <services>  
        <service name="Microsoft.Samples.Discovery.CalculatorService"  
                 behaviorConfiguration="calculatorServiceBehavior">  
          <endpoint address=""  
                    binding="wsHttpBinding"  
                    contract="Microsoft.Samples.Discovery.ICalculatorService"  
                    behaviorConfiguration="endpointBehaviorConfiguration" />  
         <!-- Define the discovery endpoint -->
<endpoint name="udpDiscovery" kind="udpDiscoveryEndpoint" endpointConfiguration="adhocDiscoveryEndpointConfiguration"/>        </service>  
      </services>  
  
      <behaviors>  
  
        <serviceBehaviors>  
          <behavior name="calculatorServiceBehavior">  
  
            <!-- Add an announcement endpoint -->  
            <serviceDiscovery>  
              <announcementEndpoints>  
                <endpoint kind="udpAnnouncementEndpoint"/>  
              </announcementEndpoints>  
            </serviceDiscovery>  
          </behavior>  
        </serviceBehaviors>  
  
        <endpointBehaviors>  
          <behavior name="endpointBehaviorConfiguration">  
            <!-- Add scopes used to identify the service -->  
            <endpointDiscovery>  
              <scopes>  
                <add scope="http://www.example.com/calculator"/>  
                <add scope="ldap:///ou=engineering,o=examplecom,c=us"/>  
              </scopes>  
            </endpointDiscovery>  
  
          </behavior>
        </endpointBehaviors>  
  
      </behaviors>  
  
      <standardEndpoints>  
        <udpDiscoveryEndpoint>  
         <!-- Configure the UDP discovery endpoint -->  
          <standardEndpoint name="adhocDiscoveryEndpointConfiguration" discoveryVersion="WSDiscovery11" maxResponseDelay="00:00:00.600" />
        </udpDiscoveryEndpoint>  
      </standardEndpoints>  
  
    </system.serviceModel>  
</configuration>  
```  
  
## <a name="client-configuration"></a><span data-ttu-id="24a91-140">客户端配置</span><span class="sxs-lookup"><span data-stu-id="24a91-140">Client Configuration</span></span>  

 <span data-ttu-id="24a91-141">在客户端的应用程序配置文件中，一个类型为 `standardEndpoint` 的 `dynamicEndpoint` 用于使用发现，如下面的配置代码段所示。</span><span class="sxs-lookup"><span data-stu-id="24a91-141">In the application configuration file for the client, a `standardEndpoint` of type `dynamicEndpoint` is used to utilize discovery as shown in the following config snippet.</span></span>  
  
```xml  
<client>  
   <!--  Create an endpoint, make kind="dynamicEndpoint" and use the endpointConfiguration to change settings of DynamicEndpoint -->  
   <endpoint name="calculatorEndpoint"  
             binding="wsHttpBinding"  
             contract="ICalculatorService"  
             kind ="dynamicEndpoint"  
             endpointConfiguration="dynamicEndpointConfiguration">  
   </endpoint>  
</client>  
```  
  
 <span data-ttu-id="24a91-142">客户端使用 `dynamicEndpoint` 时，运行时将自动执行发现。</span><span class="sxs-lookup"><span data-stu-id="24a91-142">When a client is using a `dynamicEndpoint`, the runtime performs discovery automatically.</span></span> <span data-ttu-id="24a91-143">会发现过程中会使用各种设置，如 `discoveryClientSettings` 节（该节指定要使用的发现终结点类型）中定义的设置：</span><span class="sxs-lookup"><span data-stu-id="24a91-143">Various settings are used during discovery, such as those defined in the  `discoveryClientSettings` section, which specifies the type of discovery endpoint to use:</span></span>  
  
```xml  
<endpoint kind="udpDiscoveryEndpoint" endpointConfiguration="adhocDiscoveryEndpointConfiguration" />  
```  
  
 <span data-ttu-id="24a91-144">用于搜索服务的查找条件：</span><span class="sxs-lookup"><span data-stu-id="24a91-144">The find criteria used to search for services:</span></span>  
  
```xml  
<!-- Add Scopes, ScopeMatchBy, Extensions and termination criteria in FindCriteria -->  
<findCriteria scopeMatchBy="http://schemas.microsoft.com/ws/2008/06/discovery/rfc" duration="00:00:10" maxResults="1">  
   <scopes>  
      <add scope="http://www.microsoft.com/building42/floor1"/>  
   </scopes>  
   <!-- These extensions are sent from the client to the service as part of the probe message -->  
   <extensions>  
      <CustomMetadata>This is custom metadata that is sent to the service along with the client's find request.</CustomMetadata>  
   </extensions>  
</findCriteria>  
```  
  
 <span data-ttu-id="24a91-145">此示例将此功能加以扩展，并修改客户端使用的 <xref:System.ServiceModel.Discovery.FindCriteria> 以及用于发现的标准 `updDiscoveryEndpoint` 的某些属性。</span><span class="sxs-lookup"><span data-stu-id="24a91-145">This sample extends this feature and modifies the <xref:System.ServiceModel.Discovery.FindCriteria> used by the client, as well as some properties of the standard `updDiscoveryEndpoint` used for discovery.</span></span> <span data-ttu-id="24a91-146">将修改 <xref:System.ServiceModel.Discovery.FindCriteria> 以使用一个范围和一个特定 `scopeMatchBy` 算法以及自定义终止条件。</span><span class="sxs-lookup"><span data-stu-id="24a91-146">The <xref:System.ServiceModel.Discovery.FindCriteria> are modified to use a scope and a specific `scopeMatchBy` algorithm, as well as custom termination criteria.</span></span> <span data-ttu-id="24a91-147">而且，该示例还演示客户端如何使用 `Probe` 消息来发送 XML 元素。</span><span class="sxs-lookup"><span data-stu-id="24a91-147">Furthermore, the sample also shows how a client can send XML elements using `Probe` messages.</span></span> <span data-ttu-id="24a91-148">最后，对 <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint> 进行了一些更改，如所用协议的版本以及 UDP 特定设置，如以下配置文件所示。</span><span class="sxs-lookup"><span data-stu-id="24a91-148">Lastly, some changes are made to the <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint>, such as the version of the protocol used and UDP-specific settings as shown in the following configuration file.</span></span>  
  
```xml  
<udpDiscoveryEndpoint>
        <!-- Specify the discovery protocol version and UDP transport settings. -->
        <standardEndpoint name="adhocDiscoveryEndpointConfiguration" discoveryVersion="WSDiscovery11">  
          <transportSettings duplicateMessageHistoryLength="2048"  
                             maxPendingMessageCount="5"  
                             maxReceivedMessageSize="8192"  
                             maxBufferPoolSize="262144"/>  
        </standardEndpoint>
      </udpDiscoveryEndpoint>  
```  
  
 <span data-ttu-id="24a91-149">下面是示例中使用的完整客户端配置。</span><span class="sxs-lookup"><span data-stu-id="24a91-149">The following is the complete client configuration used in the sample.</span></span>  
  
```xml  
<configuration>  
  <system.serviceModel>  
  
    <client>  
      <!--  Create an endpoint, make kind="dynamicEndpoint" and use the endpointConfiguration to change settings of DynamicEndpoint -->  
      <endpoint name="calculatorEndpoint"  
                binding="wsHttpBinding"  
                contract="ICalculatorService"  
                kind ="dynamicEndpoint"  
                endpointConfiguration="dynamicEndpointConfiguration">  
      </endpoint>  
    </client>  
  
    <standardEndpoints>  
  
      <dynamicEndpoint>
        <standardEndpoint name="dynamicEndpointConfiguration">  
          <discoveryClientSettings>  
            <!-- Controls where the discovery happens. In this case, Probe message is sent over UdpDiscoveryEndpoint. -->  
            <endpoint kind="udpDiscoveryEndpoint" endpointConfiguration="adhocDiscoveryEndpointConfiguration" />  
  
            <!-- Add Scopes, ScopeMatchBy, Extensions and termination criteria in FindCriteria -->  
            <findCriteria scopeMatchBy="http://schemas.microsoft.com/ws/2008/06/discovery/rfc" duration="00:00:10" maxResults="1">  
              <scopes>  
                <add scope="http://www.microsoft.com/building42/floor1"/>  
              </scopes>  
              <!-- These extensions are sent from the client to the service as part of the probe message -->  
              <extensions>  
                <CustomMetadata>This is custom metadata that is sent to the service along with the client's find request.</CustomMetadata>  
              </extensions>  
            </findCriteria>  
          </discoveryClientSettings>  
        </standardEndpoint>
      </dynamicEndpoint>  
  
      <udpDiscoveryEndpoint>
        <!-- Specify the discovery protocol version and UDP transport settings. -->
        <standardEndpoint name="adhocDiscoveryEndpointConfiguration" discoveryVersion="WSDiscovery11">  
          <transportSettings duplicateMessageHistoryLength="2048"  
                             maxPendingMessageCount="5"  
                             maxReceivedMessageSize="8192"  
                             maxBufferPoolSize="262144"/>  
        </standardEndpoint>
      </udpDiscoveryEndpoint>  
  
    </standardEndpoints>  
  
  </system.serviceModel>
</configuration>
```  
  
#### <a name="to-use-this-sample"></a><span data-ttu-id="24a91-150">使用此示例</span><span class="sxs-lookup"><span data-stu-id="24a91-150">To use this sample</span></span>  
  
1. <span data-ttu-id="24a91-151">此示例使用 HTTP 终结点，若要运行此示例，必须添加正确的 URL ACL。</span><span class="sxs-lookup"><span data-stu-id="24a91-151">This sample uses HTTP endpoints and to run this sample, proper URL ACLs must be added.</span></span> <span data-ttu-id="24a91-152">有关详细信息，请参阅 [配置 HTTP 和 HTTPS](../feature-details/configuring-http-and-https.md)。</span><span class="sxs-lookup"><span data-stu-id="24a91-152">For more information, see [Configuring HTTP and HTTPS](../feature-details/configuring-http-and-https.md).</span></span> <span data-ttu-id="24a91-153">使用提升的特权执行下面的命令应添加相应的 ACL。</span><span class="sxs-lookup"><span data-stu-id="24a91-153">Executing the following command at an elevated privilege should add the appropriate ACLs.</span></span> <span data-ttu-id="24a91-154">如果该命令无效，则可能需要使用你的域和用户名替换以下自变量。</span><span class="sxs-lookup"><span data-stu-id="24a91-154">You may want to substitute your Domain and Username for the following arguments if the command does not work as is.</span></span> `netsh http add urlacl url=http://+:8000/ user=%DOMAIN%\%UserName%`  
  
2. <span data-ttu-id="24a91-155">生成解决方案。</span><span class="sxs-lookup"><span data-stu-id="24a91-155">Build the solution.</span></span>  
  
3. <span data-ttu-id="24a91-156">从生成目录运行服务可执行文件。</span><span class="sxs-lookup"><span data-stu-id="24a91-156">Run the service executable from the build directory.</span></span>  
  
4. <span data-ttu-id="24a91-157">运行客户端可执行文件。</span><span class="sxs-lookup"><span data-stu-id="24a91-157">Run the client executable.</span></span> <span data-ttu-id="24a91-158">请注意，客户端能够查找该服务。</span><span class="sxs-lookup"><span data-stu-id="24a91-158">Note that the client is able to locate the service.</span></span>  
