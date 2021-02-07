---
description: 了解有关以下内容的详细信息： TransactionBridge. ParticipantStateMachineFinished
title: Microsoft.Transactions.TransactionBridge.ParticipantStateMachineFinished
ms.date: 03/30/2017
ms.assetid: 54b677f7-03ad-40f2-9c5d-297a8ad9bf90
ms.openlocfilehash: f49027b82957969779423d0895ff24a4a36d1f4f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99759375"
---
# <a name="microsofttransactionstransactionbridgeparticipantstatemachinefinished"></a><span data-ttu-id="de24d-103">Microsoft.Transactions.TransactionBridge.ParticipantStateMachineFinished</span><span class="sxs-lookup"><span data-stu-id="de24d-103">Microsoft.Transactions.TransactionBridge.ParticipantStateMachineFinished</span></span>

<span data-ttu-id="de24d-104">参与者列入的状态机进入已完成状态。</span><span class="sxs-lookup"><span data-stu-id="de24d-104">The state machine for a participant enlistment entered the finished state.</span></span>  
  
## <a name="description"></a><span data-ttu-id="de24d-105">说明</span><span class="sxs-lookup"><span data-stu-id="de24d-105">Description</span></span>  

 <span data-ttu-id="de24d-106">从属参与者列入已完成 2pc 处理时跟踪。</span><span class="sxs-lookup"><span data-stu-id="de24d-106">Traced when a subordinate participant enlistment has completed 2pc processing.</span></span> <span data-ttu-id="de24d-107">列入的结果可以是“已提交”或“已中止”。</span><span class="sxs-lookup"><span data-stu-id="de24d-107">The outcome for the enlistment can be Committed or Aborted.</span></span> <span data-ttu-id="de24d-108">此外，还会跟踪是否有参与者在“准备”过程中投票“只读”。</span><span class="sxs-lookup"><span data-stu-id="de24d-108">It is also traced if any participant votes ReadOnly during Prepare.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="de24d-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="de24d-109">See also</span></span>

- [<span data-ttu-id="de24d-110">跟踪</span><span class="sxs-lookup"><span data-stu-id="de24d-110">Tracing</span></span>](index.md)
- [<span data-ttu-id="de24d-111">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="de24d-111">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="de24d-112">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="de24d-112">Administration and Diagnostics</span></span>](../index.md)
