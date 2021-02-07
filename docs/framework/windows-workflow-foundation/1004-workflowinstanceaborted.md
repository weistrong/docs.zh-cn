---
description: 了解详细信息： 1004-WorkflowInstanceAborted
title: 1004 - WorkflowInstanceAborted
ms.date: 03/30/2017
ms.assetid: edb9ab8c-0b9a-488d-aa96-9c8c7984b53c
ms.openlocfilehash: 4aaa0899da9b0b8510684a13537a8cb8f9117ee1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99755611"
---
# <a name="1004---workflowinstanceaborted"></a>1004 - WorkflowInstanceAborted

## <a name="properties"></a>属性

|||
|-|-|
|ID|1004|
|关键字|WFRuntime|
|级别|信息|
|通道|Microsoft-Windows-应用程序服务器-应用程序/调试|

## <a name="description"></a>说明

指示工作流实例已中止但出现异常。

## <a name="message"></a>消息

WorkflowInstance Id“%1”因出现异常而中止。

## <a name="details"></a>详细信息

|数据项名称|数据项类型|说明|
|--------------------|--------------------|-----------------|
|WorkflowInstanceId|`xs:string`|工作流的实例 ID|
|异常|`xs:string`|异常的异常详细信息|
|应用程序域|`xs:string`|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
