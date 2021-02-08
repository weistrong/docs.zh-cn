---
description: 了解详细信息： 3551-BufferOutOfOrderMessageNoBookmark
title: 3551 - BufferOutOfOrderMessageNoBookmark
ms.date: 03/30/2017
ms.assetid: 7930d6c4-c843-4a83-933a-cecd71b80d1e
ms.openlocfilehash: 573056fed1753ac55c51d9a074047e8eea15e229
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99777991"
---
# <a name="3551---bufferoutofordermessagenobookmark"></a>3551 - BufferOutOfOrderMessageNoBookmark

## <a name="properties"></a>属性  
  
|||  
|-|-|  
|ID|3551|  
|关键字|WFServices|  
|级别|信息|  
|通道|Microsoft-Windows-应用程序服务器-应用程序/分析|  
  
## <a name="description"></a>说明  

 指示书签恢复已失败。 服务实例准备好处理此特定操作时，将再次尝试该缓冲的接收操作。  
  
## <a name="message"></a>消息  

 此时不能执行服务实例“%1”上的操作“%2”。 服务实例准备好处理此特定操作时，将进行另一个尝试。  
  
## <a name="details"></a>详细信息  
  
|数据项名称|数据项类型|说明|  
|--------------------|--------------------|-----------------|  
|OperationName|xs:string|操作的名称。|  
|ServiceInstanceId|xs:string|服务实例的 ID。|  
|应用程序域|xs:string|由 AppDomain.CurrentDomain.FriendlyName 返回的字符串。|
