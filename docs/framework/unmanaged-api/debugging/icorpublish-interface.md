---
description: 了解详细信息： ICorPublish 接口
title: ICorPublish 接口
ms.date: 03/30/2017
api_name:
- ICorPublish
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublish
helpviewer_keywords:
- ICorPublish interface [.NET Framework debugging]
ms.assetid: 87c4fcb2-7703-4a2e-afb6-42973381b960
topic_type:
- apiref
ms.openlocfilehash: 0cec1d3407246989c6b916ca0760e6f556566ce6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721822"
---
# <a name="icorpublish-interface"></a>ICorPublish 接口

用作发布有关进程的信息，以及有关这些进程中的应用程序域的信息。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[EnumProcesses 方法](icorpublish-enumprocesses-method.md)|获取一个 [ICorPublishProcessEnum](icorpublishprocessenum-interface.md) 实例，它包含在此计算机上运行的托管进程。|  
|[GetProcess 方法](icorpublish-getprocess-method.md)|获取一个表示具有指定标识符的进程的 [ICorPublishProcess](icorpublishprocess-interface.md) 实例。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** CorPub，CorPub  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [调试接口](debugging-interfaces.md)
- [CorpubPublish Coclass](corpubpublish-coclass.md)
