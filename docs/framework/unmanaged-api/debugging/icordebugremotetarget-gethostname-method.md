---
description: 了解详细信息： ICorDebugRemoteTarget：： GetHostName 方法
title: ICorDebugRemoteTarget::GetHostName 方法
ms.date: 03/30/2017
api_name:
- ICorDebugRemoteTarget.GetHostName
api_location:
- CorDebug.dll
api_type:
- COM
f1_keywords:
- ICorDebugRemoteTarget::GetHostName
helpviewer_keywords:
- ICorDebugRemoteTarget::GetHostName method [.NET Framework debugging]
- GetHostName method, ICorDebugRemoteTarget interface [.NET Framework debugging]
ms.assetid: 1c7276f7-7e54-470c-808c-e13745ac07a1
topic_type:
- apiref
ms.openlocfilehash: a24f34dd638c7031211c2185cd761af0aa24105e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803521"
---
# <a name="icordebugremotetargetgethostname-method"></a>ICorDebugRemoteTarget::GetHostName 方法

返回远程调试目标计算机的完全限定域名或 IPv4 地址。 此时不支持 IPV6。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetHostName (  
    [in] ULONG32      cchHostName,  
    [out] ULONG32*    pcchHostName,  
    [out, size_is(cchHostName), length_is(*pcchHostName)]  
            WCHAR szHostName[]  
```  
  
## <a name="parameters"></a>参数  

 `cchHostName`  
 中缓冲区的大小（以字符为字符） `szHostName` 。 如果此参数为 0（零），`szHostName` 必须为 null。  
  
 `pcchHostName`  
 [out] 主机名或 IP 地址中的字符数，包括 null 结束符。 此参数可以为 null。  
  
 `szHostName`  
 [out] 包含主机名或 IP 地址的缓冲区。  
  
## <a name="return-value"></a>返回值  

 S_OK  
 主机名或 IP 地址成功返回。  
  
 E_FAIL（或其他 E_ 返回代码）  
 无法返回主机名或 IP 地址。  
  
## <a name="remarks"></a>备注  

 此方法由调试器编写器实现。 它必须遵循多个调用范例：在第一次调用时，调用方将 null 传递给 `cchHostName` 和 `szHostName` ，并 `pcchHostName` 返回所需的缓冲区大小。 第二次调用时，先前返回的大小在 `cchHostName` 中传递，相应大小的缓冲区在 `szHostName` 中传递。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Cordebug.idl .idl  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：** 3.5 SP1  
  
## <a name="see-also"></a>请参阅

- [ICorDebugRemoteTarget 接口](icordebugremotetarget-interface.md)
- [ICorDebug 接口](icordebug-interface.md)
