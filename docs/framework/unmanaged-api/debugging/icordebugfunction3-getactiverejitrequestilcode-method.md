---
description: 了解详细信息： ICorDebugFunction3：： GetActiveReJitRequestILCode 方法
title: ICorDebugFunction3::GetActiveReJitRequestILCode 方法
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- ICorDebugFunction3.GetActiveReJitRequestILCode
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 88584574-ade5-45b2-9778-489ed5c4dd7f
topic_type:
- apiref
ms.openlocfilehash: 9225c5cdf97395b7e1b11c61d653cab8d52031c6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99692116"
---
# <a name="icordebugfunction3getactiverejitrequestilcode-method"></a>ICorDebugFunction3::GetActiveReJitRequestILCode 方法

[仅在 .NET Framework 4.5.2 及更高版本中受支持]  
  
 获取一个接口指针，该指针指向包含活动 ReJIT 请求中的 IL 的 [ICorDebugILCode](icordebugilcode-interface.md) 。  
  
## <a name="syntax"></a>语法  
  
```cpp
HRESULT GetActiveReJitRequestILCode(  
   ICorDebugILCode **ppReJitedILCode  
);  
```  
  
## <a name="parameters"></a>参数  

 `ppReJitedILCode`  
 指向活动 ReJIT 请求中的 IL 的指针。  
  
## <a name="remarks"></a>备注  

 如果此 `ICorDebugFunction3` 对象表示的方法具有活动 ReJIT 请求，则 `ppReJitedILCode` 将返回指向其 IL 的指针。 如果没有活动请求（这是常见情况），则 `ppReJitedILCode` 为 **null**。  
  
 ReJIT 请求在执行从 [ICorProfilerCallback4：： GetReJITParameters](../profiling/icorprofilercallback4-getrejitparameters-method.md) 方法调用返回后变为活动状态。 可能尚未对它进行 JIT 编译，而且线程可能仍然在原始版本的代码中执行。 在探查器调用 [ICorProfilerInfo4：： RequestRevert](../profiling/icorprofilerinfo4-requestrevert-method.md) 方法的过程中，ReJIT 请求将变为非活动状态。 即使还原了 IL 之后，线程仍然可在 JIT 编译 (ReJIT) 的代码中执行。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICorDebugFunction3 接口](icordebugfunction3-interface.md)
- [调试接口](debugging-interfaces.md)
- [ReJIT： How-To 指南](/archive/blogs/davbr/rejit-a-how-to-guide)
