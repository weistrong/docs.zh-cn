---
description: 了解详细信息： IHostControl 接口
title: IHostControl 接口
ms.date: 03/30/2017
api_name:
- IHostControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostControl
helpviewer_keywords:
- IHostControl interface [.NET Framework hosting]
ms.assetid: a4ae0d1f-ade9-4b0a-a122-93ed11a5e6b3
topic_type:
- apiref
ms.openlocfilehash: e7a242ed0fdaa734425bec9b48f01fe45cba5182
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789458"
---
# <a name="ihostcontrol-interface"></a>IHostControl 接口

提供用于配置程序集加载和确定宿主支持哪些宿主接口的方法。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[GetHostManager 方法](ihostcontrol-gethostmanager-method.md)|获取一个接口指针，该指针指向具有指定的接口的主机实现 `IID` 。|  
|[SetAppDomainManager 方法](ihostcontrol-setappdomainmanager-method.md)|通知宿主已创建应用程序域。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- <xref:System.AppDomainManager>
- [ICLRRuntimeHost 接口](iclrruntimehost-interface.md)
- [ICLRControl 接口](iclrcontrol-interface.md)
- [承载接口](hosting-interfaces.md)
