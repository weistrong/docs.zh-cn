---
description: 了解详细信息： ICorDebugModule2：： ResolveAssembly 方法
title: ICorDebugModule2::ResolveAssembly 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule2.ResolveAssembly
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule2::ResolveAssembly
helpviewer_keywords:
- ICorDebugModule2::ResolveAssembly method [.NET Framework debugging]
- ResolveAssembly method [.NET Framework debugging]
ms.assetid: ddf9085c-7161-44bd-9609-cd2732b9009f
topic_type:
- apiref
ms.openlocfilehash: fba53b8ff76e4d3deb1876d2a20a7a2edc20bd06
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722589"
---
# <a name="icordebugmodule2resolveassembly-method"></a>ICorDebugModule2::ResolveAssembly 方法

解析指定的元数据标记所引用的程序集。

## <a name="syntax"></a>语法

```cpp
HRESULT ResolveAssembly (
    [in]  mdToken             tkAssemblyRef,
    [out] ICorDebugAssembly   **ppAssembly
);
```

## <a name="parameters"></a>参数

`tkAssemblyRef`\
中一个 `mdToken` 引用程序集的值。

`ppAssembly`\
弄指向表示程序集的 ICorDebugAssembly 对象地址的指针。

## <a name="remarks"></a>备注

如果在调用时尚未加载该程序集 `ResolveAssembly` ，则将返回 CORDBG_E_CANNOT_RESOLVE_ASSEMBLY 的 HRESULT 值。

## <a name="requirements"></a>要求

**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。

**标头**：CorDebug.idl、CorDebug.h

**库：** CorGuids.lib

**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]
