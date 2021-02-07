---
description: 了解详细信息： ISymUnmanagedReader：： GetDocument 方法
title: ISymUnmanagedReader::GetDocument 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetDocument
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetDocument
helpviewer_keywords:
- ISymUnmanagedReader::GetDocument method [.NET Framework debugging]
- GetDocument method [.NET Framework debugging]
ms.assetid: bb203853-6a6d-4027-b9e9-603a7f28b9d3
topic_type:
- apiref
ms.openlocfilehash: 7f2f31467cfd00de68737224a2c1af5b1e78efed
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99764094"
---
# <a name="isymunmanagedreadergetdocument-method"></a><span data-ttu-id="41fba-103">ISymUnmanagedReader::GetDocument 方法</span><span class="sxs-lookup"><span data-stu-id="41fba-103">ISymUnmanagedReader::GetDocument Method</span></span>

<span data-ttu-id="41fba-104">查找文档。</span><span class="sxs-lookup"><span data-stu-id="41fba-104">Finds a document.</span></span> <span data-ttu-id="41fba-105">文档语言、供应商和类型是可选的。</span><span class="sxs-lookup"><span data-stu-id="41fba-105">The document language, vendor, and type are optional.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="41fba-106">语法</span><span class="sxs-lookup"><span data-stu-id="41fba-106">Syntax</span></span>  
  
```cpp  
HRESULT GetDocument (  
    [in]  WCHAR  *url,  
    [in]  GUID   language,  
    [in]  GUID   languageVendor,  
    [in]  GUID   documentType,  
    [out, retval] ISymUnmanagedDocument** pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="41fba-107">参数</span><span class="sxs-lookup"><span data-stu-id="41fba-107">Parameters</span></span>  

 `url`  
 <span data-ttu-id="41fba-108">中标识文档的 URL。</span><span class="sxs-lookup"><span data-stu-id="41fba-108">[in] The URL that identifies the document.</span></span>  
  
 `language`  
 <span data-ttu-id="41fba-109">中文档语言。</span><span class="sxs-lookup"><span data-stu-id="41fba-109">[in] The document language.</span></span> <span data-ttu-id="41fba-110">此参数可选。</span><span class="sxs-lookup"><span data-stu-id="41fba-110">This parameter is optional.</span></span>  
  
 `languageVendor`  
 <span data-ttu-id="41fba-111">中文档语言的供应商标识。</span><span class="sxs-lookup"><span data-stu-id="41fba-111">[in] The identity of the vendor for the document language.</span></span> <span data-ttu-id="41fba-112">此参数可选。</span><span class="sxs-lookup"><span data-stu-id="41fba-112">This parameter is optional.</span></span>  
  
 `documentType`  
 <span data-ttu-id="41fba-113">中文档的类型。</span><span class="sxs-lookup"><span data-stu-id="41fba-113">[in] The type of the document.</span></span> <span data-ttu-id="41fba-114">此参数可选。</span><span class="sxs-lookup"><span data-stu-id="41fba-114">This parameter is optional.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="41fba-115">弄指向返回的接口的指针。</span><span class="sxs-lookup"><span data-stu-id="41fba-115">[out] A pointer to the returned interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="41fba-116">返回值</span><span class="sxs-lookup"><span data-stu-id="41fba-116">Return Value</span></span>  

 <span data-ttu-id="41fba-117">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="41fba-117">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="41fba-118">要求</span><span class="sxs-lookup"><span data-stu-id="41fba-118">Requirements</span></span>  

 <span data-ttu-id="41fba-119">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="41fba-119">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="41fba-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="41fba-120">See also</span></span>

- [<span data-ttu-id="41fba-121">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="41fba-121">ISymUnmanagedReader Interface</span></span>](isymunmanagedreader-interface.md)
