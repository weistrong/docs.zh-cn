---
description: 了解详细信息： ISymUnmanagedWriter：:D efineDocument 方法
title: ISymUnmanagedWriter::DefineDocument 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.DefineDocument
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::DefineDocument
helpviewer_keywords:
- ISymUnmanagedWriter::DefineDocument method [.NET Framework debugging]
- DefineDocument method [.NET Framework debugging]
ms.assetid: c3bf15b0-3250-4bbe-b9b5-c5d695289b6f
topic_type:
- apiref
ms.openlocfilehash: 35e918292e6ee50e17932645e003d19513e2397a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99762534"
---
# <a name="isymunmanagedwriterdefinedocument-method"></a>ISymUnmanagedWriter::DefineDocument 方法

定义源文档。 为已知语言、供应商和文档类型提供了 Guid。  
  
## <a name="syntax"></a>语法  
  
```cpp  
HRESULT DefineDocument(  
    [in]  const WCHAR  *url,  
    [in]  const GUID   *language,  
    [in]  const GUID   *languageVendor,  
    [in]  const GUID   *documentType,  
    [out, retval] ISymUnmanagedDocumentWriter**  pRetVal);  
```  
  
## <a name="parameters"></a>参数  

 `url`  
 中指向的指针 `WCHAR` ，该指针定义标识文档 (URL) 的统一资源定位器。  
  
 `language`  
 中指向定义文档语言的 GUID 的指针。  
  
 `languageVendor`  
 中一个指针，指向用于定义文档语言的供应商标识的 GUID。  
  
 `documentType`  
 中指向定义文档类型的 GUID 的指针。  
  
 `pRetVal`  
 弄指向返回的 [ISymUnmanagedWriter](isymunmanagedwriter-interface.md) 接口的指针。  
  
## <a name="return-value"></a>返回值  

 如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。  
  
## <a name="requirements"></a>要求  

 **标头：** CorSym，CorSym  
  
## <a name="see-also"></a>请参阅

- [ISymUnmanagedWriter 接口](isymunmanagedwriter-interface.md)
