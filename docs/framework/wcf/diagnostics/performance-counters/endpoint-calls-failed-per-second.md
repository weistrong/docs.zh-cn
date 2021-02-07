---
description: 了解详细信息： Endpoint：每秒调用失败数
title: 终结点：Calls Failed Per Second（每秒失败的调用次数）
ms.date: 03/30/2017
ms.assetid: bcbe9da4-c8dd-4e27-b630-11611adc7580
ms.openlocfilehash: 262f0fdf0750e8fdb179d41d1a99788784270023
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99759635"
---
# <a name="endpoint-calls-failed-per-second"></a><span data-ttu-id="e3f67-103">终结点：Calls Failed Per Second（每秒失败的调用次数）</span><span class="sxs-lookup"><span data-stu-id="e3f67-103">Endpoint: Calls Failed Per Second</span></span>

<span data-ttu-id="e3f67-104">计数器名称：Calls Failed Per Second（每秒失败的调用次数）。</span><span class="sxs-lookup"><span data-stu-id="e3f67-104">Counter Name: Calls Failed Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="e3f67-105">说明</span><span class="sxs-lookup"><span data-stu-id="e3f67-105">Description</span></span>  

 <span data-ttu-id="e3f67-106">一秒钟内通过此终结点收到且具有未处理的异常的调用次数。</span><span class="sxs-lookup"><span data-stu-id="e3f67-106">Number of calls that have unhandled exceptions and are received by this endpoint in a second.</span></span>  
  
 <span data-ttu-id="e3f67-107">此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。</span><span class="sxs-lookup"><span data-stu-id="e3f67-107">This counter is of performance counter type [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10)), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="e3f67-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="e3f67-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>  
  
 <span data-ttu-id="e3f67-109">每当此终结点处有未处理的异常时，此计数器就会增加。</span><span class="sxs-lookup"><span data-stu-id="e3f67-109">This counter is incremented every time there is an unhandled exception at this endpoint.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e3f67-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="e3f67-110">See also</span></span>

- [<span data-ttu-id="e3f67-111">在协定和服务中指定和处理错误</span><span class="sxs-lookup"><span data-stu-id="e3f67-111">Specifying and Handling Faults in Contracts and Services</span></span>](../../specifying-and-handling-faults-in-contracts-and-services.md)
