---
description: 了解有关以下内容的详细信息： WF 中的事务活动
title: WF 中的事务活动
ms.date: 03/30/2017
ms.assetid: fb33378e-82c6-4ea0-870f-76dc77e7f0fe
ms.openlocfilehash: f088c586998d3dbec8b94dcf0f02603a68b55a40
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755130"
---
# <a name="transaction-activities-in-wf"></a><span data-ttu-id="db125-103">WF 中的事务活动</span><span class="sxs-lookup"><span data-stu-id="db125-103">Transaction Activities in WF</span></span>

<span data-ttu-id="db125-104">[!INCLUDE[netfx_current_long](../../../includes/netfx-current-long-md.md)]包含几个系统提供的活动，它们用于对事务、补偿和取消进行建模。</span><span class="sxs-lookup"><span data-stu-id="db125-104">The [!INCLUDE[netfx_current_long](../../../includes/netfx-current-long-md.md)] has several system-provided activities for modeling transactions, compensation, and cancellation.</span></span> <span data-ttu-id="db125-105">通过这些编程模型，工作流可以在业务逻辑和错误处理中发生更改时继续向前推进。</span><span class="sxs-lookup"><span data-stu-id="db125-105">These programming models allow the workflow to continue forward progress in the event of changes in business logic and error handling.</span></span> <span data-ttu-id="db125-106">有关事务、补偿和取消的详细信息，请参阅 [事务](workflow-transactions.md)、 [补偿](compensation.md)和 [取消](modeling-cancellation-behavior-in-workflows.md)。</span><span class="sxs-lookup"><span data-stu-id="db125-106">For more information about transactions, compensation, and cancellation, see [Transactions](workflow-transactions.md), [Compensation](compensation.md), and [Cancellation](modeling-cancellation-behavior-in-workflows.md).</span></span>  
  
## <a name="transaction-activities"></a><span data-ttu-id="db125-107">事务活动</span><span class="sxs-lookup"><span data-stu-id="db125-107">Transaction Activities</span></span>  
  
|||  
|-|-|  
|<xref:System.Activities.Statements.CancellationScope>|<span data-ttu-id="db125-108">将活动形式的取消逻辑与执行的主要路径（也表示为活动）相关联。</span><span class="sxs-lookup"><span data-stu-id="db125-108">Associates cancellation logic, in the form of an activity, with a main path of execution, also expressed as an activity.</span></span>|  
|<xref:System.Activities.Statements.CompensableActivity>|<span data-ttu-id="db125-109">支持对其子活动的补偿。</span><span class="sxs-lookup"><span data-stu-id="db125-109">Supports compensation of its child activities.</span></span>|  
|<xref:System.Activities.Statements.Compensate>|<span data-ttu-id="db125-110">显式调用 <xref:System.Activities.Statements.CompensableActivity> 的补偿处理程序。</span><span class="sxs-lookup"><span data-stu-id="db125-110">Explicitly invokes the compensation handler of a <xref:System.Activities.Statements.CompensableActivity>.</span></span>|  
|<xref:System.Activities.Statements.Confirm>|<span data-ttu-id="db125-111">显式调用 <xref:System.Activities.Statements.CompensableActivity> 的确认处理程序。</span><span class="sxs-lookup"><span data-stu-id="db125-111">Explicitly invokes the confirmation handler of a <xref:System.Activities.Statements.CompensableActivity>.</span></span>|  
|<xref:System.Activities.Statements.TransactionScope>|<span data-ttu-id="db125-112">划分事务边界。</span><span class="sxs-lookup"><span data-stu-id="db125-112">Demarcates a transaction boundary.</span></span>|  
|<xref:System.ServiceModel.Activities.TransactedReceiveScope>|<span data-ttu-id="db125-113">确定接收的消息启动的事务的生存期范围。</span><span class="sxs-lookup"><span data-stu-id="db125-113">Scopes the lifetime of a transaction that is initiated by a received message.</span></span> <span data-ttu-id="db125-114">事务可以流入发起消息的工作流中，也可以在收到消息时由调度程序创建。</span><span class="sxs-lookup"><span data-stu-id="db125-114">The transaction may be flowed into the workflow on the initiating message, or created by the dispatcher when the message is received.</span></span> <span data-ttu-id="db125-115">**注意：** 位于 "工具箱" 的 <xref:System.ServiceModel.Activities.TransactedReceiveScope> "**消息传送**" 部分。</span><span class="sxs-lookup"><span data-stu-id="db125-115">**Note:**  The <xref:System.ServiceModel.Activities.TransactedReceiveScope> is located in the **Messaging** section of the **Toolbox**.</span></span>|
