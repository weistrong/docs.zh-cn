---
description: 了解详细信息： GetCachePath 函数
title: GetCachePath 函数
ms.date: 03/30/2017
api_name:
- GetCachePath
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- GetCachePath
helpviewer_keywords:
- GetCachePath function [.NET Framework fusion]
ms.assetid: d977ad29-6619-42e1-b0be-bc25ea950e80
topic_type:
- apiref
ms.openlocfilehash: 4f5045d4110ca9aae33ef54eb85a2146f855e6c7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761028"
---
# <a name="getcachepath-function"></a>GetCachePath 函数

使用指定的标志获取缓存的程序集的路径。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetCachePath (  
    [in]      ASM_CACHE_FLAGS  dwCacheFlags,  
    [in]      LPWSTR           pwzCachePath,  
    [in, out] PDWORD           pcchPath  
 );  
```  
  
## <a name="parameters"></a>参数  

 `dwCacheFlags`  
 中一个 [ASM_CACHE_FLAGS](asm-cache-flags-enumeration.md) 值，该值指示缓存的程序集的源。  
  
 `pwzCachePath`  
 弄指向路径的返回指针。  
  
 `pcchPath`  
 [in，out]请求的最大长度 `pwzCachePath` ，返回时为的实际长度 `pwzCachePath` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** 合成。h  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [ASM_CACHE_FLAGS 枚举](asm-cache-flags-enumeration.md)
- [合成全局静态函数](fusion-global-static-functions.md)
