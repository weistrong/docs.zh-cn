---
description: 了解更多： VisualStudio. ClientActivityBuilder。ctor
title: Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder..ctor
ms.date: 03/30/2017
ms.topic: reference
api_name:
- Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder..ctor
api_location:
- Microsoft.VisualStudio.Activities.dll
api_type:
- Assembly
ms.assetid: 6b44b13c-7a23-4df2-8f9f-45e2b1430002
ms.openlocfilehash: 1a1b436c2b15fdf07f924aa0db2a13598422e988
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99739984"
---
# <a name="microsoftvisualstudioactivitiesasrclientactivitybuilderctor"></a>Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder..ctor

创建 VisualStudio 的实例。 [ClientActivityBuilder](microsoft-visualstudio-activities-asr-clientactivitybuilder.md) 类的实例。  
  
## <a name="syntax"></a>语法  
  
```csharp  
public ClientActivityBuilder(OperationDescription operationDescription, string configurationName, string proxyNamespace);  
```  
  
## <a name="parameters"></a>参数  
  
## <a name="parameter-values"></a>参数值  

 *operationDescription*  
  
 描述要在生成的工作流活动中执行的操作，包括操作名称、返回类型和参数信息。 此参数的值不得为 **null**。 它应描述使用消息协定并且取得具有一个消息的参数的同步操作。 如果不满足这些条件，则使用此类的构造函数和其他方法的运行时结果未被定义。  
  
 *configurationName*  
  
 指定终结点配置名称。 此参数的值不能为 **null** 或为空。 如果不满足这些条件，则使用此类的构造函数和其他方法的运行时结果未被定义。  
  
 *proxyNamespace*  
  
 指定操作的服务命名空间。 此参数的值不能为 **null** 或为空。 如果不满足这些条件，则使用此类的构造函数和其他方法的运行时结果未被定义。  
  
## <a name="see-also"></a>请参阅

- [Microsoft.VisualStudio.Activities.Asr.ClientActivityBuilder](microsoft-visualstudio-activities-asr-clientactivitybuilder.md)
