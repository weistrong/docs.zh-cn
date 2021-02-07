---
description: 了解详细信息： CorRuntimeHost 组件类
title: CorRuntimeHost 组件类
ms.date: 03/30/2017
api_name:
- CorRuntimeHost Coclass
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorRuntimeHost
helpviewer_keywords:
- CoRuntimeHost coclass [.NET Framework hosting]
ms.assetid: 5833740b-7d67-44b4-865c-b5bf45e291e3
topic_type:
- apiref
ms.openlocfilehash: cd2d01075e5c8264337e1e989b3d9fdc6bf68962
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760631"
---
# <a name="corruntimehost-coclass"></a>CorRuntimeHost 组件类

提供用于管理由公共语言运行时执行的应用程序的接口。  
  
## <a name="syntax"></a>语法  
  
```cpp  
coclass CorRuntimeHost {  
    [default] interface ICorRuntimeHost;  
    interface IGCHost;  
    interface ICorConfiguration;  
    interface IValidator;  
    interface IDebuggerInfo;  
};  
```  
  
## <a name="interfaces"></a>界面  
  
|接口|说明|  
|---------------|-----------------|  
|[ICorConfiguration 接口](icorconfiguration-interface.md)|提供 (CLR) 配置公共语言运行时的方法。|  
|[ICorRuntimeHost 接口](icorruntimehost-interface.md)|提供使宿主可以显式启动和停止公共语言运行时、创建和配置应用程序域、访问默认域和枚举进程中运行的所有域的方法。|  
|[IDebuggerInfo 接口](idebuggerinfo-interface.md)|提供用于获取有关调试服务状态的信息的方法。|  
|[IGCHost 接口](igchost-interface.md)|提供一些方法，用于获取有关垃圾回收系统的信息并控制垃圾回收的某些方面。|  
|IValidator|提供可移植可执行映像的验证和验证错误的详细报告的方法。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [承载组件类](hosting-coclasses.md)
