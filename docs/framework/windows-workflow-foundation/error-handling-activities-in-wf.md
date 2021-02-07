---
description: 了解详细信息： WF 中的错误处理活动
title: WF 中的错误处理活动
ms.date: 03/30/2017
ms.assetid: 24b68bd3-cef5-4413-ab82-2e2625f209aa
ms.openlocfilehash: ef26c47d8d99f2d2186ef02820f9bebe691c2ff8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99742441"
---
# <a name="error-handling-activities-in-wf"></a>WF 中的错误处理活动

[!INCLUDE[netfx_current_long](../../../includes/netfx-current-long-md.md)]提供多个系统提供的活动，用于实现错误处理和恢复。 有关更多信息，请参见 [异常](exceptions.md)中定义的接口的私有 C++ 特定实现。  
  
## <a name="error-handling-activities"></a>错误处理活动  
  
|||  
|-|-|  
|<xref:System.Activities.Statements.Rethrow>|重新引发从 `TryCatch` 活动中引发的最后一个异常。|  
|<xref:System.Activities.Statements.Throw>|引发异常。|  
|<xref:System.Activities.Statements.TryCatch>|实现异常处理。|
