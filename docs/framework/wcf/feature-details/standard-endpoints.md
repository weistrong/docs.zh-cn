---
description: 了解更多：标准终结点
title: 标准终结点
ms.date: 03/30/2017
ms.assetid: 3fcb4225-addc-44f2-935d-30e4943a8812
ms.openlocfilehash: 5879bab5dff4dee8ac574bad1c4452a60cf7c323
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99793436"
---
# <a name="standard-endpoints"></a><span data-ttu-id="8cc10-103">标准终结点</span><span class="sxs-lookup"><span data-stu-id="8cc10-103">Standard Endpoints</span></span>

<span data-ttu-id="8cc10-104">通过指定地址、绑定和协定来定义终结点。</span><span class="sxs-lookup"><span data-stu-id="8cc10-104">Endpoints are defined by specifying an address, a binding, and a contract.</span></span> <span data-ttu-id="8cc10-105">终结点上可以设置的其他参数包括行为配置、标头和侦听 URI。</span><span class="sxs-lookup"><span data-stu-id="8cc10-105">Other parameters that may be set on an endpoint include behavior configuration, headers, and listen URIs.</span></span>  <span data-ttu-id="8cc10-106">对于特定类型的终结点，这些值不会更改。</span><span class="sxs-lookup"><span data-stu-id="8cc10-106">For certain types of endpoints these values do not change.</span></span> <span data-ttu-id="8cc10-107">例如，元数据交换终结点始终使用 <xref:System.ServiceModel.Description.IMetadataExchange> 协定，</span><span class="sxs-lookup"><span data-stu-id="8cc10-107">For example, metadata exchange endpoints always use the <xref:System.ServiceModel.Description.IMetadataExchange> contract.</span></span> <span data-ttu-id="8cc10-108">其他终结点（如 <xref:System.ServiceModel.Description.WebHttpEndpoint>）始终需要指定的终结点行为。</span><span class="sxs-lookup"><span data-stu-id="8cc10-108">Other endpoints, such as <xref:System.ServiceModel.Description.WebHttpEndpoint> always require a specified endpoint behavior.</span></span> <span data-ttu-id="8cc10-109">通过为常用终结点属性设置默认值可以提高终结点的可用性。</span><span class="sxs-lookup"><span data-stu-id="8cc10-109">The usability of an endpoint can be improved by having endpoints with default values for commonly used endpoint properties.</span></span> <span data-ttu-id="8cc10-110">开发人员可以通过标准终结点定义具有默认值的终结点，或者定义一个或多个终结点属性不会更改的终结点。</span><span class="sxs-lookup"><span data-stu-id="8cc10-110">Standard endpoints enable a developer to define an endpoint that has default values or where one or more endpoint’s properties does not change.</span></span>  <span data-ttu-id="8cc10-111">这些终结点的优点是，可以使用此类终结点而无需指定静态性质的信息。</span><span class="sxs-lookup"><span data-stu-id="8cc10-111">These endpoints allow you to use such an endpoint without having to specify information of a static nature.</span></span> <span data-ttu-id="8cc10-112">标准终结点可供基础结构终结点和应用程序终结点使用。</span><span class="sxs-lookup"><span data-stu-id="8cc10-112">Standard endpoints can be used for infrastructure and application endpoints.</span></span>  
  
## <a name="infrastructure-endpoints"></a><span data-ttu-id="8cc10-113">基础结构终结点</span><span class="sxs-lookup"><span data-stu-id="8cc10-113">Infrastructure Endpoints</span></span>  

 <span data-ttu-id="8cc10-114">服务可能会公开这样的终结点：其中部分属性未由服务作者显式实现。</span><span class="sxs-lookup"><span data-stu-id="8cc10-114">A service may expose endpoints with some of the properties not explicitly implemented by the service author.</span></span> <span data-ttu-id="8cc10-115">例如，元数据交换终结点公开 <xref:System.ServiceModel.Description.IMetadataExchange> 协定，但服务作者并不实现该接口，而是由 WCF 实现。</span><span class="sxs-lookup"><span data-stu-id="8cc10-115">For example, the metadata exchange endpoint exposes the <xref:System.ServiceModel.Description.IMetadataExchange> contract but as a service author you do not implement that interface, it is implemented by WCF.</span></span> <span data-ttu-id="8cc10-116">此类基础结构终结点的一个或多个终结点属性具有默认值，其中部分属性可能无法更改。</span><span class="sxs-lookup"><span data-stu-id="8cc10-116">Such infrastructure endpoints have default values for one or more endpoint properties, some of which may be unalterable.</span></span> <span data-ttu-id="8cc10-117">元数据交换终结点的 <xref:System.ServiceModel.Description.ServiceEndpoint.Contract%2A> 属性必须为 <xref:System.ServiceModel.Description.IMetadataExchange>，而其他属性（如绑定）可由开发人员提供。</span><span class="sxs-lookup"><span data-stu-id="8cc10-117">The <xref:System.ServiceModel.Description.ServiceEndpoint.Contract%2A> property of the metadata exchange endpoint must be <xref:System.ServiceModel.Description.IMetadataExchange>, while other properties like binding can be supplied by the developer.</span></span> <span data-ttu-id="8cc10-118">通过将 <xref:System.ServiceModel.Description.ServiceEndpoint.IsSystemEndpoint%2A> 属性设置为 `true` 来标识基础结构终结点。</span><span class="sxs-lookup"><span data-stu-id="8cc10-118">Infrastructure endpoints are identified by setting the <xref:System.ServiceModel.Description.ServiceEndpoint.IsSystemEndpoint%2A> property to `true`.</span></span>  
  
## <a name="application-endpoints"></a><span data-ttu-id="8cc10-119">应用程序终结点</span><span class="sxs-lookup"><span data-stu-id="8cc10-119">Application Endpoints</span></span>  

 <span data-ttu-id="8cc10-120">应用程序开发人员可以定义自己的标准终结点，为地址、绑定或协定指定默认值。</span><span class="sxs-lookup"><span data-stu-id="8cc10-120">Application developers can define their own standard endpoints which specify default values for the address, binding, or contract.</span></span> <span data-ttu-id="8cc10-121">可以从 <xref:System.ServiceModel.Description.ServiceEndpoint> 派生类并设置相应的终结点属性来定义标准终结点。</span><span class="sxs-lookup"><span data-stu-id="8cc10-121">You define a standard endpoint by deriving a class from <xref:System.ServiceModel.Description.ServiceEndpoint> and setting the appropriate endpoint properties.</span></span> <span data-ttu-id="8cc10-122">可以为能够更改的属性提供默认值。</span><span class="sxs-lookup"><span data-stu-id="8cc10-122">You can provide default values for properties that can be changed.</span></span> <span data-ttu-id="8cc10-123">其他一些属性将具有无法更改的静态值。</span><span class="sxs-lookup"><span data-stu-id="8cc10-123">Some other properties will have static values that cannot change.</span></span> <span data-ttu-id="8cc10-124">下面的示例演示如何实现标准终结点。</span><span class="sxs-lookup"><span data-stu-id="8cc10-124">The following example shows how to implement a standard endpoint.</span></span>  
  
```csharp
public class CustomEndpoint : ServiceEndpoint
{
    public CustomEndpoint()
        : this(string.Empty)
    { }  

    public CustomEndpoint(string address)
        : this(address, ContractDescription.GetContract(typeof(ICalculator)))
    { }  

    // Create the custom endpoint with a fixed binding
    public CustomEndpoint(string address, ContractDescription contract)
        : base(contract)
    {
        this.Binding = new BasicHttpBinding();
        this.IsSystemEndpoint = false;
    }

    // Definition of the additional property of this endpoint
    public bool Property { get; set; }
}
```
  
 <span data-ttu-id="8cc10-125">若要在配置文件中使用用户定义的自定义终结点，你必须从派生一个类 <xref:System.ServiceModel.Configuration.StandardEndpointElement> ，从派生一个类， <xref:System.ServiceModel.Configuration.StandardEndpointCollectionElement%602> 并在 app.config 或 machine.config 的 extensions 节中注册新的标准终结点。 <xref:System.ServiceModel.Configuration.StandardEndpointElement> 为标准终结点提供配置支持，如以下示例中所示。</span><span class="sxs-lookup"><span data-stu-id="8cc10-125">To use a user-defined custom endpoint in a configuration file you must derive a class from <xref:System.ServiceModel.Configuration.StandardEndpointElement>, derive a class from <xref:System.ServiceModel.Configuration.StandardEndpointCollectionElement%602>, and register the new standard endpoint in the extensions section in app.config or machine.config.  The <xref:System.ServiceModel.Configuration.StandardEndpointElement> provides configuration support for the standard endpoint, as shown in the following example.</span></span>  
  
```csharp
public class CustomEndpointElement : StandardEndpointElement
{
    // Definition of the additional property for the standard endpoint element
    public bool Property
    {
        get { return (bool)base["property"]; }
        set { base["property"] = value; }
    }

    // The additional property needs to be added to the properties of the standard endpoint element
    protected override ConfigurationPropertyCollection Properties
    {
        get
        {
            ConfigurationPropertyCollection properties = base.Properties;
            properties.Add(new ConfigurationProperty("property", typeof(bool), false, ConfigurationPropertyOptions.None));
            return properties;
        }
    }

    // Return the type of this standard endpoint
    protected override Type EndpointType
    {
        get { return typeof(CustomEndpoint); }
    }

    // Create the custom service endpoint
    protected override ServiceEndpoint CreateServiceEndpoint(ContractDescription contract)
    {
        return new CustomEndpoint();
    }

    // Read the value given to the property in config and save it
    protected override void OnApplyConfiguration(ServiceEndpoint endpoint, ServiceEndpointElement serviceEndpointElement)
    {
        CustomEndpoint customEndpoint = (CustomEndpoint)endpoint;
        customEndpoint.Property = this.Property;
    }

    // Read the value given to the property in config and save it
    protected override void OnApplyConfiguration(ServiceEndpoint endpoint, ChannelEndpointElement channelEndpointElement)
    {
        CustomEndpoint customEndpoint = (CustomEndpoint)endpoint;
        customEndpoint.Property = this.Property;
    }

    // No validation in this sample
    protected override void OnInitializeAndValidate(ServiceEndpointElement serviceEndpointElement)
    {
    }

    // No validation in this sample
    protected override void OnInitializeAndValidate(ChannelEndpointElement channelEndpointElement)
    {
    }
}
```  
  
 <span data-ttu-id="8cc10-126">为在 <xref:System.ServiceModel.Configuration.StandardEndpointCollectionElement%602> `standardEndpoints` 标准终结点的配置中 <> 部分下显示的集合提供支持类型。</span><span class="sxs-lookup"><span data-stu-id="8cc10-126">The <xref:System.ServiceModel.Configuration.StandardEndpointCollectionElement%602> provides the backing type for the collection that appears under the <`standardEndpoints`> section in the configuration for the standard endpoint.</span></span>  <span data-ttu-id="8cc10-127">下面的示例演示如何实现此类。</span><span class="sxs-lookup"><span data-stu-id="8cc10-127">The following example shows how to implement this class.</span></span>  
  
```csharp
public class CustomEndpointCollectionElement : StandardEndpointCollectionElement<CustomEndpoint, CustomEndpointElement>
{
    // ...
}
```

<span data-ttu-id="8cc10-128">下面的示例演示如何在 extensions 节中注册标准终结点。</span><span class="sxs-lookup"><span data-stu-id="8cc10-128">The following example shows how to register a standard endpoint in the extensions section.</span></span>

```xml  
<extensions>  
      <standardEndpointExtensions>  
        <add  
          name="customStandardEndpoint"  
          type="CustomEndpointCollectionElement, Example.dll,  
                Version=1.0.0.0, Culture=neutral, PublicKeyToken=ffffffffffffffff"/>  
      </standardEndpointExtensions>
</extensions>  
```  
  
## <a name="configuring-a-standard-endpoint"></a><span data-ttu-id="8cc10-129">配置标准终结点</span><span class="sxs-lookup"><span data-stu-id="8cc10-129">Configuring a Standard Endpoint</span></span>  

 <span data-ttu-id="8cc10-130">可以将标准终结点添加到代码或配置中。</span><span class="sxs-lookup"><span data-stu-id="8cc10-130">Standard endpoints can be added in code or in configuration.</span></span>  <span data-ttu-id="8cc10-131">若要将标准终结点添加到代码中，只需实例化相应的标准终结点类型，然后将标准终结点添加到服务主机，如下面的示例所示：</span><span class="sxs-lookup"><span data-stu-id="8cc10-131">To add a standard endpoint in code simply instantiate the appropriate standard endpoint type and add it to the service host as shown in the following example:</span></span>  
  
```csharp  
serviceHost.AddServiceEndpoint(new CustomEndpoint());  
```  
  
 <span data-ttu-id="8cc10-132">若要在配置中添加标准终结点，请将 <`endpoint`> 元素添加到 <`service`> 元素中，并将任何所需的配置设置添加到 <`standardEndpoints`> 元素中。</span><span class="sxs-lookup"><span data-stu-id="8cc10-132">To add a standard endpoint in configuration, add an <`endpoint`> element to the <`service`> element and any needed configuration settings in the <`standardEndpoints`> element.</span></span> <span data-ttu-id="8cc10-133">下面的示例演示如何添加 <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint>，它是随 [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)] 一起提供的标准终结点之一。</span><span class="sxs-lookup"><span data-stu-id="8cc10-133">The following example shows how to add a <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint>, one of the standard endpoints that ships with [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)].</span></span>  
  
```xml  
<services>  
  <service>  
    <endpoint isSystemEndpoint="true" kind="udpDiscoveryEndpoint" />  
  </service>  
</services>  
<standardEndpoints>
  <udpDiscoveryEndpoint>  
     <standardEndpoint multicastAddress="soap.udp://239.255.255.250:3702" />
  </udpDiscoveryEndpoint>
</standardEndpoints>
```  
  
 <span data-ttu-id="8cc10-134">使用 <> 元素中的 kind 特性指定标准终结点的类型 `endpoint` 。</span><span class="sxs-lookup"><span data-stu-id="8cc10-134">The type of standard endpoint is specified using the kind attribute in the <`endpoint`> element.</span></span> <span data-ttu-id="8cc10-135">终结点在 <> 元素中进行配置 `standardEndpoints` 。</span><span class="sxs-lookup"><span data-stu-id="8cc10-135">The endpoint is configured within the <`standardEndpoints`> element.</span></span> <span data-ttu-id="8cc10-136">在上例中，添加并配置了一个 <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint> 终结点。</span><span class="sxs-lookup"><span data-stu-id="8cc10-136">In the example above, a <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint> endpoint is added and configured.</span></span> <span data-ttu-id="8cc10-137"><`udpDiscoveryEndpoint`> 元素包含 `standardEndpoint` 设置的属性的 <> <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint.MulticastAddress%2A> <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint> 。</span><span class="sxs-lookup"><span data-stu-id="8cc10-137">The <`udpDiscoveryEndpoint`> element contains a <`standardEndpoint`> that sets the <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint.MulticastAddress%2A> property of the <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint>.</span></span>  
  
## <a name="standard-endpoints-shipped-with-the-net-framework"></a><span data-ttu-id="8cc10-138">随 .NET Framework 一起提供的标准终结点</span><span class="sxs-lookup"><span data-stu-id="8cc10-138">Standard Endpoints Shipped with the .NET Framework</span></span>  

 <span data-ttu-id="8cc10-139">下表列出了随 [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)] 一起提供的标准终结点。</span><span class="sxs-lookup"><span data-stu-id="8cc10-139">The following table lists the standard endpoints shipped with [!INCLUDE[netfx_current_long](../../../../includes/netfx-current-long-md.md)].</span></span>  
  
 `Mex Endpoint`  
 <span data-ttu-id="8cc10-140">用于公开服务元数据的标准终结点。</span><span class="sxs-lookup"><span data-stu-id="8cc10-140">A standard endpoint that is used to expose service metadata.</span></span>  
  
 <xref:System.ServiceModel.Discovery.AnnouncementEndpoint>  
 <span data-ttu-id="8cc10-141">由服务用于发送公告消息的标准终结点。</span><span class="sxs-lookup"><span data-stu-id="8cc10-141">A standard endpoint that is used by services to send announcement messages.</span></span>  
  
 <xref:System.ServiceModel.Discovery.DiscoveryEndpoint>  
 <span data-ttu-id="8cc10-142">由服务用于发送发现消息的标准终结点。</span><span class="sxs-lookup"><span data-stu-id="8cc10-142">A standard endpoint that is used by services to send discovery messages.</span></span>  
  
 <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint>  
 <span data-ttu-id="8cc10-143">通过 UDP 多播绑定为发现操作预配的标准终结点。</span><span class="sxs-lookup"><span data-stu-id="8cc10-143">A standard endpoint that is pre-configured for discovery operations over a UDP multicast binding.</span></span>  
  
 <xref:System.ServiceModel.Discovery.UdpAnnouncementEndpoint>  
 <span data-ttu-id="8cc10-144">由服务用于通过 UDP 绑定发送公告消息的标准终结点。</span><span class="sxs-lookup"><span data-stu-id="8cc10-144">A standard endpoint that is used by services to send announcement messages over a UDP binding.</span></span>  
  
 <xref:System.ServiceModel.Discovery.DynamicEndpoint>  
 <span data-ttu-id="8cc10-145">使用 WS-Discovery 在运行时动态查找终结点地址的标准终结点。</span><span class="sxs-lookup"><span data-stu-id="8cc10-145">A standard endpoint that uses WS-Discovery to find the endpoint address dynamically at runtime.</span></span>  
  
 <xref:System.ServiceModel.Description.ServiceMetadataEndpoint>  
 <span data-ttu-id="8cc10-146">用于元数据交换的标准终结点。</span><span class="sxs-lookup"><span data-stu-id="8cc10-146">A standard endpoint for metadata exchange.</span></span>  
  
 <xref:System.ServiceModel.Description.WebHttpEndpoint>  
 <span data-ttu-id="8cc10-147">带有自动添加 <xref:System.ServiceModel.WebHttpBinding> 行为的 <xref:System.ServiceModel.Description.WebHttpBehavior> 绑定的标准终结点。</span><span class="sxs-lookup"><span data-stu-id="8cc10-147">A standard endpoint with a <xref:System.ServiceModel.WebHttpBinding> binding that automatically adds the <xref:System.ServiceModel.Description.WebHttpBehavior> behavior</span></span>  
  
 <xref:System.ServiceModel.Description.WebScriptEndpoint>  
 <span data-ttu-id="8cc10-148">带有自动添加 <xref:System.ServiceModel.WebHttpBinding> 行为的 <xref:System.ServiceModel.Description.WebScriptEnablingBehavior> 绑定的标准终结点。</span><span class="sxs-lookup"><span data-stu-id="8cc10-148">A standard endpoint with a <xref:System.ServiceModel.WebHttpBinding> binding that automatically adds the <xref:System.ServiceModel.Description.WebScriptEnablingBehavior> behavior.</span></span>  
  
 <xref:System.ServiceModel.Description.WebServiceEndpoint>  
 <span data-ttu-id="8cc10-149">带有 <xref:System.ServiceModel.WebHttpBinding> 绑定的标准终结点。</span><span class="sxs-lookup"><span data-stu-id="8cc10-149">A standard endpoint with a <xref:System.ServiceModel.WebHttpBinding> binding.</span></span>  
  
 <xref:System.ServiceModel.Activities.WorkflowControlEndpoint>  
 <span data-ttu-id="8cc10-150">可用于对工作流实例调用控制操作的标准终结点。</span><span class="sxs-lookup"><span data-stu-id="8cc10-150">A standard endpoint that enables you to call control operations on workflow instances.</span></span>  
  
 <xref:System.ServiceModel.Activities.WorkflowHostingEndpoint>  
 <span data-ttu-id="8cc10-151">支持工作流创建和书签恢复的标准终结点。</span><span class="sxs-lookup"><span data-stu-id="8cc10-151">A standard endpoint that supports workflow creation and bookmark resumption.</span></span>
