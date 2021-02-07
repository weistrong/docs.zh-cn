---
description: 了解详细信息： ISymUnmanagedWriter：:D efineField 方法
title: ISymUnmanagedWriter::DefineField 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.DefineField
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::DefineField
helpviewer_keywords:
- ISymUnmanagedWriter::DefineField method [.NET Framework debugging]
- DefineField method, ISymUnmanagedWriter interface [.NET Framework debugging]
ms.assetid: c6a1f797-dbf4-40f5-ab99-d9b4bfb26148
topic_type:
- apiref
ms.openlocfilehash: f5bb47d4691780d94baf50cc9ceb3c14b1fa16ec
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762391"
---
# <a name="isymunmanagedwriterdefinefield-method"></a>ISymUnmanagedWriter::DefineField 方法

定义不在方法中的单个变量。 此方法用于类中的某些字段、位域等。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT DefineField(  
    [in] mdTypeDef    parent,  
    [in] const WCHAR  *name,  
    [in] ULONG32      attributes,  
    [in] ULONG32      cSig,  
    [in, size_is(cSig)] unsigned char signature[],  
    [in] ULONG32      addrKind,  
    [in] ULONG32      addr1,  
    [in] ULONG32      addr2,  
    [in] ULONG32      addr3);  
```  
  
## <a name="parameters"></a>参数  

 `parent`  
 中元数据类型或方法标记。  
  
 `name`  
 中字段名称。  
  
 `attributes`  
 中字段特性。  
  
 `cSig`  
 中一个 `ULONG32` ，它是包含字段签名所需的缓冲区大小（以字符数表示）。  
  
 `signature`  
 中字段签名的数组。  
  
 `addrKind`  
 中地址类型。  
  
 `addr1`  
 中字段规范的第一个地址。  
  
 `addr2`  
 中字段规格的第二个地址。  
  
 `addr3`  
 中字段规格的第三个地址。  
  
## <a name="return-value"></a>返回值  

 如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。  
  
## <a name="requirements"></a>要求  

 **标头：** CorSym，CorSym  
  
## <a name="see-also"></a>请参阅

- [ISymUnmanagedWriter 接口](isymunmanagedwriter-interface.md)
