---
description: 了解详细信息： IAppDomainBinding 接口
title: IAppDomainBinding 接口
ms.date: 03/30/2017
api_name:
- IAppDomainBinding
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IAppDomainBinding
helpviewer_keywords:
- IAppDomainBinding interface [.NET Framework hosting]
ms.assetid: 368881ab-c4ea-4731-bf22-c596aac7c66c
topic_type:
- apiref
ms.openlocfilehash: 3de559af023311f705f9f7dc6eb9785788216a83
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760610"
---
# <a name="iappdomainbinding-interface"></a>IAppDomainBinding 接口

提供一个方法，该方法由公共语言运行时 (CLR) ，用于通知宿主应用程序已创建应用程序域。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[OnAppDomain 方法](iappdomainbinding-onappdomain-method.md)|由公共语言运行时 (CLR) 调用，以通知宿主已创建应用程序域。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [承载接口](hosting-interfaces.md)
