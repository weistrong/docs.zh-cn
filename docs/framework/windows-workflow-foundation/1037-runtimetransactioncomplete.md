---
description: 了解详细信息： 1037-RuntimeTransactionComplete
title: 1037 - RuntimeTransactionComplete
ms.date: 03/30/2017
ms.assetid: 2c8c31e0-42a9-4f46-865b-2da9ab16a0ba
ms.openlocfilehash: 5784dc1b0eede5ddad0e6aae4cb79c6e859f325e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99667858"
---
# <a name="1037---runtimetransactioncomplete"></a>1037 - RuntimeTransactionComplete

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|1037|  
|关键字|WFRuntime|  
|级别|“详细”|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/调试|  
  
## <a name="description"></a>说明  

 指示运行时事务已完成。  
  
## <a name="message"></a>消息  

 运行时事务已完成，状态为“%1”。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|状态|xs:string|事务的状态。|  
|应用程序域|xs:string|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
