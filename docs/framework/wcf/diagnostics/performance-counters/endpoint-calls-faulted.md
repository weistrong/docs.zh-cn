---
description: 了解详细信息：终结点：调用出错
title: 终结点：Calls Faulted（出错的调用次数）
ms.date: 03/30/2017
ms.assetid: 271e6284-9c4b-465f-b619-069e1555a5e4
ms.openlocfilehash: c1e65582f39a8512bb62b41044d49d32d9d38743
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99759583"
---
# <a name="endpoint-calls-faulted"></a><span data-ttu-id="98d37-103">终结点：Calls Faulted（出错的调用次数）</span><span class="sxs-lookup"><span data-stu-id="98d37-103">Endpoint: Calls Faulted</span></span>

<span data-ttu-id="98d37-104">计数器名称：Calls Faulted（出错的调用次数）。</span><span class="sxs-lookup"><span data-stu-id="98d37-104">Counter Name: Calls Faulted.</span></span>  
  
## <a name="description"></a><span data-ttu-id="98d37-105">说明</span><span class="sxs-lookup"><span data-stu-id="98d37-105">Description</span></span>  

 <span data-ttu-id="98d37-106">对此终结点返回错误的调用次数。</span><span class="sxs-lookup"><span data-stu-id="98d37-106">Number of calls to this endpoint that have returned faults.</span></span> <span data-ttu-id="98d37-107">在 Windows Communication Foundation (WCF) 应用程序中，服务方法使用 SOAP 错误消息来传递处理错误信息。</span><span class="sxs-lookup"><span data-stu-id="98d37-107">In Windows Communication Foundation (WCF) applications, service methods communicate processing error information using SOAP fault messages.</span></span> <span data-ttu-id="98d37-108">SOAP 错误是包括在服务操作元数据中的消息类型，因此会创建一个错误协定，客户端可使用该协定来使执行更加可靠或更具交互性。</span><span class="sxs-lookup"><span data-stu-id="98d37-108">SOAP faults are message types that are included in the metadata for a service operation and therefore create a fault contract that clients can use to make their execution more robust or interactive.</span></span> <span data-ttu-id="98d37-109">由于 SOAP 错误在客户端以 XML 格式表示，因此具有高度的互操作性。</span><span class="sxs-lookup"><span data-stu-id="98d37-109">Since SOAP faults are expressed to clients in XML form, they are highly interoperable.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="98d37-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="98d37-110">See also</span></span>

- [<span data-ttu-id="98d37-111">在协定和服务中指定和处理错误</span><span class="sxs-lookup"><span data-stu-id="98d37-111">Specifying and Handling Faults in Contracts and Services</span></span>](../../specifying-and-handling-faults-in-contracts-and-services.md)
