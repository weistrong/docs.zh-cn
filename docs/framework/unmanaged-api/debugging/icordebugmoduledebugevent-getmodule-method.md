---
description: 了解详细信息： ICorDebugModuleDebugEvent：： GetModule 方法
title: ICorDebugModuleDebugEvent::GetModule 方法
ms.date: 03/30/2017
ms.assetid: b1141c35-4253-4e34-b3e4-ed406a9dea4f
ms.openlocfilehash: c6d7171da231576ff90f54aaefe4b473af0afd40
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790732"
---
# <a name="icordebugmoduledebugeventgetmodule-method"></a>ICorDebugModuleDebugEvent::GetModule 方法

获取刚加载或卸载的合并模块。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetModule(  
   [out]ICorDebugModule **ppModule  
);  
```  
  
## <a name="parameters"></a>参数  

 `ppModule`  
 [out] 指向 ICorDebugModule 对象地址的指针，该对象表示刚加载或卸载的合并模块。  
  
## <a name="remarks"></a>备注  

 可以调用 [GetEventKind](icordebugdebugevent-geteventkind-method.md) 方法来确定是加载还是卸载该模块。  
  
> [!NOTE]
> 此方法仅适用于 .NET Native。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICorDebugModuleDebugEvent 接口](icordebugmoduledebugevent-interface.md)
- [调试接口](debugging-interfaces.md)
