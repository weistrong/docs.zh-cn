---
description: 了解详细信息： IsFrameworkAssembly 函数
title: IsFrameworkAssembly 函数
ms.date: 03/30/2017
api_name:
- IsFrameworkAssembly
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IsFrameworkAssembly
helpviewer_keywords:
- IsFrameworkAssembly function [.NET Framework fusion]
ms.assetid: b0c6f19b-d4fd-4971-88f0-12ffb5793da3
topic_type:
- apiref
ms.openlocfilehash: 8f264df7b1ae5c494298b11ebd94cc93aed5543a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800014"
---
# <a name="isframeworkassembly-function"></a>IsFrameworkAssembly 函数

获取一个值，该值指示是否托管指定的程序集。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT IsFrameworkAssembly (  
    [in]  LPCWSTR pwzAssemblyReference,  
    [out] LPBOOL  pbIsFrameworkAssembly,  
    [in]  LPWSTR  pwzFrameworkAssemblyIdentity,  
    [in]  LPDWORD pccSize  
 );  
```  
  
## <a name="parameters"></a>参数  

 `pwzAssemblyReference`  
 中要检查的程序集的名称。  
  
 `pbIsFrameworkAssembly`  
 弄指示程序集是否为托管程序集的布尔值。  
  
 `pwzFrameworkAssemblyIdentity`  
 中一个 uncanonicalized 字符串，其中包含程序集的唯一标识。  
  
 `pccSize`  
 [输入] `pwzFrameworkAssemblyIdentity` 的大小。  
  
## <a name="remarks"></a>备注  

 `pwzAssemblyReference`参数是指向字符串的指针，该字符串包含程序集的名称。  
  
 如果此程序集是 .NET Framework 的一部分，则 `pbIsFrameworkAssembly` 参数将包含的布尔值 `true` 。  
  
 如果命名的程序集不是 .NET Framework 的一部分，或者如果 `pwzAssemblyReference` 参数不命名程序集， `pbIsFrameworkAssembly` 则将包含的布尔值 `false` 。  
  
## <a name="requirements"></a>要求  

 **平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。  
  
## <a name="see-also"></a>请参阅

- [合成全局静态函数](fusion-global-static-functions.md)
