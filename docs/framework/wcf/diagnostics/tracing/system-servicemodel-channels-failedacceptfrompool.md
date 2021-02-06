---
description: 了解有关以下方面的详细信息： FailedAcceptFromPool
title: System.ServiceModel.Channels.FailedAcceptFromPool
ms.date: 03/30/2017
ms.assetid: d535b1b5-ee58-45e8-b400-7d9570f4eb9a
ms.openlocfilehash: 1b3c15594611726fd4872197b97ad4ed56c085c4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99635254"
---
# <a name="systemservicemodelchannelsfailedacceptfrompool"></a><span data-ttu-id="a96b7-103">System.ServiceModel.Channels.FailedAcceptFromPool</span><span class="sxs-lookup"><span data-stu-id="a96b7-103">System.ServiceModel.Channels.FailedAcceptFromPool</span></span>

<span data-ttu-id="a96b7-104">尝试重新使用已入池连接失败。</span><span class="sxs-lookup"><span data-stu-id="a96b7-104">An attempt to reuse a pooled connection failed.</span></span> <span data-ttu-id="a96b7-105">将在指定的超时期限内再次进行尝试。</span><span class="sxs-lookup"><span data-stu-id="a96b7-105">Another attempt is made within the specified timeout period.</span></span>  
  
## <a name="description"></a><span data-ttu-id="a96b7-106">说明</span><span class="sxs-lookup"><span data-stu-id="a96b7-106">Description</span></span>  

 <span data-ttu-id="a96b7-107">此信息跟踪指示尝试重新使用已入池连接时发生错误。</span><span class="sxs-lookup"><span data-stu-id="a96b7-107">This informational trace indicates that an error has occurred while attempting to reuse a pooled connection.</span></span> <span data-ttu-id="a96b7-108">之所以发生此情况，原因在于已入池连接不兼容、未就绪或仍处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="a96b7-108">This could happen because the pooled connection was not compatible, ready, or still active.</span></span> <span data-ttu-id="a96b7-109">在给定的超时范围内将进行重新使用其他已入池连接的更多尝试，如果未找到任何可使用的连接，则会创建新的连接。</span><span class="sxs-lookup"><span data-stu-id="a96b7-109">Additional attempts to reuse other pooled connection are made within a given timeout and a new connection is created in case no usable connections are found.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a96b7-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="a96b7-110">See also</span></span>

- [<span data-ttu-id="a96b7-111">跟踪</span><span class="sxs-lookup"><span data-stu-id="a96b7-111">Tracing</span></span>](index.md)
- [<span data-ttu-id="a96b7-112">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="a96b7-112">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="a96b7-113">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="a96b7-113">Administration and Diagnostics</span></span>](../index.md)
