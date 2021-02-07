---
description: 了解详细信息： Endpoint：每秒调用数
title: 终结点：Calls Per Second（每秒调用次数）
ms.date: 03/30/2017
ms.assetid: ca0fc06d-d68f-4236-bd5f-c7ff6214acdd
ms.openlocfilehash: 10e3cb892119999225abaa8b85ea59065650795d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99759570"
---
# <a name="endpoint-calls-per-second"></a><span data-ttu-id="4144c-103">终结点：Calls Per Second（每秒调用次数）</span><span class="sxs-lookup"><span data-stu-id="4144c-103">Endpoint: Calls Per Second</span></span>

<span data-ttu-id="4144c-104">计数器名称：Calls Per Second（每秒调用次数）</span><span class="sxs-lookup"><span data-stu-id="4144c-104">Counter Name: Calls Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="4144c-105">说明</span><span class="sxs-lookup"><span data-stu-id="4144c-105">Description</span></span>  

 <span data-ttu-id="4144c-106">一秒内对此终结点的调用次数。</span><span class="sxs-lookup"><span data-stu-id="4144c-106">Number of calls to this endpoint in a second.</span></span>  
  
 <span data-ttu-id="4144c-107">此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。</span><span class="sxs-lookup"><span data-stu-id="4144c-107">This counter is of performance counter type [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10)), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="4144c-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="4144c-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
