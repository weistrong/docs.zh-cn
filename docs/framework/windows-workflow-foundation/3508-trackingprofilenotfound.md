---
description: 了解详细信息： 3508-TrackingProfileNotFound
title: 3508 - TrackingProfileNotFound
ms.date: 03/30/2017
ms.assetid: 4cee3c4a-0490-4c94-aa19-ef7ce7287c02
ms.openlocfilehash: 3e97af1689a868fb103b06413a0c4f28b0c1f652
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99778004"
---
# <a name="3508---trackingprofilenotfound"></a>3508 - TrackingProfileNotFound

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|3508|  
|关键字|WFServices|  
|级别|“详细”|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/分析|  
  
## <a name="description"></a>说明  

 指示在配置文件中找不到 TrackingProfile，或 ActivityDefinitionId 与配置文件不匹配。  
  
## <a name="message"></a>消息  

 未找到 ActivityDefinitionId“%2”的 TrackingProfile“%1”。 在配置文件中找不到 TrackingProfile，或 ActivityDefinitionId 不匹配。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|TrackingProfile|xs:string|跟踪配置文件的名称。|  
|ActivityDefinitionId|xs:string|活动定义 ID。|  
|应用程序域|xs:string|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
