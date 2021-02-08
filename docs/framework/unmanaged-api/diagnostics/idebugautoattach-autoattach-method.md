---
description: 了解详细信息： IDebugAutoAttach：： AutoAttach 方法
title: IDebugAutoAttach::AutoAttach 方法
ms.date: 03/30/2017
api_name:
- IDebugAutoAttach.AutoAttach
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- IDebugAutoAttach::AutoAttach
helpviewer_keywords:
- AutoAttach method [.NET Framework debugging]
- IDebugAutoAttach::AutoAttach method [.NET Framework debugging]
ms.assetid: 3cf3bd9c-7d88-4afa-a476-94cdc7609aa6
topic_type:
- apiref
ms.openlocfilehash: 8abd35b1d94fc074d4dafe424c52c274b1de1541
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800352"
---
# <a name="idebugautoattachautoattach-method"></a>IDebugAutoAttach::AutoAttach 方法

执行服务器调用的调试器自动附加。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT AutoAttach  
(  
    [in]  REFGUID   guidPort,  
    [in]  DWORD     dwPid,  
    [in]  AUTOATTACH_PROGRAM_TYPE dwProgramType,  
    [in]  DWORD     dwProgramId,  
    [in]  LPCWSTR   pszSessionId  
);  
```  
  
## <a name="parameters"></a>参数  

 `guidPort`  
 中始终设置为 `GUID_NULL` 。  
  
 `dwPid`  
 中进程 ID，通常通过函数检索 `GetCurrentProcessId` 。  
  
 `dwProgramType`  
 中程序类型： `AUTOATTACH_PROGRAM_WIN32` 、 `AUTOATTACH_PROGRAM_COMPLUS` 或 `AUTOATTACH_PROGRAM_UNKNOWN` 。  
  
 `dwProgramId`  
 中程序 ID。  
  
 `pszSessionId`  
 中调试谓词传递的字符串。  
  
## <a name="return-value"></a>返回值  

 如果方法成功，则 S_OK。  
  
## <a name="requirements"></a>要求  

 **标头：** DbgAutoAttach  
  
## <a name="see-also"></a>请参阅

- [IDebugAutoAttach 接口](idebugautoattach-interface.md)
