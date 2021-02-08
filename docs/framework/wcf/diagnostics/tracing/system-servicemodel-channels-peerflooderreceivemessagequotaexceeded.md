---
description: 了解有关以下方面的详细信息： PeerFlooderReceiveMessageQuotaExceeded
title: System.ServiceModel.Channels.PeerFlooderReceiveMessageQuotaExceeded
ms.date: 03/30/2017
ms.assetid: b8371d0a-843e-440b-b86a-6996db131cb0
ms.openlocfilehash: 8ad164b253491f3a533c4828cd76f915eb5aed68
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99780864"
---
# <a name="systemservicemodelchannelspeerflooderreceivemessagequotaexceeded"></a><span data-ttu-id="356e5-103">System.ServiceModel.Channels.PeerFlooderReceiveMessageQuotaExceeded</span><span class="sxs-lookup"><span data-stu-id="356e5-103">System.ServiceModel.Channels.PeerFlooderReceiveMessageQuotaExceeded</span></span>

<span data-ttu-id="356e5-104">消息的入站接收速率过高。</span><span class="sxs-lookup"><span data-stu-id="356e5-104">The inbound receive rate of messages is too high.</span></span>  
  
## <a name="description"></a><span data-ttu-id="356e5-105">说明</span><span class="sxs-lookup"><span data-stu-id="356e5-105">Description</span></span>  

 <span data-ttu-id="356e5-106">此跟踪在尝试处理入站消息时发生。</span><span class="sxs-lookup"><span data-stu-id="356e5-106">This trace occurs when attempting to process inbound messages.</span></span> <span data-ttu-id="356e5-107">无法将消息转发给特定的邻居，因为已经超过了为该邻居设置的配额。</span><span class="sxs-lookup"><span data-stu-id="356e5-107">A message could not be forwarded to a specific neighbor because the quota set for that neighbor has been exceeded.</span></span> <span data-ttu-id="356e5-108">当无响应邻居无法清除为该邻居挂起的积压工作 (backlog) 消息时会发生此情况。</span><span class="sxs-lookup"><span data-stu-id="356e5-108">This occurs when an unresponsive neighbor fails to clear a backlog of messages pending for that neighbor.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="356e5-109">疑难解答</span><span class="sxs-lookup"><span data-stu-id="356e5-109">Troubleshooting</span></span>  

 <span data-ttu-id="356e5-110">降低在网格中发送消息的速率。</span><span class="sxs-lookup"><span data-stu-id="356e5-110">Reduce the rate at which messages are sent within the mesh.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="356e5-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="356e5-111">See also</span></span>

- [<span data-ttu-id="356e5-112">跟踪</span><span class="sxs-lookup"><span data-stu-id="356e5-112">Tracing</span></span>](index.md)
- [<span data-ttu-id="356e5-113">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="356e5-113">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="356e5-114">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="356e5-114">Administration and Diagnostics</span></span>](../index.md)
