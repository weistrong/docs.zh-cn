---
description: 了解详细信息： IDebuggerThreadControl：： StartBlockingForDebugger 方法
title: IDebuggerThreadControl::StartBlockingForDebugger 方法
ms.date: 03/30/2017
api_name:
- IDebuggerThreadControl.StartBlockingForDebugger
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- StartBlockingForDebugger
helpviewer_keywords:
- IDebuggerThreadControl::StartBlockingForDebugger method [.NET Framework hosting]
- StartBlockingForDebugger method [.NET Framework hosting]
ms.assetid: 5c8f11b4-35d3-4c39-9bbd-58b896ba5ba6
topic_type:
- apiref
ms.openlocfilehash: 3e19817c4adbefd1dd70be047656b3fea261c389
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709667"
---
# <a name="idebuggerthreadcontrolstartblockingfordebugger-method"></a>IDebuggerThreadControl::StartBlockingForDebugger 方法

通知宿主调试服务即将开始阻塞所有线程。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT StartBlockingForDebugger (  
    [in] DWORD dwUnused  
);  
```  
  
## <a name="parameters"></a>参数  

 `dwUnused`  
 中保留供将来使用。  
  
## <a name="remarks"></a>备注  

 `StartBlockingForDebugger`可以在运行时线程上调用方法。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IDebuggerThreadControl 接口](idebuggerthreadcontrol-interface.md)
