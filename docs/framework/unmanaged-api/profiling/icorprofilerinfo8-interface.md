---
description: 了解详细信息： ICorProfilerInfo8 接口
title: ICorProfilerInfo8 接口
ms.date: 08/06/2019
author: davmason
ms.author: davmason
ms.openlocfilehash: 4538c9d314283c67ab0bfe6af3f3768062cffda4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99646538"
---
# <a name="icorprofilerinfo8-interface"></a>ICorProfilerInfo8 接口

[ICorProfilerInfo7](icorprofilerinfo7-interface.md)的子类，提供查询有关动态方法的信息的方法。

## <a name="methods"></a>方法  

| 方法|说明|  
| ------------|-----------------|  
|[IsFunctionDynamic 方法](icorprofilerinfo8-isfunctiondynamic-method.md)| 确定函数是否没有关联的元数据。|
|[GetFunctionFromIP3 方法](icorprofilerinfo8-getfunctionfromip3-method.md)| 将托管代码指令指针映射到 FunctionID。 此方法适用于动态和非动态方法。 |
|[GetDynamicFunctionInfo 方法](icorprofilerinfo8-getdynamicfunctioninfo-method.md)| 检索有关动态方法的信息。 |

## <a name="requirements"></a>要求  

**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
**头文件：** CorProf.idl、CorProf.h  
**.NET Framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]  

## <a name="see-also"></a>请参阅

- [分析接口](profiling-interfaces.md)
