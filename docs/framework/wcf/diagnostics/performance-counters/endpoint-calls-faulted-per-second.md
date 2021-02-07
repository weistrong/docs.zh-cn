---
description: 了解详细信息： Endpoint：每秒出错的调用数
title: 终结点：Calls Faulted Per Second（每秒出错的调用次数）
ms.date: 03/30/2017
ms.assetid: 9840fc0a-0e4d-4638-96fd-40e3ab9e4667
ms.openlocfilehash: 160680f215dbb3eea5ad15c756c7dc68a0629a90
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99759608"
---
# <a name="endpoint-calls-faulted-per-second"></a><span data-ttu-id="fd148-103">终结点：Calls Faulted Per Second（每秒出错的调用次数）</span><span class="sxs-lookup"><span data-stu-id="fd148-103">Endpoint: Calls Faulted Per Second</span></span>

<span data-ttu-id="fd148-104">计数器名称：Calls Faulted Per Second（每秒出错的调用次数）。</span><span class="sxs-lookup"><span data-stu-id="fd148-104">Counter Name: Calls Faulted Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="fd148-105">说明</span><span class="sxs-lookup"><span data-stu-id="fd148-105">Description</span></span>  

 <span data-ttu-id="fd148-106">一秒内向此终结点返回了错误的调用的数目。</span><span class="sxs-lookup"><span data-stu-id="fd148-106">Number of calls that have returned faults to this endpoint in a second.</span></span>  
  
 <span data-ttu-id="fd148-107">此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。</span><span class="sxs-lookup"><span data-stu-id="fd148-107">This counter is of performance counter type [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10)), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="fd148-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="fd148-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>  
  
 <span data-ttu-id="fd148-109">在 Windows Communication Foundation (WCF) 应用程序中，服务方法使用 SOAP 错误消息来传递处理错误信息。</span><span class="sxs-lookup"><span data-stu-id="fd148-109">In Windows Communication Foundation (WCF) applications, service methods communicate processing error information using SOAP fault messages.</span></span> <span data-ttu-id="fd148-110">SOAP 错误是包括在服务操作元数据中的消息类型，因此会创建一个错误协定，客户端可使用该协定来使执行更加可靠或更具交互性。</span><span class="sxs-lookup"><span data-stu-id="fd148-110">SOAP faults are message types that are included in the metadata for a service operation and therefore create a fault contract that clients can use to make their execution more robust or interactive.</span></span> <span data-ttu-id="fd148-111">由于 SOAP 错误在客户端以 XML 格式表示，因此具有高度的互操作性。</span><span class="sxs-lookup"><span data-stu-id="fd148-111">Since SOAP faults are expressed to clients in XML form, they are highly interoperable.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fd148-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="fd148-112">See also</span></span>

- [<span data-ttu-id="fd148-113">在协定和服务中指定和处理错误</span><span class="sxs-lookup"><span data-stu-id="fd148-113">Specifying and Handling Faults in Contracts and Services</span></span>](../../specifying-and-handling-faults-in-contracts-and-services.md)
