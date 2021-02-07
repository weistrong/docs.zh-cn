---
description: 了解详细信息： 4207-MaximumRetriesExceededForSqlCommand
title: 4207 - MaximumRetriesExceededForSqlCommand
ms.date: 03/30/2017
ms.assetid: 8c8bee26-9ad4-4e01-bd16-0e1fd510fb6b
ms.openlocfilehash: e831da08e37010afaa33f3a52cd7cf7a9b4d713b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99742714"
---
# <a name="4207---maximumretriesexceededforsqlcommand"></a>4207 - MaximumRetriesExceededForSqlCommand

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|4207|  
|关键字|配额，FInstanceStore|  
|级别|信息|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/调试|  
  
## <a name="description"></a>说明  

 指示 SQL 提供程序正在放弃重试 SQL 命令，因为执行次数已达到了允许的最多重试次数。  
  
## <a name="message"></a>消息  

 正在放弃重试 SQL 命令，因为执行次数已达到了允许的最多重试次数。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|应用程序域|xs:string|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
