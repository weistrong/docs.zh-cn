---
description: 了解详细信息：自定义服务主机
title: 自定义服务主机
ms.date: 03/30/2017
ms.assetid: fe16ff50-7156-4499-9c32-13d8a79dc100
ms.openlocfilehash: a18c3ec10eef5fc2c436a2fc2665ea73ed963384
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99752439"
---
# <a name="custom-service-host"></a><span data-ttu-id="087b4-103">自定义服务主机</span><span class="sxs-lookup"><span data-stu-id="087b4-103">Custom Service Host</span></span>

<span data-ttu-id="087b4-104">本示例演示如何使用 <xref:System.ServiceModel.ServiceHost> 类的自定义派生来改变服务的运行时行为。</span><span class="sxs-lookup"><span data-stu-id="087b4-104">This sample demonstrates how to use a custom derivative of the <xref:System.ServiceModel.ServiceHost> class to alter the run-time behavior of a service.</span></span> <span data-ttu-id="087b4-105">此方法为通过通用方式配置大量服务提供了一个可重用的替代方法。</span><span class="sxs-lookup"><span data-stu-id="087b4-105">This approach provides a reusable alternative to configuring a large number of services in a common way.</span></span> <span data-ttu-id="087b4-106">此示例还演示如何使用 <xref:System.ServiceModel.Activation.ServiceHostFactory> 类在 Internet 信息服务 (IIS) 或 Windows 进程激活服务 (WAS) 承载环境中使用自定义 ServiceHost。</span><span class="sxs-lookup"><span data-stu-id="087b4-106">The sample also demonstrates how to use the <xref:System.ServiceModel.Activation.ServiceHostFactory> class to use a custom ServiceHost in the Internet Information Services (IIS) or Windows Process Activation Service (WAS) hosting environment.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="087b4-107">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="087b4-107">The samples may already be installed on your machine.</span></span> <span data-ttu-id="087b4-108">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="087b4-108">Check for the following (default) directory before continuing.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples`  
>
> <span data-ttu-id="087b4-109">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="087b4-109">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="087b4-110">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="087b4-110">This sample is located in the following directory.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Extensibility\Hosting\CustomServiceHost`  
  
## <a name="about-the-scenario"></a><span data-ttu-id="087b4-111">关于方案</span><span class="sxs-lookup"><span data-stu-id="087b4-111">About the scenario</span></span>

 <span data-ttu-id="087b4-112">为了避免无意中泄漏可能敏感的服务元数据，Windows Communication Foundation 的默认配置 (WCF) 服务将禁用元数据发布。</span><span class="sxs-lookup"><span data-stu-id="087b4-112">To prevent unintentional disclosure of potentially sensitive service metadata, the default configuration for Windows Communication Foundation (WCF) services disables metadata publishing.</span></span> <span data-ttu-id="087b4-113">默认情况下，此行为是安全的，但也意味着你无法使用元数据导入工具 (例如 Svcutil.exe) 生成调用服务所需的客户端代码，除非在配置中显式启用服务的元数据发布行为。</span><span class="sxs-lookup"><span data-stu-id="087b4-113">This behavior is secure by default, but also means that you cannot use a metadata import tool (such as Svcutil.exe) to generate the client code required to call the service unless the service's metadata publishing behavior is explicitly enabled in configuration.</span></span>  
  
 <span data-ttu-id="087b4-114">对大量服务启用元数据发布需要向每个单独的服务添加相同的配置元素，这会生成实质上相同的大量配置信息。</span><span class="sxs-lookup"><span data-stu-id="087b4-114">Enabling metadata publishing for a large number of services involves adding the same configuration elements to each individual service, which results in a large amount of configuration information that is essentially the same.</span></span> <span data-ttu-id="087b4-115">作为分别配置每个服务的一种替代方法，可以编写命令性代码来启用一次元数据发布，然后在多个不同的服务中重复使用该代码。</span><span class="sxs-lookup"><span data-stu-id="087b4-115">As an alternative to configuring each service individually, it is possible to write the imperative code that enables metadata publishing once and then reuse that code across several different services.</span></span> <span data-ttu-id="087b4-116">这是通过创建一个从 <xref:System.ServiceModel.ServiceHost> 派生的新类并重写 `ApplyConfiguration`() 方法以便强制添加元数据发布行为来实现的。</span><span class="sxs-lookup"><span data-stu-id="087b4-116">This is accomplished by creating a new class that derives from <xref:System.ServiceModel.ServiceHost> and overrides the `ApplyConfiguration`() method to imperatively add the metadata publishing behavior.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="087b4-117">为清楚起见，本示例演示如何创建不安全的元数据发布终结点。</span><span class="sxs-lookup"><span data-stu-id="087b4-117">For clarity, this sample demonstrates how to create an unsecured metadata publishing endpoint.</span></span> <span data-ttu-id="087b4-118">此类终结点可能可供匿名未经身份验证的使用者使用，因此在部署此类终结点之前必须小心，以确保公开公开服务的元数据。</span><span class="sxs-lookup"><span data-stu-id="087b4-118">Such endpoints are potentially available to anonymous unauthenticated consumers and care must be taken before deploying such endpoints to ensure that publicly disclosing a service's metadata is appropriate.</span></span>  
  
## <a name="implementing-a-custom-servicehost"></a><span data-ttu-id="087b4-119">实现自定义 ServiceHost</span><span class="sxs-lookup"><span data-stu-id="087b4-119">Implementing a custom ServiceHost</span></span>

 <span data-ttu-id="087b4-120"><xref:System.ServiceModel.ServiceHost> 类公开多个有用的虚拟方法，继承者可以重写这些方法以改变服务的运行时行为。</span><span class="sxs-lookup"><span data-stu-id="087b4-120">The <xref:System.ServiceModel.ServiceHost> class exposes several useful virtual methods that inheritors can override to alter the run-time behavior of a service.</span></span> <span data-ttu-id="087b4-121">例如，`ApplyConfiguration`() 方法可从配置存储中读取服务配置信息并相应地改变主机的 <xref:System.ServiceModel.Description.ServiceDescription>。</span><span class="sxs-lookup"><span data-stu-id="087b4-121">For example, the `ApplyConfiguration`() method reads service configuration information from the configuration store and alters the host's <xref:System.ServiceModel.Description.ServiceDescription> accordingly.</span></span> <span data-ttu-id="087b4-122">默认实现读取应用程序配置文件中的配置。</span><span class="sxs-lookup"><span data-stu-id="087b4-122">The default implementation reads configuration from the application's configuration file.</span></span> <span data-ttu-id="087b4-123">自定义实现可以重写 `ApplyConfiguration`() 以便使用命令性代码进一步改变 <xref:System.ServiceModel.Description.ServiceDescription>，甚至完全替换默认配置存储。</span><span class="sxs-lookup"><span data-stu-id="087b4-123">Custom implementations can override `ApplyConfiguration`() to further alter the <xref:System.ServiceModel.Description.ServiceDescription> using imperative code or even replace the default configuration store entirely.</span></span> <span data-ttu-id="087b4-124">例如，从数据库而不是应用程序的配置文件中读取服务的终结点配置。</span><span class="sxs-lookup"><span data-stu-id="087b4-124">For example, to read a service's endpoint configuration from a database instead of the application's configuration file.</span></span>  
  
 <span data-ttu-id="087b4-125">在此示例中，我们想要生成一个自定义 ServiceHost，该 ServiceHost 添加了可启用元数据) 发布的 ServiceMetadataBehavior (，即使未在服务的配置文件中显式添加此行为也是如此。</span><span class="sxs-lookup"><span data-stu-id="087b4-125">In this sample, we want to build a custom ServiceHost that adds the ServiceMetadataBehavior (which enables metadata publishing) even if this behavior is not explicitly added in the service's configuration file.</span></span> <span data-ttu-id="087b4-126">若要实现此目的，请创建一个继承自的新类， <xref:System.ServiceModel.ServiceHost> 并覆盖 `ApplyConfiguration` ( # A1。</span><span class="sxs-lookup"><span data-stu-id="087b4-126">To accomplish this, create a new class that inherits from <xref:System.ServiceModel.ServiceHost> and overrides `ApplyConfiguration`().</span></span>  
  
```csharp
class SelfDescribingServiceHost : ServiceHost  
{  
    public SelfDescribingServiceHost(Type serviceType, params Uri[] baseAddresses)  
        : base(serviceType, baseAddresses) { }  
  
    //Overriding ApplyConfiguration() allows us to
    //alter the ServiceDescription prior to opening  
    //the service host.
    protected override void ApplyConfiguration()  
    {  
        //First, we call base.ApplyConfiguration()  
        //to read any configuration that was provided for  
        //the service we're hosting. After this call,  
        //this.Description describes the service  
        //as it was configured.  
        base.ApplyConfiguration();
  
        //(rest of implementation elided for clarity)  
    }  
}  
```  
  
 <span data-ttu-id="087b4-127">由于我们不想忽略应用程序配置文件中提供的任何配置，因此我们的第一件事 `ApplyConfiguration` 是 ( # A1 的替代将调用基实现。</span><span class="sxs-lookup"><span data-stu-id="087b4-127">Because we do not want to ignore any configuration that has been provided in the application's configuration file, the first thing our override of `ApplyConfiguration`() does is call the base implementation.</span></span> <span data-ttu-id="087b4-128">完成此方法后，我们可以使用下面的命令性代码向说明中强制添加 <xref:System.ServiceModel.Description.ServiceMetadataBehavior>。</span><span class="sxs-lookup"><span data-stu-id="087b4-128">Once this method completes, we can imperatively add the <xref:System.ServiceModel.Description.ServiceMetadataBehavior> to the description using the following imperative code.</span></span>  
  
```csharp
ServiceMetadataBehavior mexBehavior = this.Description.Behaviors.Find<ServiceMetadataBehavior>();  
if (mexBehavior == null)  
{  
    mexBehavior = new ServiceMetadataBehavior();  
    this.Description.Behaviors.Add(mexBehavior);  
}  
else  
{  
    //Metadata behavior has already been configured,
    //so we do not have any work to do.  
    return;  
}  
```  
  
 <span data-ttu-id="087b4-129">重写 `ApplyConfiguration`() 必须执行的最后一步是添加默认元数据终结点。</span><span class="sxs-lookup"><span data-stu-id="087b4-129">The last thing our `ApplyConfiguration`() override must do is add the default metadata endpoint.</span></span> <span data-ttu-id="087b4-130">按照约定，为服务主机的 BaseAddresses 集合中的每个 URI 创建一个元数据终结点。</span><span class="sxs-lookup"><span data-stu-id="087b4-130">By convention, one metadata endpoint is created for each URI in the service host's BaseAddresses collection.</span></span>  
  
```csharp
//Add a metadata endpoint at each base address  
//using the "/mex" addressing convention  
foreach (Uri baseAddress in this.BaseAddresses)  
{  
    if (baseAddress.Scheme == Uri.UriSchemeHttp)  
    {  
        mexBehavior.HttpGetEnabled = true;  
        this.AddServiceEndpoint(ServiceMetadataBehavior.MexContractName,  
                                MetadataExchangeBindings.CreateMexHttpBinding(),  
                                "mex");  
    }  
    else if (baseAddress.Scheme == Uri.UriSchemeHttps)  
    {  
        mexBehavior.HttpsGetEnabled = true;  
        this.AddServiceEndpoint(ServiceMetadataBehavior.MexContractName,  
                                MetadataExchangeBindings.CreateMexHttpsBinding(),  
                                "mex");  
    }  
    else if (baseAddress.Scheme == Uri.UriSchemeNetPipe)  
    {  
        this.AddServiceEndpoint(ServiceMetadataBehavior.MexContractName,  
                                MetadataExchangeBindings.CreateMexNamedPipeBinding(),  
                                "mex");  
    }  
    else if (baseAddress.Scheme == Uri.UriSchemeNetTcp)  
    {  
        this.AddServiceEndpoint(ServiceMetadataBehavior.MexContractName,  
                                MetadataExchangeBindings.CreateMexTcpBinding(),  
                                "mex");  
    }  
}  
```  
  
## <a name="using-a-custom-servicehost-in-self-host"></a><span data-ttu-id="087b4-131">在自承载方案中使用自定义 ServiceHost</span><span class="sxs-lookup"><span data-stu-id="087b4-131">Using a custom ServiceHost in self-host</span></span>  

 <span data-ttu-id="087b4-132">由于已完成了自定义 ServiceHost 实现，因此可以使用它通过在 `SelfDescribingServiceHost` 的实例内承载任何服务向该服务添加元数据发布行为。</span><span class="sxs-lookup"><span data-stu-id="087b4-132">Now that we have completed our custom ServiceHost implementation, we can use it to add metadata publishing behavior to any service by hosting that service inside of an instance of our `SelfDescribingServiceHost`.</span></span> <span data-ttu-id="087b4-133">下面的代码演示如何在自承载方案中使用自定义 ServiceHost。</span><span class="sxs-lookup"><span data-stu-id="087b4-133">The following code shows how to use it in the self-host scenario.</span></span>  
  
```csharp
SelfDescribingServiceHost host =
         new SelfDescribingServiceHost( typeof( Calculator ) );  
host.Open();  
```  
  
 <span data-ttu-id="087b4-134">自定义主机仍将从应用程序的配置文件中读取服务的终结点配置，就像我们使用了默认 <xref:System.ServiceModel.ServiceHost> 类来承载服务一样。</span><span class="sxs-lookup"><span data-stu-id="087b4-134">Our custom host still reads the service's endpoint configuration from the application's configuration file, as if we had used the default <xref:System.ServiceModel.ServiceHost> class to host the service.</span></span> <span data-ttu-id="087b4-135">但由于我们添加了在自定义主机内启用元数据发布的逻辑，因此不再需要在配置中显式启用元数据发布行为。</span><span class="sxs-lookup"><span data-stu-id="087b4-135">However, because we added the logic to enable metadata publishing inside of our custom host, we no longer must explicitly enable the metadata publishing behavior in configuration.</span></span> <span data-ttu-id="087b4-136">如果要生成的应用程序包含多个服务并需要在每个服务上启用元数据发布，而不想反复编写同样的配置元素，则使用此方法具有明显的优势。</span><span class="sxs-lookup"><span data-stu-id="087b4-136">This approach has a distinct advantage when you are building an application that contains several services and you want to enable metadata publishing on each of them without writing the same configuration elements over and over.</span></span>  
  
## <a name="using-a-custom-servicehost-in-iis-or-was"></a><span data-ttu-id="087b4-137">在 IIS 或 WAS 中使用自定义 ServiceHost</span><span class="sxs-lookup"><span data-stu-id="087b4-137">Using a custom ServiceHost in IIS or WAS</span></span>  

 <span data-ttu-id="087b4-138">在自承载方案中使用自定义服务主机非常简单，因为最终负责创建和打开服务主机实例的是应用程序代码。</span><span class="sxs-lookup"><span data-stu-id="087b4-138">Using a custom service host in self-host scenarios is straightforward, because it is your application code that is ultimately responsible for creating and opening the service host instance.</span></span> <span data-ttu-id="087b4-139">但在 IIS 或 WAS 宿主环境中，WCF 基础结构会动态地实例化服务的主机，以响应传入消息。</span><span class="sxs-lookup"><span data-stu-id="087b4-139">In the IIS or WAS hosting environment, however, the WCF infrastructure is dynamically instantiating your service's host in response to incoming messages.</span></span> <span data-ttu-id="087b4-140">自定义服务主机也可用于此承载环境，但它们需要一些 ServiceHostFactory 形式的附加代码。</span><span class="sxs-lookup"><span data-stu-id="087b4-140">Custom service hosts can also be used in this hosting environment, but they require some additional code in the form of a ServiceHostFactory.</span></span> <span data-ttu-id="087b4-141">下面的代码演示可返回自定义 <xref:System.ServiceModel.Activation.ServiceHostFactory> 的实例的 `SelfDescribingServiceHost` 的派生。</span><span class="sxs-lookup"><span data-stu-id="087b4-141">The following code shows a derivative of <xref:System.ServiceModel.Activation.ServiceHostFactory> that returns instances of our custom `SelfDescribingServiceHost`.</span></span>  
  
```csharp
public class SelfDescribingServiceHostFactory : ServiceHostFactory  
{  
    protected override ServiceHost CreateServiceHost(Type serviceType,
     Uri[] baseAddresses)  
    {  
        //All the custom factory does is return a new instance  
        //of our custom host class. The bulk of the custom logic should  
        //live in the custom host (as opposed to the factory)
        //for maximum  
        //reuse value outside of the IIS/WAS hosting environment.  
        return new SelfDescribingServiceHost(serviceType,
                                             baseAddresses);  
    }  
}  
```  
  
 <span data-ttu-id="087b4-142">如您所见，实现自定义 ServiceHostFactory 非常简单。</span><span class="sxs-lookup"><span data-stu-id="087b4-142">As you can see, implementing a custom ServiceHostFactory is straightforward.</span></span> <span data-ttu-id="087b4-143">所有自定义逻辑都位于 ServiceHost 实现的内部；工厂返回派生类的实例。</span><span class="sxs-lookup"><span data-stu-id="087b4-143">All of the custom logic resides inside of the ServiceHost implementation; the factory returns an instance of the derived class.</span></span>  
  
 <span data-ttu-id="087b4-144">若要将自定义工厂与服务实现一起使用，必须将一些其他元数据添加到服务的 .svc 文件中。</span><span class="sxs-lookup"><span data-stu-id="087b4-144">To use a custom factory with a service implementation, we must add some additional metadata to the service's .svc file.</span></span>  
  
```aspx-csharp
<% @ServiceHost Service="Microsoft.ServiceModel.Samples.CalculatorService"
               Factory="Microsoft.ServiceModel.Samples.SelfDescribingServiceHostFactory"
               language=c# Debug="true" %>
```
  
 <span data-ttu-id="087b4-145">在这里，我们向指令添加了一个附加 `Factory` 属性 `@ServiceHost` ，并将自定义工厂的 CLR 类型名称传递为该属性的值。</span><span class="sxs-lookup"><span data-stu-id="087b4-145">Here we have added an additional `Factory` attribute to the `@ServiceHost` directive, and passed the CLR type name of our custom factory as the attribute's value.</span></span> <span data-ttu-id="087b4-146">当 IIS 或 WAS 接收到此服务的消息时，WCF 托管基础结构首先会创建 ServiceHostFactory 的实例，然后通过调用实例化服务主机本身 `ServiceHostFactory.CreateServiceHost()` 。</span><span class="sxs-lookup"><span data-stu-id="087b4-146">When IIS or WAS receives a message for this service, the WCF hosting infrastructure first creates an instance of the ServiceHostFactory and then instantiates the service host itself by calling `ServiceHostFactory.CreateServiceHost()`.</span></span>  
  
## <a name="running-the-sample"></a><span data-ttu-id="087b4-147">运行示例</span><span class="sxs-lookup"><span data-stu-id="087b4-147">Running the sample</span></span>  

 <span data-ttu-id="087b4-148">尽管此示例提供了一个功能完备的客户端和服务实现，但该示例的目的是说明如何通过自定义宿主来更改服务的运行时行为。请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="087b4-148">Although this sample does provide a fully functional client and service implementation, the point of the sample is to illustrate how to alter a service's run-time behavior by means of a custom host., do the following steps:</span></span>  
  
### <a name="observe-the-effect-of-the-custom-host"></a><span data-ttu-id="087b4-149">观察自定义主机的效果</span><span class="sxs-lookup"><span data-stu-id="087b4-149">Observe the effect of the custom host</span></span>
  
1. <span data-ttu-id="087b4-150">打开该服务的 Web.config 文件，并观察没有为该服务显式启用元数据的配置。</span><span class="sxs-lookup"><span data-stu-id="087b4-150">Open the service's Web.config file and observe that there is no configuration explicitly enabling metadata for the service.</span></span>  
  
2. <span data-ttu-id="087b4-151">打开服务的 .svc 文件，并观察它的 @ServiceHost 指令是否包含一个工厂属性，该属性指定自定义 ServiceHostFactory 的名称。</span><span class="sxs-lookup"><span data-stu-id="087b4-151">Open the service's .svc file and observe that its @ServiceHost directive contains a Factory attribute that specifies the name of a custom ServiceHostFactory.</span></span>  
  
### <a name="set-up-build-and-run-the-sample"></a><span data-ttu-id="087b4-152">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="087b4-152">Set up, build, and run the sample</span></span>
  
1. <span data-ttu-id="087b4-153">确保已对 [Windows Communication Foundation 示例执行了一次性安装过程](one-time-setup-procedure-for-the-wcf-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="087b4-153">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>

2. <span data-ttu-id="087b4-154">若要生成解决方案，请按照 [生成 Windows Communication Foundation 示例](building-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="087b4-154">To build the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>

3. <span data-ttu-id="087b4-155">构建解决方案后，运行 Setup.bat 在 IIS 7.0 中设置 ServiceModelSamples 应用程序。</span><span class="sxs-lookup"><span data-stu-id="087b4-155">After the solution has been built, run Setup.bat to set up the ServiceModelSamples Application in IIS 7.0.</span></span> <span data-ttu-id="087b4-156">现在，ServiceModelSamples 目录应显示为 IIS 7.0 应用程序。</span><span class="sxs-lookup"><span data-stu-id="087b4-156">The ServiceModelSamples directory should now appear as an IIS 7.0 Application.</span></span>

4. <span data-ttu-id="087b4-157">若要以单机配置或跨计算机配置来运行示例，请按照 [运行 Windows Communication Foundation 示例](running-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="087b4-157">To run the sample in a single- or cross-machine configuration, follow the instructions in [Running the Windows Communication Foundation Samples](running-the-samples.md).</span></span>

5. <span data-ttu-id="087b4-158">若要删除 IIS 7.0 应用程序，请运行 *Cleanup.bat*。</span><span class="sxs-lookup"><span data-stu-id="087b4-158">To remove the IIS 7.0 application, run *Cleanup.bat*.</span></span>

## <a name="see-also"></a><span data-ttu-id="087b4-159">请参阅</span><span class="sxs-lookup"><span data-stu-id="087b4-159">See also</span></span>

- [<span data-ttu-id="087b4-160">如何：在 IIS 中承载 WCF 服务</span><span class="sxs-lookup"><span data-stu-id="087b4-160">How to: Host a WCF Service in IIS</span></span>](../feature-details/how-to-host-a-wcf-service-in-iis.md)
