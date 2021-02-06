---
description: 了解详细信息： 3502-InferredOperationDescription
title: 3502 - InferredOperationDescription
ms.date: 03/30/2017
ms.assetid: 6aebb614-3c72-4537-ba11-3cc7200ef1f1
ms.openlocfilehash: 5068a3553484b38242951ef985886190f8027035
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99631484"
---
# <a name="3502---inferredoperationdescription"></a>3502 - InferredOperationDescription

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|3502|  
|关键字|WFServices|  
|级别|信息|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/分析|  
  
## <a name="description"></a>说明  

 指示已从 WorkflowService 中推断出 OperationDescription。  
  
## <a name="message"></a>消息  

 已从 WorkflowService 中推断出协定“%2”中含有 Name='%1' 的 OperationDescription。 IsOneWay=%3。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|OperationName|xs:string|操作的名称。|  
|ContractName|xs:string|协定的名称。|  
|IsOneWay|xs:string|true 或 false 指示协定是否为单向。|  
|应用程序域|xs:string|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
