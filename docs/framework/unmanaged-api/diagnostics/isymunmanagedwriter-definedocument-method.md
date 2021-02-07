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
# <a name="isymunmanagedwriterdefinedocument-method"></a><span data-ttu-id="6e0f8-103">ISymUnmanagedWriter::DefineDocument 方法</span><span class="sxs-lookup"><span data-stu-id="6e0f8-103">ISymUnmanagedWriter::DefineDocument Method</span></span>

<span data-ttu-id="6e0f8-104">定义源文档。</span><span class="sxs-lookup"><span data-stu-id="6e0f8-104">Defines a source document.</span></span> <span data-ttu-id="6e0f8-105">为已知语言、供应商和文档类型提供了 Guid。</span><span class="sxs-lookup"><span data-stu-id="6e0f8-105">GUIDs are provided for known languages, vendors, and document types.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6e0f8-106">语法</span><span class="sxs-lookup"><span data-stu-id="6e0f8-106">Syntax</span></span>  
  
```cpp  
HRESULT DefineDocument(  
    [in]  const WCHAR  *url,  
    [in]  const GUID   *language,  
    [in]  const GUID   *languageVendor,  
    [in]  const GUID   *documentType,  
    [out, retval] ISymUnmanagedDocumentWriter**  pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6e0f8-107">参数</span><span class="sxs-lookup"><span data-stu-id="6e0f8-107">Parameters</span></span>  

 `url`  
 <span data-ttu-id="6e0f8-108">中指向的指针 `WCHAR` ，该指针定义标识文档 (URL) 的统一资源定位器。</span><span class="sxs-lookup"><span data-stu-id="6e0f8-108">[in] A pointer to a `WCHAR` that defines the uniform resource locator (URL) that identifies the document.</span></span>  
  
 `language`  
 <span data-ttu-id="6e0f8-109">中指向定义文档语言的 GUID 的指针。</span><span class="sxs-lookup"><span data-stu-id="6e0f8-109">[in] A pointer to a GUID that defines the document language.</span></span>  
  
 `languageVendor`  
 <span data-ttu-id="6e0f8-110">中一个指针，指向用于定义文档语言的供应商标识的 GUID。</span><span class="sxs-lookup"><span data-stu-id="6e0f8-110">[in] A pointer to a GUID that defines the identity of the vendor for the document language.</span></span>  
  
 `documentType`  
 <span data-ttu-id="6e0f8-111">中指向定义文档类型的 GUID 的指针。</span><span class="sxs-lookup"><span data-stu-id="6e0f8-111">[in] A pointer to a GUID that defines the type of the document.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="6e0f8-112">弄指向返回的 [ISymUnmanagedWriter](isymunmanagedwriter-interface.md) 接口的指针。</span><span class="sxs-lookup"><span data-stu-id="6e0f8-112">[out] A pointer to the returned [ISymUnmanagedWriter](isymunmanagedwriter-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6e0f8-113">返回值</span><span class="sxs-lookup"><span data-stu-id="6e0f8-113">Return Value</span></span>  

 <span data-ttu-id="6e0f8-114">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="6e0f8-114">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6e0f8-115">要求</span><span class="sxs-lookup"><span data-stu-id="6e0f8-115">Requirements</span></span>  

 <span data-ttu-id="6e0f8-116">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="6e0f8-116">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6e0f8-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="6e0f8-117">See also</span></span>

- [<span data-ttu-id="6e0f8-118">ISymUnmanagedWriter 接口</span><span class="sxs-lookup"><span data-stu-id="6e0f8-118">ISymUnmanagedWriter Interface</span></span>](isymunmanagedwriter-interface.md)
