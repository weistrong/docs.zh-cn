---
description: 了解详细信息： ISymUnmanagedDocument：： GetLanguageVendor 方法
title: ISymUnmanagedDocument::GetLanguageVendor 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetLanguageVendor
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetLanguageVendor
helpviewer_keywords:
- GetLanguageVendor method [.NET Framework debugging]
- ISymUnmanagedDocument::GetLanguageVendor method [.NET Framework debugging]
ms.assetid: 1d4b702e-4922-441d-8b44-03804284f70b
topic_type:
- apiref
ms.openlocfilehash: 247c6c24f57211b3b46ad773d8e77d7e0f16fd01
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710239"
---
# <a name="isymunmanageddocumentgetlanguagevendor-method"></a><span data-ttu-id="b672f-103">ISymUnmanagedDocument::GetLanguageVendor 方法</span><span class="sxs-lookup"><span data-stu-id="b672f-103">ISymUnmanagedDocument::GetLanguageVendor Method</span></span>

<span data-ttu-id="b672f-104">获取此文档的语言供应商。</span><span class="sxs-lookup"><span data-stu-id="b672f-104">Gets the language vendor of this document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b672f-105">语法</span><span class="sxs-lookup"><span data-stu-id="b672f-105">Syntax</span></span>  
  
```cpp  
HRESULT GetLanguageVendor(  
    [out, retval]  GUID*  pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="b672f-106">参数</span><span class="sxs-lookup"><span data-stu-id="b672f-106">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="b672f-107">弄指向接收语言供应商的变量的指针。</span><span class="sxs-lookup"><span data-stu-id="b672f-107">[out] A pointer to a variable that receives the language vendor.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b672f-108">返回值</span><span class="sxs-lookup"><span data-stu-id="b672f-108">Return Value</span></span>  

 <span data-ttu-id="b672f-109">如果方法成功，则 S_OK。</span><span class="sxs-lookup"><span data-stu-id="b672f-109">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b672f-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="b672f-110">See also</span></span>

- [<span data-ttu-id="b672f-111">ISymUnmanagedDocument 接口</span><span class="sxs-lookup"><span data-stu-id="b672f-111">ISymUnmanagedDocument Interface</span></span>](isymunmanageddocument-interface.md)
