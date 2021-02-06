---
description: 了解详细信息： ICorProfilerInfo9：： GetNativeCodeStartAddresses 方法
title: ICorProfilerInfo9::GetNativeCodeStartAddresses
ms.date: 08/06/2019
dev_langs:
- cpp
api_name:
- ICorProfilerInfo9.GetNativeCodeStartAddresses
api_location:
- mscorwks.dll
api_type:
- COM
author: davmason
ms.author: davmason
ms.openlocfilehash: 1ca686cef4a45ebb9e05190fa790ed5300c0d816
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99646486"
---
# <a name="icorprofilerinfo9getnativecodestartaddresses-method"></a>ICorProfilerInfo9：： GetNativeCodeStartAddresses 方法

给定一个 functionId 和 rejitId，枚举此代码当前存在的所有实时编译版本的本机代码起始地址。

## <a name="syntax"></a>语法

```cpp
HRESULT GetNativeCodeStartAddresses( [in]  FunctionID functionID,
                                     [in]  ReJITID reJitId,
                                     [in]  ULONG32 cCodeStartAddresses,
                                     [out] ULONG32 *pcCodeStartAddresses,
                                     [out] UINT_PTR codeStartAddresses[]);
```

## <a name="parameters"></a>参数

- `functionId`

  \[in] 应返回其本机代码起始地址的函数的 ID。

- `reJitId`

  \[in] JIT 重新编译的函数的标识。

- `cCodeStartAddresses`

  \[in] 数组的最大大小 `codeStartAddresses` 。

- `pcCodeStartAddresses`

  \[out] 可用地址的数量。

- `codeStartAddresses`

  \[out] 的数组 `UINT_PTR` ，其中每个都是指定函数的本机正文的开始地址。

## <a name="remarks"></a>备注

启用分层编译后，函数可能有多个本机代码体。

## <a name="requirements"></a>要求

**平台：** 请参阅 [支持 .Net Core 的操作系统](../../../core/install/windows.md?pivots=os-windows)。

**头文件：** CorProf.idl、CorProf.h

**库：** CorGuids.lib

**.Net 版本：**[!INCLUDE[net_core_22](../../../../includes/net-core-22-md.md)]

## <a name="see-also"></a>请参阅

- [ICorProfilerInfo9 接口](icorprofilerinfo9-interface.md)
