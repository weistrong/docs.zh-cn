---
description: 了解详细信息：服务：每秒未授权的安全调用数
title: 服务：Security Calls Not Authorized Per Second（每秒未授权的安全调用次数）
ms.date: 03/30/2017
ms.assetid: 1eeade5a-ea62-4757-b1f9-1b1b1746abd1
ms.openlocfilehash: 7203b62a1dd2f01aabd8502c992d357742ddc4e7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99635696"
---
# <a name="service-security-calls-not-authorized-per-second"></a><span data-ttu-id="315e5-103">服务：Security Calls Not Authorized Per Second（每秒未授权的安全调用次数）</span><span class="sxs-lookup"><span data-stu-id="315e5-103">Service: Security Calls Not Authorized Per Second</span></span>

<span data-ttu-id="315e5-104">计数器名称：每秒未授权的安全调用次数</span><span class="sxs-lookup"><span data-stu-id="315e5-104">Counter name: Security Calls Not Authorized Per Second</span></span>  
  
## <a name="description"></a><span data-ttu-id="315e5-105">说明</span><span class="sxs-lookup"><span data-stu-id="315e5-105">Description</span></span>  

 <span data-ttu-id="315e5-106">一秒钟内来自有效用户并得到适当保护，但未授权用户执行特定任务的传入消息的数量。</span><span class="sxs-lookup"><span data-stu-id="315e5-106">Number of incoming messages in one second, which are from a valid user and protected properly, but the user is not authorized to do specific tasks.</span></span>  
  
 <span data-ttu-id="315e5-107">当 <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccess%2A> 方法返回 `false` 时，此计数器将递增。</span><span class="sxs-lookup"><span data-stu-id="315e5-107">This counter is incremented when the <xref:System.ServiceModel.ServiceAuthorizationManager.CheckAccess%2A> method returns `false`.</span></span>  
  
 <span data-ttu-id="315e5-108">此计数器的性能计数器类型 [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10))，其值使用以下公式进行计算。</span><span class="sxs-lookup"><span data-stu-id="315e5-108">This counter is of performance counter type [PERF_COUNTER_COUNTER](/previous-versions/windows/it-pro/windows-server-2003/cc740048(v=ws.10)), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="315e5-109">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="315e5-109">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
