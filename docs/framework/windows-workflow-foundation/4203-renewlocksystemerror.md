---
description: 了解详细信息： 4203-RenewLockSystemError
title: 4203 - RenewLockSystemError
ms.date: 03/30/2017
ms.assetid: 6ec9ec6f-4ae2-45cf-b99b-02cdb9dc9ec9
ms.openlocfilehash: 0e62c501391fcaec56f2016631707832170775ed
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99792773"
---
# <a name="4203---renewlocksystemerror"></a>4203 - RenewLockSystemError

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|4203|  
|关键字|WFInstanceStore|  
|级别|错误|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/调试|  
  
## <a name="description"></a>说明  

 指示 SQL 提供程序由于锁定到期日已过或者已删除锁定所有者，未能延长锁定到期日。 SqlWorkflowInstanceStore 将被中止。  
  
## <a name="message"></a>消息  

 未能延长锁定到期日，锁定到期日已过，或者已删除锁定所有者。 正在中止 SqlWorkflowInstanceStore。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|应用程序域|xs:string|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
