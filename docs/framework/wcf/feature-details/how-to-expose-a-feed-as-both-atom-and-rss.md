---
description: 了解详细信息：如何：将源作为 Atom 和 RSS 公开
title: 如何：作为 Atom 和 RSS 公开源
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: fe374932-67f5-487d-9325-f868812b92e4
ms.openlocfilehash: 5afe08b2c1d9fc687563e124061fe7fb59257180
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99793774"
---
# <a name="how-to-expose-a-feed-as-both-atom-and-rss"></a><span data-ttu-id="0bf1a-103">如何：作为 Atom 和 RSS 公开源</span><span class="sxs-lookup"><span data-stu-id="0bf1a-103">How to: Expose a Feed as Both Atom and RSS</span></span>

<span data-ttu-id="0bf1a-104">Windows Communication Foundation (WCF) 允许您创建公开联合源的服务。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-104">Windows Communication Foundation (WCF) allows you to create a service that exposes a syndication feed.</span></span> <span data-ttu-id="0bf1a-105">本主题讨论如何使用 Atom 1.0 和 RSS 2.0 创建公开联合源的联合服务。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-105">This topic discusses how to create a syndication service that exposes a syndication feed using both Atom 1.0 and RSS 2.0.</span></span> <span data-ttu-id="0bf1a-106">此服务公开一个可以返回任一联合格式的终结点。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-106">This service exposes one endpoint that can return either syndication format.</span></span> <span data-ttu-id="0bf1a-107">为了简单起见，本示例中使用的服务为自承载服务。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-107">For simplicity the service used in this sample is self hosted.</span></span> <span data-ttu-id="0bf1a-108">在生产环境中，此类型的服务将承载在 IIS 或 WAS 下。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-108">In a production environment a service of this type would be hosted under IIS or WAS.</span></span> <span data-ttu-id="0bf1a-109">有关不同 WCF 宿主选项的详细信息，请参阅 [托管](hosting.md)。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-109">For more information about the different WCF hosting options, see [Hosting](hosting.md).</span></span>  
  
### <a name="to-create-a-basic-syndication-service"></a><span data-ttu-id="0bf1a-110">创建基本联合服务</span><span class="sxs-lookup"><span data-stu-id="0bf1a-110">To create a basic syndication service</span></span>  
  
1. <span data-ttu-id="0bf1a-111">使用通过 <xref:System.ServiceModel.Web.WebGetAttribute> 属性标记的接口定义服务协定。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-111">Define a service contract using an interface marked with the <xref:System.ServiceModel.Web.WebGetAttribute> attribute.</span></span> <span data-ttu-id="0bf1a-112">作为联合源公开的每个操作都会返回一个 <xref:System.ServiceModel.Syndication.SyndicationFeedFormatter> 对象。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-112">Each operation that is exposed as a syndication feed returns a <xref:System.ServiceModel.Syndication.SyndicationFeedFormatter> object.</span></span> <span data-ttu-id="0bf1a-113">请注意 <xref:System.ServiceModel.Web.WebGetAttribute> 的参数。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-113">Note the parameters for the <xref:System.ServiceModel.Web.WebGetAttribute>.</span></span> <span data-ttu-id="0bf1a-114">`UriTemplate` 指定用于调用此服务操作的 URL。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-114">`UriTemplate` specifies the URL used to invoke this service operation.</span></span> <span data-ttu-id="0bf1a-115">此参数的字符串包含文本和一个用大括号括起来的变量 ( {*format*} ) 。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-115">The string for this parameter contains literals and a variable in braces ({*format*}).</span></span> <span data-ttu-id="0bf1a-116">此变量与服务操作的 `format` 参数相对应。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-116">This variable corresponds to the service operation's `format` parameter.</span></span> <span data-ttu-id="0bf1a-117">有关详细信息，请参阅 <xref:System.UriTemplate>。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-117">For more information, see <xref:System.UriTemplate>.</span></span> <span data-ttu-id="0bf1a-118">`BodyStyle` 会影响此服务操作所发送和接收的消息的写入方式。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-118">`BodyStyle` affects how the messages that this service operation sends and receives are written.</span></span> <span data-ttu-id="0bf1a-119"><xref:System.ServiceModel.Web.WebMessageBodyStyle.Bare> 指定不使用基础结构定义的 XML 元素包装发送到和接收自此服务操作的数据。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-119"><xref:System.ServiceModel.Web.WebMessageBodyStyle.Bare> specifies that the data sent to and from this service operation are not wrapped by infrastructure-defined XML elements.</span></span> <span data-ttu-id="0bf1a-120">有关详细信息，请参阅 <xref:System.ServiceModel.Web.WebMessageBodyStyle>。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-120">For more information, see <xref:System.ServiceModel.Web.WebMessageBodyStyle>.</span></span>  
  
     [!code-csharp[htAtomRss#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatomrss/cs/program.cs#0)]
     [!code-vb[htAtomRss#0](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatomrss/vb/program.vb#0)]  
  
    > [!NOTE]
    > <span data-ttu-id="0bf1a-121">在此接口中使用 <xref:System.ServiceModel.ServiceKnownTypeAttribute> 以指定服务操作返回的类型。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-121">Use the <xref:System.ServiceModel.ServiceKnownTypeAttribute> to specify the types that are returned by the service operations in this interface.</span></span>  
  
2. <span data-ttu-id="0bf1a-122">实现服务协定。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-122">Implement the service contract.</span></span>  
  
     [!code-csharp[htAtomRss#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatomrss/cs/program.cs#1)]
     [!code-vb[htAtomRss#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatomrss/vb/program.vb#1)]  
  
3. <span data-ttu-id="0bf1a-123">创建 <xref:System.ServiceModel.Syndication.SyndicationFeed> 对象，并添加作者、类别和说明。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-123">Create a <xref:System.ServiceModel.Syndication.SyndicationFeed> object and add an author, category, and description.</span></span>  
  
     [!code-csharp[htAtomRss#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatomrss/cs/program.cs#2)]
     [!code-vb[htAtomRss#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatomrss/vb/program.vb#2)]  
  
4. <span data-ttu-id="0bf1a-124">创建若干 <xref:System.ServiceModel.Syndication.SyndicationItem> 对象。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-124">Create several <xref:System.ServiceModel.Syndication.SyndicationItem> objects.</span></span>  
  
     [!code-csharp[htAtomRss#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatomrss/cs/program.cs#3)]
     [!code-vb[htAtomRss#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatomrss/vb/program.vb#3)]  
  
5. <span data-ttu-id="0bf1a-125">向源中添加 <xref:System.ServiceModel.Syndication.SyndicationItem> 对象。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-125">Add the <xref:System.ServiceModel.Syndication.SyndicationItem> objects to the feed.</span></span>  
  
     [!code-csharp[htAtomRss#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatomrss/cs/program.cs#4)]
     [!code-vb[htAtomRss#4](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatomrss/vb/program.vb#4)]  
  
6. <span data-ttu-id="0bf1a-126">使用格式参数返回请求的格式。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-126">Use the format parameter to return the requested format.</span></span>  
  
     [!code-csharp[htAtomRss#5](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatomrss/cs/program.cs#5)]
     [!code-vb[htAtomRss#5](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatomrss/vb/program.vb#5)]  
  
### <a name="to-host-the-service"></a><span data-ttu-id="0bf1a-127">承载服务</span><span class="sxs-lookup"><span data-stu-id="0bf1a-127">To host the service</span></span>  
  
1. <span data-ttu-id="0bf1a-128">创建 <xref:System.ServiceModel.Web.WebServiceHost> 对象。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-128">Create a <xref:System.ServiceModel.Web.WebServiceHost> object.</span></span> <span data-ttu-id="0bf1a-129">除非在代码或配置中指定了一个终结点，<xref:System.ServiceModel.Web.WebServiceHost> 类会自动在服务的基地址添加终结点。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-129">The <xref:System.ServiceModel.Web.WebServiceHost> class automatically adds an endpoint at the service's base address unless one is specified in code or configuration.</span></span> <span data-ttu-id="0bf1a-130">在此示例中，不指定任何终结点，因此公开默认终结点。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-130">In this sample, no endpoints are specified so the default endpoint is exposed.</span></span>  
  
     [!code-csharp[htAtomRss#6](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatomrss/cs/program.cs#6)]
     [!code-vb[htAtomRss#6](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatomrss/vb/program.vb#6)]  
  
2. <span data-ttu-id="0bf1a-131">打开服务主机，从服务加载源，显示源，然后等待用户按 Enter。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-131">Open the service host, load the feed from the service, display the feed, and wait for the user to press ENTER.</span></span>  
  
     [!code-csharp[htAtomRss#8](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatomrss/cs/program.cs#8)]
     [!code-vb[htAtomRss#8](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatomrss/vb/program.vb#8)]  
  
### <a name="to-call-getblog-with-an-http-get"></a><span data-ttu-id="0bf1a-132">使用 HTTP GET 调用 GetBlog</span><span class="sxs-lookup"><span data-stu-id="0bf1a-132">To call GetBlog with an HTTP GET</span></span>  
  
1. <span data-ttu-id="0bf1a-133">打开 Internet Explorer，键入以下 URL，然后按 ENTER： `http://localhost:8000/BlogService/GetBlog` 。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-133">Open Internet Explorer, type the following URL, and press ENTER: `http://localhost:8000/BlogService/GetBlog`.</span></span>
  
     <span data-ttu-id="0bf1a-134">URL 包含服务的基址 (`http://localhost:8000/BlogService`) 、终结点的相对地址以及要调用的服务操作。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-134">The URL contains the base address of the service (`http://localhost:8000/BlogService`), the relative address of the endpoint, and the service operation to call.</span></span>  
  
### <a name="to-call-getblog-from-code"></a><span data-ttu-id="0bf1a-135">从代码中调用 GetBlog()</span><span class="sxs-lookup"><span data-stu-id="0bf1a-135">To call GetBlog() from code</span></span>  
  
1. <span data-ttu-id="0bf1a-136">使用基址和调用的方法创建 <xref:System.Xml.XmlReader>。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-136">Create an <xref:System.Xml.XmlReader> with the base address and the method you are calling.</span></span>  
  
     [!code-csharp[htAtomRss#9](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatomrss/cs/snippets.cs#9)]
     [!code-vb[htAtomRss#9](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatomrss/vb/snippets.vb#9)]  
  
2. <span data-ttu-id="0bf1a-137">调用静态 <xref:System.ServiceModel.Syndication.SyndicationFeed.Load%28System.Xml.XmlReader%29> 方法，同时传入刚刚创建的 <xref:System.Xml.XmlReader>。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-137">Call the static <xref:System.ServiceModel.Syndication.SyndicationFeed.Load%28System.Xml.XmlReader%29> method, passing in the <xref:System.Xml.XmlReader> you just created.</span></span>  
  
     [!code-csharp[htAtomRss#10](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatomrss/cs/snippets.cs#10)]
     [!code-vb[htAtomRss#10](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatomrss/vb/snippets.vb#10)]  
  
     <span data-ttu-id="0bf1a-138">这将调用服务操作，并用从服务操作返回的格式化程序填充新的 <xref:System.ServiceModel.Syndication.SyndicationFeed>。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-138">This invokes the service operation and populates a new <xref:System.ServiceModel.Syndication.SyndicationFeed> with the formatter returned from the service operation.</span></span>  
  
3. <span data-ttu-id="0bf1a-139">访问源对象。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-139">Access the feed object.</span></span>  
  
     [!code-csharp[htAtomRss#11](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatomrss/cs/snippets.cs#11)]
     [!code-vb[htAtomRss#11](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/htatomrss/vb/snippets.vb#11)]  
  
## <a name="example"></a><span data-ttu-id="0bf1a-140">示例</span><span class="sxs-lookup"><span data-stu-id="0bf1a-140">Example</span></span>  

 <span data-ttu-id="0bf1a-141">下面列出了此示例的完整代码。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-141">The following is the full code listing for this example.</span></span>  
  
 [!code-csharp[htAtomRss#12](../../../../samples/snippets/csharp/VS_Snippets_CFX/htatomrss/cs/program.cs#12)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="0bf1a-142">编译代码</span><span class="sxs-lookup"><span data-stu-id="0bf1a-142">Compiling the Code</span></span>  

 <span data-ttu-id="0bf1a-143">编译前面的代码时，请引用 System.ServiceModel.dll 和 System.ServiceModel.Web.dll。</span><span class="sxs-lookup"><span data-stu-id="0bf1a-143">When compiling the preceding code, reference System.ServiceModel.dll and System.ServiceModel.Web.dll.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0bf1a-144">请参阅</span><span class="sxs-lookup"><span data-stu-id="0bf1a-144">See also</span></span>

- <xref:System.ServiceModel.WebHttpBinding>
- <xref:System.ServiceModel.Web.WebGetAttribute>
