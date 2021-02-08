---
description: 了解详细信息：每秒有疑问的事务操作
title: Transacted Operations In Doubt Per Second（每秒不确定的事务处理操作次数）
ms.date: 03/30/2017
ms.assetid: 7e6b0716-c107-42e5-a21d-31d988e7a691
ms.openlocfilehash: e4f8b8c9db1c92ea4348763cdc4a633f058dbaf2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99771088"
---
# <a name="transacted-operations-in-doubt-per-second"></a><span data-ttu-id="00f91-103">Transacted Operations In Doubt Per Second（每秒不确定的事务处理操作次数）</span><span class="sxs-lookup"><span data-stu-id="00f91-103">Transacted Operations In Doubt Per Second</span></span>

<span data-ttu-id="00f91-104">计数器名称：Transacted Operations In Doubt Per Second（每秒不确定的事务处理操作次数）。</span><span class="sxs-lookup"><span data-stu-id="00f91-104">Counter Name: Transacted Operations In Doubt Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="00f91-105">说明</span><span class="sxs-lookup"><span data-stu-id="00f91-105">Description</span></span>  

 <span data-ttu-id="00f91-106">此服务中每秒产生不确定结果的事务性操作的数量。</span><span class="sxs-lookup"><span data-stu-id="00f91-106">Number of transactional operations with an in-doubt outcome in this service in a second.</span></span>  
  
 <span data-ttu-id="00f91-107">此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。</span><span class="sxs-lookup"><span data-stu-id="00f91-107">This counter is of performance counter type [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10)), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="00f91-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="00f91-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
