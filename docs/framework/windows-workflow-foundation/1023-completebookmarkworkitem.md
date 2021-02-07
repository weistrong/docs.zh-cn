---
description: 了解详细信息： 1023-CompleteBookmarkWorkItem
title: 1023 - CompleteBookmarkWorkItem
ms.date: 03/30/2017
ms.assetid: fc5dac57-b3eb-4826-b505-c6d269e4774d
ms.openlocfilehash: c83972b41a844747c47b97a0dd2bd37c26ae78a9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755520"
---
# <a name="1023---completebookmarkworkitem"></a>1023 - CompleteBookmarkWorkItem

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|1023|  
|关键字|WFRuntime|  
|级别|“详细”|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/调试|  
  
## <a name="description"></a>说明  

 指示 BookmarkWorkItem 已完成。  
  
## <a name="message"></a>消息  

 Activity“%1”、DisplayName“%2”、InstanceId“%3”的 BookmarkWorkItem 已经完成。 BookmarkName: %4、BookmarkScope: %5。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|活动|xs:string|活动的类型名称。|  
|DisplayName|xs:string|活动的显示名称。|  
|InstanceId|xs:string|活动的实例 ID。|  
|BookmarkName|xs:string|书签的名称。|  
|BookmarkScope|xs:string|书签的范围。|  
|应用程序域|xs:string|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
