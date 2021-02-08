---
description: 了解详细信息： 3503-DuplicateCorrelationQuery
title: 3503 - DuplicateCorrelationQuery
ms.date: 03/30/2017
ms.assetid: b857f8e6-ce4d-4da4-bc9d-6cd63fa558a4
ms.openlocfilehash: a8e1e41aad3aa1b273d8f8a5d7b0768fabe4e658
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99778069"
---
# <a name="3503---duplicatecorrelationquery"></a>3503 - DuplicateCorrelationQuery

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|3503|  
|关键字|WFServices|  
|级别|警告|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/分析|  
  
## <a name="description"></a>说明  

 指示找到了重复 CorrelationQuery。 计算相关性时将不使用重复查询。  
  
## <a name="message"></a>消息  

 找到了含有 Where='%1' 的重复 CorrelationQuery。 计算相关性时将不使用此重复查询。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|其中|xs:string|相关查询的 Where 部分。|  
|应用程序域|xs:string|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
