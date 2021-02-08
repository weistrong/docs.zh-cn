---
description: 了解详细信息： ETaskType 枚举
title: ETaskType 枚举
ms.date: 03/30/2017
api_name:
- ETaskType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ETaskType
helpviewer_keywords:
- ETaskType enumeration [.NET Framework hosting]
ms.assetid: aa527b31-89d4-41f2-ad6f-63b76950b7df
topic_type:
- apiref
ms.openlocfilehash: 7cb241765b2ff3b4a3402221c6b3e2b7ff6305c1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785397"
---
# <a name="etasktype-enumeration"></a>ETaskType 枚举

包含一些值，这些值指示由 [ICLRTask](iclrtask-interface.md) 或 [IHostTask](ihosttask-interface.md) 接口表示的任务的类型。  
  
## <a name="syntax"></a>语法  
  
```cpp  
typedef enum ETaskType {  
    TT_DEBUGGERHELPER           = 0x1,  
    TT_GC                       = 0x2,  
    TT_FINALIZER                = 0x4,  
    TT_THREADPOOL_TIMER         = 0x8,  
    TT_THREADPOOL_GATE          = 0x10,  
    TT_THREADPOOL_WORKER        = 0x20,  
    TT_THREADPOOL_IOCOMPLETION  = 0x40,  
    TT_ADUNLOAD                 = 0x80,  
    TT_USER                     = 0x100,  
    TT_THREADPOOL_WAIT          = 0x200,  
    TT_UNKNOWN                  = 0x80000000  
} ETaskType;  
```  
  
## <a name="members"></a>成员  
  
|成员|说明|  
|------------|-----------------|  
|`TT_ADUNLOAD`|接口表示应用程序域卸载任务。|  
|`TT_DEBUGGERHELPER`|接口表示调试器帮助器任务。|  
|`TT_FINALIZER`|接口表示终结器任务。|  
|`TT_GC`|接口表示垃圾回收任务。|  
|`TT_THREADPOOL_GATE`|接口表示一个 "入口线程" 任务。|  
|`TT_THREADPOOL_IOCOMPLETION`|接口表示 i/o 线程任务或完成端口线程任务。|  
|`TT_THREADPOOL_TIMER`|接口表示计时器线程任务。|  
|`TT_THREADPOOL_WAIT`|接口表示等待线程任务。|  
|`TT_THREADPOOL_WORKER`|接口表示工作线程任务。|  
|`TT_UNKNOWN`|任务未知。|  
|`TT_USER`|接口表示用户任务。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [承载枚举](hosting-enumerations.md)
