---
description: 了解详细信息：每秒丢弃的可靠消息传递消息数
title: Reliable Messaging Messages Dropped Per Second（每秒丢弃的可靠消息传递消息数）
ms.date: 03/30/2017
ms.assetid: a11b0b80-b242-48e1-b0bb-7f756db5486b
ms.openlocfilehash: 6132316f100cecdba357a6da071e23de8c9a2181
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99655105"
---
# <a name="reliable-messaging-messages-dropped-per-second"></a><span data-ttu-id="a1028-103">Reliable Messaging Messages Dropped Per Second（每秒丢弃的可靠消息传递消息数）</span><span class="sxs-lookup"><span data-stu-id="a1028-103">Reliable Messaging Messages Dropped Per Second</span></span>

<span data-ttu-id="a1028-104">计数器名称：Reliable Messaging Sessions Dropped Per Second（每秒丢弃的可靠消息会话数）。</span><span class="sxs-lookup"><span data-stu-id="a1028-104">Counter Name: Reliable Messaging Sessions Dropped Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="a1028-105">说明</span><span class="sxs-lookup"><span data-stu-id="a1028-105">Description</span></span>  

 <span data-ttu-id="a1028-106">此服务上每秒钟丢弃的可靠传送消息总数。</span><span class="sxs-lookup"><span data-stu-id="a1028-106">Total number of reliable messaging messages that have been dropped in this service in a second.</span></span>  
  
 <span data-ttu-id="a1028-107">此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。</span><span class="sxs-lookup"><span data-stu-id="a1028-107">This counter is of performance counter type [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10)), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="a1028-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="a1028-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
