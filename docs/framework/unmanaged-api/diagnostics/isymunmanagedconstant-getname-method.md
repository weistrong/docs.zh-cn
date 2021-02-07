---
description: 了解详细信息： ISymUnmanagedConstant：： GetName 方法
title: ISymUnmanagedConstant::GetName 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedConstant.GetName
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedConstant::GetName
helpviewer_keywords:
- ISymUnmanagedConstant::GetName method [.NET Framework debugging]
- GetName method, ISymUnmanagedConstant interface [.NET Framework debugging]
ms.assetid: cbaca4e1-4473-459b-ba34-f1f59ce7c0ba
topic_type:
- apiref
ms.openlocfilehash: 57531711ed60c9e35e749a3cb1f1ba5d5c48ca66
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689815"
---
# <a name="isymunmanagedconstantgetname-method"></a>ISymUnmanagedConstant::GetName 方法

获取常数的名称。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetName(  
    [in]  ULONG32  cchName,  
    [out] ULONG32  *pcchName,  
    [out, size_is(cchName),  
        length_is(*pcchName)] WCHAR szName[]);  
```  
  
## <a name="parameters"></a>参数  

 `cchName`  
 中参数指向的缓冲区的长度 `szName` 。  
  
 `pcchName`  
 弄指向的指针， `ULONG32` 该指针接收包含名称（包括 null 终止）所需的缓冲区的大小（以字符数表示）。  
  
 `szName`  
 弄存储名称的缓冲区。  
  
## <a name="return-value"></a>返回值  

 如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。  
  
## <a name="requirements"></a>要求  

 **标头：** CorSym，CorSym  
  
## <a name="see-also"></a>请参阅

- [ISymUnmanagedConstant 接口](isymunmanagedconstant-interface.md)
- [GetSignature 方法](isymunmanagedconstant-getsignature-method.md)
- [GetValue 方法](isymunmanagedconstant-getvalue-method.md)
