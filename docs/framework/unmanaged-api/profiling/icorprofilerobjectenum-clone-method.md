---
description: 了解详细信息： ICorProfilerObjectEnum：： Clone 方法
title: ICorProfilerObjectEnum::Clone 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerObjectEnum.Clone
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerObjectEnum::Clone
helpviewer_keywords:
- Clone method, ICorProfilerObjectEnum interface [.NET Framework profiling]
- ICorProfilerObjectEnum::Clone method [.NET Framework profiling]
ms.assetid: b0b2facd-5991-4f4c-932d-c4937f45cef9
topic_type:
- apiref
ms.openlocfilehash: 59971f6f6e7edab4b4c4f796ee7bea3c4d8b4e91
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99798948"
---
# <a name="icorprofilerobjectenumclone-method"></a>ICorProfilerObjectEnum::Clone 方法

获取一个接口指针，该指针指向此 [ICorProfilerObjectEnum](icorprofilerobjectenum-interface.md) 接口的副本。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT Clone (  
    [out] ICorProfilerObjectEnum   **ppEnum);  
```  
  
## <a name="parameters"></a>参数  

 `ppEnum`  
 弄指向接口指针的指针，该指针指向此接口的副本 `ICorProfilerObjectEnum` 。 副本单独维护自己的枚举状态。 但是，副本的初始光标位置将与此枚举器的当前游标位置相同。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **头文件：** CorProf.idl、CorProf.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICorProfilerObjectEnum 接口](icorprofilerobjectenum-interface.md)
