---
description: 了解详细信息： ICLRDebugging 接口
title: ICLRDebugging 接口
ms.date: 03/30/2017
api_name:
- ICLRDebugging
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDebugging
helpviewer_keywords:
- ICLRDebugging interface [.NET Framework debugging]
ms.assetid: 429d8fce-b1b1-49d7-895c-28c1c1aa2dbd
topic_type:
- apiref
ms.openlocfilehash: 647b6f7634ef3b9f6ec6080aaff19476c027952a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99723330"
---
# <a name="iclrdebugging-interface"></a>ICLRDebugging 接口

提供一些方法，用于处理模块的加载和卸载以进行调试。  
  
## <a name="methods"></a>方法  
  
|方法|说明|  
|------------|-----------------|  
|[OpenVirtualProcess 方法](iclrdebugging-openvirtualprocess-method.md)|获取 "ICorDebugProcess" 接口，该接口对应于进程中加载的公共语言运行时 (CLR) 模块。|  
|[CanUnloadNow 方法](iclrdebugging-canunloadnow-method.md)|确定 [ICLRDebuggingLibraryProvider](iclrdebugginglibraryprovider-interface.md) 接口提供的库是否仍在使用中或是否可以卸载。|  
  
## <a name="remarks"></a>备注  

 可以 `ICLRDebugging` 使用 [CLRCreateInstance](../hosting/clrcreateinstance-function.md) 函数获取接口的实例。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [调试接口](debugging-interfaces.md)
- [调试](index.md)
