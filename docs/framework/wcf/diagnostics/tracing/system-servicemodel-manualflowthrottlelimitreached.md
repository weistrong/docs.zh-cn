---
description: 了解有关以下方面的详细信息： ManualFlowThrottleLimitReached
title: System.ServiceModel.ManualFlowThrottleLimitReached
ms.date: 03/30/2017
ms.assetid: 9aba851f-1830-493b-8e3e-60f454eb923e
ms.openlocfilehash: 90c911131259ea02023eb05a97793f00f3eb43fe
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99633330"
---
# <a name="systemservicemodelmanualflowthrottlelimitreached"></a><span data-ttu-id="5f9ea-103">System.ServiceModel.ManualFlowThrottleLimitReached</span><span class="sxs-lookup"><span data-stu-id="5f9ea-103">System.ServiceModel.ManualFlowThrottleLimitReached</span></span>

<span data-ttu-id="5f9ea-104">System.ServiceModel.ManualFlowThrottleLimitReached</span><span class="sxs-lookup"><span data-stu-id="5f9ea-104">System.ServiceModel.ManualFlowThrottleLimitReached</span></span>  
  
## <a name="description"></a><span data-ttu-id="5f9ea-105">说明</span><span class="sxs-lookup"><span data-stu-id="5f9ea-105">Description</span></span>  

 <span data-ttu-id="5f9ea-106">系统已达到为 ManualFlowControlLimit throttle 阈值设置的限制。</span><span class="sxs-lookup"><span data-stu-id="5f9ea-106">The system reached the limit set for the ManualFlowControlLimit throttle.</span></span> <span data-ttu-id="5f9ea-107">通过对 ServiceHost 或 InstanceContext 上的 ManualFlowControlLimit 属性进行适当修改，可以更改该阈值。</span><span class="sxs-lookup"><span data-stu-id="5f9ea-107">The throttle value can be changed by modifying the ManualFlowControlLimit property on either the ServiceHost or InstanceContext, as applicable.</span></span>  
  
 <span data-ttu-id="5f9ea-108">在手动流控制限制最初减少为 0 时发出此跟踪。</span><span class="sxs-lookup"><span data-stu-id="5f9ea-108">This trace is emitted when the manual flow control limit is initially reduced to 0.</span></span> <span data-ttu-id="5f9ea-109">不跟踪后续更改为 0 的情况。</span><span class="sxs-lookup"><span data-stu-id="5f9ea-109">Subsequent changes to 0 are not traced.</span></span> <span data-ttu-id="5f9ea-110">对于每个上下文只跟踪一次实例上下文上的流控制限制。</span><span class="sxs-lookup"><span data-stu-id="5f9ea-110">Flow control limit on the instance context is traced once for each context.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5f9ea-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="5f9ea-111">See also</span></span>

- [<span data-ttu-id="5f9ea-112">跟踪</span><span class="sxs-lookup"><span data-stu-id="5f9ea-112">Tracing</span></span>](index.md)
- [<span data-ttu-id="5f9ea-113">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="5f9ea-113">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="5f9ea-114">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="5f9ea-114">Administration and Diagnostics</span></span>](../index.md)
