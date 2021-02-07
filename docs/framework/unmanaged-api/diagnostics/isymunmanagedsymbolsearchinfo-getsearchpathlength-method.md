---
description: 了解详细信息： ISymUnmanagedSymbolSearchInfo：： GetSearchPathLength 方法
title: ISymUnmanagedSymbolSearchInfo::GetSearchPathLength 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedSymbolSearchInfo.GetSearchPathLength
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedSymbolSearchInfo::GetSearchPathLength
helpviewer_keywords:
- GetSearchPathLength method [.NET Framework debugging]
- ISymUnmanagedSymbolSearchInfo::GetSearchPathLength method [.NET Framework debugging]
ms.assetid: 274e73cf-8333-47ba-ac12-70214e2b0112
topic_type:
- apiref
ms.openlocfilehash: 3d5faf9d972881ff9c1eaf71bcaa6f68da46dae6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763015"
---
# <a name="isymunmanagedsymbolsearchinfogetsearchpathlength-method"></a>ISymUnmanagedSymbolSearchInfo::GetSearchPathLength 方法

获取搜索路径长度。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetSearchPathLength(  
    [out] ULONG32 *pcchPath);  
```  
  
## <a name="parameters"></a>参数  

 `pcchPath`  
 弄指向的指针， `ULONG32` 该指针接收包含搜索路径长度所需的缓冲区大小（以字符数表示）。  
  
## <a name="return-value"></a>返回值  

 如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。  
  
## <a name="requirements"></a>要求  

 **标头：** CorSym，CorSym  
  
## <a name="see-also"></a>请参阅

- [ISymUnmanagedSymbolSearchInfo 接口](isymunmanagedsymbolsearchinfo-interface.md)
