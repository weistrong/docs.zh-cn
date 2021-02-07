---
description: 了解详细信息： 1007-WorkflowApplicationPersisted
title: 1007 - WorkflowApplicationPersisted
ms.date: 03/30/2017
ms.assetid: f4ea4452-28e3-4e66-93c6-eb12ee29bcb1
ms.openlocfilehash: 6598f4490d20f84abfc95223f9d5a3f4231b4754
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755572"
---
# <a name="1007---workflowapplicationpersisted"></a>1007 - WorkflowApplicationPersisted

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|1007|  
|关键字|WFRuntime|  
|级别|信息|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/调试|  
  
## <a name="description"></a>说明  

 指示工作流应用程序已持久化。  
  
## <a name="message"></a>消息  

 WorkflowApplication ID“%1”已持久化。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|WorkflowApplicationId|`xs:string`|工作流应用程序 ID|  
|应用程序域|`xs:string`|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
