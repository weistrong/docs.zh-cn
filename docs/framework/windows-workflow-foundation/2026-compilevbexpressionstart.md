---
description: 了解详细信息： 2026-CompileVbExpressionStart
title: 2026 - CompileVbExpressionStart
ms.date: 03/30/2017
ms.assetid: daad57eb-8198-49b5-9920-aa0e7428ccf1
ms.openlocfilehash: 45d1c236c8f0abe938a9a985106eda6f22b14ca8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755403"
---
# <a name="2026---compilevbexpressionstart"></a>2026 - CompileVbExpressionStart

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|2026|  
|关键字|WFRuntime|  
|级别|“详细”|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/调试|  
  
## <a name="description"></a>说明  

 指示 Visual Basic 表达式编译的开头。  
  
## <a name="message"></a>消息  

 正在编译 Visual Basic 表达式 "%1"  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|表达式|xs:string|要编译的 VisualBasic 表达式。|  
|应用程序域|xs:string|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
