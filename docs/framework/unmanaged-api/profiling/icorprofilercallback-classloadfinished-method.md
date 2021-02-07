---
description: 了解详细信息： ICorProfilerCallback：： ClassLoadFinished 方法
title: ICorProfilerCallback::ClassLoadFinished 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.ClassLoadFinished
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::ClassLoadFinished
helpviewer_keywords:
- ClassLoadFinished method [.NET Framework profiling]
- ICorProfilerCallback::ClassLoadFinished method [.NET Framework profiling]
ms.assetid: 3dd80fbe-d62d-4d4d-acf8-5b7d0efe607e
topic_type:
- apiref
ms.openlocfilehash: ba0a6a643ab49a4e7a0ed10dda0dadff5741234d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99706417"
---
# <a name="icorprofilercallbackclassloadfinished-method"></a>ICorProfilerCallback::ClassLoadFinished 方法

通知探查器类已经完成加载。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT ClassLoadFinished(  
    [in] ClassID classId,  
    [in] HRESULT hrStatus);  
```  
  
## <a name="parameters"></a>参数

- `classId`

  \[in] 标识已加载的类。

- `hrStatus`

  \[在] 中指示是否已成功加载类的 HRESULT。

## <a name="remarks"></a>备注  

 在 `classId` 调用方法之前，的值对信息请求无效 `ClassLoadFinished` 。  
  
 在回调后，某些加载类的部分可能会继续 `ClassLoadFinished` 。 中的 HRESULT 失败 `hrStatus` 表示失败。 但是，中的成功 HRESULT `hrStatus` 仅指示加载类的第一部分已成功。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **头文件：** CorProf.idl、CorProf.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICorProfilerCallback 接口](icorprofilercallback-interface.md)
- [ClassLoadStarted 方法](icorprofilercallback-classloadstarted-method.md)
