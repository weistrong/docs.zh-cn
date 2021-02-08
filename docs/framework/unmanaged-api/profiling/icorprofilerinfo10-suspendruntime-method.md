---
description: 了解详细信息： ICorProfilerInfo10：： SuspendRuntime 方法
title: ICorProfilerInfo10::SuspendRuntime
ms.date: 08/06/2019
dev_langs:
- cpp
api_name:
- ICorProfilerInfo10.SuspendRuntime
api_location:
- mscorwks.dll
api_type:
- COM
author: davmason
ms.author: davmason
ms.openlocfilehash: d019b163c8c71331b2d9a77fc0384d42a04c1fbd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794554"
---
# <a name="icorprofilerinfo10suspendruntime-method"></a>ICorProfilerInfo10：： SuspendRuntime 方法

挂起运行时，而不执行 GC。

## <a name="syntax"></a>语法

```cpp
HRESULT SuspendRuntime();
```

## <a name="requirements"></a>要求

**平台：** 请参阅 [支持 .Net Core 的操作系统](../../../core/install/windows.md?pivots=os-windows)。

**头文件：** CorProf.idl、CorProf.h

**库：** CorGuids.lib

**.Net 版本：**[!INCLUDE[net_core_22](../../../../includes/net-core-30-md.md)]

## <a name="see-also"></a>请参阅

- [ICorProfilerInfo10 接口](icorprofilerinfo10-interface.md)
