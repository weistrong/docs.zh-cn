---
description: 了解详细信息： ICorProfilerInfo10：： GetLOHObjectSizeThreshold 方法
title: ICorProfilerInfo10::GetLOHObjectSizeThreshold
ms.date: 08/06/2019
dev_langs:
- cpp
api_name:
- ICorProfilerInfo10.GetLOHObjectSizeThreshold
api_location:
- mscorwks.dll
api_type:
- COM
author: davmason
ms.author: davmason
ms.openlocfilehash: 665a08ae226f04d5282b9584932078736751d5d0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99737302"
---
# <a name="icorprofilerinfo10getlohobjectsizethreshold-method"></a>ICorProfilerInfo10：： GetLOHObjectSizeThreshold 方法

获取已配置的大型对象堆的值 (LOH) 阈值。

## <a name="syntax"></a>语法

```cpp
HRESULT GetLOHObjectSizeThreshold( [out] DWORD *pThreshold );
```

## <a name="parameters"></a>参数

- `pThreshold`

  \[out] 大对象堆阈值（以字节为单位）。

## <a name="remarks"></a>备注

大于大型对象堆阈值的对象将在大型对象堆上分配。 从 .NET Core 3.0 开始，大型对象堆阈值是可配置的， `pThreshold` 将包含活动的大型对象堆阈值大小（以字节为单位）。

## <a name="requirements"></a>要求

**平台：** 请参阅 [支持 .Net Core 的操作系统](../../../core/install/windows.md?pivots=os-windows)。

**头文件：** CorProf.idl、CorProf.h

**库：** CorGuids.lib

**.Net 版本：**[!INCLUDE[net_core_22](../../../../includes/net-core-30-md.md)]

## <a name="see-also"></a>请参阅

- [ICorProfilerInfo10 接口](icorprofilerinfo10-interface.md)
