---
description: 了解详细信息： ICorProfilerModuleEnum：： Skip 方法
title: ICorProfilerModuleEnum::Skip 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerModuleEnum.Skip Method
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerModuleEnum::Skip
helpviewer_keywords:
- Skip method, ICorProfilerModuleEnum interface [.NET Framework profiling]
- ICorProfilerModuleEnum::Skip method [.NET Framework profiling]
ms.assetid: 8dc29c6a-e2ba-41d8-a1e0-0fdd21421e0b
topic_type:
- apiref
ms.openlocfilehash: 4d814e5e9e369fe286b471fadc9675345cfb5b94
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99798961"
---
# <a name="icorprofilermoduleenumskip-method"></a>ICorProfilerModuleEnum::Skip 方法

将枚举器的游标从其当前位置前移，以便跳过指定数量的元素。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT Skip([in] ULONG celt);  
```  
  
## <a name="parameters"></a>参数  

 `celt`  
 中要跳过的元素数。  
  
## <a name="return-value"></a>返回值  

 此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。  
  
|HRESULT|说明|  
|-------------|-----------------|  
|S_OK|`celt` 元素已被跳过。|  
|S_FALSE|`celt`跳过的元素数少于个，这表示没有更多元素。|  
  
## <a name="remarks"></a>备注  

 此枚举器的游标的新位置 (当前位置) + `celt` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **头文件：** CorProf.idl、CorProf.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICorProfilerModuleEnum 接口](icorprofilermoduleenum-interface.md)
- [分析接口](profiling-interfaces.md)
