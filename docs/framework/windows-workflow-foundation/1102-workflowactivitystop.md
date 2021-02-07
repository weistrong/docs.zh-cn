---
description: 了解详细信息： 1102-WorkflowActivityStop
title: 1102 - WorkflowActivityStop
ms.date: 03/30/2017
ms.assetid: 285e5cb8-e90d-4914-ac06-e9b176ffefa2
ms.openlocfilehash: 726af6a79058e93a066e0f486d7cf5be1ef8e4be
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99667572"
---
# <a name="1102---workflowactivitystop"></a>1102 - WorkflowActivityStop

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|1102|  
|关键字|WFRuntime|  
|级别|信息|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/调试|  
  
## <a name="description"></a>说明  

 指示工作流活动已停止。  
  
## <a name="message"></a>消息  

 WorkflowInstance Id“%1”E2E 活动  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|WorkflowInstanceId|xs:string|工作流实例 ID。|  
|应用程序域|xs:string|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
