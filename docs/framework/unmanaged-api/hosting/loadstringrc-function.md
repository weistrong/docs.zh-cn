---
description: 了解详细信息： LoadStringRC 函数
title: LoadStringRC 函数
ms.date: 03/30/2017
api_name:
- LoadStringRC
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- LoadStringRC
helpviewer_keywords:
- LoadStringRC function [.NET Framework hosting]
ms.assetid: 752e49b4-987c-4c28-a118-1a0c1ed510c5
topic_type:
- apiref
ms.openlocfilehash: 188597f9dc21b6a67fb84e91cd66b50ba5a514f3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99679880"
---
# <a name="loadstringrc-function"></a>LoadStringRC 函数

使用当前线程的默认区域性将 HRESULT 值转换为错误消息。  
  
 此函数已在 .NET Framework 4 中弃用。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT LoadStringRC (  
    [in]  UINT    iResourceID,
    [out] LPWSTR  szBuffer,
    [in]  int     iMax,
    [in]  int     bQuiet  
);  
```  
  
## <a name="parameters"></a>参数  

 `iResourceID`  
 中HRESULT。  
  
 `szBuffer`  
 弄一个缓冲区，其中包含成功完成后的错误消息。  
  
 `iMax`  
 中错误消息缓冲区的大小。  
  
 `bQuiet`  
 中掉.  
  
## <a name="return-value"></a>返回值  

 除以下值外，此方法还 (COM) 错误代码（如 Winerror.h 中所定义）返回标准组件对象模型。  
  
|返回代码|说明|  
|-----------------|-----------------|  
|S_OK|该方法已成功完成。|  
|E_INVALIDARG|`szBuffer` 为 null 或 `iMax` 为零 (0) 。|  
  
## <a name="remarks"></a>备注  

 如果该方法未成功完成，则 `szBuffer` 包含一个空字符串。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** Mscoree.dll  
  
 **库：** MSCorEE.dll 和 Mscorwks.dll。 使用 MSCorEE.dll 而不是 Mscorwks.dll 确保以正确的 .NET Framework 版本为目标。  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [LoadStringRCEx 函数](loadstringrcex-function.md)
- [弃用的 CLR 承载函数](deprecated-clr-hosting-functions.md)
