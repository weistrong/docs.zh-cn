---
description: 了解有关以下内容的详细信息： TransactionBridge. CreateTransactionFailure
title: Microsoft.Transactions.TransactionBridge.CreateTransactionFailure
ms.date: 03/30/2017
ms.assetid: c3468e23-49a9-4a84-972d-a79a658851b3
ms.openlocfilehash: 6b4a071b617de475b51ec50178e5205fa2e524d2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803303"
---
# <a name="microsofttransactionstransactionbridgecreatetransactionfailure"></a><span data-ttu-id="9d543-103">Microsoft.Transactions.TransactionBridge.CreateTransactionFailure</span><span class="sxs-lookup"><span data-stu-id="9d543-103">Microsoft.Transactions.TransactionBridge.CreateTransactionFailure</span></span>

<span data-ttu-id="9d543-104">无法创建事务。</span><span class="sxs-lookup"><span data-stu-id="9d543-104">A transaction could not be created.</span></span>  
  
## <a name="description"></a><span data-ttu-id="9d543-105">说明</span><span class="sxs-lookup"><span data-stu-id="9d543-105">Description</span></span>  

 <span data-ttu-id="9d543-106">当 MSDTC 无法创建事务时，将生成此跟踪。</span><span class="sxs-lookup"><span data-stu-id="9d543-106">This trace is generated when MSDTC is unable to create a transaction.</span></span> <span data-ttu-id="9d543-107">这可能是由资源不足、日志空间不够或其他错误引起的。</span><span class="sxs-lookup"><span data-stu-id="9d543-107">This can be due to low resources, insufficient log space, or other errors.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="9d543-108">疑难解答</span><span class="sxs-lookup"><span data-stu-id="9d543-108">Troubleshooting</span></span>  

 <span data-ttu-id="9d543-109">检查跟踪消息中的状态字符串以确定是否存在任何可操作的项。</span><span class="sxs-lookup"><span data-stu-id="9d543-109">Inspect the status string within the trace message to determine if any actionable item exists.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9d543-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="9d543-110">See also</span></span>

- [<span data-ttu-id="9d543-111">跟踪</span><span class="sxs-lookup"><span data-stu-id="9d543-111">Tracing</span></span>](index.md)
- [<span data-ttu-id="9d543-112">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="9d543-112">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="9d543-113">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="9d543-113">Administration and Diagnostics</span></span>](../index.md)
