---
description: 了解详细信息： INotifySink2 接口
title: INotifySink2 接口
ms.date: 03/30/2017
api_name:
- INotifySink2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- INotifySink2
helpviewer_keywords:
- INotifySink2 interface [.NET Framework debugging]
ms.assetid: c1018789-4206-455d-aacc-2d876fc0d0bb
topic_type:
- apiref
ms.openlocfilehash: 4d046c5566d9cb1641426f6a990f39449c33bc4d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800287"
---
# <a name="inotifysink2-interface"></a>INotifySink2 接口

声明接收器通知的方法。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[OnSyncCallEnter 方法](inotifysink2-onsynccallenter-method.md)|在输入调用时调用。|  
|[OnSyncCallExit 方法](inotifysink2-onsynccallexit-method.md)|在退出调用时调用。|  
|[OnSyncCallOut 方法](inotifysink2-onsynccallout-method.md)|在调用时调用。|  
|[OnSyncCallReturn 方法](inotifysink2-onsynccallreturn-method.md)|当调用返回时调用。|  
  
## <a name="requirements"></a>要求  

 **标头：** ProtocolNotify2 .idl  
  
## <a name="see-also"></a>请参阅

- [INotifyConnection2 接口](inotifyconnection2-interface.md)
- [INotifySource2 接口](inotifysource2-interface.md)
- [诊断符号存储区接口](diagnostics-symbol-store-interfaces.md)
