---
description: 了解详细信息： ICorDebugAssemblyEnum：： Next 方法
title: ICorDebugAssemblyEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAssemblyEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssemblyEnum::Next method
helpviewer_keywords:
- ICorDebugAssemblyEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugAssemblyEnum interface [.NET Framework debugging]
ms.assetid: b3e7d0c2-3baa-4ef8-8e3f-b865cf252940
topic_type:
- apiref
ms.openlocfilehash: feb77f22ec59fcc0e1b3f5590b7aee4efba13d01
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772219"
---
# <a name="icordebugassemblyenumnext-method"></a>ICorDebugAssemblyEnum::Next 方法

从当前游标位置开始，从集合中获取指定数目的程序集。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT Next (  
    [in] ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugAssembly *values[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a>参数  

 `celt`  
 中要检索的程序集的数目。  
  
 `values`  
 弄指针的数组，其中每个都指向表示程序集的 ICorDebugAssembly 对象。  
  
 `pceltFetched`  
 弄一个指针，指向实际返回的程序集的数目。 如果为1，则此值可以为 null `celt` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
