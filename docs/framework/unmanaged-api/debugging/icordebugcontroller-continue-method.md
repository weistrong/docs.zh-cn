---
description: 了解详细信息： ICorDebugController：： Continue 方法
title: ICorDebugController::Continue 方法
ms.date: 03/30/2017
api_name:
- ICorDebugController.Continue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugController::Continue
helpviewer_keywords:
- Continue method [.NET Framework debugging]
- ICorDebugController::Continue method [.NET Framework debugging]
ms.assetid: 8684cd06-ad3e-48ef-832e-15320e1f43a2
topic_type:
- apiref
ms.openlocfilehash: e5858a8c287e8dd5a493a85c9f427ad8acd9ecc5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710785"
---
# <a name="icordebugcontrollercontinue-method"></a>ICorDebugController::Continue 方法

在调用 [Stop 方法](icordebugcontroller-stop-method.md)后继续执行托管线程。

## <a name="syntax"></a>语法

```cpp
HRESULT Continue (
    [in] BOOL fIsOutOfBand
);
```

## <a name="parameters"></a>参数

`fIsOutOfBand`  
中 `true` 如果从带外事件继续，则设置为; 否则设置为 `false` 。

## <a name="remarks"></a>备注

`Continue` 在调用方法后继续此过程 `ICorDebugController::Stop` 。

在执行混合模式调试时，不要 `Continue` 在 Win32 事件线程上调用，除非从带外事件继续。

*带内事件* 是托管事件或普通非托管事件，在此期间，调试器支持与进程的托管状态交互。 在这种情况下，调试器接收 [ICorDebugUnmanagedCallback：:D ebugevent](icordebugunmanagedcallback-debugevent-method.md) 回调，其 `fOutOfBand` 参数设置为 `false` 。

带 *外事件* 是一种非托管事件，在此过程中，由于发生事件，进程停止时无法与进程的托管状态交互。 在这种情况下，调试器会接收 `ICorDebugUnmanagedCallback::DebugEvent` 回叫，其 `fOutOfBand` 参数设置为 `true` 。

## <a name="requirements"></a>要求

**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。

**标头**：CorDebug.idl、CorDebug.h

**库：** CorGuids.lib

**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
