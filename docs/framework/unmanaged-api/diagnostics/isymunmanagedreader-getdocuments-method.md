---
description: 了解详细信息： ISymUnmanagedReader：： GetDocuments 方法
title: ISymUnmanagedReader::GetDocuments 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetDocuments
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetDocuments
helpviewer_keywords:
- GetDocuments method [.NET Framework debugging]
- ISymUnmanagedReader::GetDocuments method [.NET Framework debugging]
ms.assetid: e3b73a3f-d089-4101-a9a9-5e0765d05b61
topic_type:
- apiref
ms.openlocfilehash: 8ee2a2d8e83fcbe2f5b39960fa99e11de2ab4cd2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800209"
---
# <a name="isymunmanagedreadergetdocuments-method"></a><span data-ttu-id="c87f3-103">ISymUnmanagedReader::GetDocuments 方法</span><span class="sxs-lookup"><span data-stu-id="c87f3-103">ISymUnmanagedReader::GetDocuments Method</span></span>

<span data-ttu-id="c87f3-104">返回在符号存储区中定义的所有文档的数组。</span><span class="sxs-lookup"><span data-stu-id="c87f3-104">Returns an array of all the documents defined in the symbol store.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c87f3-105">语法</span><span class="sxs-lookup"><span data-stu-id="c87f3-105">Syntax</span></span>  
  
```cpp  
HRESULT GetDocuments (  
    [in]  ULONG32  cDocs,  
    [out] ULONG32  *pcDocs,  
    [out, size_is (cDocs),  
        length_is (*pcDocs)] ISymUnmanagedDocument *pDocs[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c87f3-106">参数</span><span class="sxs-lookup"><span data-stu-id="c87f3-106">Parameters</span></span>  

 `cDocs`  
 <span data-ttu-id="c87f3-107">[in] `pDocs` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="c87f3-107">[in] The size of the `pDocs` array.</span></span>  
  
 `pcDocs`  
 <span data-ttu-id="c87f3-108">弄指向接收数组长度的变量的指针。</span><span class="sxs-lookup"><span data-stu-id="c87f3-108">[out] A pointer to a variable that receives the array length.</span></span>  
  
 `pDocs`  
 <span data-ttu-id="c87f3-109">弄指向接收文档数组的变量的指针。</span><span class="sxs-lookup"><span data-stu-id="c87f3-109">[out] A pointer to a variable that receives the document array.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c87f3-110">返回值</span><span class="sxs-lookup"><span data-stu-id="c87f3-110">Return Value</span></span>  

 <span data-ttu-id="c87f3-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="c87f3-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c87f3-112">要求</span><span class="sxs-lookup"><span data-stu-id="c87f3-112">Requirements</span></span>  

 <span data-ttu-id="c87f3-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="c87f3-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c87f3-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="c87f3-114">See also</span></span>

- [<span data-ttu-id="c87f3-115">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="c87f3-115">ISymUnmanagedReader Interface</span></span>](isymunmanagedreader-interface.md)
