---
description: 了解详细信息： 301-UserDefinedErrorOccurred
title: 301 - UserDefinedErrorOccurred
ms.date: 03/30/2017
ms.assetid: a0285d1c-550f-4c14-9c36-a96e97f1c4e4
ms.openlocfilehash: 15e12bb27e3626f80747498a1387aa90fc461d28
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794242"
---
# <a name="301---userdefinederroroccurred"></a>301 - UserDefinedErrorOccurred

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|301|  
|关键字|疑难解答，HealthMonitoring，UserEvents，ServiceModel，EndToEndMonitoring|  
|级别|错误|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/分析|  
  
## <a name="description"></a>说明  

 此事件从用户代码发出。 当开发人员的服务中出现自定义错误时，开发人员可以发出此事件。 可以使用 <xref:System.Diagnostics.Eventing> API 完成此操作。 此外，还提供了一个 WCF 示例，该示例包装 API 并演示如何正确发出此事件。  
  
## <a name="message"></a>消息  

 Name“%1”、Reference“%2”、Payload: %3  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|名称|`xs:string`|事件的用户定义名称。|  
|HostReference|`xs:string`|对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。 其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。 示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。|  
|Payload|`xs:string`|事件的用户定义负载。|
