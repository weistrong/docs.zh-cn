---
description: 了解详细信息： ISymUnmanagedScope2：： GetConstants 方法
title: ISymUnmanagedScope2::GetConstants 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope2.GetConstants
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope2::GetConstants
helpviewer_keywords:
- ISymUnmanagedScope2::GetConstants method [.NET Framework debugging]
- GetConstants method [.NET Framework debugging]
ms.assetid: f241b620-9ec5-42fd-92ef-3b22329db72a
topic_type:
- apiref
ms.openlocfilehash: 025bb9ddd0501f2309b2c0a3f7af20eb961604cb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763210"
---
# <a name="isymunmanagedscope2getconstants-method"></a>ISymUnmanagedScope2::GetConstants 方法

获取在此范围内定义的局部变量。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetConstants(  
     [in]  ULONG32  cConstants,  
     [out] ULONG32  *pcConstants,  
     [out, size_is(cConstants),  
         length_is(*pcConstants)] ISymUnmanagedConstant*
             constants[]);  
```  
  
## <a name="parameters"></a>参数  

 `cConstants`  
 中参数指向的缓冲区的长度 `pcConstants` 。  
  
 `pcConstants`  
 弄指向的指针， `ULONG32` 该指针接收包含常量所需的缓冲区大小（以字符数表示）。  
  
 `constants`  
 弄用于存储常量的缓冲区。  
  
## <a name="return-value"></a>返回值  

 如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。  
  
## <a name="requirements"></a>要求  

 **标头：** CorSym，CorSym  
  
## <a name="see-also"></a>请参阅

- [ISymUnmanagedScope2 接口](isymunmanagedscope2-interface.md)
