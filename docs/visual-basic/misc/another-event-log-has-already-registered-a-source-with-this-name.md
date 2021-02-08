---
description: 了解详细信息：另一个事件日志已使用此名称注册了源
title: 另一个事件日志已使用该名称注册了一个源
ms.date: 07/20/2015
ms.assetid: e6f5cd95-bb3f-4845-84fb-ae623a9bd44e
ms.openlocfilehash: ec6ae0b3ef12452a0135e5bf17dbdd5844c0f478
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99787352"
---
# <a name="another-event-log-has-already-registered-a-source-with-this-name"></a>另一个事件日志已使用该名称注册了一个源

已尝试向事件日志写入条目，其中指定的源使用其他事件日志进行注册。  
  
 在组件将条目写入日志前，必须设置 <xref:System.Diagnostics.EventLog.Source%2A> 组件实例的 <xref:System.Diagnostics.EventLog> 属性。 发生此情况时，系统将检查所指定的源是否使用写入该组件的事件日志进行注册，并在需要时调用 <xref:System.Diagnostics.EventLog.CreateEventSource%2A> 。  
  
## <a name="to-correct-this-error"></a>更正此错误  
  
1. 使用 <xref:System.Diagnostics.EventLog.DeleteEventSource%2A> 或 <xref:System.Diagnostics.EventLog.DeleteEventSource%2A> 方法删除源与第一个日志之间的关联。  
  
2. 使用新的日志注册源。  
  
## <a name="see-also"></a>请参阅

- [My. .Log](xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase.Log)
