---
description: 了解有关以下方面的详细信息： TxAsyncAbort
title: System.ServiceModel.TxAsyncAbort
ms.date: 03/30/2017
ms.assetid: bce47ff2-abd0-4b58-8667-ebf1ef3580b8
ms.openlocfilehash: 461a5e4da21cf3219114ebb4e6db2149fb94ea17
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99653883"
---
# <a name="systemservicemodeltxasyncabort"></a><span data-ttu-id="7289f-103">System.ServiceModel.TxAsyncAbort</span><span class="sxs-lookup"><span data-stu-id="7289f-103">System.ServiceModel.TxAsyncAbort</span></span>

<span data-ttu-id="7289f-104">指定的事务被异步中止。</span><span class="sxs-lookup"><span data-stu-id="7289f-104">The specified transaction was asynchronously aborted.</span></span>  
  
## <a name="description"></a><span data-ttu-id="7289f-105">说明</span><span class="sxs-lookup"><span data-stu-id="7289f-105">Description</span></span>  

 <span data-ttu-id="7289f-106">由于另一名参与者赞成中止，发生超时，或事务的参与者内部出现另一错误，因此当前事务被中止。</span><span class="sxs-lookup"><span data-stu-id="7289f-106">The current transaction was aborted due to another participant voting for Abort, time-outs occurring, or another error inside the participant of a transaction.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="7289f-107">疑难解答</span><span class="sxs-lookup"><span data-stu-id="7289f-107">Troubleshooting</span></span>  

 <span data-ttu-id="7289f-108">如果该中止是意料之外的，请检查所有系统日志，以便确定发生该中止的真正原因。</span><span class="sxs-lookup"><span data-stu-id="7289f-108">Check all system logs if this abort is unexpected to determine the real reason for the abort.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7289f-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="7289f-109">See also</span></span>

- [<span data-ttu-id="7289f-110">跟踪</span><span class="sxs-lookup"><span data-stu-id="7289f-110">Tracing</span></span>](index.md)
- [<span data-ttu-id="7289f-111">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="7289f-111">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="7289f-112">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="7289f-112">Administration and Diagnostics</span></span>](../index.md)
