---
description: 了解详细信息： 404-ResumeSignpostEvent
title: 404 - ResumeSignpostEvent
ms.date: 03/30/2017
ms.assetid: 395cc7ca-f35f-4295-be97-39a077f99c97
ms.openlocfilehash: f735df6133c9708c05b2319e7ea17d7795e901b1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760285"
---
# <a name="404---resumesignpostevent"></a>404 - ResumeSignpostEvent

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|404|  
|关键字|疑难解答|  
|级别|信息|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/分析|  
  
## <a name="description"></a>说明  

 此事件标记端对端活动的恢复， 它包含活动的名称。  
  
## <a name="message"></a>消息  

 活动边界。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|扩展数据|`xs:string`|活动的名称。|  
|应用程序域|`xs:string`|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
