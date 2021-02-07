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
# <a name="isymunmanageddocumentgeturl-method"></a><span data-ttu-id="fd988-103">ISymUnmanagedDocument::GetURL 方法</span><span class="sxs-lookup"><span data-stu-id="fd988-103">ISymUnmanagedDocument::GetURL Method</span></span>

<span data-ttu-id="fd988-104">返回此文档 (URL) 的统一资源定位符。</span><span class="sxs-lookup"><span data-stu-id="fd988-104">Returns the uniform resource locator (URL) for this document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fd988-105">语法</span><span class="sxs-lookup"><span data-stu-id="fd988-105">Syntax</span></span>  
  
```cpp  
HRESULT GetURL(  
    [in]  ULONG32  cchUrl,  
    [out] ULONG32  *pcchUrl,  
    [out, size_is(cchUrl), length_is(*pcchUrl)] WCHAR szUrl[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fd988-106">参数</span><span class="sxs-lookup"><span data-stu-id="fd988-106">Parameters</span></span>  

 `cchUrl`  
 <span data-ttu-id="fd988-107">中缓冲区的大小（以字符为字符） `szURL` 。</span><span class="sxs-lookup"><span data-stu-id="fd988-107">[in] The size, in characters, of the `szURL` buffer.</span></span>  
  
 `pcchUrl`  
 <span data-ttu-id="fd988-108">弄指向一个变量的指针，该变量接收 URL 的大小，包括 null 终止。</span><span class="sxs-lookup"><span data-stu-id="fd988-108">[out] A pointer to a variable that receives the size of the URL, including the null termination.</span></span>  
  
 `szUrl`  
 <span data-ttu-id="fd988-109">弄包含 URL 的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="fd988-109">[out] The buffer containing the URL.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fd988-110">返回值</span><span class="sxs-lookup"><span data-stu-id="fd988-110">Return Value</span></span>  

 <span data-ttu-id="fd988-111">如果该方法成功，则 S_OK;否则为错误代码。</span><span class="sxs-lookup"><span data-stu-id="fd988-111">S_OK if the method succeeds; otherwise, an error code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fd988-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="fd988-112">See also</span></span>

- [<span data-ttu-id="fd988-113">ISymUnmanagedDocument 接口</span><span class="sxs-lookup"><span data-stu-id="fd988-113">ISymUnmanagedDocument Interface</span></span>](isymunmanageddocument-interface.md)
