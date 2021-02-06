---
description: 了解有关以下内容的详细信息： TransactionBridge. EnlistTransactionFailure
title: Microsoft.Transactions.TransactionBridge.EnlistTransactionFailure
ms.date: 03/30/2017
ms.assetid: 1b9f5139-e122-4716-9ef7-2f38e1813993
ms.openlocfilehash: f0645d0f7bfc2787f4bce254ea8d6e3143dc0406
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99644601"
---
# <a name="microsofttransactionstransactionbridgeenlisttransactionfailure"></a><span data-ttu-id="20e5a-103">Microsoft.Transactions.TransactionBridge.EnlistTransactionFailure</span><span class="sxs-lookup"><span data-stu-id="20e5a-103">Microsoft.Transactions.TransactionBridge.EnlistTransactionFailure</span></span>

<span data-ttu-id="20e5a-104">WS-AT 协议服务无法使用提供的协调上下文在事务上登记。</span><span class="sxs-lookup"><span data-stu-id="20e5a-104">The WS-AT protocol service failed to enlist on a transaction using the provided coordination context.</span></span>  
  
## <a name="description"></a><span data-ttu-id="20e5a-105">说明</span><span class="sxs-lookup"><span data-stu-id="20e5a-105">Description</span></span>  

 <span data-ttu-id="20e5a-106">对于给定的 2pc 协议，当 MSDTC 无法在事务上登记时跟踪。</span><span class="sxs-lookup"><span data-stu-id="20e5a-106">Traced when MSDTC is unable to enlist on a transaction for a given 2pc protocol.</span></span>  <span data-ttu-id="20e5a-107">当事务不再存在、不再允许登记或者已存在过多的登记项时可能出现这种情况。</span><span class="sxs-lookup"><span data-stu-id="20e5a-107">This can happen because the transaction no longer exists, enlisting is no longer allowed, or too many enlistments are already present.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="20e5a-108">疑难解答</span><span class="sxs-lookup"><span data-stu-id="20e5a-108">Troubleshooting</span></span>  

 <span data-ttu-id="20e5a-109">检查跟踪消息中的状态字符串以确定是否存在任何可操作的项。</span><span class="sxs-lookup"><span data-stu-id="20e5a-109">Inspect the status string within the trace message to determine if any actionable item exists.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="20e5a-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="20e5a-110">See also</span></span>

- [<span data-ttu-id="20e5a-111">跟踪</span><span class="sxs-lookup"><span data-stu-id="20e5a-111">Tracing</span></span>](index.md)
- [<span data-ttu-id="20e5a-112">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="20e5a-112">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="20e5a-113">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="20e5a-113">Administration and Diagnostics</span></span>](../index.md)
