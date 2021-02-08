---
description: 了解详细信息： 1020-CreateBookmark
title: 1020 - CreateBookmark
ms.date: 03/30/2017
ms.assetid: 4bee948d-816f-4803-85cc-3883b5e23d10
ms.openlocfilehash: 39796eaf68d9cb52e9faa2605fc21955a2c167ac
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792838"
---
# <a name="1020---createbookmark"></a>1020 - CreateBookmark

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|1020|  
|关键字|WFRuntime|  
|级别|“详细”|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/调试|  
  
## <a name="description"></a>说明  

 指示已为活动创建了书签。  
  
## <a name="message"></a>消息  

 已为 Activity "%1"、DisplayName "%2"、InstanceId "%3" 创建了书签。  BookmarkName: %4、BookmarkScope: %5。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|活动|xs:string|活动的类型名称。|  
|DisplayName|xs:string|活动的显示名称。|  
|InstanceId|xs:string|活动的实例 ID。|  
|BookmarkName|xs:string|书签的名称。|  
|BookmarkScope|xs:string|书签的范围。|  
|应用程序域|xs:string|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
