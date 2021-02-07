---
description: 了解详细信息： ICorDebugFrame：： GetCallee 方法
title: ICorDebugFrame::GetCallee 方法
ms.date: 03/30/2017
api_name:
- ICorDebugFrame.GetCallee
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::GetCallee
helpviewer_keywords:
- ICorDebugFrame::GetCallee method [.NET Framework debugging]
- GetCallee method, ICorDebugFrame interface [.NET Framework debugging]
ms.assetid: 92d8136d-0436-4c7e-a6b2-80765f892a0d
topic_type:
- apiref
ms.openlocfilehash: 85b64933cb2f180445b88f7b19f8b78f1788252e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99693065"
---
# <a name="icordebugframegetcallee-method"></a>ICorDebugFrame::GetCallee 方法

获取一个指针，该指针指向此框架调用的当前链中的 ICorDebugFrame 对象。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetCallee (  
    [out] ICorDebugFrame     **ppFrame  
);  
```  
  
## <a name="parameters"></a>参数  

 `ppFrame`  
 弄一个指针，指向 `ICorDebugFrame` 表示被调用的帧的对象的地址。 如果调用帧是当前链中最内层的帧，则此值为 null。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
