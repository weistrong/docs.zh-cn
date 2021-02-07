---
description: 了解详细信息： 4211-QueuingSqlRetry
title: 4211 - QueuingSqlRetry
ms.date: 03/30/2017
ms.assetid: df569f88-c86b-4503-840d-1399b67f4df7
ms.openlocfilehash: 674914ee105bb0a48f8c32efbd573c685d22d9f7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99742701"
---
# <a name="4211---queuingsqlretry"></a>4211 - QueuingSqlRetry

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|4211|  
|关键字|WFInstanceStore|  
|级别|警告|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/调试|  
  
## <a name="description"></a>说明  

 指示将 SQL 重试排队。  
  
## <a name="message"></a>消息  

 正在将 SQL 重试排队，延迟 %1 毫秒。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|Delay|xs:string|重试之间的延迟。|  
|应用程序域|xs:string|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
