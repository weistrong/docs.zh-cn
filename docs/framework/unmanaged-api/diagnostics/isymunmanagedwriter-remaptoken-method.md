---
description: 了解详细信息： ISymUnmanagedWriter：： RemapToken 方法
title: ISymUnmanagedWriter::RemapToken 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.RemapToken
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::RemapToken
helpviewer_keywords:
- ISymUnmanagedWriter::RemapToken method [.NET Framework debugging]
- RemapToken method [.NET Framework debugging]
ms.assetid: bca92682-ee1e-467f-8fb0-d8d4617f82fe
topic_type:
- apiref
ms.openlocfilehash: c065d42c3d2749f0262fdd81a74de918274ba67d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762079"
---
# <a name="isymunmanagedwriterremaptoken-method"></a>ISymUnmanagedWriter::RemapToken 方法

通知符号编写器在发出元数据时已重新映射元数据标记。 如果符号编写器已将旧标记存储在符号存储区中，则必须用新值更新已存储的标记，或者必须将相应符号读取器的映射保存到读取阶段中重新映射。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT RemapToken(  
    [in] mdToken  oldToken,  
    [in] mdToken  newToken);  
```  
  
## <a name="parameters"></a>参数  

 `oldToken`  
 中重新映射的元数据标记。  
  
 `newToken`  
 中重新映射到的新的元数据标记 `oldToken` 。  
  
## <a name="return-value"></a>返回值  

 如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。  
  
## <a name="requirements"></a>要求  

 **标头：** CorSym，CorSym  
  
## <a name="see-also"></a>请参阅

- [ISymUnmanagedWriter 接口](isymunmanagedwriter-interface.md)
