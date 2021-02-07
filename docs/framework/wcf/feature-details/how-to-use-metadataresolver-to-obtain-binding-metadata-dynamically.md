---
description: 了解详细信息：如何：使用 MetadataResolver 动态获取绑定元数据
title: 如何：使用 MetadataResolver 动态获取绑定元数据
ms.date: 03/30/2017
ms.assetid: 56ffcb99-fff0-4479-aca0-e3909009f605
ms.openlocfilehash: 00f33b31504ede6868113040ba83b6f9462ee808
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99734277"
---
# <a name="how-to-use-metadataresolver-to-obtain-binding-metadata-dynamically"></a><span data-ttu-id="df3ed-103">如何：使用 MetadataResolver 动态获取绑定元数据</span><span class="sxs-lookup"><span data-stu-id="df3ed-103">How to: Use MetadataResolver to Obtain Binding Metadata Dynamically</span></span>

<span data-ttu-id="df3ed-104">本主题演示如何使用 <xref:System.ServiceModel.Description.MetadataResolver> 类来动态获取绑定元数据。</span><span class="sxs-lookup"><span data-stu-id="df3ed-104">This topic shows you how to use the <xref:System.ServiceModel.Description.MetadataResolver> class to dynamically obtain binding metadata.</span></span>  
  
### <a name="to-dynamically-obtain-binding-metadata"></a><span data-ttu-id="df3ed-105">动态获取绑定元数据</span><span class="sxs-lookup"><span data-stu-id="df3ed-105">To dynamically obtain binding metadata</span></span>  
  
1. <span data-ttu-id="df3ed-106">使用元数据终结点的地址创建一个 <xref:System.ServiceModel.EndpointAddress> 对象。</span><span class="sxs-lookup"><span data-stu-id="df3ed-106">Create an <xref:System.ServiceModel.EndpointAddress> object with the address of the metadata endpoint.</span></span>  
  
    ```csharp
    EndpointAddress metaAddress  
      = new EndpointAddress(new Uri("http://localhost:8080/SampleService/mex"));  
    ```  
  
2. <span data-ttu-id="df3ed-107">调用 <xref:System.ServiceModel.Description.MetadataResolver.Resolve%28System.Type%2CSystem.ServiceModel.EndpointAddress%29>，它传入服务类型和元数据终结点地址。</span><span class="sxs-lookup"><span data-stu-id="df3ed-107">Call <xref:System.ServiceModel.Description.MetadataResolver.Resolve%28System.Type%2CSystem.ServiceModel.EndpointAddress%29>, which passes in the service type and the metadata endpoint address.</span></span> <span data-ttu-id="df3ed-108">这将返回实现了指定协定的终结点的集合。</span><span class="sxs-lookup"><span data-stu-id="df3ed-108">This returns a collection of endpoints that implement the specified contract.</span></span> <span data-ttu-id="df3ed-109">仅从元数据导入绑定信息；不导入协定信息。</span><span class="sxs-lookup"><span data-stu-id="df3ed-109">Only binding information is imported from the metadata; contract information is not imported.</span></span> <span data-ttu-id="df3ed-110">改用所提供的协定。</span><span class="sxs-lookup"><span data-stu-id="df3ed-110">The supplied contract is used instead.</span></span>  
  
    ```csharp  
    ServiceEndpointCollection endpoints = MetadataResolver.Resolve(typeof(SampleServiceClient),metaAddress);  
    ```  
  
3. <span data-ttu-id="df3ed-111">然后，可以遍历该服务终结点集合，以提取所需的绑定信息。</span><span class="sxs-lookup"><span data-stu-id="df3ed-111">You can then iterate through the collection of service endpoints to extract the binding information you need.</span></span> <span data-ttu-id="df3ed-112">下面的代码遍历终结点，创建一个服务客户端对象（该对象传入与当前终结点关联的绑定和地址），然后调用该服务上的一个方法。</span><span class="sxs-lookup"><span data-stu-id="df3ed-112">The following code iterates through the endpoints, creates a service client object that passes in the binding and address associated with the current endpoint, and then calls a method on the service.</span></span>  
  
    ```csharp  
    foreach (ServiceEndpoint point in endpoints)  
    {  
       if (point != null)  
       {  
          // Create a new wcfClient using retrieved endpoints.  
          using (wcfClient = new SampleServiceClient(point.Binding, point.Address))  
          {  
             Console.WriteLine(  
               wcfClient.SampleMethod("Client used the "  
               + point.Address.ToString() + " address."));  
          }  
      }  
    }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="df3ed-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="df3ed-113">See also</span></span>

- <span data-ttu-id="df3ed-114">Metadata </span><span class="sxs-lookup"><span data-stu-id="df3ed-114">[Metadata](metadata.md)</span></span>
