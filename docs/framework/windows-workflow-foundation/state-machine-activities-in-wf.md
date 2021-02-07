---
description: 了解有关以下内容的详细信息： WF 中的状态机活动
title: WF 中的状态机活动
ms.date: 03/30/2017
ms.assetid: 93312eaf-07e0-4a55-b4f7-4cdbbc4dee2d
ms.openlocfilehash: 4571bdbabc30e721523ae18449454627c0bf7319
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755247"
---
# <a name="state-machine-activities-in-wf"></a>WF 中的状态机活动

.NET Framework 4.5 提供多个系统提供的活动和活动设计器，用于创建状态机工作流。  
  
|||  
|-|-|  
|<xref:System.Activities.Statements.StateMachine>|使用熟悉的状态机范例执行包含的活动。|  
|<xref:System.Activities.Statements.State>|代表状态机中的状态。|  
|<xref:System.Activities.Core.Presentation.FinalState>|表示状态机中的终止状态。 <xref:System.Activities.Core.Presentation.FinalState> 是在创建预配置为终止状态的 <xref:System.Activities.Statements.State> 时所使用的活动设计器。 有关详细信息，请参阅 [FinalState 活动设计器](/visualstudio/workflow-designer/finalstate-activity-designer)。|  
|<xref:System.Activities.Statements.Transition>|表示两个状态间的转换。 没有用于的 **工具箱** 项 <xref:System.Activities.Statements.Transition> ; 通过在两个状态之间拖放线条，或在一个状态悬停在另一个状态上时，在工作流设计器上创建转换。 有关详细信息，请参阅 [转变活动设计器](/visualstudio/workflow-designer/transition-activity-designer)。|  
  
## <a name="see-also"></a>请参阅

- [入门教程](getting-started-tutorial.md)
