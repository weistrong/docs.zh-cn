---
description: 了解有关以下内容的详细信息： TransactionBridge. CommitMessageRetry
title: Microsoft.Transactions.TransactionBridge.CommitMessageRetry
ms.date: 03/30/2017
ms.assetid: 4abe01f0-6398-4fba-b2f3-c054b7f7e971
ms.openlocfilehash: 8f45463ac31c210acd8534df2c4e1ef2922f1c8e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99720600"
---
# <a name="microsofttransactionstransactionbridgecommitmessageretry"></a><span data-ttu-id="cdb8a-103">Microsoft.Transactions.TransactionBridge.CommitMessageRetry</span><span class="sxs-lookup"><span data-stu-id="cdb8a-103">Microsoft.Transactions.TransactionBridge.CommitMessageRetry</span></span>

<span data-ttu-id="cdb8a-104">已向无反应参与者发送提交消息重试。</span><span class="sxs-lookup"><span data-stu-id="cdb8a-104">A commit message retry was sent to an unresponsive participant.</span></span>  
  
## <a name="description"></a><span data-ttu-id="cdb8a-105">说明</span><span class="sxs-lookup"><span data-stu-id="cdb8a-105">Description</span></span>  

 <span data-ttu-id="cdb8a-106">如果本地事务管理器在给定时间内未收到响应，因而需要向从属参与者重新发送“提交”消息，则进行跟踪。</span><span class="sxs-lookup"><span data-stu-id="cdb8a-106">Traced if the local Transaction Manager needed to resend a Commit message to a subordinate participant because it did not receive a response in a given amount of time.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="cdb8a-107">疑难解答</span><span class="sxs-lookup"><span data-stu-id="cdb8a-107">Troubleshooting</span></span>  

 <span data-ttu-id="cdb8a-108">调查导致响应未及时传送的潜在网络或产品问题。</span><span class="sxs-lookup"><span data-stu-id="cdb8a-108">Investigate potential network or product issues that prevent the response from being delivered on time.</span></span>  <span data-ttu-id="cdb8a-109">如果看到很多这样的消息，可能表明基础结构有问题或响应时间异常长。</span><span class="sxs-lookup"><span data-stu-id="cdb8a-109">If many of these messages are seen, it can indicate infrastructure problems or abnormally long response times.</span></span> <span data-ttu-id="cdb8a-110">这两种问题都会明显降低系统中事务的吞吐量。</span><span class="sxs-lookup"><span data-stu-id="cdb8a-110">Both issues will drastically reduce the throughput of transactions within the system.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cdb8a-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="cdb8a-111">See also</span></span>

- [<span data-ttu-id="cdb8a-112">跟踪</span><span class="sxs-lookup"><span data-stu-id="cdb8a-112">Tracing</span></span>](index.md)
- [<span data-ttu-id="cdb8a-113">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="cdb8a-113">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="cdb8a-114">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="cdb8a-114">Administration and Diagnostics</span></span>](../index.md)
