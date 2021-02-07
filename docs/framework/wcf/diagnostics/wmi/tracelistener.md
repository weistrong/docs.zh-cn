---
description: 了解详细信息： TraceListener
title: TraceListener
ms.date: 03/30/2017
ms.assetid: c2c0b595-a384-4eb3-b94d-1b3be7cc7a5c
ms.openlocfilehash: 4c351e71740e132ac4127108d2be2d7c2866c755
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99757314"
---
# <a name="tracelistener"></a>TraceListener

TraceListener。  
  
## <a name="syntax"></a>语法  
  
```csharp
class TraceListener  
{  
  string Name;  
  TraceListenerArgument TraceListenerArguments[];  
};  
```  
  
## <a name="methods"></a>方法  

 TraceListener 类不定义任何方法。  
  
## <a name="properties"></a>属性  

 TraceListener 类具有以下属性：  
  
### <a name="name"></a>名称  

 数据类型：字符串  
  
 访问类型：只读  
  
 跟踪侦听器的名称。  
  
### <a name="tracelistenerarguments"></a>TraceListenerArguments  

 数据类型：TraceListenerArgument 数组  
  
 访问类型：只读  
  
 跟踪侦听器的自变量。  
  
## <a name="requirements"></a>要求  
  
|MOF|已在 Servicemodel.mof 中声明。|  
|---------|-----------------------------------|  
|命名空间|已在 root\ServiceModel 中定义|
