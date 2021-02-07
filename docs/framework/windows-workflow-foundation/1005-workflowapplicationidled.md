---
description: 了解详细信息： 1005-WorkflowApplicationIdled
title: 1005 - WorkflowApplicationIdled
ms.date: 03/30/2017
ms.assetid: 74d77dfa-f20d-4fe9-a6ae-e6d1b5fe4182
ms.openlocfilehash: ee8d0b7ff2155333213a718a04c3966024fda89d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755598"
---
# <a name="1005---workflowapplicationidled"></a>1005 - WorkflowApplicationIdled

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|1005|  
|关键字|WFRuntime|  
|级别|信息|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/调试|  
  
## <a name="description"></a>说明  

 指示工作流应用程序已处于空闲状态。  
  
## <a name="message"></a>消息  

 WorkflowApplication ID“%1”变为空闲状态。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|WorkflowInstanceId|`xs:string`|工作流应用程序 ID|  
|应用程序域|`xs:string`|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
