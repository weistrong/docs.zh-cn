---
description: 了解详细信息： ICorProfilerCallback：： JITFunctionPitched 方法
title: ICorProfilerCallback::JITFunctionPitched 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.JITFunctionPitched
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::JITFunctionPitched
helpviewer_keywords:
- JITFunctionPitched method [.NET Framework profiling]
- ICorProfilerCallback::JITFunctionPitched method [.NET Framework profiling]
ms.assetid: 116085df-7a77-404a-afac-d0557a12b986
topic_type:
- apiref
ms.openlocfilehash: 11729de2188fe2f2cec7ec16ff7a5d1928cbd75d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99705715"
---
# <a name="icorprofilercallbackjitfunctionpitched-method"></a>ICorProfilerCallback::JITFunctionPitched 方法

通知探查器已将实时 (JIT) 编译的函数从内存中删除。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT JITFunctionPitched(  
    [in] FunctionID functionId);  
```  
  
## <a name="parameters"></a>参数  

 `functionId`  
 中已移除的函数的 ID。  
  
## <a name="remarks"></a>备注  

 如果调用删除的函数，则在重新编译该函数时，探查器将接收新的 JIT 编译事件。 当前，公共语言运行时 (CLR) JIT 编译器不会从内存中删除函数，因此，当前不使用此回调，探查器将不会接收该回调。  
  
 重新 `functionId` 编译该函数之前，的值无效。 重新编译函数时， `functionId` 将使用相同的值。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **头文件：** CorProf.idl、CorProf.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICorProfilerCallback 接口](icorprofilercallback-interface.md)
