---
description: 了解详细信息： 225-TraceCorrelationKeys
title: 225 - TraceCorrelationKeys
ms.date: 03/30/2017
ms.assetid: d9083aaf-3816-4c1c-bae0-2d7f49628345
ms.openlocfilehash: c5fdb9305815cdc4df6bbae3e54209d2b5cffd9d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99778108"
---
# <a name="225---tracecorrelationkeys"></a>225 - TraceCorrelationKeys

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|225|  
|关键字|疑难解答，ServiceModel|  
|级别|信息|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/分析|  
  
## <a name="description"></a>说明  

 将基于内容的相关用于工作流服务时将发出此事件。 该事件包含为关联消息和实例而应用的相关键。  
  
## <a name="message"></a>消息  

 使用父作用域“%3”中的值“%2”计算出的相关键“%1”。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|实例键|`xs:GUID`|依据相关值生成的键。|  
|值|`xs:string`|用于计算相关实例键的值。|  
|父作用域|`xs:string`||  
|HostReference|`xs:string`|对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。 其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。 示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。|  
|应用程序域|`xs:string`|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
