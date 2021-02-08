---
description: 了解详细信息： ICorProfilerObjectEnum：： Skip 方法
title: ICorProfilerObjectEnum::Skip 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerObjectEnum.Skip
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerObjectEnum::Skip
helpviewer_keywords:
- ICorProfilerObjectEnum::Skip method [.NET Framework profiling]
- Skip method, ICorProfilerObjectEnum interface [.NET Framework profiling]
ms.assetid: f8e498f8-f93a-4b82-bd22-55bdbf5e8d45
topic_type:
- apiref
ms.openlocfilehash: 8a2aa5dd2b905931b97fafa4db6709aab16aacc4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99781254"
---
# <a name="icorprofilerobjectenumskip-method"></a>ICorProfilerObjectEnum::Skip 方法

将此枚举器的光标从其当前位置前移，以便跳过指定数目的元素。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT Skip (  
    [in] ULONG   celt  
);  
```  
  
## <a name="parameters"></a>参数  

 `celt`  
 中要跳过的元素数。  
  
## <a name="remarks"></a>备注  

 此枚举器的游标的新位置为： (当前位置) + `celt` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **头文件：** CorProf.idl、CorProf.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICorProfilerObjectEnum 接口](icorprofilerobjectenum-interface.md)
