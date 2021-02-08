---
description: 了解有关以下内容的详细信息：创建和运行工作流实例
title: 创建和运行工作流实例
ms.date: 03/30/2017
ms.assetid: 19d27f47-0491-4569-8f53-51bc1d940e80
ms.openlocfilehash: 2efd4a0017f450c21954e363af33be69c659624e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99787846"
---
# <a name="creating-and-running-a-workflow-instance"></a>创建和运行工作流实例

此示例演示如何运行工作流实例。 它演示如何以同步方式和异步方式执行这一操作。

## <a name="demonstrates"></a>演示

<xref:System.Activities.WorkflowInvoker>, <xref:System.Activities.WorkflowApplication>.

## <a name="discussion"></a>讨论 (Discussion)

此示例的第一部分使用 <xref:System.Activities.WorkflowInvoker.Invoke%2A>。 这是执行工作流的最基本方法。 使用 <xref:System.Activities.WorkflowInvoker.Invoke%2A> 执行的工作流以同步方式执行。

该示例的第二部分使用 <xref:System.Activities.WorkflowApplication> 类。 利用 <xref:System.Activities.WorkflowApplication>，您可以对每个实例进行更多控制，包括与正在运行的工作流进行交互的能力和异步运行工作流的能力。

> [!IMPORTANT]
> 您的计算机上可能已安装这些示例。 在继续操作之前，请先检查以下（默认）目录：
>
> `<InstallDrive>:\WF_WCF_Samples`
>
> 如果此目录不存在，请参阅[Windows Communication Foundation (wcf) ，并 Windows Workflow Foundation (的 WF](https://www.microsoft.com/download/details.aspx?id=21459)) .NET Framework Windows Communication Foundation ([!INCLUDE[wf1](../../../../includes/wf1-md.md)] 此示例位于以下目录：
>
> `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Execution\CreatingWorkflowInstances`

## <a name="see-also"></a>请参阅

- [使用 WorkflowInvoker 和 WorkflowApplication](../using-workflowinvoker-and-workflowapplication.md)
