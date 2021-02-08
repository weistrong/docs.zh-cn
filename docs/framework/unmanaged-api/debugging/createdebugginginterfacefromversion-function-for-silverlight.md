---
description: 了解有关以下内容的详细信息： Silverlight 的 CreateDebuggingInterfaceFromVersion 函数
title: Silverlight 的 CreateDebuggingInterfaceFromVersion 函数
ms.date: 03/30/2017
f1_keywords:
- CreateDebuggingInterfaceFromVersion
helpviewer_keywords:
- CreateDebuggingInterfaceFromVersion function
- debugging API [Silverlight]
- Silverlight, debugging
ms.assetid: 35c7a18f-133a-4584-bd25-bb338568b0c6
ms.openlocfilehash: 8c61593f2e912260ecca65efce9f905ce56e88dc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801444"
---
# <a name="createdebugginginterfacefromversion-function-for-silverlight"></a>Silverlight 的 CreateDebuggingInterfaceFromVersion 函数

接受公共语言运行时 (从 [CreateVersionStringFromModule 函数](createversionstringfrommodule-function.md)返回的 CLR) 版本字符串，并返回 (通常为 [ICorDebug](icordebug-interface.md)) 的相应调试器接口。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT CreateDebuggingInterfaceFromVersion (  
    [in]  LPCWSTR      szDebuggeeVersion,  
    [out] IUnknown**   ppCordb,  
);  
```  
  
## <a name="parameters"></a>参数  

 `szDebuggeeVersion`\
 中目标调试对象（由 [CreateVersionStringFromModule 函数](createversionstringfrommodule-function.md)返回）中的 CLR 的版本字符串。  
  
 `ppCordb`\
 [out] 指向“COM 对象的指针”的指针 (`IUnknown`)。 此对象将在返回之前强制转换为 [ICorDebug](icordebug-interface.md) 对象。  
  
## <a name="return-value"></a>返回值

 `S_OK`\
 `ppCordb` 引用实现 [ICorDebug 接口](icordebug-interface.md) 接口的有效对象。  
  
 `E_INVALIDARG`\
 `szDebuggeeVersion` 或 `ppCordb` 为 null。  
  
 `CORDBG_E_DEBUG_COMPONENT_MISSING`\
 找不到 CLR 调试所需的组件。 在目标 CoreCLR.dll 所在的同一目录中找不到 _mscordbi.dll_ 或 _mscordaccore.dll_ 。  
  
 `CORDBG_E_INCOMPATIBLE_PROTOCOL`\
 mscordbi.dll 或 mscordaccore.dll 与目标 CoreCLR.dll 版本不一致。  
  
 `E_FAIL` (或其他 `E_` 返回代码) \
 无法返回 [ICorDebug 接口](icordebug-interface.md)。  
  
## <a name="remarks"></a>备注

 返回的接口提供用于附加到目标进程中的 CLR 和调试 CLR 正在运行的托管代码的功能。  
  
## <a name="requirements"></a>要求

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** dbgshim.dll  
  
 **库：** dbgshim.dll  
  
 **.NET Framework 版本：** 3.5 SP1
