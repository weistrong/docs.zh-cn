---
description: 了解详细信息： ISymUnmanagedMethod：： GetSourceStartEnd 方法
title: ISymUnmanagedMethod::GetSourceStartEnd 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetSourceStartEnd
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetSourceStartEnd
helpviewer_keywords:
- GetSourceStartEnd method [.NET Framework debugging]
- ISymUnmanagedMethod::GetSourceStartEnd method [.NET Framework debugging]
ms.assetid: 2a420900-01f1-4461-8777-3a34a6dc1426
topic_type:
- apiref
ms.openlocfilehash: 0d247427998970d86c1ad1ec37f5b32a846a6f7c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709979"
---
# <a name="isymunmanagedmethodgetsourcestartend-method"></a><span data-ttu-id="a87ad-103">ISymUnmanagedMethod::GetSourceStartEnd 方法</span><span class="sxs-lookup"><span data-stu-id="a87ad-103">ISymUnmanagedMethod::GetSourceStartEnd Method</span></span>

<span data-ttu-id="a87ad-104">获取此方法的源的起始和结束文档位置。</span><span class="sxs-lookup"><span data-stu-id="a87ad-104">Gets the start and end document positions for the source of this method.</span></span> <span data-ttu-id="a87ad-105">第一个数组位置是开始，第二个数组位置是结束。</span><span class="sxs-lookup"><span data-stu-id="a87ad-105">The first array position is the start, and the second array position is the end.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a87ad-106">语法</span><span class="sxs-lookup"><span data-stu-id="a87ad-106">Syntax</span></span>  
  
```cpp  
HRESULT GetSourceStartEnd(  
    [in]  ISymUnmanagedDocument  *docs[2],  
    [in]  ULONG32                lines[2],  
    [in]  ULONG32                columns[2],  
    [out] BOOL                   *pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a87ad-107">参数</span><span class="sxs-lookup"><span data-stu-id="a87ad-107">Parameters</span></span>  

 `docs`  
 <span data-ttu-id="a87ad-108">中起始和结束源文档。</span><span class="sxs-lookup"><span data-stu-id="a87ad-108">[in] The starting and ending source documents.</span></span>  
  
 `lines`  
 <span data-ttu-id="a87ad-109">中对应的源文档中的起始和结束行。</span><span class="sxs-lookup"><span data-stu-id="a87ad-109">[in] The starting and ending lines in the corresponding source documents.</span></span>  
  
 `columns`  
 <span data-ttu-id="a87ad-110">中对应的源文档中的起始和结束列。</span><span class="sxs-lookup"><span data-stu-id="a87ad-110">[in] The starting and ending columns in the corresponding source documents.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="a87ad-111">[out] `true` 如果定义了位置，则为;否则为 `false` 。</span><span class="sxs-lookup"><span data-stu-id="a87ad-111">[out] `true` if positions were defined; otherwise, `false`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="a87ad-112">返回值</span><span class="sxs-lookup"><span data-stu-id="a87ad-112">Return Value</span></span>  

 <span data-ttu-id="a87ad-113">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="a87ad-113">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a87ad-114">要求</span><span class="sxs-lookup"><span data-stu-id="a87ad-114">Requirements</span></span>  

 <span data-ttu-id="a87ad-115">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="a87ad-115">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a87ad-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="a87ad-116">See also</span></span>

- [<span data-ttu-id="a87ad-117">ISymUnmanagedMethod 接口</span><span class="sxs-lookup"><span data-stu-id="a87ad-117">ISymUnmanagedMethod Interface</span></span>](isymunmanagedmethod-interface.md)
