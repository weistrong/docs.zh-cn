---
description: 了解详细信息： 1006-WorkflowApplicationUnhandledException
title: 1006 - WorkflowApplicationUnhandledException
ms.date: 03/30/2017
ms.assetid: dfe0f316-e03b-47fb-b6a3-622c56bfd753
ms.openlocfilehash: bfccd0d12c5dac4caad1e84e95f1cd096a551aa0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755585"
---
# <a name="1006---workflowapplicationunhandledexception"></a>1006 - WorkflowApplicationUnhandledException

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|1006|  
|关键字|WFRuntime|  
|级别|错误|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/调试|  
  
## <a name="description"></a>说明  

 指示工作流应用程序遇到了未经处理的异常。  
  
## <a name="message"></a>消息  

 WorkflowInstance Id "%1" 遇到未经处理的异常。  此异常源自 Activity "%2"、DisplayName "%3"。  将执行以下操作： %4。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|WorkflowInstanceId|`xs:string`|工作流的实例 ID|  
|异常|`xs:string`|异常的异常详细信息|  
|应用程序域|`xs:string`|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
