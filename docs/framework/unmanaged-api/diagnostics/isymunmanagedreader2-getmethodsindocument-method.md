---
description: 了解详细信息： ISymUnmanagedReader2：： GetMethodsInDocument 方法
title: ISymUnmanagedReader2::GetMethodsInDocument 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader2.GetMethodsInDocument
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader2::GetMethodsInDocument
helpviewer_keywords:
- ISymUnmanagedReader2::GetMethodsInDocument method [.NET Framework debugging]
- GetMethodsInDocument method [.NET Framework debugging]
ms.assetid: c7ae84d6-81e8-4cb7-a1f9-d48b6cde5d79
topic_type:
- apiref
ms.openlocfilehash: 1f75594a479edbf2e0160c9d3543384c0cbf68a0
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763678"
---
# <a name="isymunmanagedreader2getmethodsindocument-method"></a><span data-ttu-id="2c8be-103">ISymUnmanagedReader2::GetMethodsInDocument 方法</span><span class="sxs-lookup"><span data-stu-id="2c8be-103">ISymUnmanagedReader2::GetMethodsInDocument Method</span></span>

<span data-ttu-id="2c8be-104">获取所提供文档中包含行信息的每个方法。</span><span class="sxs-lookup"><span data-stu-id="2c8be-104">Gets every method that has line information in the provided document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2c8be-105">语法</span><span class="sxs-lookup"><span data-stu-id="2c8be-105">Syntax</span></span>  
  
```cpp  
HRESULT GetMethodsInDocument(  
    [in]  ISymUnmanagedDocument *document,  
    [in]  ULONG32 cMethod,  
    [out] ULONG32* pcMethod,  
    [out, size_is(cMethod),  
        length_is(*pcMethod)] ISymUnmanagedMethod* pRetVal[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2c8be-106">参数</span><span class="sxs-lookup"><span data-stu-id="2c8be-106">Parameters</span></span>  

 `document`  
 <span data-ttu-id="2c8be-107">中指向文档的指针。</span><span class="sxs-lookup"><span data-stu-id="2c8be-107">[in] A pointer to the document.</span></span>  
  
 `cMethod`  
 <span data-ttu-id="2c8be-108">中 `ULONG32` 指示数组大小的  `pRetVal` 。</span><span class="sxs-lookup"><span data-stu-id="2c8be-108">[in] A `ULONG32` that indicates the size of the  `pRetVal` array.</span></span>  
  
 `pcMethod`  
 <span data-ttu-id="2c8be-109">弄指向的指针 `ULONG32` ，该指针接收包含方法所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="2c8be-109">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the methods.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="2c8be-110">弄指向接收方法的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="2c8be-110">[out] A pointer to the buffer that receives the methods.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2c8be-111">返回值</span><span class="sxs-lookup"><span data-stu-id="2c8be-111">Return Value</span></span>  

 <span data-ttu-id="2c8be-112">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="2c8be-112">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2c8be-113">要求</span><span class="sxs-lookup"><span data-stu-id="2c8be-113">Requirements</span></span>  

 <span data-ttu-id="2c8be-114">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="2c8be-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2c8be-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="2c8be-115">See also</span></span>

- [<span data-ttu-id="2c8be-116">ISymUnmanagedReader2 接口</span><span class="sxs-lookup"><span data-stu-id="2c8be-116">ISymUnmanagedReader2 Interface</span></span>](isymunmanagedreader2-interface.md)
