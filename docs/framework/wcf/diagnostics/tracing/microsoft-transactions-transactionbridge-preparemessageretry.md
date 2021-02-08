---
description: 了解有关以下内容的详细信息： TransactionBridge. PrepareMessageRetry
title: Microsoft.Transactions.TransactionBridge.PrepareMessageRetry
ms.date: 03/30/2017
ms.assetid: ada4baa5-b60d-46b8-ad46-4d69f8d8a9fa
ms.openlocfilehash: 7555336f1082eb097017f9440015f6ab201cdeae
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99770776"
---
# <a name="microsofttransactionstransactionbridgepreparemessageretry"></a><span data-ttu-id="8f7bf-103">Microsoft.Transactions.TransactionBridge.PrepareMessageRetry</span><span class="sxs-lookup"><span data-stu-id="8f7bf-103">Microsoft.Transactions.TransactionBridge.PrepareMessageRetry</span></span>

<span data-ttu-id="8f7bf-104">准备消息重试发送到的参与者无响应。</span><span class="sxs-lookup"><span data-stu-id="8f7bf-104">A prepare message retry was sent to an unresponsive participant.</span></span>  
  
## <a name="description"></a><span data-ttu-id="8f7bf-105">说明</span><span class="sxs-lookup"><span data-stu-id="8f7bf-105">Description</span></span>  

 <span data-ttu-id="8f7bf-106">如果本地事务管理器因为在指定的时间内没有收到响应，而需要向从属参与者重新发行一条 Prepare 消息，就会进行此跟踪。</span><span class="sxs-lookup"><span data-stu-id="8f7bf-106">Traced if the local Transaction Manager needed to resend a Prepare message to a subordinate participant because it did not receive a response in a given amount of time.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="8f7bf-107">疑难解答</span><span class="sxs-lookup"><span data-stu-id="8f7bf-107">Troubleshooting</span></span>  

 <span data-ttu-id="8f7bf-108">调查导致响应未及时传送的潜在网络或产品问题。</span><span class="sxs-lookup"><span data-stu-id="8f7bf-108">Investigate potential network or product issues that prevent the response from being delivered on time.</span></span>  <span data-ttu-id="8f7bf-109">如果看到很多这样的消息，可能表明基础结构有问题或响应时间异常长。</span><span class="sxs-lookup"><span data-stu-id="8f7bf-109">If many of these messages are seen, it can indicate infrastructure problems or abnormally long response times.</span></span> <span data-ttu-id="8f7bf-110">这两种问题都会明显降低系统中事务的吞吐量。</span><span class="sxs-lookup"><span data-stu-id="8f7bf-110">Both issues can drastically reduce the throughput of transactions within the system.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8f7bf-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="8f7bf-111">See also</span></span>

- [<span data-ttu-id="8f7bf-112">跟踪</span><span class="sxs-lookup"><span data-stu-id="8f7bf-112">Tracing</span></span>](index.md)
- [<span data-ttu-id="8f7bf-113">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="8f7bf-113">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="8f7bf-114">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="8f7bf-114">Administration and Diagnostics</span></span>](../index.md)
