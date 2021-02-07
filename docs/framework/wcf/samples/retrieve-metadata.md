---
description: 了解详细信息：检索元数据
title: 检索元数据
ms.date: 03/30/2017
ms.assetid: e8a6ef8c-a195-495a-a15e-7d92bdf0b28c
ms.openlocfilehash: 819683452630e6750d839c9922538a6056e2556e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99703804"
---
# <a name="retrieve-metadata"></a><span data-ttu-id="706cf-103">检索元数据</span><span class="sxs-lookup"><span data-stu-id="706cf-103">Retrieve Metadata</span></span>

<span data-ttu-id="706cf-104">本示例演示如何实现一个客户端，它能从服务中动态检索元数据以选择用来通信的终结点。</span><span class="sxs-lookup"><span data-stu-id="706cf-104">This sample demonstrates how to implement a client that dynamically retrieves metadata from a service to choose an endpoint with which to communicate.</span></span> <span data-ttu-id="706cf-105">此示例基于 [入门](getting-started-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="706cf-105">This sample is based on the [Getting Started](getting-started-sample.md).</span></span> <span data-ttu-id="706cf-106">已将服务修改为公开两个终结点（使用绑定的基址处的终结点） `basicHttpBinding` 和使用绑定的 {*baseaddress*}/secure 的安全终结点 `wsHttpBinding` 。</span><span class="sxs-lookup"><span data-stu-id="706cf-106">The service has been modified to expose two endpoints—an endpoint at the base address using the `basicHttpBinding` binding, and a secure endpoint at {*baseaddress*}/secure using the `wsHttpBinding` binding.</span></span> <span data-ttu-id="706cf-107">不必使用终结点地址和绑定配置客户端，客户端可以使用 <xref:System.ServiceModel.Description.MetadataExchangeClient> 类动态检索服务的元数据，然后使用 <xref:System.ServiceModel.Description.ServiceEndpointCollection> 类以 <xref:System.ServiceModel.Description.WsdlImporter> 的形式导入元数据。</span><span class="sxs-lookup"><span data-stu-id="706cf-107">Instead of configuring the client with the endpoint addresses and bindings, the client dynamically retrieves the metadata for the service using the <xref:System.ServiceModel.Description.MetadataExchangeClient> class and then imports the metadata as a <xref:System.ServiceModel.Description.ServiceEndpointCollection> using the <xref:System.ServiceModel.Description.WsdlImporter> class.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="706cf-108">本主题的最后介绍了此示例的设置过程和生成说明。</span><span class="sxs-lookup"><span data-stu-id="706cf-108">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>  
  
 <span data-ttu-id="706cf-109">客户端应用程序使用导入的 <xref:System.ServiceModel.Description.ServiceEndpointCollection> 来创建与服务通信的客户端。</span><span class="sxs-lookup"><span data-stu-id="706cf-109">The client application uses the imported <xref:System.ServiceModel.Description.ServiceEndpointCollection> to create clients to communicate with the service.</span></span> <span data-ttu-id="706cf-110">客户端应用程序会遍历每个检索到的终结点并与每个实现 `ICalculator` 协定的终结点通信。</span><span class="sxs-lookup"><span data-stu-id="706cf-110">The client application iterates through each retrieved endpoint and communicates with each endpoint that implements the `ICalculator` contract.</span></span> <span data-ttu-id="706cf-111">会为相应的地址和绑定提供检索到的终结点，以便将客户端配置成可与每个终结点通信，如下面的示例代码所示。</span><span class="sxs-lookup"><span data-stu-id="706cf-111">The appropriate address and binding are provided with the retrieved endpoint, so that the client is configured to communicate with each endpoint, as shown in the following sample code.</span></span>  
  
```csharp
// Create a MetadataExchangeClient for retrieving metadata.  
EndpointAddress mexAddress = new EndpointAddress(ConfigurationManager.AppSettings["mexAddress"]);  
MetadataExchangeClient mexClient = new MetadataExchangeClient(mexAddress);  
  
// Retrieve the metadata for all endpoints using metadata exchange protocol (mex).  
MetadataSet metadataSet = mexClient.GetMetadata();  
  
//Convert the metadata into endpoints.  
WsdlImporter importer = new WsdlImporter(metadataSet);  
ServiceEndpointCollection endpoints = importer.ImportAllEndpoints();  
  
CalculatorClient client = null;  
ContractDescription contract = ContractDescription.GetContract(typeof(ICalculator));  
// Communicate with each endpoint that supports the ICalculator contract.  
foreach (ServiceEndpoint ep in endpoints)  
{  
    if (ep.Contract.Namespace.Equals(contract.Namespace) && ep.Contract.Name.Equals(contract.Name))  
    {  
        // Create a client using the endpoint address and binding.  
        client = new CalculatorClient(ep.Binding, new EndpointAddress(ep.Address.Uri));  
        Console.WriteLine("Communicate with endpoint: ");  
        Console.WriteLine("   AddressPath={0}", ep.Address.Uri.PathAndQuery);  
        Console.WriteLine("   Binding={0}", ep.Binding.Name);  
        // Call operations.  
        DoCalculations(client);  
  
        //Closing the client gracefully closes the connection and cleans up resources.  
        client.Close();  
    }  
}  
```  
  
 <span data-ttu-id="706cf-112">客户端控制台窗口将显示发送到每个终结点的操作，同时显示地址路径和绑定名称。</span><span class="sxs-lookup"><span data-stu-id="706cf-112">The client console window displays the operations sent to each of the endpoints, displaying the address path and binding name.</span></span>  
  
### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="706cf-113">设置、生成和运行示例</span><span class="sxs-lookup"><span data-stu-id="706cf-113">To set up, build, and run the sample</span></span>  
  
1. <span data-ttu-id="706cf-114">确保已对 [Windows Communication Foundation 示例执行了一次性安装过程](one-time-setup-procedure-for-the-wcf-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="706cf-114">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](one-time-setup-procedure-for-the-wcf-samples.md).</span></span>  
  
2. <span data-ttu-id="706cf-115">若要生成 c #、c + + 或 Visual Basic .NET 版本的解决方案，请按照 [生成 Windows Communication Foundation 示例](building-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="706cf-115">To build the C#, C++, or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](building-the-samples.md).</span></span>  
  
3. <span data-ttu-id="706cf-116">若要以单机配置或跨计算机配置来运行示例，请按照 [运行 Windows Communication Foundation 示例](running-the-samples.md)中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="706cf-116">To run the sample in a single- or cross-machine configuration, follow the instructions in [Running the Windows Communication Foundation Samples](running-the-samples.md).</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="706cf-117">您的计算机上可能已安装这些示例。</span><span class="sxs-lookup"><span data-stu-id="706cf-117">The samples may already be installed on your machine.</span></span> <span data-ttu-id="706cf-118">在继续操作之前，请先检查以下（默认）目录：</span><span class="sxs-lookup"><span data-stu-id="706cf-118">Check for the following (default) directory before continuing.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples`  
>
> <span data-ttu-id="706cf-119">如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)]</span><span class="sxs-lookup"><span data-stu-id="706cf-119">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://www.microsoft.com/download/details.aspx?id=21459) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="706cf-120">此示例位于以下目录：</span><span class="sxs-lookup"><span data-stu-id="706cf-120">This sample is located in the following directory.</span></span>  
>
> `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Client\RetrieveMetadata`  
