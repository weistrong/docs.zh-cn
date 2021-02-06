---
description: 了解有关以下内容的详细信息： TransactionBridge. DurableParticipantReplayWhilePreparing
title: Microsoft.Transactions.TransactionBridge.DurableParticipantReplayWhilePreparing
ms.date: 03/30/2017
ms.assetid: 10ef3876-6f8e-4d4e-8444-f47847b64795
ms.openlocfilehash: fcaa50dd4faa548cad8ff085f1c66f94c63bd010
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99635657"
---
# <a name="microsofttransactionstransactionbridgedurableparticipantreplaywhilepreparing"></a><span data-ttu-id="f8bb8-103">Microsoft.Transactions.TransactionBridge.DurableParticipantReplayWhilePreparing</span><span class="sxs-lookup"><span data-stu-id="f8bb8-103">Microsoft.Transactions.TransactionBridge.DurableParticipantReplayWhilePreparing</span></span>

<span data-ttu-id="f8bb8-104">WS-AT 协议服务从不响应 Prepare 的持久参与者接收到重播消息。</span><span class="sxs-lookup"><span data-stu-id="f8bb8-104">The WS-AT protocol service received a Replay message from a durable participant, which did not respond to Prepare.</span></span> <span data-ttu-id="f8bb8-105">因此，中止了事务。</span><span class="sxs-lookup"><span data-stu-id="f8bb8-105">Consequently, the transaction was aborted.</span></span>  
  
## <a name="description"></a><span data-ttu-id="f8bb8-106">说明</span><span class="sxs-lookup"><span data-stu-id="f8bb8-106">Description</span></span>  

 <span data-ttu-id="f8bb8-107">如果持久参与者仍然在准备时接收到重播消息，则进行跟踪。</span><span class="sxs-lookup"><span data-stu-id="f8bb8-107">Traced if a Replay message is received while a Durable participant is still Preparing.</span></span> <span data-ttu-id="f8bb8-108">这是此状态的非法消息，将中止事务。</span><span class="sxs-lookup"><span data-stu-id="f8bb8-108">This is an illegal message for this state and the transaction is going to be aborted.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="f8bb8-109">疑难解答</span><span class="sxs-lookup"><span data-stu-id="f8bb8-109">Troubleshooting</span></span>

<span data-ttu-id="f8bb8-110">如果收到此错误，则可能表示持久参与者 (包括从故障中恢复) 从属 TransactionManagers;但是，它不能确定事务结果并请求其状态。</span><span class="sxs-lookup"><span data-stu-id="f8bb8-110">Receiving this error can indicate that a Durable participant (including Subordinate TransactionManagers) has recovered from failure; however, it is unsure of the transaction outcome and requests its status.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f8bb8-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="f8bb8-111">See also</span></span>

- [<span data-ttu-id="f8bb8-112">跟踪</span><span class="sxs-lookup"><span data-stu-id="f8bb8-112">Tracing</span></span>](index.md)
- [<span data-ttu-id="f8bb8-113">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="f8bb8-113">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="f8bb8-114">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="f8bb8-114">Administration and Diagnostics</span></span>](../index.md)
