---
description: 了解更多相关信息：没有配置的 AJAX 服务
title: 无配置的 AJAX 服务
ms.date: 03/30/2017
ms.assetid: e6db7acd-5679-45d4-b98a-8449c6873838
ms.openlocfilehash: 137f0845f042d1919c1cb070c91a473ff81863cd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99779031"
---
# <a name="ajax-service-without-configuration"></a><span data-ttu-id="ef80e-103">无配置的 AJAX 服务</span><span class="sxs-lookup"><span data-stu-id="ef80e-103">AJAX Service Without Configuration</span></span>

<span data-ttu-id="ef80e-104">此示例演示如何使用 Windows Communication Foundation (WCF) 创建 ASP.NET 的基本的异步 JavaScript 和 XML (AJAX) service (可通过使用 Web 浏览器客户端中的 JavaScript 代码访问的服务) ，而无需使用任何配置设置。</span><span class="sxs-lookup"><span data-stu-id="ef80e-104">This sample demonstrates how to use Windows Communication Foundation (WCF) to create a basic ASP.NET Asynchronous JavaScript and XML (AJAX) service (a service that you can access by using JavaScript code from a Web browser client) without using any configuration settings.</span></span> <span data-ttu-id="ef80e-105">该服务在 .svc 文件中使用特殊语法来自动启用 AJAX 终结点。</span><span class="sxs-lookup"><span data-stu-id="ef80e-105">The service uses special syntax in the .svc file to automatically enable an AJAX endpoint.</span></span>

<span data-ttu-id="ef80e-106">WCF 中的 AJAX 支持经过优化，可在控件中与 ASP.NET AJAX 一起使用 `ScriptManager` 。</span><span class="sxs-lookup"><span data-stu-id="ef80e-106">AJAX support in WCF is optimized for use with ASP.NET AJAX through the `ScriptManager` control.</span></span> <span data-ttu-id="ef80e-107">有关将 WCF 与 ASP.NET AJAX 一起使用的示例，请参阅 [Ajax 示例](ajax.md)。</span><span class="sxs-lookup"><span data-stu-id="ef80e-107">For an example of using WCF with ASP.NET AJAX, see the [Ajax Samples](ajax.md).</span></span>

> [!NOTE]
> <span data-ttu-id="ef80e-108">本主题的最后介绍了此示例的设置过程和生成说明。</span><span class="sxs-lookup"><span data-stu-id="ef80e-108">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>

 <span data-ttu-id="ef80e-109">此示例是基于使用 HTTP POST 的 AJAX 服务生成的。</span><span class="sxs-lookup"><span data-stu-id="ef80e-109">This sample builds upon the AJAX Service Using HTTP POST.</span></span> <span data-ttu-id="ef80e-110">如 [基本 AJAX 服务](basic-ajax-service.md) 示例中所述， <xref:System.ServiceModel.Activation.WebScriptServiceHostFactory> 用于宿主服务。</span><span class="sxs-lookup"><span data-stu-id="ef80e-110">As described in the [Basic AJAX Service](basic-ajax-service.md) sample, <xref:System.ServiceModel.Activation.WebScriptServiceHostFactory> is used to host the service.</span></span>

```text
<%ServiceHost
    language=c#
    Debug="true"
    Service="Microsoft.Ajax.Samples.CalculatorService
    Factory="System.ServiceModel.Activation.WebScriptServiceHostFactory"
%>
```

<span data-ttu-id="ef80e-111"><xref:System.ServiceModel.Activation.WebScriptServiceHostFactory> 自动将 <xref:System.ServiceModel.Description.WebScriptEndpoint> 添加到服务。</span><span class="sxs-lookup"><span data-stu-id="ef80e-111"><xref:System.ServiceModel.Activation.WebScriptServiceHostFactory> automatically adds a <xref:System.ServiceModel.Description.WebScriptEndpoint> to the service.</span></span> <span data-ttu-id="ef80e-112">如果不需要对终结点进行任何配置更改，则可从服务的 Web.config 文件中完全移除 `<system.ServiceModel>` 部分。</span><span class="sxs-lookup"><span data-stu-id="ef80e-112">If no configuration changes need to be made to the endpoint, the `<system.ServiceModel>` section can be completely removed from the Web.config file for the service.</span></span> <span data-ttu-id="ef80e-113">Web.config 文件包含一些由 ConfigFreeClientPage.aspx 使用的 ASP.NET 设置。</span><span class="sxs-lookup"><span data-stu-id="ef80e-113">The Web.config file contains some ASP.NET settings, which are used by ConfigFreeClientPage.aspx.</span></span> <span data-ttu-id="ef80e-114">如果不是这样，则可以移除整个 Web.config 文件。</span><span class="sxs-lookup"><span data-stu-id="ef80e-114">If that were not the case, the entire Web.config file could be removed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ef80e-115">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="ef80e-115">The samples may already be installed on your computer.</span></span> <span data-ttu-id="ef80e-116">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="ef80e-116">Check for the following (default) directory before continuing.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> <span data-ttu-id="ef80e-117">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ef80e-117">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="ef80e-118">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="ef80e-118">This sample is located in the following directory.</span></span>
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Ajax\ConfigFreeAjaxService`

#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="ef80e-119">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="ef80e-119">To set up, build, and run the sample</span></span>

1. <span data-ttu-id="ef80e-120">确保在 [Windows Communication Foundation 示例的一次性安装过程](one-time-setup-procedure-for-the-wcf-samples.md)中执行设置说明。</span><span class="sxs-lookup"><span data-stu-id="ef80e-120">Ensure that you perform the setup instructions in [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>

2. <span data-ttu-id="ef80e-121">按照 [生成 Windows Communication Foundation 示例](building-the-samples.md)中所述生成解决方案 ConfigFreeAjaxService。</span><span class="sxs-lookup"><span data-stu-id="ef80e-121">Build the solution ConfigFreeAjaxService.sln as described in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>

3. <span data-ttu-id="ef80e-122">定位到 `http://localhost/ServiceModelSamples/ConfigFreeClientPage.aspx` (不要在浏览器中从项目目录) 中打开 configfreeclientpage.aspx。</span><span class="sxs-lookup"><span data-stu-id="ef80e-122">Navigate to `http://localhost/ServiceModelSamples/ConfigFreeClientPage.aspx` (do not open ConfigFreeClientPage.aspx in the browser from within the project directory).</span></span>

> [!NOTE]
> <span data-ttu-id="ef80e-123">运行此示例时，请确保不要对 IIS 中的 ServiceModelSamples 文件夹同时启用匿名身份验证和 Windows 身份验证。</span><span class="sxs-lookup"><span data-stu-id="ef80e-123">When running this sample, please ensure that Anonymous Authentication and Windows Authentication are not enabled simultaneously for the ServiceModelSamples folder in IIS.</span></span> <span data-ttu-id="ef80e-124">如果同时启用了这两种身份验证，请禁用 Windows 身份验证。</span><span class="sxs-lookup"><span data-stu-id="ef80e-124">If that is the case, please disable Windows Authentication.</span></span> <span data-ttu-id="ef80e-125">运行了该示例后，请启用 Windows 身份验证并运行“iisreset”。</span><span class="sxs-lookup"><span data-stu-id="ef80e-125">Once you have run the sample, enable Windows Authentication and run "iisreset".</span></span>

## <a name="see-also"></a><span data-ttu-id="ef80e-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="ef80e-126">See also</span></span>

- [<span data-ttu-id="ef80e-127">基本 AJAX 服务</span><span class="sxs-lookup"><span data-stu-id="ef80e-127">Basic AJAX Service</span></span>](basic-ajax-service.md)
