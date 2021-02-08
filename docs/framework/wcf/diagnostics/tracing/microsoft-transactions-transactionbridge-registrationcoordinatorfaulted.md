---
description: 了解有关以下内容的详细信息： TransactionBridge. RegistrationCoordinatorFaulted
title: Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorFaulted
ms.date: 03/30/2017
ms.assetid: 8193027e-9db2-4af9-a072-27300cd24330
ms.openlocfilehash: aae2d5824f4205a05e98c7ef00d27c6a844e1566
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99770594"
---
# <a name="microsofttransactionstransactionbridgeregistrationcoordinatorfaulted"></a><span data-ttu-id="ef3fb-103">Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorFaulted</span><span class="sxs-lookup"><span data-stu-id="ef3fb-103">Microsoft.Transactions.TransactionBridge.RegistrationCoordinatorFaulted</span></span>

<span data-ttu-id="ef3fb-104">WS-AT 协议服务从其协调程序接收到错误作为对注册消息的响应。</span><span class="sxs-lookup"><span data-stu-id="ef3fb-104">The WS-AT protocol service received a fault from its coordinator in response to a Register message.</span></span>  
  
## <a name="description"></a><span data-ttu-id="ef3fb-105">说明</span><span class="sxs-lookup"><span data-stu-id="ef3fb-105">Description</span></span>  

 <span data-ttu-id="ef3fb-106">在本地 TransactionManager 由于所返回的错误而无法向其上级 TransactionManager 注册时跟踪。</span><span class="sxs-lookup"><span data-stu-id="ef3fb-106">Traced if the local TransactionManager is not able to Register with its superior TransactionManager due to a fault being returned.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="ef3fb-107">疑难解答</span><span class="sxs-lookup"><span data-stu-id="ef3fb-107">Troubleshooting</span></span>  

 <span data-ttu-id="ef3fb-108">检查返回的错误的跟踪消息。</span><span class="sxs-lookup"><span data-stu-id="ef3fb-108">Inspect the trace message for the fault returned.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ef3fb-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="ef3fb-109">See also</span></span>

- [<span data-ttu-id="ef3fb-110">跟踪</span><span class="sxs-lookup"><span data-stu-id="ef3fb-110">Tracing</span></span>](index.md)
- [<span data-ttu-id="ef3fb-111">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="ef3fb-111">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="ef3fb-112">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="ef3fb-112">Administration and Diagnostics</span></span>](../index.md)
