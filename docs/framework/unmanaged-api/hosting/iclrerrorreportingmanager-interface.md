---
description: 了解详细信息： ICLRErrorReportingManager 接口
title: ICLRErrorReportingManager 接口
ms.date: 03/30/2017
api_name:
- ICLRErrorReportingManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRErrorReportingManager
helpviewer_keywords:
- ICLRErrorReportingManager interface [.NET Framework hosting]
ms.assetid: ea8af0d5-4133-4472-8a1f-50570d7e85fa
topic_type:
- apiref
ms.openlocfilehash: 094fe52858983fd0e1e5826e823932cb150b6087
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689269"
---
# <a name="iclrerrorreportingmanager-interface"></a>ICLRErrorReportingManager 接口

提供允许主机配置自定义堆栈转储以用于错误报告的方法。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[BeginCustomDump 方法](iclrerrorreportingmanager-begincustomdump-method.md)|指定用于错误报告的自定义堆栈转储配置。|  
|[EndCustomDump 方法](iclrerrorreportingmanager-endcustomdump-method.md)|清除由先前对的调用设置的自定义堆栈转储配置 `BeginCustomDump` 。|  
|[GetBucketParametersForCurrentException 方法](iclrerrorreportingmanager-getbucketparametersforcurrentexception-method.md)|获取调用线程上的当前异常的 Watson 存储桶。|  
  
## <a name="remarks"></a>备注  

 `BeginCustomDump`方法设置自定义堆栈转储配置。 `EndCustomDump`方法清除自定义堆栈转储配置并释放任何关联的状态。 应在自定义转储完成后调用它。  
  
> [!IMPORTANT]
> 调用失败 `EndCustomDump` 会导致内存泄露。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ECustomDumpItemKind 枚举](ecustomdumpitemkind-enumeration.md)
- [承载接口](hosting-interfaces.md)
