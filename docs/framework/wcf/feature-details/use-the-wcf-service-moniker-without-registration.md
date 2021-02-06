---
description: 了解更多相关信息：如何：在不注册的情况下使用 Windows Communication Foundation 服务名字对象
title: 如何：使用未注册的 Windows Communication Foundation 服务名字对象
ms.date: 03/30/2017
helpviewer_keywords:
- COM [WCF], service monikers without registration
ms.assetid: ee3cf5c0-24f0-4ae7-81da-73a60de4a1a8
ms.openlocfilehash: ed3ea221bc32c4334f609b6740fa10bb63cb2830
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99632381"
---
# <a name="how-to-use-the-windows-communication-foundation-service-moniker-without-registration"></a><span data-ttu-id="60fea-103">如何：使用未注册的 Windows Communication Foundation 服务名字对象</span><span class="sxs-lookup"><span data-stu-id="60fea-103">How to: Use the Windows Communication Foundation Service Moniker without Registration</span></span>

<span data-ttu-id="60fea-104">若要连接到 Windows Communication Foundation (WCF) 服务并与之通信，WCF 客户端应用程序必须具有服务地址、绑定配置和服务协定的详细信息。</span><span class="sxs-lookup"><span data-stu-id="60fea-104">To connect to and communicate with a Windows Communication Foundation (WCF) service, a WCF client application must have the details of the service address, the binding configuration, and the service contract.</span></span>  
  
 <span data-ttu-id="60fea-105">WCF 服务标记通常会在先前注册所需的属性类型之前获得所需的协定，但可能会出现这种情况。</span><span class="sxs-lookup"><span data-stu-id="60fea-105">The WCF service moniker typically obtains the required contract through prior registration of the required attribute types, but there might be cases where this is not feasible.</span></span> <span data-ttu-id="60fea-106">不进行注册时，标记可以通过使用 `wsdl` 参数、通过元数据交换或通过使用 `mexAddress` 参数来获取 Web 服务定义语言 (WSDL) 文档形式的协定定义。</span><span class="sxs-lookup"><span data-stu-id="60fea-106">In place of registration, the moniker can obtain the definition of the contract in the form of a Web Services Definition Language (WSDL) document, through the use of the `wsdl` parameter or through Metadata Exchange, through the use of the `mexAddress` parameter.</span></span>  
  
 <span data-ttu-id="60fea-107">这将启用诸如分发 Excel 电子表格（其中，某些单元格值通过 Web 服务交互进行计算）之类的方案。</span><span class="sxs-lookup"><span data-stu-id="60fea-107">This enables scenarios such as the distribution of an Excel spreadsheet where some of the cell values are calculated through Web service interactions.</span></span> <span data-ttu-id="60fea-108">在此方案中，在可能打开该文档的所有客户端上注册服务协定程序集也许并不可行。</span><span class="sxs-lookup"><span data-stu-id="60fea-108">In this scenario, it might not be feasible to register the service contract assembly on all clients that might open the document.</span></span> <span data-ttu-id="60fea-109">`wsdl` 参数或 `mexAddress` 参数将启用独立的解决方案。</span><span class="sxs-lookup"><span data-stu-id="60fea-109">The `wsdl` parameter or the `mexAddress` parameter enables a self-contained solution.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="60fea-110">必须使用相互身份验证来防止篡改或伪造请求和响应。</span><span class="sxs-lookup"><span data-stu-id="60fea-110">Mutual authentication must be used to protect against request and response tampering or spoofing.</span></span> <span data-ttu-id="60fea-111">具体而言，就是保证要做出响应的元数据交换终结点是预期的可信方，这一点对于客户端相当重要。</span><span class="sxs-lookup"><span data-stu-id="60fea-111">Specifically, it is important for clients to be assured that the Metadata Exchange endpoint that is responding is the intended trusted party.</span></span>  
  
## <a name="example"></a><span data-ttu-id="60fea-112">示例</span><span class="sxs-lookup"><span data-stu-id="60fea-112">Example</span></span>  

 <span data-ttu-id="60fea-113">此示例演示具有 MEX 协定的服务标记的用法。</span><span class="sxs-lookup"><span data-stu-id="60fea-113">This example shows the use of the service moniker with a MEX contract.</span></span> <span data-ttu-id="60fea-114">具有以下协定的服务通过 wsHttpBinding 公开。</span><span class="sxs-lookup"><span data-stu-id="60fea-114">A service with the following contract is exposed with a wsHttpBinding.</span></span>  
  
```csharp
using System.ServiceModel;  
  
// ...
  
[ServiceContract(Namespace = "http://Microsoft.ServiceModel.Demo")]  
public interface IAffiliate  
{  
    [OperationContract]  
    bool NewAffiliate(string ID, string company, string fullname, string accountsCode);  
    [OperationContract]  
    bool RemoveAffiliate(string ID);  
    [OperationContract]  
    double RevenueCheckMonthly(ref string ID);  
    [OperationContract]  
    double RevenueCheckTotal(ref string ID);  
}  
```  
  
 <span data-ttu-id="60fea-115">若要为远程服务构造 WCF 客户端，可以使用以下示例标记字符串。</span><span class="sxs-lookup"><span data-stu-id="60fea-115">To construct a WCF client for the remote service the following example moniker string can be used.</span></span>  
  
```
service4:mexAddress="http://servername/Affiliates/service.svc/mex",  
address="http://servername/Affiliates/service.svc",  
contract=IAffiliate, contractNamespace=http://Microsoft.ServiceModel.Demo,  
binding=WSHttpBinding_IAffiliate, bindingNamespace=http://tempuri.org/  
```  
  
 <span data-ttu-id="60fea-116">在客户端应用程序执行过程中，客户端将使用提供的 `WS-MetadataExchange` 执行 `mexAddress`。</span><span class="sxs-lookup"><span data-stu-id="60fea-116">During the execution of the client application, the client performs a `WS-MetadataExchange` with the provided `mexAddress`.</span></span> <span data-ttu-id="60fea-117">这可能会返回多个服务的地址、绑定和协定详细信息。</span><span class="sxs-lookup"><span data-stu-id="60fea-117">This might return the address, binding and contract details for a number of services.</span></span> <span data-ttu-id="60fea-118">`address`、`contract`、`contractNamespace`、`binding` 和 `bindingNamespace` 参数用于标识所需的服务。</span><span class="sxs-lookup"><span data-stu-id="60fea-118">The `address`, `contract`, `contractNamespace`, `binding` and `bindingNamespace` parameters are used to identify the intended service.</span></span> <span data-ttu-id="60fea-119">匹配这些参数后，名字对象将构造具有相应协定定义的 WCF 客户端，然后就可以使用 WCF 客户端发出调用，就像类型化协定一样。</span><span class="sxs-lookup"><span data-stu-id="60fea-119">Once those parameters have been matched, the moniker constructs a WCF client with the appropriate contract definition and calls can then be made using the WCF client, as with the typed contract.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="60fea-120">如果标记格式不正确或者服务不可用，则对 `GetObject` 的调用将返回一个错误，指示“语法无效”。</span><span class="sxs-lookup"><span data-stu-id="60fea-120">If the moniker is malformed or if the service is unavailable, the call to `GetObject` returns an error saying "Invalid Syntax".</span></span> <span data-ttu-id="60fea-121">如果您收到此错误，请确保所使用的标记正确无误且服务可用。</span><span class="sxs-lookup"><span data-stu-id="60fea-121">If you receive this error, make sure the moniker you are using is correct and the service is available.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="60fea-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="60fea-122">See also</span></span>

- [<span data-ttu-id="60fea-123">如何：注册和配置服务名字对象</span><span class="sxs-lookup"><span data-stu-id="60fea-123">How to: Register and Configure a Service Moniker</span></span>](how-to-register-and-configure-a-service-moniker.md)
