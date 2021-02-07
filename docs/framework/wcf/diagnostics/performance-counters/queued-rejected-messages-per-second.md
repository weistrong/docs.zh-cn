---
description: 了解详细信息：每秒排队拒绝的消息数
title: 每秒拒绝的排队消息数
ms.date: 03/30/2017
ms.assetid: 77ea9aa3-b9e2-4a1d-a65e-5ca115ba0567
ms.openlocfilehash: d0d227a26a49921449786d2c9f885fac13a82bde
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99744066"
---
# <a name="queued-rejected-messages-per-second"></a><span data-ttu-id="62da4-103">每秒拒绝的排队消息数</span><span class="sxs-lookup"><span data-stu-id="62da4-103">Queued Rejected Messages Per Second</span></span>

<span data-ttu-id="62da4-104">计数器名称：Queued Messages Rejected Per Second（每秒拒绝的排队消息数）。</span><span class="sxs-lookup"><span data-stu-id="62da4-104">Counter Name: Queued Messages Rejected Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="62da4-105">说明</span><span class="sxs-lookup"><span data-stu-id="62da4-105">Description</span></span>  

 <span data-ttu-id="62da4-106">此服务中每秒被排队传输拒绝的消息数。</span><span class="sxs-lookup"><span data-stu-id="62da4-106">Number of messages that are rejected by the queued transport at this service in a second.</span></span>  
  
 <span data-ttu-id="62da4-107">此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。</span><span class="sxs-lookup"><span data-stu-id="62da4-107">This counter is of performance counter type [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10)), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="62da4-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="62da4-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
