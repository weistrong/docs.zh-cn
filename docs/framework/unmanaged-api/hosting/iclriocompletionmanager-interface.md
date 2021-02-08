---
description: 了解详细信息： ICLRIoCompletionManager 接口
title: ICLRIoCompletionManager 接口
ms.date: 03/30/2017
api_name:
- ICLRIoCompletionManager
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRIoCompletionManager
helpviewer_keywords:
- ICLRIoCompletionManager interface [.NET Framework hosting]
ms.assetid: c6c3ace6-e5e7-4450-8cc5-a9a48208c493
topic_type:
- apiref
ms.openlocfilehash: b2d18f9c9900d448f0c6517520c303eb4258f8d3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789877"
---
# <a name="iclriocompletionmanager-interface"></a>ICLRIoCompletionManager 接口

实现一个回调方法，该方法允许宿主通知公共语言运行时 (CLR) 指定 i/o 请求的状态。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[OnComplete 方法](iclriocompletionmanager-oncomplete-method.md)|使用对 [IHostIoCompletionManager：： Bind](ihostiocompletionmanager-bind-method.md) 方法的调用，将发出的 i/o 请求状态通知给 CLR。|  
  
## <a name="remarks"></a>备注  

 宿主通过使用 [IHostIoCompletionManager](ihostiocompletionmanager-interface.md) 接口实现 i/o 完成抽象。 CLR 通过此接口发出 i/o 请求，主机使用接口通知运行时此类请求的结果 `ICLRIoCompletionManager` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IHostIoCompletionManager 接口](ihostiocompletionmanager-interface.md)
- [IHostThreadPoolManager 接口](ihostthreadpoolmanager-interface.md)
- [承载接口](hosting-interfaces.md)
