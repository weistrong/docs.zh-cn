---
description: 了解详细信息： ICorProfilerInfo8：： GetFunctionFromIP3 方法
title: ICorProfilerInfo8::GetFunctionFromIP3
ms.date: 08/06/2019
dev_langs:
- cpp
api_name:
- ICorProfilerInfo8.GetFunctionFromIP3
api_location:
- mscorwks.dll
api_type:
- COM
author: davmason
ms.author: davmason
ms.openlocfilehash: 3ce0a0964e26254ab09e515826b6bceb657e07bc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99783828"
---
# <a name="icorprofilerinfo8getfunctionfromip3-method"></a>ICorProfilerInfo8：： GetFunctionFromIP3 方法

将托管代码指令指针映射到 FunctionID。 此方法适用于动态和非动态方法。

## <a name="syntax"></a>语法

```cpp
HRESULT GetFunctionFromIP3([in] LPCBYTE ip,
                           [out] FunctionID *functionId,
                           [out] ReJITID * pReJitId);
```

## <a name="parameters"></a>参数

- `ip`

  \[in] 托管代码中的指令指针。

- `pFunctionId`

  \[out] 函数 ID。

- `pReJitId`

  \[out] 函数的 JIT 重新编译版本的标识。

## <a name="remarks"></a>备注

此方法适用于动态和非动态方法。 它是 [GetFunctionFromIP2](icorprofilerinfo4-getfunctionfromip2-method.md)的超集，只适用于具有元数据的函数。

## <a name="requirements"></a>要求

**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。

**头文件：** CorProf.idl、CorProf.h

**库：** CorGuids.lib

**.NET Framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]

## <a name="see-also"></a>请参阅

- [ICorProfilerInfo8 接口](icorprofilerinfo8-interface.md)
