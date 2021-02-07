---
description: 了解详细信息： ActivityTransfer
title: ActivityTransfer
ms.date: 03/30/2017
ms.assetid: fc40ef17-2a92-4ce2-853c-6ba8e5d571f3
ms.openlocfilehash: 28f7d1c0d1056327313e7aa6be293eb325d8f265
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99758003"
---
# <a name="activitytransfer"></a>ActivityTransfer

活动传输事件  
  
## <a name="syntax"></a>语法  
  
```csharp
class ActivityTransfer : WSAT_TraceEvent  
{  
  object ActivityID;  
  object RelatedActivityID;  
};  
```  
  
## <a name="methods"></a>方法  

 ActivityTransfer 类不定义任何方法。  
  
## <a name="properties"></a>属性  

 ActivityTransfer 类具有以下属性：  
  
### <a name="activityid"></a>ActivityID  
  
- 数据类型：object  
    访问类型：只读  
  
- 活动 ID  
  
### <a name="relatedactivityid"></a>RelatedActivityID  
  
- 数据类型：object  
    访问类型：只读  
  
- 相关活动 ID  
  
## <a name="requirements"></a>要求  
  
|MOF|已在 Servicemodel.mof 中声明。|  
|---------|-----------------------------------|  
|命名空间|已在 root\ServiceModel 中定义。|
