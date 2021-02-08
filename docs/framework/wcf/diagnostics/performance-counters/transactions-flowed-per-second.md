---
description: 了解详细信息：每秒流动的事务数
title: Transactions Flowed Per Second（每秒流动的事务数）
ms.date: 03/30/2017
ms.assetid: b9f661e1-576c-48fc-9fdf-91853e0749e8
ms.openlocfilehash: f37c79e89efb8a013719f44350772919b7222a61
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99770997"
---
# <a name="transactions-flowed-per-second"></a><span data-ttu-id="cf370-103">Transactions Flowed Per Second（每秒流动的事务数）</span><span class="sxs-lookup"><span data-stu-id="cf370-103">Transactions Flowed Per Second</span></span>

<span data-ttu-id="cf370-104">计数器名称：Transactions Flowed Per Second（每秒流动的事务数）</span><span class="sxs-lookup"><span data-stu-id="cf370-104">Counter Name:  Transactions Flowed Per Second</span></span>  
  
## <a name="description"></a><span data-ttu-id="cf370-105">说明</span><span class="sxs-lookup"><span data-stu-id="cf370-105">Description</span></span>  

 <span data-ttu-id="cf370-106">一秒内向此操作流动的事务数量。</span><span class="sxs-lookup"><span data-stu-id="cf370-106">Number of transactions flowed to this operation in a second.</span></span> <span data-ttu-id="cf370-107">每当发送到此操作的消息中存在事务 ID 时，此计数器就会增加。</span><span class="sxs-lookup"><span data-stu-id="cf370-107">This counter is incremented any time a transaction ID is present in a message that is sent to the operation.</span></span>  
  
 <span data-ttu-id="cf370-108">此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。</span><span class="sxs-lookup"><span data-stu-id="cf370-108">This counter is of performance counter type [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10)), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="cf370-109">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="cf370-109">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
