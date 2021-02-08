---
description: 了解详细信息： 2577-TryCatchExceptionDuringCancelation
title: 2577 - TryCatchExceptionDuringCancelation
ms.date: 03/30/2017
ms.assetid: 35ee9f55-227f-4566-bcb4-4c7c75dea85b
ms.openlocfilehash: e02e7722dadfe38b9fc1fbb92e809ae8f80cbd2f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99778095"
---
# <a name="2577---trycatchexceptionduringcancelation"></a>2577 - TryCatchExceptionDuringCancelation

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|2577|  
|关键字|WFActivities|  
|级别|警告|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/调试|  
  
## <a name="description"></a>说明  

 支持 TryCatch 活动的子活动在取消过程中引发了异常。  
  
## <a name="message"></a>消息  

 TryCatch 活动“%1”的子活动在取消过程中引发了异常。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|DisplayName|xs:string|活动的显示名称。|  
|应用程序域|xs:string|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
