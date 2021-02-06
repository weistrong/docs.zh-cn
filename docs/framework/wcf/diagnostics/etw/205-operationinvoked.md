---
description: 了解详细信息： 205-OperationInvoked
title: 205 - OperationInvoked
ms.date: 03/30/2017
ms.assetid: 9c8d6c90-dfa5-4ae0-a589-96679a8fb3ba
ms.openlocfilehash: 09afe4c29c5f56b06bbf524dd13d88ddf2319063
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99644965"
---
# <a name="205---operationinvoked"></a>205 - OperationInvoked

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|205|  
|关键字|疑难解答，ServiceModel|  
|级别|信息|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/分析|  
  
## <a name="description"></a>说明  

 恰好在服务模型的默认 `OperationInvoker` 开始调用方法之前发出此事件。  
  
## <a name="message"></a>消息  

 OperationInvoker 调用了“%1”方法。 调用方信息:“%2”。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|方法名|`xs:string`|由 `OperationInvoker` 调用的方法的 CLR 名称。|  
|调用方信息|`xs:string`|客户端 IP 地址和端口号（格式为“IPAddress:PortNumber”）。 需要从操作上下文的“System.ServiceModel.Channels.RemoteEndpointMessageProperty”消息属性中检索这两个值。 请注意，对于非 TCP 绑定，该值为 `null`。|  
|HostReference|`xs:string`|对于 Web 承载的服务，此字段唯一标识 Web 层次结构中的服务。 其格式定义为 "网站名称应用程序虚拟路径&#124;服务虚拟路径&#124;ServiceName"。 示例： "Default Web Site//Calculatorapplication&#124;/CalculatorService.svc&#124;CalculatorService"。|  
|应用程序域|`xs:string`|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
