---
description: 了解有关以下方面的详细信息： TxCompletionStatusAbortedOnSessionClose
title: System.ServiceModel.TxCompletionStatusAbortedOnSessionClose
ms.date: 03/30/2017
ms.assetid: 7e142e9d-e81b-4309-974a-02e9cc064ea0
ms.openlocfilehash: d47dc1a87c7f44b58f70f9590b4233f1e0a9074e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99735707"
---
# <a name="systemservicemodeltxcompletionstatusabortedonsessionclose"></a><span data-ttu-id="9b756-103">System.ServiceModel.TxCompletionStatusAbortedOnSessionClose</span><span class="sxs-lookup"><span data-stu-id="9b756-103">System.ServiceModel.TxCompletionStatusAbortedOnSessionClose</span></span>

<span data-ttu-id="9b756-104">指定的事务被中止，因为当会话被关闭时尚未完成，且 TransactionAutoCompleteOnSessionClose OperationBehaviorAttribute 被设置为 false。</span><span class="sxs-lookup"><span data-stu-id="9b756-104">The specified transaction was aborted because it was uncompleted when the session was closed and the TransactionAutoCompleteOnSessionClose OperationBehaviorAttribute was set to false.</span></span>  
  
## <a name="description"></a><span data-ttu-id="9b756-105">说明</span><span class="sxs-lookup"><span data-stu-id="9b756-105">Description</span></span>  

 <span data-ttu-id="9b756-106">如果当前活动会话已关闭，事务未完成，并且 TransactionAutoCompleteOnSessionClose 设置为 `false`，则进行跟踪。</span><span class="sxs-lookup"><span data-stu-id="9b756-106">Traced if the current active session was closed, and the transaction was not completed, and TransactionAutoCompleteOnSessionClose is set to `false`.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="9b756-107">疑难解答</span><span class="sxs-lookup"><span data-stu-id="9b756-107">Troubleshooting</span></span>  

 <span data-ttu-id="9b756-108">此跟踪指示一个应予调查的潜在应用程序 Bug。</span><span class="sxs-lookup"><span data-stu-id="9b756-108">This trace indicates a potential application bug that should be investigated.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9b756-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="9b756-109">See also</span></span>

- [<span data-ttu-id="9b756-110">跟踪</span><span class="sxs-lookup"><span data-stu-id="9b756-110">Tracing</span></span>](index.md)
- [<span data-ttu-id="9b756-111">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="9b756-111">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="9b756-112">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="9b756-112">Administration and Diagnostics</span></span>](../index.md)
