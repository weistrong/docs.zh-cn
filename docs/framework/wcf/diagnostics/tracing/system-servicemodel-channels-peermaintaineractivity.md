---
description: 了解有关以下方面的详细信息： PeerMaintainerActivity
title: System.ServiceModel.Channels.PeerMaintainerActivity
ms.date: 03/30/2017
ms.assetid: ef28d086-d7fb-4e81-82e9-45a54647783b
ms.openlocfilehash: da4e4cf87da808cb6779445b6507b51d098132b3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99780876"
---
# <a name="systemservicemodelchannelspeermaintaineractivity"></a><span data-ttu-id="eeb7f-103">System.ServiceModel.Channels.PeerMaintainerActivity</span><span class="sxs-lookup"><span data-stu-id="eeb7f-103">System.ServiceModel.Channels.PeerMaintainerActivity</span></span>

<span data-ttu-id="eeb7f-104">PeerMaintainer 模块正在执行特定操作（详细信息包含在跟踪消息正文中）。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-104">The PeerMaintainer module is performing a specific operation (details contained within the trace message body).</span></span>  
  
## <a name="description"></a><span data-ttu-id="eeb7f-105">说明</span><span class="sxs-lookup"><span data-stu-id="eeb7f-105">Description</span></span>  

 <span data-ttu-id="eeb7f-106">此跟踪在各种 PeerMaintainer 操作期间发生。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-106">This trace occurs during various PeerMaintainer operations.</span></span>  
  
 <span data-ttu-id="eeb7f-107">PeerMaintainer 是 PeerNode 的内部组件。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-107">PeerMaintainer is an internal component of PeerNode.</span></span> <span data-ttu-id="eeb7f-108">每隔一分钟，或者每当接收到 32 条消息，该组件就向它的邻居发送一条 LinkUtility 消息，该消息中包含有关交换了多少条消息以及其中有多少条有用消息（不重复也未经篡改的消息）的统计信息。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-108">Every minute, or every 32 messages received, it sends a LinkUtility message to its neighbors with statistics about how many messages are exchanged and how many are useful (non-duplicates, untampered).</span></span> <span data-ttu-id="eeb7f-109">这有助于确定特定邻居的链接利用率。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-109">This helps determine a particular neighbor's Link Utility.</span></span> <span data-ttu-id="eeb7f-110">该维护组件大约每五分钟检查一次邻居连接的运行状况。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-110">Approximately every five minutes, the maintainer checks the health of neighbor connections.</span></span> <span data-ttu-id="eeb7f-111">如果邻居连接的数目超过理想的数值，该维护组件将去除用处最小的一些连接。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-111">If the number of neighbor connections exceeds the ideal amount, the maintainer prunes off the least useful connections.</span></span> <span data-ttu-id="eeb7f-112">如果连接数目不足，该维护组件将获取新的连接。</span><span class="sxs-lookup"><span data-stu-id="eeb7f-112">If there are not enough connections, the maintainer acquires new connections.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eeb7f-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="eeb7f-113">See also</span></span>

- [<span data-ttu-id="eeb7f-114">跟踪</span><span class="sxs-lookup"><span data-stu-id="eeb7f-114">Tracing</span></span>](index.md)
- [<span data-ttu-id="eeb7f-115">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="eeb7f-115">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="eeb7f-116">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="eeb7f-116">Administration and Diagnostics</span></span>](../index.md)
