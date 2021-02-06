---
description: 了解详细信息： ICorDebugManagedCallback：： LoadModule 方法
title: ICorDebugManagedCallback::LoadModule 方法
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback.LoadModule
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback::LoadModule
helpviewer_keywords:
- ICorDebugManagedCallback::LoadModule method [.NET Framework debugging]
- LoadModule method [.NET Framework debugging]
ms.assetid: 66ec04e9-87cb-42ce-9720-81522abb5d5a
topic_type:
- apiref
ms.openlocfilehash: 9a547d384b3f450054ebc70072664c6dcfb5992f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99660488"
---
# <a name="icordebugmanagedcallbackloadmodule-method"></a>ICorDebugManagedCallback::LoadModule 方法

通知调试器已成功加载公共语言运行时 (CLR) 模块。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT LoadModule (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugModule    *pModule  
);  
```  
  
## <a name="parameters"></a>参数  

 `pAppDomain`  
 中指向 ICorDebugAppDomain 对象的指针，该对象表示已加载该模块的应用程序域。  
  
 `pModule`  
 中指向 ICorDebugModule 对象的指针，该对象表示 CLR 模块。  
  
## <a name="remarks"></a>备注  

 `LoadModule`回调提供适当的时间来检查模块的元数据、设置实时 (JIT) 编译器标志，或者为模块启用或禁用类加载回调。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [UnloadModule 方法](icordebugmanagedcallback-unloadmodule-method.md)
- [ICorDebugManagedCallback 接口](icordebugmanagedcallback-interface.md)
