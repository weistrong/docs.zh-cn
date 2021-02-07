---
description: 了解详细信息： 1034-CompleteRuntimeWorkItem
title: 1034 - CompleteRuntimeWorkItem
ms.date: 03/30/2017
ms.assetid: 45620011-8b04-4f87-ab5a-65b24145e17d
ms.openlocfilehash: dd8a9fcb2fb692ab3b69df8f07f6a96cf48fc806
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99667962"
---
# <a name="1034---completeruntimeworkitem"></a>1034 - CompleteRuntimeWorkItem

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|1034|  
|关键字|WFRuntime|  
|级别|“详细”|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/调试|  
  
## <a name="description"></a>说明  

 指示 RuntimeWorkItem 已完成。  
  
## <a name="message"></a>消息  

 Activity“%1”、DisplayName“%2”、InstanceId“%3”的运行时工作项已经完成。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|活动|xs:string|活动的类型名称。|  
|DisplayName|xs:string|活动的显示名称。|  
|InstanceId|xs:string|活动的实例 ID。|  
|应用程序域|xs:string|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
