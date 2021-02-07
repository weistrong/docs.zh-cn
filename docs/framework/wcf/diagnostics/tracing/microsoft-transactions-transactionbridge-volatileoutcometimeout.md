---
description: 了解有关以下内容的详细信息： TransactionBridge. VolatileOutcomeTimeout
title: Microsoft.Transactions.TransactionBridge.VolatileOutcomeTimeout
ms.date: 03/30/2017
ms.assetid: 2dbe34c5-57c7-4b64-9257-63021911d03c
ms.openlocfilehash: 5dd6ecce995d315581e1335e4dc83c425a6381b7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99677231"
---
# <a name="microsofttransactionstransactionbridgevolatileoutcometimeout"></a><span data-ttu-id="34c60-103">Microsoft.Transactions.TransactionBridge.VolatileOutcomeTimeout</span><span class="sxs-lookup"><span data-stu-id="34c60-103">Microsoft.Transactions.TransactionBridge.VolatileOutcomeTimeout</span></span>

<span data-ttu-id="34c60-104">WS-AT 协议服务在等待可变参与方对结果消息的响应时超时。</span><span class="sxs-lookup"><span data-stu-id="34c60-104">The WS-AT protocol service timed out waiting for a response to an outcome message from a volatile participant.</span></span> <span data-ttu-id="34c60-105">如果参与方返回，则事务结果可能不确定。</span><span class="sxs-lookup"><span data-stu-id="34c60-105">The transaction outcome may be in doubt if the participant returns.</span></span>  
  
## <a name="description"></a><span data-ttu-id="34c60-106">说明</span><span class="sxs-lookup"><span data-stu-id="34c60-106">Description</span></span>  

 <span data-ttu-id="34c60-107">当可变参与方已决定提交或中止，但未在给定时间内响应提交或回滚请求时跟踪。</span><span class="sxs-lookup"><span data-stu-id="34c60-107">Traced when a Volatile participant has decided to Commit or Abort but has not responded to a Commit or Rollback request within a given amount of time.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="34c60-108">疑难解答</span><span class="sxs-lookup"><span data-stu-id="34c60-108">Troubleshooting</span></span>  

 <span data-ttu-id="34c60-109">确保所有可变参与方都能在给定时间内响应。</span><span class="sxs-lookup"><span data-stu-id="34c60-109">Ensure that all Volatile participants are able to respond within the given amount of time.</span></span> <span data-ttu-id="34c60-110">默认时间为 180 秒。</span><span class="sxs-lookup"><span data-stu-id="34c60-110">The default time period is 180 seconds.</span></span>  <span data-ttu-id="34c60-111">如果此时间不够，请增加 WS-AT 的 `VolatileOutcomeDelay` 计时器策略。</span><span class="sxs-lookup"><span data-stu-id="34c60-111">If this is insufficient, increase the `VolatileOutcomeDelay` timer policy for WS-AT.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="34c60-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="34c60-112">See also</span></span>

- [<span data-ttu-id="34c60-113">跟踪</span><span class="sxs-lookup"><span data-stu-id="34c60-113">Tracing</span></span>](index.md)
- [<span data-ttu-id="34c60-114">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="34c60-114">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="34c60-115">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="34c60-115">Administration and Diagnostics</span></span>](../index.md)
