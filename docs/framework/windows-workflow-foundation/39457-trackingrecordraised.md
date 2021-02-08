---
description: 了解详细信息： 39457-TrackingRecordRaised
title: 39457 - TrackingRecordRaised
ms.date: 03/30/2017
ms.assetid: 5a2731d1-c731-4b79-bb69-016cb69ef481
ms.openlocfilehash: 551e13e32dbb690458877ceed0b532799f238966
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99777900"
---
# <a name="39457---trackingrecordraised"></a>39457 - TrackingRecordRaised

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|39457|  
|关键字|WFRuntime|  
|级别|信息|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/调试|  
  
## <a name="description"></a>说明  

 指示 TrackingRecord 已提升为 TrackingParticipant。  
  
## <a name="message"></a>消息  

 跟踪记录 %1 提升为 %2。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|RecordNumber|xs:string|跟踪记录编号。|  
|ParticipantId|xs:string|跟踪参与者。|  
|应用程序域|xs:string|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
