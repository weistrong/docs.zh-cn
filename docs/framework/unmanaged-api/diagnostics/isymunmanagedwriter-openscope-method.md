---
description: 了解详细信息： ISymUnmanagedWriter：： OpenScope 方法
title: ISymUnmanagedWriter::OpenScope 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.OpenScope
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::OpenScope
helpviewer_keywords:
- OpenScope method, ISymUnmanagedWriter interface [.NET Framework debugging]
- ISymUnmanagedWriter::OpenScope method [.NET Framework debugging]
ms.assetid: dbea0644-3873-4329-90b8-624163e87467
topic_type:
- apiref
ms.openlocfilehash: 1e47d97941b053fedcf08c7582e1083988a9fed4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762105"
---
# <a name="isymunmanagedwriteropenscope-method"></a>ISymUnmanagedWriter::OpenScope 方法

在当前方法中打开新的词法范围。 范围将成为新的当前范围，并推送到作用域的堆栈上。 范围必须构成层次结构。 同级不允许重叠。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT OpenScope(  
    [in] ULONG32 startOffset,  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a>参数  

 `startOffset`  
 中词法范围中第一个指令的偏移量（以字节为单位），从方法的开头开始。  
  
 `pRetVal`  
 弄指向的指针 `ULONG32` ，该指针接收作用域标识符。  
  
## <a name="return-value"></a>返回值  

 如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。  
  
## <a name="remarks"></a>备注  

 `ISymUnmanagedWriter::OpenScope` 返回一个不透明的范围标识符，该标识符可以与 [ISymUnmanagedWriter：： SetScopeRange](isymunmanagedwriter-setscoperange-method.md) 一起使用，以定义范围的起始和结束偏移量。 在这种情况下，将忽略传递到 `ISymUnmanagedWriter::OpenScope` 和 [ISymUnmanagedWriter：： CloseScope](isymunmanagedwriter-closescope-method.md) 的偏移量。 范围标识符只在当前方法中有效。  
  
## <a name="requirements"></a>要求  

 **标头：** CorSym，CorSym  
  
## <a name="see-also"></a>请参阅

- [ISymUnmanagedWriter 接口](isymunmanagedwriter-interface.md)
