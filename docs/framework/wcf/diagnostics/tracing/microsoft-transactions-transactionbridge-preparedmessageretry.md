---
description: 了解有关以下内容的详细信息： TransactionBridge. PreparedMessageRetry
title: Microsoft.Transactions.TransactionBridge.PreparedMessageRetry
ms.date: 03/30/2017
ms.assetid: 2194292d-bf5f-4aef-9336-cd3c4795cb71
ms.openlocfilehash: 99106493f0eec900875a713b439111fadb150c62
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99677270"
---
# <a name="microsofttransactionstransactionbridgepreparedmessageretry"></a><span data-ttu-id="fb8bc-103">Microsoft.Transactions.TransactionBridge.PreparedMessageRetry</span><span class="sxs-lookup"><span data-stu-id="fb8bc-103">Microsoft.Transactions.TransactionBridge.PreparedMessageRetry</span></span>

<span data-ttu-id="fb8bc-104">准备的消息重试发送到的协调程序无响应。</span><span class="sxs-lookup"><span data-stu-id="fb8bc-104">A prepared message retry was sent to an unresponsive coordinator.</span></span>  
  
## <a name="description"></a><span data-ttu-id="fb8bc-105">说明</span><span class="sxs-lookup"><span data-stu-id="fb8bc-105">Description</span></span>  

 <span data-ttu-id="fb8bc-106">跟踪本地事务管理器在给定时间内未接收到响应时是否需要向上级协调器重新发送准备的消息/</span><span class="sxs-lookup"><span data-stu-id="fb8bc-106">Traced if the local Transaction Manager needed to resend a Prepared message to a superior coordinator because it did not receive a response in a given amount of time/</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="fb8bc-107">疑难解答</span><span class="sxs-lookup"><span data-stu-id="fb8bc-107">Troubleshooting</span></span>  

 <span data-ttu-id="fb8bc-108">调查导致响应未及时传送的潜在网络或产品问题。</span><span class="sxs-lookup"><span data-stu-id="fb8bc-108">Investigate potential network or product issues that prevent the response from being delivered on time.</span></span>  <span data-ttu-id="fb8bc-109">如果看到很多这样的消息，可能表明基础结构有问题或响应时间异常长。</span><span class="sxs-lookup"><span data-stu-id="fb8bc-109">If many of these messages are seen, it can indicate infrastructure problems or abnormally long response times.</span></span> <span data-ttu-id="fb8bc-110">这两种问题都会明显降低系统中事务的吞吐量。</span><span class="sxs-lookup"><span data-stu-id="fb8bc-110">Both issues will drastically reduce the throughput of transactions within the system.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fb8bc-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="fb8bc-111">See also</span></span>

- [<span data-ttu-id="fb8bc-112">跟踪</span><span class="sxs-lookup"><span data-stu-id="fb8bc-112">Tracing</span></span>](index.md)
- [<span data-ttu-id="fb8bc-113">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="fb8bc-113">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="fb8bc-114">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="fb8bc-114">Administration and Diagnostics</span></span>](../index.md)
