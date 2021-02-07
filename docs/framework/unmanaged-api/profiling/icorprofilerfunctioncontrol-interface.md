---
description: 了解详细信息： ICorProfilerFunctionControl 接口
title: ICorProfilerFunctionControl 接口
ms.date: 03/30/2017
api_name:
- ICorProfilerFunctionControl
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerFunctionControl
helpviewer_keywords:
- ICorProfilerFunctionControl interface [.NET Framework profiling]
ms.assetid: 4e3d3141-4662-4166-8f05-bc857c1b4216
topic_type:
- apiref
ms.openlocfilehash: 7b4ac58d2b8754108b4e10493596776987a93a49
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753310"
---
# <a name="icorprofilerfunctioncontrol-interface"></a>ICorProfilerFunctionControl 接口

提供允许代码探查器与公共语言运行时 (CLR) 进行通信的方法，从而在重新编译特定方法时控制 JIT 探查器应生成代码的方式。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[SetCodegenFlags 方法](icorprofilerfunctioncontrol-setcodegenflags-method.md)|设置 [COR_PRF_CODEGEN_FLAGS](cor-prf-codegen-flags-enumeration.md) 枚举中的一个或多个标志，以控制实时 (JIT) 重新编译函数的代码生成。|  
|[SetILFunctionBody 方法](icorprofilerfunctioncontrol-setilfunctionbody-method.md)|替换方法的公共中间语言 (CIL) 主体。|  
|[SetILInstrumentedCodeMap 方法](icorprofilerfunctioncontrol-setilinstrumentedcodemap-method.md)|使用指定的公共中间语言 (CIL) 映射项为指定的函数设置代码图。|  
  
## <a name="remarks"></a>备注  

 `ICorProfilerFunctionControl` 接口提供了用于控制单个重新编译函数的代码生成的方法。 探查器通过 [ICorProfilerCallback4：： GetReJITParameters](icorprofilercallback4-getrejitparameters-method.md) 回调获取此接口的实例。 `ICorProfilerFunctionControl` 的每个实例都可控制一个函数的所有实例。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **头文件：** CorProf.idl、CorProf.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICorProfilerInfo4 接口](icorprofilerinfo4-interface.md)
- [分析接口](profiling-interfaces.md)
- [EnumJITedFunctions2 方法](icorprofilerinfo4-enumjitedfunctions2-method.md)
