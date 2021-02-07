---
description: 了解详细信息： ISymUnmanagedWriter：： OpenMethod 方法
title: ISymUnmanagedWriter::OpenMethod 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.OpenMethod
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::OpenMethod
helpviewer_keywords:
- ISymUnmanagedWriter::OpenMethod method [.NET Framework debugging]
- OpenMethod method [.NET Framework debugging]
ms.assetid: fb90cb7f-af88-45e8-a99f-80a0bbddb08b
topic_type:
- apiref
ms.openlocfilehash: 2cf7e6bf7c632449c25a2b49c7658fa7b1cc287e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762222"
---
# <a name="isymunmanagedwriteropenmethod-method"></a>ISymUnmanagedWriter::OpenMethod 方法

打开要在其中发出符号信息的方法。 给定方法将成为定义序列点、参数和词法范围的调用的当前方法。 围绕整个方法，存在一个隐式词法范围。 重新打开先前关闭的方法将会清除以前为该方法定义的所有符号。 一次只能有一个 open 方法。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT OpenMethod(  
    [in] mdMethodDef method);  
```  
  
## <a name="parameters"></a>参数  

 `method`  
 中要打开的方法的元数据标记。  
  
## <a name="return-value"></a>返回值  

 如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。  
  
## <a name="requirements"></a>要求  

 **标头：** CorSym，CorSym  
  
## <a name="see-also"></a>请参阅

- [ISymUnmanagedWriter 接口](isymunmanagedwriter-interface.md)
- [CloseMethod 方法](isymunmanagedwriter-closemethod-method.md)
- [OpenMethod2 方法](isymunmanagedwriter3-openmethod2-method.md)
