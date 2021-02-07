---
description: 了解详细信息： 1140-FlowchartStart
title: 1140 - FlowchartStart
ms.date: 03/30/2017
ms.assetid: 9aa2c71e-a4ab-4aed-b76d-4795e8493b70
ms.openlocfilehash: cfeda4b6abba0839944c9be11a781903840a87df
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99667169"
---
# <a name="1140---flowchartstart"></a>1140 - FlowchartStart

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|1140|  
|关键字|WFActivities|  
|级别|信息|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/调试|  
  
## <a name="description"></a>说明  

 指示已安排流程图启动。  
  
## <a name="message"></a>消息  

 Flowchart“%1”- 已安排启动。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|FlowChart|xs:string|FlowChart 的显示名称。|  
|应用程序域|xs:string|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
