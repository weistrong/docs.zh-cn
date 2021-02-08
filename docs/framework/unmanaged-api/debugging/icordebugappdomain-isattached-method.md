---
description: 了解详细信息： ICorDebugAppDomain：： IsAttached 方法
title: ICorDebugAppDomain::IsAttached 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.IsAttached
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::IsAttached
helpviewer_keywords:
- IsAttached method [.NET Framework debugging]
- ICorDebugAppDomain::IsAttached method [.NET Framework debugging]
ms.assetid: af0c67c7-f53e-47c9-b84b-be50bd04903e
topic_type:
- apiref
ms.openlocfilehash: 79427d08be9ffea253695b67767d68589edf6979
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772375"
---
# <a name="icordebugappdomainisattached-method"></a>ICorDebugAppDomain::IsAttached 方法

获取一个值，该值指示调试器是否已附加到应用程序域。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT IsAttached (  
    [out] BOOL  *pbAttached  
);  
```  
  
## <a name="parameters"></a>参数  

 `pbAttached`  
 [out] `true` 如果调试器附加到应用程序域，则为; 否则为。否则为 `false` 。  
  
## <a name="remarks"></a>备注  

 在调试器附加到应用程序域之前，不能使用 ICorDebugController 方法。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头**：CorDebug.idl、CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
