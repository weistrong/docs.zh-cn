---
description: 了解详细信息： ICorDebugAppDomain：： GetName 方法
title: ICorDebugAppDomain::GetName 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.GetName
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::GetName
helpviewer_keywords:
- ICorDebugAppDomain::GetName method [.NET Framework debugging]
- GetName method, ICorDebugAppDomain interface [.NET Framework debugging]
ms.assetid: 02c596d7-00b0-4e2c-856b-5425158fcefd
topic_type:
- apiref
ms.openlocfilehash: 56995f544e1576534e35b899a659ed409972305f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772414"
---
# <a name="icordebugappdomaingetname-method"></a>ICorDebugAppDomain::GetName 方法

获取应用程序域的名称。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetName (  
    [in]  ULONG32           cchName,  
    [out] ULONG32           *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]
         WCHAR              szName[]  
);  
```  
  
## <a name="parameters"></a>参数  

 `cchName`  
 [in] `szName` 数组的大小。 将此值设置为零可以在查询模式下放置此方法。  
  
 `pcchName`  
 弄一个指针，指向在中实际返回的名称的大小或字符数 `szName` 。 在查询模式下，此值允许调用方了解要为名称分配的缓冲区大小。  
  
 `szName`  
 弄一个数组，该数组存储应用程序域的名称。  
  
## <a name="remarks"></a>备注  

 调试器调用 `GetName` 方法一次，以获取该名称所需的缓冲区大小。 调试器将分配缓冲区，然后再次调用方法来填充缓冲区。 要获取名称大小的第一次调用称为 *查询模式*。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
