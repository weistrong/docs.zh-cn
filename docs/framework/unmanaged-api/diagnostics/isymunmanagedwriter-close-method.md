---
description: 了解详细信息： ISymUnmanagedWriter：： Close 方法
title: ISymUnmanagedWriter::Close 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.Close
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::Close
helpviewer_keywords:
- Close method, ISymUnmanagedWriter interface [.NET Framework debugging]
- ISymUnmanagedWriter::Close method [.NET Framework debugging]
ms.assetid: 4cce59e1-80b9-4fc4-b3aa-126f1c5876bc
topic_type:
- apiref
ms.openlocfilehash: 02f4d8d4a232240160ad5065947282f40af42f4e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762625"
---
# <a name="isymunmanagedwriterclose-method"></a>ISymUnmanagedWriter::Close 方法

将符号提交到符号存储区后关闭符号编写器。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT Close();  
```  
  
## <a name="return-value"></a>返回值  

 如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。  
  
## <a name="remarks"></a>备注  

 在此调用之后，符号编写器将变为无效以便进一步更新。 若要在不提交符号的情况下关闭符号编写器，请改用 [ISymUnmanagedWriter：： Abort](isymunmanagedwriter-abort-method.md) 方法。  
  
## <a name="requirements"></a>要求  

 **标头：** CorSym，CorSym  
  
## <a name="see-also"></a>请参阅

- [ISymUnmanagedWriter 接口](isymunmanagedwriter-interface.md)
