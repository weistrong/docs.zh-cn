---
description: 了解详细信息： CreateApplicationContext 函数
title: CreateApplicationContext 函数
ms.date: 03/30/2017
api_name:
- CreateApplicationContext
api_location:
- fusion.dll
api_type:
- DLLExport
f1_keywords:
- CreateApplicationContext
helpviewer_keywords:
- CreateApplicationContext function [.NET Framework fusion]
ms.assetid: 7bf8a141-b2c0-4058-9885-1cef7dcaa811
topic_type:
- apiref
ms.openlocfilehash: f192e1ccc371cb6d50e4a41a286c412825ee4181
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761174"
---
# <a name="createapplicationcontext-function"></a>CreateApplicationContext 函数

此函数支持 .NET Framework 基础结构，不应在代码中直接使用。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT CreateApplicationContext (  
    [in]  IAssemblyName  *pName,  
    [out] LPPAPPLICATIONCONTEXT  *ppCtx  
 );  
```  
  
## <a name="parameters"></a>参数  

 `pName`  
 中指向友好名称的指针。  
  
 `ppCtx`  
 弄指向应用程序上下文的指针。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
 **标头：** 合成。h  
  
 **库：** 作为中的资源包含 Fusion.dll  
  
 **.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅

- [IAssemblyCache 接口](iassemblycache-interface.md)
- [合成全局静态函数](fusion-global-static-functions.md)
- [全局程序集缓存](../../app-domains/gac.md)
