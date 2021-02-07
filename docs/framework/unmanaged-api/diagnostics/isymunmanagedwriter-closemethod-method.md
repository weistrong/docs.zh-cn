---
description: 了解详细信息： ISymUnmanagedWriter：： CloseMethod 方法
title: ISymUnmanagedWriter::CloseMethod 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.CloseMethod
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::CloseMethod
helpviewer_keywords:
- ISymUnmanagedWriter::CloseMethod method [.NET Framework debugging]
- CloseMethod method [.NET Framework debugging]
ms.assetid: b8025e04-f0e5-40c8-849c-8cd51323420e
topic_type:
- apiref
ms.openlocfilehash: 8d19de0827f94d52c92852b0d1f2b5567e109c15
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762573"
---
# <a name="isymunmanagedwriterclosemethod-method"></a>ISymUnmanagedWriter::CloseMethod 方法

关闭当前方法。 方法关闭后，不能在其中定义更多符号。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT CloseMethod();  
```  
  
## <a name="return-value"></a>返回值  

 如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。  
  
## <a name="requirements"></a>要求  

 **标头：** CorSym，CorSym  
  
## <a name="see-also"></a>请参阅

- [ISymUnmanagedWriter 接口](isymunmanagedwriter-interface.md)
- [OpenMethod 方法](isymunmanagedwriter-openmethod-method.md)
