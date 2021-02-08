---
description: 了解有关以下内容的详细信息： TransactionBridge. ReplayMessageRetry
title: Microsoft.Transactions.TransactionBridge.ReplayMessageRetry
ms.date: 03/30/2017
ms.assetid: e5b820ae-504d-405a-926a-9effa41d2369
ms.openlocfilehash: e4de1416fab2cf7098d0276b6130999c01ea6e3e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803251"
---
# <a name="microsofttransactionstransactionbridgereplaymessageretry"></a><span data-ttu-id="4b54a-103">Microsoft.Transactions.TransactionBridge.ReplayMessageRetry</span><span class="sxs-lookup"><span data-stu-id="4b54a-103">Microsoft.Transactions.TransactionBridge.ReplayMessageRetry</span></span>

<span data-ttu-id="4b54a-104">已向无响应的协调程序发送重播消息重试。</span><span class="sxs-lookup"><span data-stu-id="4b54a-104">A replay message retry was sent to an unresponsive coordinator.</span></span>  
  
## <a name="description"></a><span data-ttu-id="4b54a-105">说明</span><span class="sxs-lookup"><span data-stu-id="4b54a-105">Description</span></span>  

 <span data-ttu-id="4b54a-106">如果本地事务管理器因未在给定的时间内收到响应而需要向上级协调程序重新发送重播消息，则进行跟踪。</span><span class="sxs-lookup"><span data-stu-id="4b54a-106">Traced if the local Transaction Manager needed to resend a Replay message to a superior coordinator because it did not receive a response in a given amount of time.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="4b54a-107">疑难解答</span><span class="sxs-lookup"><span data-stu-id="4b54a-107">Troubleshooting</span></span>  

 <span data-ttu-id="4b54a-108">调查导致响应未及时传送的潜在网络或产品问题。</span><span class="sxs-lookup"><span data-stu-id="4b54a-108">Investigate potential network or product issues that prevent the response from being delivered on time.</span></span>  <span data-ttu-id="4b54a-109">如果看到很多这样的消息，可能表明基础结构有问题或响应时间异常长。</span><span class="sxs-lookup"><span data-stu-id="4b54a-109">If many of these messages are seen, it can indicate infrastructure problems or abnormally long response times.</span></span> <span data-ttu-id="4b54a-110">这两种问题都会明显降低系统中事务的吞吐量。</span><span class="sxs-lookup"><span data-stu-id="4b54a-110">Both issues will drastically reduce the throughput of transactions within the system.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4b54a-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="4b54a-111">See also</span></span>

- [<span data-ttu-id="4b54a-112">跟踪</span><span class="sxs-lookup"><span data-stu-id="4b54a-112">Tracing</span></span>](index.md)
- [<span data-ttu-id="4b54a-113">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="4b54a-113">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="4b54a-114">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="4b54a-114">Administration and Diagnostics</span></span>](../index.md)
