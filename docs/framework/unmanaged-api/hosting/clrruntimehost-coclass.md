---
description: 了解详细信息： CLRRuntimeHost 组件类
title: CLRRuntimeHost 组件类
ms.date: 03/30/2017
api_name:
- CLRRuntimeHost Coclass
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CLRRuntimeHost
helpviewer_keywords:
- CLRRuntimeHost coclass [.NET Framework hosting]
ms.assetid: 2ac9cbf5-8a2d-4e4f-8831-0dad8ef0a897
topic_type:
- apiref
ms.openlocfilehash: a371b9b7263f8bb58b5c513de6647320f000beed
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799884"
---
# <a name="clrruntimehost-coclass"></a>CLRRuntimeHost 组件类

提供用于管理运行时执行的代码的接口。  
  
## <a name="syntax"></a>语法  
  
```cpp  
coclass CLRRuntimeHost {  
    [default] interface  ICLRRuntimeHost;  
    interface            ICLRValidator;  
};  
```  
  
## <a name="interfaces"></a>界面  
  
|接口|说明|  
|---------------|-----------------|  
|[ICLRRuntimeHost 接口](iclrruntimehost-interface.md)|提供通过运行时控制应用程序执行的方法。|  
|[ICLRValidator 接口](iclrvalidator-interface.md)|提供可移植可执行映像的验证方法，并提供验证错误的详细报告。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [承载组件类](hosting-coclasses.md)
