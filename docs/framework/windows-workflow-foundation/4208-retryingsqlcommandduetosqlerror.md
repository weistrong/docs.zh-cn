---
description: 了解详细信息： 4208-RetryingSqlCommandDueToSqlError
title: 4208 - RetryingSqlCommandDueToSqlError
ms.date: 03/30/2017
ms.assetid: a8e6483a-a6e4-4bbf-82ec-cd8b6e711aad
ms.openlocfilehash: 11ea2260f6a2ceffc1ffdbfce2cb3e3ce784076d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755299"
---
# <a name="4208---retryingsqlcommandduetosqlerror"></a>4208 - RetryingSqlCommandDueToSqlError

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|4208|  
|关键字|WFInstanceStore|  
|级别|信息|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/调试|  
  
## <a name="description"></a>说明  

 指示 SQL 提供程序由于 SQL 错误正在重试 SQL 命令。  
  
## <a name="message"></a>消息  

 因 SQL 错误号 %1，正在重试 SQL 命令。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|ErrorNumber|xs:string|SQL 错误号。|  
|应用程序域|xs:string|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
