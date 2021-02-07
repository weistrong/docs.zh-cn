---
description: 了解详细信息：每秒调用失败数
title: Calls Failed Per Second（每秒失败的调用次数）
ms.date: 03/30/2017
ms.assetid: e4ef3773-f650-4876-99cf-4d0c02aa03d4
ms.openlocfilehash: 3961754eb73743a1213922f7c9e1bd164334cd6e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99759713"
---
# <a name="calls-failed-per-second"></a><span data-ttu-id="2213d-103">Calls Failed Per Second（每秒失败的调用次数）</span><span class="sxs-lookup"><span data-stu-id="2213d-103">Calls Failed Per Second</span></span>

<span data-ttu-id="2213d-104">计数器名称：Calls Failed Per Second（每秒失败的调用次数）</span><span class="sxs-lookup"><span data-stu-id="2213d-104">Counter Name: Calls Failed Per Second</span></span>  
  
## <a name="description"></a><span data-ttu-id="2213d-105">说明</span><span class="sxs-lookup"><span data-stu-id="2213d-105">Description</span></span>  

 <span data-ttu-id="2213d-106">该操作中每秒钟出现未处理异常的调用数目。</span><span class="sxs-lookup"><span data-stu-id="2213d-106">Number of calls with unhandled exceptions in this operation in a second.</span></span>  
  
 <span data-ttu-id="2213d-107">此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。</span><span class="sxs-lookup"><span data-stu-id="2213d-107">This counter is of performance counter type [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10)), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="2213d-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="2213d-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>  
  
 <span data-ttu-id="2213d-109">此操作中每次出现未处理的异常时，此计数器都会递增。</span><span class="sxs-lookup"><span data-stu-id="2213d-109">This counter is incremented every time there is an unhandled exception in this operation.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2213d-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="2213d-110">See also</span></span>

- [<span data-ttu-id="2213d-111">在协定和服务中指定和处理错误</span><span class="sxs-lookup"><span data-stu-id="2213d-111">Specifying and Handling Faults in Contracts and Services</span></span>](../../specifying-and-handling-faults-in-contracts-and-services.md)
