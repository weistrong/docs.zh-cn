---
description: 了解详细信息： ICLRDebugManager：： SetDacl 方法
title: ICLRDebugManager::SetDacl 方法
ms.date: 03/30/2017
api_name:
- ICLRDebugManager.SetDacl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRDebugManager::SetDacl
helpviewer_keywords:
- SetDacl method [.NET Framework hosting]
- ICLRDebugManager::SetDacl method [.NET Framework hosting]
ms.assetid: 52f4af3f-e02b-4c20-9fd9-e8e4f4d6fc31
topic_type:
- apiref
ms.openlocfilehash: b507d94f9e23e509d279a0fd4e32c8c996a4668b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689551"
---
# <a name="iclrdebugmanagersetdacl-method"></a>ICLRDebugManager::SetDacl 方法

未实现此方法。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT SetDacl (  
    [in] PACL pacl  
);  
```  
  
## <a name="parameters"></a>参数  

 `pacl`  
 中指向访问控制列表 (ACL) 的指针。  
  
## <a name="return-value"></a>返回值  
  
|HRESULT|说明|  
|-------------|-----------------|  
|E_NOTIMPL|该方法未实现。|  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** 作为中的资源包含 MSCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICLRControl 接口](iclrcontrol-interface.md)
- [ICLRDebugManager 接口](iclrdebugmanager-interface.md)
- [GetDacl 方法](iclrdebugmanager-getdacl-method.md)
- [IHostControl 接口](ihostcontrol-interface.md)
