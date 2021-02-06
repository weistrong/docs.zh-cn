---
description: 了解详细信息： ICorProfilerInfo3：： GetRuntimeInformation 方法
title: ICorProfilerInfo3::GetRuntimeInformation 方法
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo3.GetRuntimeInformation Method
api_location:
- Mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo3::GetRuntimeInformation
helpviewer_keywords:
- GetRuntimeInformation method [.NET Framework profiling]
- ICorProfilerInfo3::GetRuntimeInformation method [.NET Framework profiling]
ms.assetid: 4400fb8c-0407-4791-8557-f011fd2aee51
topic_type:
- apiref
ms.openlocfilehash: f615cc54e12b6f2f6eaa7335353f2f5f6a8ecfce
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99646707"
---
# <a name="icorprofilerinfo3getruntimeinformation-method"></a>ICorProfilerInfo3::GetRuntimeInformation 方法

提供有关正在分析的 (CLR) 的公共语言运行时的版本信息。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetRuntimeInformation(  
       [out] USHORT *pClrInstanceId,  
       [out] COR_PRF_RUNTIME_TYPE *pRuntimeType,  
       [out] USHORT *pMajorVersion,  
       [out] USHORT *pMinorVersion,  
       [out] USHORT *pBuildNumber,  
       [out] USHORT *pQFEVersion,  
       [in]  ULONG  cchVersionString,  
       [out] ULONG  *pcchVersionString,  
       [out, size_is(cchVersionString), length_is(*pcchVersionString)]  
                   WCHAR  szVersionString[]);  
```  
  
## <a name="parameters"></a>参数  

 `pClrInstanceId`  
 弄进程中正在运行的 CLR 实例的代表 ID。 这与 `ClrInstanceID` Windows 事件跟踪 (ETW) 启动事件报告相同。  
  
 `pRuntimeType`  
 弄运行时类型。 此参数 `COR_PRF_DESKTOP_CLR` 为 clr 的桌面版本或 `COR_PRF_CORE_CLR` Silverlight 中使用的 clr 的核心版本返回。  
  
 `pMajorVersion`  
 弄CLR 的主版本号。  
  
 `pMinorVersion`  
 弄CLR 的次版本号。  
  
 `pBuildVersion`  
 弄CLR 的内部版本号。  
  
 `pQFEVersion`  
 弄与软件更新关联的 CLR 的版本号。  
  
 `cchVersionString`  
 中指向的缓冲区的长度（以字符为单位） `szVersionString` 。  
  
 `pcchVersionString`  
 弄的长度，以字符为字符 `szVersionString` 。  
  
 `szVersionString`  
 弄CLR 版本字符串。  
  
## <a name="remarks"></a>备注  

 可以为任何参数传递 null。 但是， `pcchVersionString` 除非也为 null，否则不能为 null `szVersionString` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **头文件：** CorProf.idl、CorProf.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ICorProfilerInfo3 接口](icorprofilerinfo3-interface.md)
- [分析接口](profiling-interfaces.md)
- [分析](index.md)
