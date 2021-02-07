---
description: 了解详细信息： ISymUnmanagedWriter：:D efineLocalVariable 方法
title: ISymUnmanagedWriter::DefineLocalVariable 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.DefineLocalVariable
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::DefineLocalVariable
helpviewer_keywords:
- ISymUnmanagedWriter::DefineLocalVariable method [.NET Framework debugging]
- DefineLocalVariable method [.NET Framework debugging]
ms.assetid: 6fab8a58-3883-490f-8b27-64042c90f104
topic_type:
- apiref
ms.openlocfilehash: cd817e3002c2a55fd8bbd7e565283752926f746b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762365"
---
# <a name="isymunmanagedwriterdefinelocalvariable-method"></a>ISymUnmanagedWriter::DefineLocalVariable 方法

在当前词法范围内定义单个变量。 对于在整个范围内具有多个住宅的同名变量，可以多次调用此方法。 但在这种情况下， `startOffset` 和参数的值 `endOffset` 不能重叠。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT DefineLocalVariable(  
    [in] const WCHAR  *name,  
    [in] ULONG32      attributes,  
    [in] ULONG32      cSig,  
    [in, size_is(cSig)] unsigned char signature[],  
    [in] ULONG32      addrKind,  
    [in] ULONG32      addr1,  
    [in] ULONG32      addr2,  
    [in] ULONG32      addr3,  
    [in] ULONG32      startOffset,  
    [in] ULONG32      endOffset);  
```  
  
## <a name="parameters"></a>参数  

 `name`  
 中指向 `WCHAR` 的指针，该指针定义局部变量的名称。  
  
 `attributes`  
 中局部变量特性。  
  
 `cSig`  
 中一个 `ULONG32` ，该值指示缓冲区的大小（以字节为单位） `signature` 。  
  
 `signature`  
 中局部变量签名。  
  
 `addrKind`  
 中地址类型。  
  
 `addr1`  
 中参数规范的第一个地址。  
  
 `addr2`  
 中参数规范的第二个地址。  
  
 `addr3`  
 中参数规范的第三个地址。  
  
 `startOffset`  
 中变量的起始偏移量。 此参数可选。 如果为0，则忽略此参数，并在整个范围内定义变量。 如果它是非零值，则该变量将处于当前范围的偏移量内。  
  
 `endOffset`  
 中变量的结束偏移量。 此参数可选。 如果为0，则忽略此参数，并在整个范围内定义变量。 如果它是非零值，则该变量将处于当前范围的偏移量内。  
  
## <a name="return-value"></a>返回值  

 如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。  
  
## <a name="requirements"></a>要求  

 **标头：** CorSym，CorSym  
  
## <a name="see-also"></a>请参阅

- [ISymUnmanagedWriter 接口](isymunmanagedwriter-interface.md)
- [DefineGlobalVariable 方法](isymunmanagedwriter-defineglobalvariable-method.md)
- [DefineLocalVariable2 方法](isymunmanagedwriter2-definelocalvariable2-method.md)
