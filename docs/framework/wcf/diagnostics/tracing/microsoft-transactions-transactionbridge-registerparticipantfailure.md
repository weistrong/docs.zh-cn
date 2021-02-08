---
description: 了解有关以下内容的详细信息： TransactionBridge. RegisterParticipantFailure
title: Microsoft.Transactions.TransactionBridge.RegisterParticipantFailure
ms.date: 03/30/2017
ms.assetid: 3a4ead79-8550-4037-84e3-fd70ff56e001
ms.openlocfilehash: e930ee66720a9f397999d729e8d680fce9a37e29
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99770620"
---
# <a name="microsofttransactionstransactionbridgeregisterparticipantfailure"></a><span data-ttu-id="76a09-103">Microsoft.Transactions.TransactionBridge.RegisterParticipantFailure</span><span class="sxs-lookup"><span data-stu-id="76a09-103">Microsoft.Transactions.TransactionBridge.RegisterParticipantFailure</span></span>

<span data-ttu-id="76a09-104">WS-AT 协议服务未能注册某个控制协议的参与者。</span><span class="sxs-lookup"><span data-stu-id="76a09-104">The WS-AT protocol service failed to register a participant for a control protocol.</span></span>  
  
## <a name="description"></a><span data-ttu-id="76a09-105">说明</span><span class="sxs-lookup"><span data-stu-id="76a09-105">Description</span></span>  

 <span data-ttu-id="76a09-106">跟踪 MSDTC 是否检测到无效的注册请求。</span><span class="sxs-lookup"><span data-stu-id="76a09-106">Traced if MSDTC detects an invalid Registration request.</span></span> <span data-ttu-id="76a09-107">这可能是由于多个完成注册请求和内部错误造成的。</span><span class="sxs-lookup"><span data-stu-id="76a09-107">This can be caused by  multiple Completion registration requests and internal errors.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="76a09-108">疑难解答</span><span class="sxs-lookup"><span data-stu-id="76a09-108">Troubleshooting</span></span>  

 <span data-ttu-id="76a09-109">不要尝试多次“为完成而注册”。</span><span class="sxs-lookup"><span data-stu-id="76a09-109">Do not try to Register for Completion more than once.</span></span>  <span data-ttu-id="76a09-110">此外，检查跟踪消息中的状态字符串以确定是否存在任何可操作的项。</span><span class="sxs-lookup"><span data-stu-id="76a09-110">Also, inspect the status string within the trace message to determine if any actionable item exists.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="76a09-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="76a09-111">See also</span></span>

- [<span data-ttu-id="76a09-112">跟踪</span><span class="sxs-lookup"><span data-stu-id="76a09-112">Tracing</span></span>](index.md)
- [<span data-ttu-id="76a09-113">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="76a09-113">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="76a09-114">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="76a09-114">Administration and Diagnostics</span></span>](../index.md)
