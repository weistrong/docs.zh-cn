---
description: 了解详细信息： IGCThreadControl：： SuspensionEnding 方法
title: IGCThreadControl::SuspensionEnding 方法
ms.date: 03/30/2017
api_name:
- IGCThreadControl.SuspensionEnding
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- SuspensionEnding
helpviewer_keywords:
- IGCThreadControl::SuspensionEnding method [.NET Framework hosting]
- SuspensionEnding method, IGCThreadControl interface [.NET Framework hosting]
ms.assetid: 70814265-c734-4ddc-9502-fe8b28d2b414
topic_type:
- apiref
ms.openlocfilehash: 5ff889f45ea3664312060f373907e65c367276f1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709264"
---
# <a name="igcthreadcontrolsuspensionending-method"></a>IGCThreadControl::SuspensionEnding 方法

向宿主通知运行时在垃圾回收或其他挂起后正在恢复线程。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT SuspensionEnding (  
    [in] DWORD Generation  
);  
```  
  
## <a name="parameters"></a>参数  

 `Generation`  
 中已对其执行垃圾回收的代。  
  
## <a name="remarks"></a>备注  

 不要在回调过程中重新计划任何线程 `SuspensionEnding` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IGCThreadControl 接口](igcthreadcontrol-interface.md)
