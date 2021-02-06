---
description: 了解详细信息：实例
title: 实例数
ms.date: 03/30/2017
ms.assetid: c8cf3460-0ca1-4411-8262-e9ecaf7f0a31
ms.openlocfilehash: 9cd602164816a419b481ff600a7537593d4f500e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99655261"
---
# <a name="instances"></a>实例数

计数器名称：Instances（实例数）。  
  
## <a name="description"></a>说明  

 服务当前包含的实例上下文的数量。  
  
 在大部分时间里，实例上下文的数量都等于实例数。 但是，下列方案例外。  
  
- 服务方法显式调用 <xref:System.ServiceModel.Dispatcher.IInstanceProvider.ReleaseInstance%2A> 方法。  
  
- 一个 <xref:System.ServiceModel.ReleaseInstanceMode> 被应用于一个 <xref:System.ServiceModel.OperationBehaviorAttribute> 实例。  
  
## <a name="see-also"></a>请参阅

- <xref:System.ServiceModel.OperationBehaviorAttribute>
