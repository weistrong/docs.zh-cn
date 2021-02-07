---
description: 了解详细信息： ISymUnmanagedDocument：： GetLanguage 方法
title: ISymUnmanagedDocument::GetLanguage 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.GetLanguage
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetLanguage
helpviewer_keywords:
- ISymUnmanagedDocument::GetLanguage method [.NET Framework debugging]
- GetLanguage method [.NET Framework debugging]
ms.assetid: c6639418-e9f2-4a99-8ce2-ec9876e0bc79
topic_type:
- apiref
ms.openlocfilehash: f30636303d310ed91aa4229f52a3197a29190d3a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710304"
---
# <a name="isymunmanageddocumentgetlanguage-method"></a><span data-ttu-id="065ea-103">ISymUnmanagedDocument::GetLanguage 方法</span><span class="sxs-lookup"><span data-stu-id="065ea-103">ISymUnmanagedDocument::GetLanguage Method</span></span>

<span data-ttu-id="065ea-104">获取此文档的语言标识符</span><span class="sxs-lookup"><span data-stu-id="065ea-104">Gets the language identifier of this document</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="065ea-105">语法</span><span class="sxs-lookup"><span data-stu-id="065ea-105">Syntax</span></span>  
  
```cpp  
HRESULT GetLanguage(  
    [out, retval]  GUID*  pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="065ea-106">参数</span><span class="sxs-lookup"><span data-stu-id="065ea-106">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="065ea-107">弄指向接收语言标识符的变量的指针。</span><span class="sxs-lookup"><span data-stu-id="065ea-107">[out] A pointer to a variable that receives the language identifier.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="065ea-108">返回值</span><span class="sxs-lookup"><span data-stu-id="065ea-108">Return Value</span></span>  

 <span data-ttu-id="065ea-109">如果方法成功，则 S_OK。</span><span class="sxs-lookup"><span data-stu-id="065ea-109">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="065ea-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="065ea-110">See also</span></span>

- [<span data-ttu-id="065ea-111">ISymUnmanagedDocument 接口</span><span class="sxs-lookup"><span data-stu-id="065ea-111">ISymUnmanagedDocument Interface</span></span>](isymunmanageddocument-interface.md)
