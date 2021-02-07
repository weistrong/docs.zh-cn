---
description: 了解详细信息： ISymUnmanagedDocument：： GetURL 方法
title: ISymUnmanagedDocument::GetURL 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetURL
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetURL
helpviewer_keywords:
- GetURL method [.NET Framework debugging]
- ISymUnmanagedDocument::GetURL method [.NET Framework debugging]
ms.assetid: 60600178-c2b5-4cab-b3a5-f0f61acebaf1
topic_type:
- apiref
ms.openlocfilehash: b39b36054d80f9ad2f9dd076e2055ccbc6526973
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710187"
---
# <a name="isymunmanageddocumentgeturl-method"></a>ISymUnmanagedDocument::GetURL 方法

返回此文档 (URL) 的统一资源定位符。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT GetURL(  
    [in]  ULONG32  cchUrl,  
    [out] ULONG32  *pcchUrl,  
    [out, size_is(cchUrl), length_is(*pcchUrl)] WCHAR szUrl[]);  
```  
  
## <a name="parameters"></a>参数  

 `cchUrl`  
 中缓冲区的大小（以字符为字符） `szURL` 。  
  
 `pcchUrl`  
 弄指向一个变量的指针，该变量接收 URL 的大小，包括 null 终止。  
  
 `szUrl`  
 弄包含 URL 的缓冲区。  
  
## <a name="return-value"></a>返回值  

 如果该方法成功，则 S_OK;否则为错误代码。  
  
## <a name="see-also"></a>请参阅

- [ISymUnmanagedDocument 接口](isymunmanageddocument-interface.md)
