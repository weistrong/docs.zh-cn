---
description: 了解详细信息： 1002-WorkflowApplicationTerminated
title: 1002 - WorkflowApplicationTerminated
ms.date: 03/30/2017
ms.assetid: 4e8b111f-79dc-4898-bb4a-e9b36f69420f
ms.openlocfilehash: 8ceef41515231833767fc7e2095ab3850bf80e41
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755617"
---
# <a name="1002---workflowapplicationterminated"></a>1002 - WorkflowApplicationTerminated

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|1002|  
|关键字|WFRuntime|  
|级别|信息|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/调试|  
  
## <a name="description"></a>说明  

 指示工作流应用程序因出现异常而在“出错”状态下终止。  
  
## <a name="message"></a>消息  

 WorkflowApplication Id“%1”已终止。 该应用程序因出现异常而在“出错”状态下完成。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|WorkflowApplicationId|`xs:string`|工作流应用程序 ID|  
|异常|`xs:string`|异常的异常详细信息|  
|应用程序域|`xs:string`|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
