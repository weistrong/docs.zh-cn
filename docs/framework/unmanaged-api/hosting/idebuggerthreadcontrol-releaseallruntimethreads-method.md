---
description: 了解详细信息： IDebuggerThreadControl：： ReleaseAllRuntimeThreads 方法
title: IDebuggerThreadControl::ReleaseAllRuntimeThreads 方法
ms.date: 03/30/2017
api_name:
- IDebuggerThreadControl.ReleaseAllRuntimeThreads
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ReleaseAllRuntimeThreads
helpviewer_keywords:
- ReleaseAllRuntimeThreads method [.NET Framework hosting]
- IDebuggerThreadControl::ReleaseAllRuntimeThreads method [.NET Framework hosting]
ms.assetid: 1a2995ff-5f02-4b49-84dc-3a5f9cfd7d55
topic_type:
- apiref
ms.openlocfilehash: bf551ccc2ae5bde3333dc8e3957099590a494dd3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709723"
---
# <a name="idebuggerthreadcontrolreleaseallruntimethreads-method"></a>IDebuggerThreadControl::ReleaseAllRuntimeThreads 方法

向宿主通知调试服务将要释放被阻止的所有线程。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT ReleaseAllRuntimeThreads ( );  
```  
  
## <a name="remarks"></a>备注  

 `ReleaseAllRuntimeThreads`永远不会在运行时线程上调用方法。 如果主机已阻止运行时线程，则它现在应释放它。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IDebuggerThreadControl 接口](idebuggerthreadcontrol-interface.md)
