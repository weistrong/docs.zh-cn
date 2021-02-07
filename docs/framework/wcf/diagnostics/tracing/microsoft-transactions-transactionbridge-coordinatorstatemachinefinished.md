---
description: 了解有关以下内容的详细信息： TransactionBridge. CoordinatorStateMachineFinished
title: Microsoft.Transactions.TransactionBridge.CoordinatorStateMachineFinished
ms.date: 03/30/2017
ms.assetid: 16cb428d-d886-4789-a961-6fded4b0dbba
ms.openlocfilehash: 83cbc6fe80d0fc611c88e8074805cae870261305
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99759388"
---
# <a name="microsofttransactionstransactionbridgecoordinatorstatemachinefinished"></a><span data-ttu-id="5a4dc-103">Microsoft.Transactions.TransactionBridge.CoordinatorStateMachineFinished</span><span class="sxs-lookup"><span data-stu-id="5a4dc-103">Microsoft.Transactions.TransactionBridge.CoordinatorStateMachineFinished</span></span>

<span data-ttu-id="5a4dc-104">用于协调器登记的状态机已进入已完成状态。</span><span class="sxs-lookup"><span data-stu-id="5a4dc-104">The state machine for a coordinator enlistment has entered the finished state.</span></span>  
  
## <a name="description"></a><span data-ttu-id="5a4dc-105">说明</span><span class="sxs-lookup"><span data-stu-id="5a4dc-105">Description</span></span>  

 <span data-ttu-id="5a4dc-106">本地事务管理器认为高级协调器登记已完成 2pc 处理时跟踪。</span><span class="sxs-lookup"><span data-stu-id="5a4dc-106">Traced when the local Transaction Manager believes a superior coordinator enlistment has completed 2pc processing.</span></span> <span data-ttu-id="5a4dc-107">登记的结果可以是“已提交”、“已中止”或“已忘记”。</span><span class="sxs-lookup"><span data-stu-id="5a4dc-107">The outcome for the enlistment can be Committed or Aborted or Forgotten.</span></span> <span data-ttu-id="5a4dc-108">本地事务管理器在“准备”过程中对“只读”投票时也会进行跟踪。</span><span class="sxs-lookup"><span data-stu-id="5a4dc-108">It is also traced if the local Transaction Manager votes ReadOnly during Prepare.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5a4dc-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="5a4dc-109">See also</span></span>

- [<span data-ttu-id="5a4dc-110">跟踪</span><span class="sxs-lookup"><span data-stu-id="5a4dc-110">Tracing</span></span>](index.md)
- [<span data-ttu-id="5a4dc-111">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="5a4dc-111">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="5a4dc-112">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="5a4dc-112">Administration and Diagnostics</span></span>](../index.md)
