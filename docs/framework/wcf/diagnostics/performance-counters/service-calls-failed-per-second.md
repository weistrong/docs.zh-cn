---
description: 了解详细信息：服务：每秒调用失败数
title: 服务：Calls Failed Per Second（每秒失败的调用次数）
ms.date: 03/30/2017
ms.assetid: 5a2c7939-107d-4f0c-b43c-e02e079e8a9d
ms.openlocfilehash: b271d5076d0f0c89c4d33b124e0184584795466a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803355"
---
# <a name="service-calls-failed-per-second"></a><span data-ttu-id="6c014-103">服务：Calls Failed Per Second（每秒失败的调用次数）</span><span class="sxs-lookup"><span data-stu-id="6c014-103">Service: Calls Failed Per Second</span></span>

<span data-ttu-id="6c014-104">计数器名称：Calls Failed Per Second（每秒失败的调用次数）。</span><span class="sxs-lookup"><span data-stu-id="6c014-104">Counter Name: Calls Failed Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="6c014-105">说明</span><span class="sxs-lookup"><span data-stu-id="6c014-105">Description</span></span>  

 <span data-ttu-id="6c014-106">一秒钟内由此服务收到且具有未处理异常的调用次数。</span><span class="sxs-lookup"><span data-stu-id="6c014-106">Number of calls that have unhandled exceptions, and are received by this service in a second.</span></span>  
  
 <span data-ttu-id="6c014-107">此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。</span><span class="sxs-lookup"><span data-stu-id="6c014-107">This counter is of performance counter type [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10)), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="6c014-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="6c014-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>  
  
 <span data-ttu-id="6c014-109">在托管代码中，出现错误条件时引发异常。</span><span class="sxs-lookup"><span data-stu-id="6c014-109">In managed code, exceptions are thrown when error conditions occur.</span></span>  
  
 <span data-ttu-id="6c014-110">在托管代码中，出现错误条件时引发异常。</span><span class="sxs-lookup"><span data-stu-id="6c014-110">In managed code, exceptions are thrown when error conditions occur.</span></span>  
  
 <span data-ttu-id="6c014-111">此服务中每出现一个未处理异常，此计数器就会递增。</span><span class="sxs-lookup"><span data-stu-id="6c014-111">This counter is incremented every time there is an unhandled exception in this service.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6c014-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="6c014-112">See also</span></span>

- [<span data-ttu-id="6c014-113">在协定和服务中指定和处理错误</span><span class="sxs-lookup"><span data-stu-id="6c014-113">Specifying and Handling Faults in Contracts and Services</span></span>](../../specifying-and-handling-faults-in-contracts-and-services.md)
