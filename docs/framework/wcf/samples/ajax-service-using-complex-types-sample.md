---
description: 了解更多：使用复杂类型的 AJAX 服务示例
title: 使用复杂类型的 AJAX 服务示例
ms.date: 03/30/2017
ms.assetid: 88242b99-4811-4cbe-8201-52ddf48fb174
ms.openlocfilehash: 438bceb91f10f5ba91d02272d2ba266a50a05f82
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99779122"
---
# <a name="ajax-service-using-complex-types-sample"></a><span data-ttu-id="5da77-103">使用复杂类型的 AJAX 服务示例</span><span class="sxs-lookup"><span data-stu-id="5da77-103">AJAX Service Using Complex Types Sample</span></span>

<span data-ttu-id="5da77-104">此示例演示如何使用 Windows Communication Foundation (WCF) 创建 ASP.NET 的异步 JavaScript 和 XML (AJAX) 服务，该服务可创建复杂类型的实例，并在服务和客户端之间以 JavaScript 对象表示法 (JSON) 的形式发送它们。</span><span class="sxs-lookup"><span data-stu-id="5da77-104">This sample demonstrates how to use Windows Communication Foundation (WCF) to create an ASP.NET Asynchronous JavaScript and XML (AJAX) service that creates instances of complex types and sends them between service and client as JavaScript Object Notation (JSON).</span></span> <span data-ttu-id="5da77-105">可以从 Web 浏览器客户端使用 JavaScript 代码来访问 AJAX 服务。</span><span class="sxs-lookup"><span data-stu-id="5da77-105">You can access an AJAX service by using JavaScript code from a Web browser client.</span></span> <span data-ttu-id="5da77-106">此示例以 [基本 AJAX 服务](basic-ajax-service.md) 示例为基础。</span><span class="sxs-lookup"><span data-stu-id="5da77-106">This sample builds on the [Basic AJAX Service](basic-ajax-service.md) sample.</span></span>

<span data-ttu-id="5da77-107">WCF 中的 AJAX 支持经过优化，可在控件中与 ASP.NET AJAX 一起使用 <xref:System.Web.UI.ScriptManager> 。</span><span class="sxs-lookup"><span data-stu-id="5da77-107">AJAX support in WCF is optimized for use with ASP.NET AJAX through the <xref:System.Web.UI.ScriptManager> control.</span></span> <span data-ttu-id="5da77-108">有关将 WCF 与 ASP.NET AJAX 一起使用的示例，请参阅 [Ajax 示例](ajax.md)。</span><span class="sxs-lookup"><span data-stu-id="5da77-108">For an example of using WCF with ASP.NET AJAX, see the [AJAX Samples](ajax.md).</span></span>

> [!NOTE]
> <span data-ttu-id="5da77-109">本主题的最后介绍了此示例的设置过程和生成说明。</span><span class="sxs-lookup"><span data-stu-id="5da77-109">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>

<span data-ttu-id="5da77-110">以下示例中的服务是不包含 AJAX 特定代码的 WCF 服务。</span><span class="sxs-lookup"><span data-stu-id="5da77-110">The service in the following sample is a WCF service with no AJAX-specific code.</span></span> <span data-ttu-id="5da77-111">由于未应用 <xref:System.ServiceModel.Web.WebGetAttribute> 属性，因此将使用默认的 HTTP 谓词（“POST”）。</span><span class="sxs-lookup"><span data-stu-id="5da77-111">Because the <xref:System.ServiceModel.Web.WebGetAttribute> attribute is not applied, the default HTTP verb ("POST") is used.</span></span> <span data-ttu-id="5da77-112">该服务有一个操作 `DoMath`，该操作返回一个名为 `MathResult` 的复杂类型。</span><span class="sxs-lookup"><span data-stu-id="5da77-112">The service has one operation, `DoMath`, which returns a complex type named `MathResult`.</span></span> <span data-ttu-id="5da77-113">该复杂类型是标准的数据协定类型，也不包含特定于 AJAX 的代码。</span><span class="sxs-lookup"><span data-stu-id="5da77-113">The complex type is a standard data contract type, which also contains no AJAX-specific code.</span></span>

```csharp
[DataContract]
public class MathResult
{
    [DataMember]
    public double sum;
    [DataMember]
    public double difference;
    [DataMember]
    public double product;
    [DataMember]
    public double quotient;
}
```

<span data-ttu-id="5da77-114">通过使用 <xref:System.ServiceModel.Activation.WebScriptServiceHostFactory> 在服务上创建 AJAX 终结点，就像在基本 AJAX 服务示例中一样。</span><span class="sxs-lookup"><span data-stu-id="5da77-114">Create an AJAX endpoint on the service by using the <xref:System.ServiceModel.Activation.WebScriptServiceHostFactory>, just as in the Basic AJAX Service sample.</span></span>

<span data-ttu-id="5da77-115">当用户单击页面上的 " **执行计算** " 按钮时，客户端网页 complextypeclientpage.aspx 包含用于调用服务的 ASP.NET 和 JavaScript 代码。</span><span class="sxs-lookup"><span data-stu-id="5da77-115">The client Web page ComplexTypeClientPage.aspx contains ASP.NET and JavaScript code to invoke the service when the user clicks the **Perform calculation** button on the page.</span></span> <span data-ttu-id="5da77-116">用于调用服务的代码构造 JSON 正文并使用 HTTP POST 发送它，类似于 [使用 HTTP post 的 AJAX 服务](ajax-service-using-http-post.md) 示例。</span><span class="sxs-lookup"><span data-stu-id="5da77-116">The code to invoke the service constructs a JSON body and sends it using HTTP POST, similar to the [AJAX Service Using HTTP POST](ajax-service-using-http-post.md) sample.</span></span>

<span data-ttu-id="5da77-117">在服务调用成功之后，您可以在所得到的 JavaScript 对象上访问各个数据成员（`sum`、`difference`、`product` 和 `quotient`）。</span><span class="sxs-lookup"><span data-stu-id="5da77-117">After the service call succeeds, you can access the individual data members (`sum`, `difference`, `product` and `quotient`) on the resulting JavaScript object.</span></span>

```javascript
function onSuccess(mathResult){
     document.getElementById("sum").value = mathResult.sum;
     document.getElementById("difference").value = mathResult.difference;
     document.getElementById("product").value = mathResult.product;
     document.getElementById("quotient").value = mathResult.quotient;
}
```

### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="5da77-118">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="5da77-118">To set up, build, and run the sample</span></span>

1. <span data-ttu-id="5da77-119">确保已对 [Windows Communication Foundation 示例执行了一次性安装过程](one-time-setup-procedure-for-the-wcf-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="5da77-119">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>

2. <span data-ttu-id="5da77-120">按照 [生成 Windows Communication Foundation 示例](building-the-samples.md)中所述生成解决方案 ComplexTypeAjaxService。</span><span class="sxs-lookup"><span data-stu-id="5da77-120">Build the solution ComplexTypeAjaxService.sln as described in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>

3. <span data-ttu-id="5da77-121">定位到 `http://localhost/ServiceModelSamples/ComplexTypeClientPage.aspx` (不要在浏览器中从项目目录) 打开 complextypeclientpage.aspx。</span><span class="sxs-lookup"><span data-stu-id="5da77-121">Navigate to `http://localhost/ServiceModelSamples/ComplexTypeClientPage.aspx` (do not open ComplexTypeClientPage.aspx in the browser from the project directory).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5da77-122">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="5da77-122">The samples may already be installed on your computer.</span></span> <span data-ttu-id="5da77-123">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="5da77-123">Check for the following (default) directory before continuing.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> <span data-ttu-id="5da77-124">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5da77-124">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="5da77-125">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="5da77-125">This sample is located in the following directory.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Ajax\ComplexTypeAjaxService`

## <a name="see-also"></a><span data-ttu-id="5da77-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="5da77-126">See also</span></span>

- [<span data-ttu-id="5da77-127">基本 AJAX 服务</span><span class="sxs-lookup"><span data-stu-id="5da77-127">Basic AJAX Service</span></span>](basic-ajax-service.md)
