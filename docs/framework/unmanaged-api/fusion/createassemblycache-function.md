---
description: 了解详细信息： CreateAssemblyCache 函数
title: CreateAssemblyCache 函数
ms.date: 03/30/2017
api_name:
- CreateAssemblyCache
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- CreateAssemblyCache
helpviewer_keywords:
- CreateAssemblyCache function [.NET Framework fusion]
ms.assetid: 348c7c8c-8578-46ae-97cf-480d6015c3c6
topic_type:
- apiref
ms.openlocfilehash: 1646e1d33401c557b13ae5c025f53aef48042004
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761153"
---
# <a name="createassemblycache-function"></a>CreateAssemblyCache 函数

获取一个指针，该指针指向表示全局程序集缓存的新 [IAssemblyCache](iassemblycache-interface.md) 实例。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT CreateAssemblyCache (  
    [out] IAssemblyCache  **ppAsmCache,  
    [in]  DWORD           dwReserved  
 );  
```  
  
## <a name="parameters"></a>参数  

 `ppAsmCache`  
 弄返回的 `IAssemblyCache` 指针。  
  
 `dwReserved`  
 中保留以供将来进行扩展。 `dwReserved` 必须为 0 (零) 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** 合成。h  
  
 **库：** 作为中的资源包含 MsCorEE.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IAssemblyCache 接口](iassemblycache-interface.md)
- [合成全局静态函数](fusion-global-static-functions.md)
- [全局程序集缓存](../../app-domains/gac.md)
