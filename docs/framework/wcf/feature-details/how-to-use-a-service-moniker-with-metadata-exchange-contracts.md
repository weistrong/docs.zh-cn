---
description: 了解详细信息：如何：将服务名字对象用于元数据交换协定
title: 如何：将服务名字对象与元数据交换协定一起使用
ms.date: 03/30/2017
ms.assetid: c41a07e5-cb9d-45d6-9ea4-34511e227faf
ms.openlocfilehash: 220132a10cb637be9e3724232d0ddaf80a13551a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99643093"
---
# <a name="how-to-use-a-service-moniker-with-metadata-exchange-contracts"></a><span data-ttu-id="b6398-103">如何：将服务名字对象与元数据交换协定一起使用</span><span class="sxs-lookup"><span data-stu-id="b6398-103">How to: Use a Service Moniker with Metadata Exchange Contracts</span></span>

<span data-ttu-id="b6398-104">开发一些新的 WCF 服务后，你可能会决定希望能够从脚本或 Visual Basic 6.0 应用程序调用这些服务。</span><span class="sxs-lookup"><span data-stu-id="b6398-104">After developing some new WCF services, you may decide that you want to be able to call these services from a script or a Visual Basic 6.0 application.</span></span> <span data-ttu-id="b6398-105">一种方法是生成 WCF 客户端程序集，使用 COM 注册该程序集，将程序集安装到 GAC 中，然后从 Visual Basic 代码引用 COM 类型。</span><span class="sxs-lookup"><span data-stu-id="b6398-105">One method would be to generate a WCF client assembly, register the assembly with COM, install the assembly in the GAC, and then reference the COM types from your Visual Basic code.</span></span> <span data-ttu-id="b6398-106">分发应用程序时，还必须分发 WCF 客户端程序集。</span><span class="sxs-lookup"><span data-stu-id="b6398-106">When you distribute the application, you will have to distribute the WCF Client assembly as well.</span></span> <span data-ttu-id="b6398-107">然后，用户必须使用 COM 注册 WCF 客户端程序集，并且将该程序集放置在 GAC 中。</span><span class="sxs-lookup"><span data-stu-id="b6398-107">The user will then have to register the WCF client assembly with COM and place it in the GAC.</span></span> <span data-ttu-id="b6398-108">WCF COM 互操作还允许您在不依赖 WCF 客户端程序集的情况下进行相同的服务调用。</span><span class="sxs-lookup"><span data-stu-id="b6398-108">WCF COM Interop also allows you to make the same service calls without relying on a WCF client assembly.</span></span> <span data-ttu-id="b6398-109">利用 WCF 名字对象，您可以从任何与 COM 兼容的语言中调用任何 WCF 服务 (Visual Basic、VBScript、Visual Basic for Applications (VBA) 等) 上，通过指定服务标记使用的元数据交换 (Mex) 终结点 URI 来提取有关服务的类型信息。</span><span class="sxs-lookup"><span data-stu-id="b6398-109">The WCF moniker allows you to call any WCF service from any COM-compatible language (Visual Basic, VBScript, Visual Basic for Applications (VBA), and so on) by specifying a metadata exchange (Mex) endpoint URI that the service moniker uses to extract type information about the service.</span></span> <span data-ttu-id="b6398-110">本主题说明如何使用指定 Mex 终结点的 WCF 名字对象调用入门 WCF 示例。</span><span class="sxs-lookup"><span data-stu-id="b6398-110">This topic describes how to call the Getting Started WCF sample using a WCF moniker that specifies a Mex endpoint.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="b6398-111">WCF 客户端程序集定义的类型永远不会实际实例化。</span><span class="sxs-lookup"><span data-stu-id="b6398-111">The types defined by the WCF client assembly are never actually instantiated.</span></span> <span data-ttu-id="b6398-112">该程序集只用于元数据。</span><span class="sxs-lookup"><span data-stu-id="b6398-112">The assembly is used only for metadata.</span></span>  
  
### <a name="using-the-service-moniker-with-a-mex-address"></a><span data-ttu-id="b6398-113">使用带有 Mex 地址的服务标记</span><span class="sxs-lookup"><span data-stu-id="b6398-113">Using the service moniker with a Mex address</span></span>  
  
1. <span data-ttu-id="b6398-114">生成入门示例，并使用 Internet Explorer 浏览到其 URL (`http://localhost/ServiceModelSamples/Service.svc`) ，以确保服务正常工作。</span><span class="sxs-lookup"><span data-stu-id="b6398-114">Build the Getting Started sample and use Internet Explorer to browse to its URL (`http://localhost/ServiceModelSamples/Service.svc`) to ensure that the service is working.</span></span>  
  
2. <span data-ttu-id="b6398-115">生成 Visual Basic 脚本或包含以下代码的 Visual Basic 应用程序：</span><span class="sxs-lookup"><span data-stu-id="b6398-115">Create a Visual Basic script or Visual Basic application that contains the following code:</span></span>  
  
    ```vb
    monString = "service:mexaddress=http://localhost/ServiceModelSamples/Service.svc/MEX"  
    monString = monString + ", address=http://localhost/ServiceModelSamples/Service.svc"  
    monString = monString + ", contract=ICalculator, contractNamespace=http://Microsoft.ServiceModel.Samples"  
    monString = monString + ", binding=WSHttpBinding_ICalculator, bindingNamespace=http://Microsoft.ServiceModel.Samples"  
  
    Set calc = GetObject(monString)  
    MsgBox calc.Add(3, 4)  
    ```  
  
3. <span data-ttu-id="b6398-116">运行 Visual Basic 应用程序或脚本。</span><span class="sxs-lookup"><span data-stu-id="b6398-116">Run the Visual Basic application or script.</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="b6398-117">您所调用的服务必须公开标记的 Mex 终结点，以便能够从服务中读取元数据。</span><span class="sxs-lookup"><span data-stu-id="b6398-117">The service you are calling must expose a Mex endpoint for the moniker to be able to read the metadata from the service.</span></span> <span data-ttu-id="b6398-118">有关详细信息，请参阅 [如何：使用配置文件发布服务的元数据](how-to-publish-metadata-for-a-service-using-a-configuration-file.md)。</span><span class="sxs-lookup"><span data-stu-id="b6398-118">For more information, see [How to: Publish Metadata for a Service Using a Configuration File](how-to-publish-metadata-for-a-service-using-a-configuration-file.md).</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="b6398-119">如果标记格式不正确，或如果服务不可用，则对 `GetObject` 的调用将返回一个错误，指示“语法无效”。</span><span class="sxs-lookup"><span data-stu-id="b6398-119">If the moniker is malformed or if the service is unavailable, the call to `GetObject` will return an error saying "Invalid Syntax."</span></span>  <span data-ttu-id="b6398-120">如果您收到此错误，请确保所使用的标记正确无误且服务可用。</span><span class="sxs-lookup"><span data-stu-id="b6398-120">If you receive this error, make sure the moniker you are using is correct and the service is available.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b6398-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="b6398-121">See also</span></span>

- [<span data-ttu-id="b6398-122">如何：使用未注册的 Windows Communication Foundation 服务名字对象</span><span class="sxs-lookup"><span data-stu-id="b6398-122">How to: Use the Windows Communication Foundation Service Moniker without Registration</span></span>](use-the-wcf-service-moniker-without-registration.md)
- [<span data-ttu-id="b6398-123">如何：将服务名字对象用于 WSDL 协定</span><span class="sxs-lookup"><span data-stu-id="b6398-123">How to: Use a Service Moniker with WSDL Contracts</span></span>](how-to-use-a-service-moniker-with-wsdl-contracts.md)
