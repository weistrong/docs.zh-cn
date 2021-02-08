---
description: 了解有关以下内容的详细信息：具有 JSON 和 XML 的 AJAX 服务示例
title: 具有 JSON 和 XML 的 AJAX 服务示例
ms.date: 03/30/2017
ms.assetid: 8ea5860d-0c42-4ae9-941a-e07efdd8e29c
ms.openlocfilehash: e47f6cbd7e4659488325e158e5594ca94322c520
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99779057"
---
# <a name="ajax-service-with-json-and-xml-sample"></a><span data-ttu-id="8c4a0-103">具有 JSON 和 XML 的 AJAX 服务示例</span><span class="sxs-lookup"><span data-stu-id="8c4a0-103">AJAX Service with JSON and XML Sample</span></span>

<span data-ttu-id="8c4a0-104">此示例演示如何使用 Windows Communication Foundation (WCF) 来创建返回) JavaScript 对象表示法 JSON (或 XML 数据的异步 JavaScript 和 XML (AJAX) 服务。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-104">This sample demonstrates how to use Windows Communication Foundation (WCF) to create an Asynchronous JavaScript and XML (AJAX) service that returns either JavaScript Object Notation (JSON) or XML data.</span></span> <span data-ttu-id="8c4a0-105">可以从 Web 浏览器客户端使用 JavaScript 代码来访问 AJAX 服务。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-105">You can access an AJAX service by using JavaScript code from a Web browser client.</span></span> <span data-ttu-id="8c4a0-106">此示例以 [基本 AJAX 服务](basic-ajax-service.md) 示例为基础。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-106">This sample builds on the [Basic AJAX Service](basic-ajax-service.md) sample.</span></span>

<span data-ttu-id="8c4a0-107">与其他 AJAX 示例不同的是，此示例不使用 ASP.NET AJAX 和 <xref:System.Web.UI.ScriptManager> 控件。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-107">Unlike the other AJAX samples, this sample does not use ASP.NET AJAX and the <xref:System.Web.UI.ScriptManager> control.</span></span> <span data-ttu-id="8c4a0-108">利用一些附加配置，可以通过 JavaScript 从任何 HTML 页面访问 WCF AJAX 服务，此处显示了这种情况。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-108">With some additional configuration, WCF AJAX services can be accessed from any HTML page through JavaScript, and this scenario is shown here.</span></span> <span data-ttu-id="8c4a0-109">有关将 WCF 与 ASP.NET AJAX 一起使用的示例，请参阅 [Ajax 示例](ajax.md)。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-109">For an example of using WCF with ASP.NET AJAX, see [AJAX Samples](ajax.md).</span></span>

<span data-ttu-id="8c4a0-110">此示例演示如何在 JSON 和 XML 之间切换操作的响应类型。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-110">This sample shows how to switch the response type of an operation between JSON and XML.</span></span> <span data-ttu-id="8c4a0-111">无论服务是配置为由 ASP.NET AJAX 访问还是由 HTML/JavaScript 客户端页面访问，此功能均可用。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-111">This functionality is available regardless of whether the service is configured to be accessed by ASP.NET AJAX or by an HTML/JavaScript client page.</span></span>

> [!NOTE]
> <span data-ttu-id="8c4a0-112">本主题的最后介绍了此示例的设置过程和生成说明。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-112">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>

<span data-ttu-id="8c4a0-113">为了启用非 ASP.NET AJAX 客户端，请在 .svc 文件中使用 <xref:System.ServiceModel.Activation.WebServiceHostFactory>（而不是 <xref:System.ServiceModel.Activation.WebScriptServiceHostFactory>）。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-113">To enable the use of non-ASP.NET AJAX clients, use <xref:System.ServiceModel.Activation.WebServiceHostFactory> (not <xref:System.ServiceModel.Activation.WebScriptServiceHostFactory>) in the .svc file.</span></span> <span data-ttu-id="8c4a0-114"><xref:System.ServiceModel.Activation.WebServiceHostFactory> 将 <xref:System.ServiceModel.Description.WebHttpEndpoint> 标准终结点添加到服务中。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-114"><xref:System.ServiceModel.Activation.WebServiceHostFactory> adds a <xref:System.ServiceModel.Description.WebHttpEndpoint> standard endpoint to the service.</span></span> <span data-ttu-id="8c4a0-115">在相对于 .svc 文件的空地址处配置终结点;这意味着服务的地址是 `http://localhost/ServiceModelSamples/service.svc` ，除操作名称外没有其他后缀。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-115">The endpoint is configured at an empty address relative to the .svc file; this means that the address of the service is `http://localhost/ServiceModelSamples/service.svc`, with no additional suffixes other than the operation name.</span></span>

`<%@ServiceHost language="c#" Debug="true" Service="Microsoft.Samples.XmlAjaxService.CalculatorService" Factory="System.ServiceModel.Activation.WebServiceHostFactory" %>`

<span data-ttu-id="8c4a0-116">可以使用 Web.config 中的以下节对终结点进行其他配置更改。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-116">The following section in Web.config can be used to make additional configuration changes to the endpoint.</span></span> <span data-ttu-id="8c4a0-117">如果不需要额外更改，则可以移除该节。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-117">It can be removed if no extra changes are needed.</span></span>

```xml
<system.serviceModel>
  <standardEndpoints>
    <webHttpEndpoint>
      <!-- Use this element to configure the endpoint -->
      <standardEndpoint name="" />
    </webHttpEndpoint>
  </standardEndpoints>
</system.serviceModel>
```

<span data-ttu-id="8c4a0-118">的默认数据格式 <xref:System.ServiceModel.Description.WebHttpEndpoint> 为 XML，而的默认数据格式 <xref:System.ServiceModel.Description.WebScriptEndpoint> 为 JSON。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-118">The default data format for <xref:System.ServiceModel.Description.WebHttpEndpoint> is XML, while the default data format for <xref:System.ServiceModel.Description.WebScriptEndpoint> is JSON.</span></span> <span data-ttu-id="8c4a0-119">有关详细信息，请参阅在 [不 ASP.NET 的情况下创建 WCF AJAX 服务](../feature-details/creating-wcf-ajax-services-without-aspnet.md)。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-119">For more information, see [Creating WCF AJAX Services without ASP.NET](../feature-details/creating-wcf-ajax-services-without-aspnet.md).</span></span>

<span data-ttu-id="8c4a0-120">以下示例中的服务是一个包含两个操作的标准 WCF 服务。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-120">The service in the following sample is a standard WCF service with two operations.</span></span> <span data-ttu-id="8c4a0-121">这两个操作都需要针对 <xref:System.ServiceModel.Web.WebMessageBodyStyle.Wrapped> 或 <xref:System.ServiceModel.Web.WebGetAttribute> 属性使用 <xref:System.ServiceModel.Web.WebInvokeAttribute> 正文样式，该样式特定于 `webHttp` 行为，对于 JSON/XML 数据格式开关没有任何影响。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-121">Both operations require the <xref:System.ServiceModel.Web.WebMessageBodyStyle.Wrapped> body style on the <xref:System.ServiceModel.Web.WebGetAttribute> or <xref:System.ServiceModel.Web.WebInvokeAttribute> attributes, which is specific to the `webHttp` behavior and has no bearing on the JSON/XML data format switch.</span></span>

```csharp
[OperationContract]
[WebInvoke(ResponseFormat = WebMessageFormat.Xml, BodyStyle = WebMessageBodyStyle.Wrapped)]
MathResult DoMathXml(double n1, double n2);
```

<span data-ttu-id="8c4a0-122">操作的响应格式指定为 XML，这是行为的默认设置 [\<webHttp>](../../configure-apps/file-schema/wcf/webhttp.md) 。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-122">The response format for the operation is specified as XML, which is the default setting for the [\<webHttp>](../../configure-apps/file-schema/wcf/webhttp.md) behavior.</span></span> <span data-ttu-id="8c4a0-123">但是，最好显式指定响应格式。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-123">However, it is good practice explicitly specify the response format.</span></span>

<span data-ttu-id="8c4a0-124">另一个操作使用 `WebInvokeAttribute` 属性并显式指定响应的 JSON（而不是 XML）。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-124">The other operation uses the `WebInvokeAttribute` attribute and explicitly specifies JSON instead of XML for the response.</span></span>

```csharp
[OperationContract]
[WebInvoke(ResponseFormat = WebMessageFormat.Json, BodyStyle = WebMessageBodyStyle.Wrapped)]
MathResult DoMathJson(double n1, double n2);
```

<span data-ttu-id="8c4a0-125">请注意，在这两种情况下，操作都返回复杂类型，即 `MathResult` 标准 WCF 数据协定类型。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-125">Note that in both cases the operations return a complex type, `MathResult`, which is a standard WCF data contract type.</span></span>

<span data-ttu-id="8c4a0-126">XmlAjaxClientPage.htm 的客户端网页包含 JavaScript 代码，该代码在用户单击 " **执行计算" (返回 JSON)** 或 **执行计算 (在页面上返回 XML)** 按钮时调用上述两个操作之一。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-126">The client Web page XmlAjaxClientPage.htm contains JavaScript code that invokes one of the preceding two operations when the user clicks the **Perform calculation (return JSON)** or **Perform calculation (return XML)** buttons on the page.</span></span> <span data-ttu-id="8c4a0-127">用来调用服务的代码将构造 JSON 正文并使用 HTTP POST 发送它。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-127">The code to invoke the service constructs a JSON body and sends it using HTTP POST.</span></span> <span data-ttu-id="8c4a0-128">该请求是在 JavaScript 中手动创建的，不同于 [基本 AJAX 服务](basic-ajax-service.md) 示例和其他使用 ASP.NET ajax 的示例。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-128">The request is created manually in JavaScript, unlike the [Basic AJAX Service](basic-ajax-service.md) sample and the other samples using ASP.NET AJAX.</span></span>

```csharp
// Create HTTP request
var xmlHttp;
// Request instantiation code omitted…
// Result handler code omitted…

// Build the operation URL
var url = "service.svc/ajaxEndpoint/";
url = url + operation;

// Build the body of the JSON message
var body = '{"n1":';
body = body + document.getElementById("num1").value + ',"n2":';
body = body + document.getElementById("num2").value + '}';

// Send the HTTP request
xmlHttp.open("POST", url, true);
xmlHttp.setRequestHeader("Content-type", "application/json");
xmlHttp.send(body);
```

<span data-ttu-id="8c4a0-129">当服务进行响应时，响应将显示出来，而不会在页面上的文本框中进一步执行任何处理。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-129">When the service responds, the response is displayed without any further processing in a textbox on the page.</span></span> <span data-ttu-id="8c4a0-130">这是为了进行演示而实现的，您可以直接遵循所使用的 XML 和 JSON 数据格式。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-130">This is implemented for demonstration purposes to allow you to directly observe the XML and JSON data formats used.</span></span>

```javascript
// Create result handler
xmlHttp.onreadystatechange=function(){
     if(xmlHttp.readyState == 4){
          document.getElementById("result").value = xmlHttp.responseText;
     }
}
```

> [!IMPORTANT]
> <span data-ttu-id="8c4a0-131">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-131">The samples may already be installed on your machine.</span></span> <span data-ttu-id="8c4a0-132">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="8c4a0-132">Check for the following (default) directory before continuing.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> <span data-ttu-id="8c4a0-133">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8c4a0-133">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="8c4a0-134">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="8c4a0-134">This sample is located in the following directory.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\AJAX\XmlAjaxService`

#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="8c4a0-135">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="8c4a0-135">To set up, build, and run the sample</span></span>

1. <span data-ttu-id="8c4a0-136">确保已对 [Windows Communication Foundation 示例执行了一次性安装过程](one-time-setup-procedure-for-the-wcf-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-136">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>

2. <span data-ttu-id="8c4a0-137">按照 [生成 Windows Communication Foundation 示例](building-the-samples.md)中所述生成解决方案 XmlAjaxService。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-137">Build the solution XmlAjaxService.sln as described in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>

3. <span data-ttu-id="8c4a0-138">定位到 `http://localhost/ServiceModelSamples/XmlAjaxClientPage.htm` (不要在浏览器中从项目目录) 打开 XmlAjaxClientPage.htm。</span><span class="sxs-lookup"><span data-stu-id="8c4a0-138">Navigate to `http://localhost/ServiceModelSamples/XmlAjaxClientPage.htm` (do not open XmlAjaxClientPage.htm in the browser from the project directory).</span></span>

## <a name="see-also"></a><span data-ttu-id="8c4a0-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="8c4a0-139">See also</span></span>

- [<span data-ttu-id="8c4a0-140">使用 HTTP POST 的 AJAX 服务</span><span class="sxs-lookup"><span data-stu-id="8c4a0-140">AJAX Service Using HTTP POST</span></span>](ajax-service-using-http-post.md)
