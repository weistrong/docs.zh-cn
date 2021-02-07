---
description: 了解详细信息： ISymUnmanagedDocument：： GetDocumentType 方法
title: ISymUnmanagedDocument::GetDocumentType 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetDocumentType
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetDocumentType
helpviewer_keywords:
- ISymUnmanagedDocument::GetDocumentType method [.NET Framework debugging]
- GetDocumentType method [.NET Framework debugging]
ms.assetid: 2d381ab1-7e7c-4281-af2b-e54d879b3ef8
topic_type:
- apiref
ms.openlocfilehash: cf2ceffccb33eb7cba0d45af203e12d1e4244f60
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710317"
---
# <a name="isymunmanageddocumentgetdocumenttype-method"></a><span data-ttu-id="d913f-103">ISymUnmanagedDocument::GetDocumentType 方法</span><span class="sxs-lookup"><span data-stu-id="d913f-103">ISymUnmanagedDocument::GetDocumentType Method</span></span>

<span data-ttu-id="d913f-104">获取此文档的文档类型。</span><span class="sxs-lookup"><span data-stu-id="d913f-104">Gets the document type of this document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d913f-105">语法</span><span class="sxs-lookup"><span data-stu-id="d913f-105">Syntax</span></span>  
  
```cpp  
HRESULT GetDocumentType(  
    [out, retval] GUID*  pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d913f-106">参数</span><span class="sxs-lookup"><span data-stu-id="d913f-106">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="d913f-107">弄指向接收文档类型的变量的指针。</span><span class="sxs-lookup"><span data-stu-id="d913f-107">[out] Pointer to a variable that receives the document type.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d913f-108">返回值</span><span class="sxs-lookup"><span data-stu-id="d913f-108">Return Value</span></span>  

 <span data-ttu-id="d913f-109">如果方法成功，则 S_OK。</span><span class="sxs-lookup"><span data-stu-id="d913f-109">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d913f-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="d913f-110">See also</span></span>

- [<span data-ttu-id="d913f-111">ISymUnmanagedDocument 接口</span><span class="sxs-lookup"><span data-stu-id="d913f-111">ISymUnmanagedDocument Interface</span></span>](isymunmanageddocument-interface.md)
