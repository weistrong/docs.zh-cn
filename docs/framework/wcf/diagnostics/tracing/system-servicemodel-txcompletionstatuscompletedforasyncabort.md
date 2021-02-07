---
description: 了解有关以下方面的详细信息： TxCompletionStatusCompletedForAsyncAbort
title: System.ServiceModel.TxCompletionStatusCompletedForAsyncAbort
ms.date: 03/30/2017
ms.assetid: 155c3203-2e17-4709-b896-2254e22da45e
ms.openlocfilehash: 892a867607d1c6d34c06a59947cc336db067fb19
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99735681"
---
# <a name="systemservicemodeltxcompletionstatuscompletedforasyncabort"></a><span data-ttu-id="8fd56-103">System.ServiceModel.TxCompletionStatusCompletedForAsyncAbort</span><span class="sxs-lookup"><span data-stu-id="8fd56-103">System.ServiceModel.TxCompletionStatusCompletedForAsyncAbort</span></span>

<span data-ttu-id="8fd56-104">指定操作的指定事务由于异步中止而完成。</span><span class="sxs-lookup"><span data-stu-id="8fd56-104">The specified transaction for the specified operation was completed due to asynchronous abort.</span></span>  
  
## <a name="description"></a><span data-ttu-id="8fd56-105">说明</span><span class="sxs-lookup"><span data-stu-id="8fd56-105">Description</span></span>  

 <span data-ttu-id="8fd56-106">由于另一名参与者赞成中止，发生超时，或事务的参与者内部出现另一错误，因此当前事务被中止。</span><span class="sxs-lookup"><span data-stu-id="8fd56-106">The current transaction was aborted due to another participant voting for Abort, time-outs occurring, or another error inside the participant of a transaction.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="8fd56-107">疑难解答</span><span class="sxs-lookup"><span data-stu-id="8fd56-107">Troubleshooting</span></span>  

 <span data-ttu-id="8fd56-108">如果这是意外中止，请检查所有系统日志，以确定发生该中止的真正原因。</span><span class="sxs-lookup"><span data-stu-id="8fd56-108">If this abort is unexpected, check all system logs to determine the real reason for the abort.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8fd56-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="8fd56-109">See also</span></span>

- [<span data-ttu-id="8fd56-110">跟踪</span><span class="sxs-lookup"><span data-stu-id="8fd56-110">Tracing</span></span>](index.md)
- [<span data-ttu-id="8fd56-111">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="8fd56-111">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="8fd56-112">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="8fd56-112">Administration and Diagnostics</span></span>](../index.md)
