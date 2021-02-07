---
description: 了解详细信息： ISymENCUnmanagedMethod：： GetSourceExtentInDocument 方法
title: ISymENCUnmanagedMethod::GetSourceExtentInDocument 方法
ms.date: 03/30/2017
api_name:
- ISymENCUnmanagedMethod.GetSourceExtentInDocument
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymENCUnmanagedMethod::GetSourceExtentInDocument
helpviewer_keywords:
- GetSourceExtentInDocument method [.NET Framework debugging]
- ISymENCUnmanagedMethod::GetSourceExtentInDocument method [.NET Framework debugging]
ms.assetid: 9c5566ab-4ec7-4b61-9753-839bb90ae78c
topic_type:
- apiref
ms.openlocfilehash: 6fa9edb524a59b4420ebc737eb8d34eaf0c5c873
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99737878"
---
# <a name="isymencunmanagedmethodgetsourceextentindocument-method"></a><span data-ttu-id="11b82-103">ISymENCUnmanagedMethod::GetSourceExtentInDocument 方法</span><span class="sxs-lookup"><span data-stu-id="11b82-103">ISymENCUnmanagedMethod::GetSourceExtentInDocument Method</span></span>

<span data-ttu-id="11b82-104">获取特定文档中该方法的最小起始行和最大结束行。</span><span class="sxs-lookup"><span data-stu-id="11b82-104">Gets the smallest start line and largest end line for the method in a specific document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="11b82-105">语法</span><span class="sxs-lookup"><span data-stu-id="11b82-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSourceExtentInDocument(  
    [in]  ISymUnmanagedDocument *document,  
    [out] ULONG32* pstartLine,  
    [out] ULONG32* pendLine);  
```  
  
## <a name="parameters"></a><span data-ttu-id="11b82-106">参数</span><span class="sxs-lookup"><span data-stu-id="11b82-106">Parameters</span></span>  

 `document`  
 <span data-ttu-id="11b82-107">中指向文档的指针。</span><span class="sxs-lookup"><span data-stu-id="11b82-107">[in] A pointer to the document.</span></span>  
  
 `pstartLine`  
 <span data-ttu-id="11b82-108">弄指向的指针 `ULONG32` ，该指针接收起始行。</span><span class="sxs-lookup"><span data-stu-id="11b82-108">[out] A pointer to a `ULONG32` that receives the start line.</span></span>  
  
 `pendLine`  
 <span data-ttu-id="11b82-109">弄指向 `ULONG32` 的指针，该指针接收结束行。</span><span class="sxs-lookup"><span data-stu-id="11b82-109">[out] A pointer to a `ULONG32` that receives the end line.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="11b82-110">返回值</span><span class="sxs-lookup"><span data-stu-id="11b82-110">Return Value</span></span>  

 <span data-ttu-id="11b82-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="11b82-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="11b82-112">要求</span><span class="sxs-lookup"><span data-stu-id="11b82-112">Requirements</span></span>  

 <span data-ttu-id="11b82-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="11b82-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="11b82-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="11b82-114">See also</span></span>

- [<span data-ttu-id="11b82-115">ISymENCUnmanagedMethod 接口</span><span class="sxs-lookup"><span data-stu-id="11b82-115">ISymENCUnmanagedMethod Interface</span></span>](isymencunmanagedmethod-interface.md)
