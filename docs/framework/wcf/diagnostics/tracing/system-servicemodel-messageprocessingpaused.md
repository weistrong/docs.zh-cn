---
description: 了解有关以下方面的详细信息： MessageProcessingPaused
title: System.ServiceModel.MessageProcessingPaused
ms.date: 03/30/2017
ms.assetid: 36b5302a-93cc-478a-9bb2-8a1601fba1df
ms.openlocfilehash: 77e4742bc5617904136b2ddd9cb90fe886d38b10
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99716173"
---
# <a name="systemservicemodelmessageprocessingpaused"></a><span data-ttu-id="374bc-103">System.ServiceModel.MessageProcessingPaused</span><span class="sxs-lookup"><span data-stu-id="374bc-103">System.ServiceModel.MessageProcessingPaused</span></span>

<span data-ttu-id="374bc-104">System.ServiceModel.MessageProcessingPaused</span><span class="sxs-lookup"><span data-stu-id="374bc-104">System.ServiceModel.MessageProcessingPaused</span></span>  
  
## <a name="description"></a><span data-ttu-id="374bc-105">说明</span><span class="sxs-lookup"><span data-stu-id="374bc-105">Description</span></span>  

 <span data-ttu-id="374bc-106">线程在处理消息时切换。</span><span class="sxs-lookup"><span data-stu-id="374bc-106">The threads were switched while processing a message.</span></span>  
  
 <span data-ttu-id="374bc-107">消息处理可以因为以下原因而暂停：</span><span class="sxs-lookup"><span data-stu-id="374bc-107">Message processing can be paused by the following reasons:</span></span>  
  
- <span data-ttu-id="374bc-108">ConcurrencyMode 为 single 或 reentrant，并且服务正在处理另一条消息。</span><span class="sxs-lookup"><span data-stu-id="374bc-108">ConcurrencyMode is single or reentrant, and the service is processing another message.</span></span>  
  
- <span data-ttu-id="374bc-109">启用了事务，并且服务正在处理另一个事务。</span><span class="sxs-lookup"><span data-stu-id="374bc-109">Transaction is enabled and the service is processing another transaction.</span></span>  
  
- <span data-ttu-id="374bc-110">同步上下文不是最新。</span><span class="sxs-lookup"><span data-stu-id="374bc-110">Synchronization context is not current.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="374bc-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="374bc-111">See also</span></span>

- [<span data-ttu-id="374bc-112">跟踪</span><span class="sxs-lookup"><span data-stu-id="374bc-112">Tracing</span></span>](index.md)
- [<span data-ttu-id="374bc-113">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="374bc-113">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="374bc-114">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="374bc-114">Administration and Diagnostics</span></span>](../index.md)
