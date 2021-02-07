---
description: 了解详细信息： ICorDebugModule：： EnableJITDebugging 方法
title: ICorDebugModule::EnableJITDebugging 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule.EnableJITDebugging
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule::EnableJITDebugging
helpviewer_keywords:
- ICorDebugModule::EnableJITDebugging method [.NET Framework debugging]
- EnableJITDebugging method [.NET Framework debugging]
ms.assetid: 0a65e2a4-5bb6-496c-ae6f-40474426b5a6
topic_type:
- apiref
ms.openlocfilehash: 30077bd586e1cb9cb8766290804e31f5999d9e72
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722680"
---
# <a name="icordebugmoduleenablejitdebugging-method"></a>ICorDebugModule::EnableJITDebugging 方法

控制实时 (JIT) 编译器是否保留此模块内方法的调试信息。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT EnableJITDebugging(  
    [in] BOOL bTrackJITInfo,  
    [in] BOOL bAllowJitOpts  
);  
```  
  
## <a name="parameters"></a>参数  

 `bTrackJITInfo`  
 中将此值设置为 `true` ，以使 JIT 编译器能够在此模块中的每个方法的 Microsoft 中间语言 (MSIL) 版本和 JIT 编译版本之间保留映射信息。  
  
 `bAllowJitOpts`  
 中将此值设置为 `true` ，可让 jit 编译器生成代码，并使用特定于 JIT 的优化进行调试。  
  
## <a name="remarks"></a>备注  

 默认情况下，调试程序处于活动状态时加载的所有模块都已启用 JIT 调试。 以编程方式启用或禁用设置将覆盖全局设置。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]
