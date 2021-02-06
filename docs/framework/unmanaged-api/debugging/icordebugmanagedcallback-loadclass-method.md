---
description: 了解详细信息： ICorDebugManagedCallback：： LoadClass 方法
title: ICorDebugManagedCallback::LoadClass 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.LoadClass
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::LoadClass
helpviewer_keywords:
- ICorDebugManagedCallback::LoadClass method [.NET Framework debugging]
- LoadClass method [.NET Framework debugging]
ms.assetid: e58dac7b-85c3-41ca-b9aa-3a7fc9ae6680
topic_type:
- apiref
ms.openlocfilehash: 6f670a2f0798c7edfdc4292334cf9534e59a3007
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99660601"
---
# <a name="icordebugmanagedcallbackloadclass-method"></a>ICorDebugManagedCallback::LoadClass 方法

通知调试器已加载某个类。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT LoadClass (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugClass     *c  
);  
```  
  
## <a name="parameters"></a>参数  

 `pAppDomain`  
 中指向 ICorDebugAppDomain 对象的指针，该对象表示要将该类加载到其中的应用程序域。  
  
 `c`  
 中指向 ICorDebugClass 对象的指针，该对象表示类。  
  
## <a name="remarks"></a>备注  

 只有在为包含类的模块启用了类加载的情况下，才会发生此回调。 对于动态模块，始终启用类加载。  
  
 `LoadClass`回调提供适当的时间将断点绑定到动态模块中新生成的类。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [UnloadClass 方法](icordebugmanagedcallback-unloadclass-method.md)
- [ICorDebugManagedCallback 接口](icordebugmanagedcallback-interface.md)
