---
description: 了解详细信息： 451-MessageLogInfo
title: 451 - MessageLogInfo
ms.date: 03/30/2017
ms.assetid: 485b4b29-dc21-4a35-93f8-5f4726d6aa5a
ms.openlocfilehash: 9df1911eaee3300b770175f2af26e6dafd3de90c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760272"
---
# <a name="451---messageloginfo"></a>451 - MessageLogInfo

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|451|  
|关键字|疑难解答，WCFMessageLogging|  
|级别|信息|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/分析|  
  
## <a name="description"></a>说明  

 此事件是发送消息日志信息时发出的。  
  
## <a name="message"></a>消息  

 %1  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|data1|`xs:string`||  
|应用程序域|`xs:string`|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
