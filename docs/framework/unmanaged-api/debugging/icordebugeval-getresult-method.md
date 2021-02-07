---
description: 了解详细信息： ICorDebugEval：： GetResult 方法
title: ICorDebugEval::GetResult 方法
ms.date: 03/30/2017
api_name:
- ICorDebugEval.GetResult
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugEval::GetResult
helpviewer_keywords:
- ICorDebugEval::GetResult method [.NET Framework debugging]
- GetResult method [.NET Framework debugging]
ms.assetid: 50dbb9af-58a1-41f4-b56d-3da20011884f
topic_type:
- apiref
ms.openlocfilehash: 03ab00f5c9a538e11a2046da9cbfd5ad7225231c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99694209"
---
# <a name="icordebugevalgetresult-method"></a>ICorDebugEval::GetResult 方法

获取此计算的结果。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetResult (  
    [out] ICorDebugValue    **ppResult  
);  
```  
  
## <a name="parameters"></a>参数  

 `ppResult`  
 弄一个指针，指向表示此计算结果的 ICorDebugValue 对象的地址（如果计算正常完成）。  
  
## <a name="remarks"></a>备注  

 此 `GetResult` 方法仅在计算完成后有效。  
  
 如果计算正常完成，则 `ppResult` 指定结果。 如果终止时出现异常，则结果为引发的异常。 如果计算为新的对象，则结果是对新的对象的引用。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
