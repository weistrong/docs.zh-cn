---
description: 了解详细信息： Stand-Alone 诊断源示例
title: 独立诊断源示例
ms.date: 03/30/2017
ms.assetid: d31c6c1f-292c-4d95-8e23-ed8565970ea5
ms.openlocfilehash: 98fd65a44f9f6f0183b879627bd8eb444152a8ef
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99668859"
---
# <a name="stand-alone-diagnostics-feed-sample"></a><span data-ttu-id="c1b24-103">独立诊断源示例</span><span class="sxs-lookup"><span data-stu-id="c1b24-103">Stand-Alone Diagnostics Feed Sample</span></span>

<span data-ttu-id="c1b24-104">此示例演示如何使用 Windows Communication Foundation (WCF) 为联合创建 RSS/Atom 源。</span><span class="sxs-lookup"><span data-stu-id="c1b24-104">This sample demonstrates how to create an RSS/Atom feed for syndication with Windows Communication Foundation (WCF).</span></span> <span data-ttu-id="c1b24-105">它是一个基本的 "Hello World" 程序，它显示对象模型的基础知识，以及如何在 Windows Communication Foundation (WCF) 服务上对其进行设置。</span><span class="sxs-lookup"><span data-stu-id="c1b24-105">It is a basic "Hello World" program that shows the basics of the object model and how to set it up on a Windows Communication Foundation (WCF) service.</span></span>  
  
 <span data-ttu-id="c1b24-106">WCF 将联合源建模为返回特殊数据类型的服务操作 <xref:System.ServiceModel.Syndication.SyndicationFeedFormatter> 。</span><span class="sxs-lookup"><span data-stu-id="c1b24-106">WCF models syndication feeds as service operations that return a special data type, <xref:System.ServiceModel.Syndication.SyndicationFeedFormatter>.</span></span> <span data-ttu-id="c1b24-107"><xref:System.ServiceModel.Syndication.SyndicationFeedFormatter> 的实例可以将源序列化为 RSS 2.0 和 Atom 1.0 格式。</span><span class="sxs-lookup"><span data-stu-id="c1b24-107">Instances of <xref:System.ServiceModel.Syndication.SyndicationFeedFormatter> can serialize a feed into both the RSS 2.0 and Atom 1.0 formats.</span></span> <span data-ttu-id="c1b24-108">下面的示例代码演示所使用的协定。</span><span class="sxs-lookup"><span data-stu-id="c1b24-108">The following sample code shows the contract used.</span></span>  
  
```csharp  
[ServiceContract(Namespace = "")]  
    interface IDiagnosticsService  
    {  
        [OperationContract]  
        //The [WebGet] attribute controls how WCF dispatches  
        //HTTP requests to service operations based on a URI suffix  
        //(the part of the request URI after the endpoint address)  
        //using the HTTP GET method. The UriTemplate specifies a relative  
        //path of 'feed', and specifies that the format is  
        //supplied using a query string.
        [WebGet(UriTemplate="feed?format={format}")]  
        [ServiceKnownType(typeof(Atom10FeedFormatter))]  
        [ServiceKnownType(typeof(Rss20FeedFormatter))]  
        SyndicationFeedFormatter GetProcesses(string format);  
    }  
```  
  
 <span data-ttu-id="c1b24-109">此 `GetProcesses` 操作用属性进行批注 <xref:System.ServiceModel.Web.WebGetAttribute> ，该属性使您能够控制 WCF 如何向服务操作调度 HTTP GET 请求并指定所发送消息的格式。</span><span class="sxs-lookup"><span data-stu-id="c1b24-109">The `GetProcesses` operation is annotated with the <xref:System.ServiceModel.Web.WebGetAttribute> attribute that enables you to control how WCF dispatches HTTP GET requests to service operations and specify the format of the messages sent.</span></span>  
  
 <span data-ttu-id="c1b24-110">与任何 WCF 服务一样，联合源可在任何托管的应用程序中自承载。</span><span class="sxs-lookup"><span data-stu-id="c1b24-110">Like any WCF service, syndication feeds can be self hosted in any managed application.</span></span> <span data-ttu-id="c1b24-111">联合服务需要使用特定绑定 (<xref:System.ServiceModel.WebHttpBinding>) 和特定终结点行为 (<xref:System.ServiceModel.Description.WebHttpBehavior>) 才能正常运行。</span><span class="sxs-lookup"><span data-stu-id="c1b24-111">Syndication services require a specific binding (the <xref:System.ServiceModel.WebHttpBinding>) and a specific endpoint behavior (the <xref:System.ServiceModel.Description.WebHttpBehavior>) to function correctly.</span></span> <span data-ttu-id="c1b24-112">新的 <xref:System.ServiceModel.Web.WebServiceHost> 类提供了一个方便的 API，用于在不使用特定配置的情况下创建此类终结点。</span><span class="sxs-lookup"><span data-stu-id="c1b24-112">The new <xref:System.ServiceModel.Web.WebServiceHost> class provides a convenient API for creating such endpoints without specific configuration.</span></span>  
  
```csharp  
WebServiceHost host = new WebServiceHost(typeof(ProcessService), new Uri("http://localhost:8000/diagnostics"));  
  
            //The WebServiceHost will automatically provide a default endpoint at the base address  
            //using the proper binding (the WebHttpBinding) and endpoint behavior (the WebHttpBehavior)  
```  
  
 <span data-ttu-id="c1b24-113">或者，可在 IIS 承载的 .svc 文件中使用 <xref:System.ServiceModel.Activation.WebServiceHostFactory> 来提供等效的功能（此技术未在此示例代码中演示）。</span><span class="sxs-lookup"><span data-stu-id="c1b24-113">Alternatively, you can use <xref:System.ServiceModel.Activation.WebServiceHostFactory> from within an IIS-hosted .svc file to provide equivalent functionality (this technique is not demonstrated in this sample code).</span></span>  
  
```xml
<% @ServiceHost Language="C#|VB" Debug="true" Service="ProcessService" %>
```
  
 <span data-ttu-id="c1b24-114">由于此服务使用标准 HTTP GET 接收请求，因此可以使用任何识别 RSS 或 ATOM 的客户端来访问此服务。</span><span class="sxs-lookup"><span data-stu-id="c1b24-114">Because this service receives requests using the standard HTTP GET, you can use any RSS or ATOM-aware client to access the service.</span></span> <span data-ttu-id="c1b24-115">例如，可以通过在 `http://localhost:8000/diagnostics/feed/?format=atom` `http://localhost:8000/diagnostics/feed/?format=rss` 识别 RSS 的浏览器中导航到或来查看此服务的输出。</span><span class="sxs-lookup"><span data-stu-id="c1b24-115">For example, you can view the output of this service by navigating to `http://localhost:8000/diagnostics/feed/?format=atom` or `http://localhost:8000/diagnostics/feed/?format=rss` in an RSS-aware browser.</span></span>
  
 <span data-ttu-id="c1b24-116">你还可以使用 [WCF 联合对象模型如何映射到 Atom 和 RSS](../feature-details/how-the-wcf-syndication-object-model-maps-to-atom-and-rss.md) 来读取联合数据并使用命令性代码对其进行处理。</span><span class="sxs-lookup"><span data-stu-id="c1b24-116">You can also use the [How the WCF Syndication Object Model Maps to Atom and RSS](../feature-details/how-the-wcf-syndication-object-model-maps-to-atom-and-rss.md) to read syndicated data and process it using imperative code.</span></span>  
  
```csharp
XmlReader reader = XmlReader.Create( "http://localhost:8000/diagnostics/feed/?format=rss",
    new XmlReaderSettings()
    {
        //MaxCharactersInDocument can be used to control the maximum amount of data
        //read from the reader and helps prevent OutOfMemoryException
        MaxCharactersInDocument = 1024 * 64
    } );

SyndicationFeed feed = SyndicationFeed.Load(reader);

foreach (SyndicationItem i in feed.Items)
{
    XmlSyndicationContent content = i.Content as XmlSyndicationContent;
    ProcessData pd = content.ReadContent<ProcessData>();

    Console.WriteLine(i.Title.Text);
    Console.WriteLine(pd.ToString());
}
```
  
## <a name="set-up-build-and-run-the-sample"></a><span data-ttu-id="c1b24-117">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="c1b24-117">Set up, build, and run the sample</span></span>
  
1. <span data-ttu-id="c1b24-118">请确保对计算机上的 HTTP 和 HTTPS 具有正确的地址注册权限，如在 [Windows Communication Foundation 示例的一次性安装过程](one-time-setup-procedure-for-the-wcf-samples.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="c1b24-118">Ensure that you have the right address registration permission for HTTP and HTTPS on the computer as explained in the set up instructions in [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>

2. <span data-ttu-id="c1b24-119">生成解决方案。</span><span class="sxs-lookup"><span data-stu-id="c1b24-119">Build the solution.</span></span>

3. <span data-ttu-id="c1b24-120">运行控制台应用程序。</span><span class="sxs-lookup"><span data-stu-id="c1b24-120">Run the console application.</span></span>

4. <span data-ttu-id="c1b24-121">当控制台应用程序正在运行时，导航到 `http://localhost:8000/diagnostics/feed/?format=atom` 或 `http://localhost:8000/diagnostics/feed/?format=rss` 使用识别 RSS 的浏览器。</span><span class="sxs-lookup"><span data-stu-id="c1b24-121">While the console application is running, navigate to `http://localhost:8000/diagnostics/feed/?format=atom` or `http://localhost:8000/diagnostics/feed/?format=rss` using an RSS-aware browser.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c1b24-122">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="c1b24-122">The samples may already be installed on your computer.</span></span> <span data-ttu-id="c1b24-123">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="c1b24-123">Check for the following (default) directory before continuing.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> <span data-ttu-id="c1b24-124">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c1b24-124">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="c1b24-125">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="c1b24-125">This sample is located in the following directory.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Syndication\DiagnosticsFeed`

## <a name="see-also"></a><span data-ttu-id="c1b24-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="c1b24-126">See also</span></span>

- [<span data-ttu-id="c1b24-127">WCF Web HTTP 编程模型</span><span class="sxs-lookup"><span data-stu-id="c1b24-127">WCF Web HTTP Programming Model</span></span>](../feature-details/wcf-web-http-programming-model.md)
- [<span data-ttu-id="c1b24-128">WCF 联合</span><span class="sxs-lookup"><span data-stu-id="c1b24-128">WCF Syndication</span></span>](../feature-details/wcf-syndication.md)
