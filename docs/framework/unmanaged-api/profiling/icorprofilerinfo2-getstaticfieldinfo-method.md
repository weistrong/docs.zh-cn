---
description: 了解详细信息： ICorProfilerInfo2：： GetStaticFieldInfo 方法
title: ICorProfilerInfo2::GetStaticFieldInfo 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo2.GetStaticFieldInfo
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo2::GetStaticFieldInfo
helpviewer_keywords:
- ICorProfilerInfo2::GetStaticFieldInfo method [.NET Framework profiling]
- GetStaticFieldInfo method [.NET Framework profiling]
ms.assetid: fc663e76-e23f-49a8-bdd5-52cdf1a3b2b3
topic_type:
- apiref
ms.openlocfilehash: 1acde9d5ad1a35b11cb036bced99c1909f0b6b04
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99716349"
---
# <a name="icorprofilerinfo2getstaticfieldinfo-method"></a>ICorProfilerInfo2::GetStaticFieldInfo 方法

获取一个值，该值指示应用于指定字段的静态类型。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetStaticFieldInfo (  
    [in] ClassID               classId,  
    [in] mdFieldDef            fieldToken,  
    [out] COR_PRF_STATIC_TYPE  *pFieldInfo);  
```  
  
## <a name="parameters"></a>参数  

 `classId`  
 中在其中定义静态字段的类的 ID。  
  
 `fieldToken`  
 中静态字段的元数据标记。  
  
 `pFieldInfo`  
 弄一个指针，指向 [COR_PRF_STATIC_TYPE](cor-prf-static-type-enumeration.md) 枚举的值，该值指示指定字段是否为静态的，如果为，则为应用于该字段的静态类型。  
  
## <a name="remarks"></a>备注  

 此信息可用于确定要调用哪个函数以获取静态字段的地址。  
  
 探查器代码仍应检查静态字段的元数据，以确保它实际具有地址。 静态文本 (也就是说，常量) 只存在于元数据中，并且没有地址。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **头文件：** CorProf.idl、CorProf.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICorProfilerInfo 接口](icorprofilerinfo-interface.md)
- [ICorProfilerInfo2 接口](icorprofilerinfo2-interface.md)
