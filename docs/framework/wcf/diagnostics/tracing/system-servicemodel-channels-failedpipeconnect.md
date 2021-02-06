---
description: 了解有关以下方面的详细信息： FailedPipeConnect
title: System.ServiceModel.Channels.FailedPipeConnect
ms.date: 03/30/2017
ms.assetid: 9a827e0f-fb91-46bb-bd54-926d4b74d8a6
ms.openlocfilehash: dbbb3ba2848eaefe70a6d6308daecf84e0a8c7a0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99644471"
---
# <a name="systemservicemodelchannelsfailedpipeconnect"></a><span data-ttu-id="e21d6-103">System.ServiceModel.Channels.FailedPipeConnect</span><span class="sxs-lookup"><span data-stu-id="e21d6-103">System.ServiceModel.Channels.FailedPipeConnect</span></span>

<span data-ttu-id="e21d6-104">尝试连接到指定的管道终结点失败。</span><span class="sxs-lookup"><span data-stu-id="e21d6-104">An attempt to connect to the named pipe endpoint failed.</span></span> <span data-ttu-id="e21d6-105">将在指定的超时期限内再次进行尝试。</span><span class="sxs-lookup"><span data-stu-id="e21d6-105">Another attempt is made within the specified timeout period.</span></span>  
  
## <a name="description"></a><span data-ttu-id="e21d6-106">说明</span><span class="sxs-lookup"><span data-stu-id="e21d6-106">Description</span></span>  

 <span data-ttu-id="e21d6-107">此信息跟踪指示未能连接到指定的管道终结点。</span><span class="sxs-lookup"><span data-stu-id="e21d6-107">This informational trace indicates a failure to connect to a named pipe endpoint.</span></span> <span data-ttu-id="e21d6-108">如果未找到指定的管道终结点或指定的管道终结点正忙，则可能会发生此情况。</span><span class="sxs-lookup"><span data-stu-id="e21d6-108">This could happen if the named pipe endpoint is not found or is busy.</span></span> <span data-ttu-id="e21d6-109">将进行更多的尝试（两次尝试之间的时间较短），直到尝试成功或 OpenTimeout 过期。</span><span class="sxs-lookup"><span data-stu-id="e21d6-109">Additional attempts are made, each separated by a short amount of time, until one succeeds or the OpenTimeout expires.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e21d6-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="e21d6-110">See also</span></span>

- [<span data-ttu-id="e21d6-111">跟踪</span><span class="sxs-lookup"><span data-stu-id="e21d6-111">Tracing</span></span>](index.md)
- [<span data-ttu-id="e21d6-112">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="e21d6-112">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="e21d6-113">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="e21d6-113">Administration and Diagnostics</span></span>](../index.md)
