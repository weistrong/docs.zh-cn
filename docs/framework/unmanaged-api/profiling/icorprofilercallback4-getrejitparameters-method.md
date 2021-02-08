---
description: 了解详细信息： ICorProfilerCallback4：： GetReJITParameters 方法
title: ICorProfilerCallback4::GetReJITParameters 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback4.GetReJITParameters
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback4::GetReJITParameters
helpviewer_keywords:
- ICorProfilerCallback4::GetReJITParameters method [.NET Framework profiling]
- GetReJITParameters method, ICorProfilerCallback4 interface [.NET Framework profiling]
ms.assetid: 0e9bfe07-9f20-498c-b568-9017c8f6056c
topic_type:
- apiref
ms.openlocfilehash: f8dbf2c6ae80e41b8427fdaf0ef617a83138bb14
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99788756"
---
# <a name="icorprofilercallback4getrejitparameters-method"></a>ICorProfilerCallback4::GetReJITParameters 方法

允许代码探查器为新的重新编译的方法体设置备用代码生成标志。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetReJITParameters(     [in] ModuleID moduleId,     [in] mdMethodDef methodId,     [in] ICorProfilerFunctionControl *pFunctionControl);  
```  
  
## <a name="parameters"></a>参数  

 `moduleID`  
 中包含 CLR 需要 JIT 重新编译参数的方法的模块。  
  
 `methodId`  
 中 `MethodDef` CLR 需要 JIT 重新编译参数的方法的。  
  
 `pFunctionControl`  
 中指向 [ICorProfilerFunctionControl](icorprofilerfunctioncontrol-interface.md) 接口的指针，探查器可以使用该接口为要重新编译的方法提供 JIT 重新编译信息。  
  
## <a name="remarks"></a>备注  

 CLR 发出 `GetReJITParameters` 回调，以便探查器可以指定用于重新编译给定方法的参数。 `GetReJITParameters`仅对每个函数发出一次回调; 探查器提供的参数将应用于该函数的所有实例。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **头文件：** CorProf.idl、CorProf.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICorProfilerCallback 接口](icorprofilercallback-interface.md)
- [ICorProfilerCallback4 接口](icorprofilercallback4-interface.md)
- [JITCompilationStarted 方法](icorprofilercallback-jitcompilationstarted-method.md)
- [ReJITCompilationStarted 方法](icorprofilercallback4-rejitcompilationstarted-method.md)
