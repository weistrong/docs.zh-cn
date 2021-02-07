---
description: 了解详细信息： ISymUnmanagedScope：： GetStartOffset 方法
title: ISymUnmanagedScope::GetStartOffset 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetStartOffset
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetStartOffset
helpviewer_keywords:
- GetStartOffset method, ISymUnmanagedScope interface [.NET Framework debugging]
- ISymUnmanagedScope::GetStartOffset method [.NET Framework debugging]
ms.assetid: da6bbc75-94d1-4354-9722-0d455b4428fb
topic_type:
- apiref
ms.openlocfilehash: c95fbc5229512f08052ffc00f0092f64983ea3f6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763314"
---
# <a name="isymunmanagedscopegetstartoffset-method"></a><span data-ttu-id="3f202-103">ISymUnmanagedScope::GetStartOffset 方法</span><span class="sxs-lookup"><span data-stu-id="3f202-103">ISymUnmanagedScope::GetStartOffset Method</span></span>

<span data-ttu-id="3f202-104">获取此范围的起始偏移量。</span><span class="sxs-lookup"><span data-stu-id="3f202-104">Gets the start offset for this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3f202-105">语法</span><span class="sxs-lookup"><span data-stu-id="3f202-105">Syntax</span></span>  
  
```cpp  
HRESULT GetStartOffset(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3f202-106">参数</span><span class="sxs-lookup"><span data-stu-id="3f202-106">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="3f202-107">弄指向的指针 `ULONG32` ，该指针包含起始偏移量。</span><span class="sxs-lookup"><span data-stu-id="3f202-107">[out] A pointer to a `ULONG32` that contains the starting offset.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3f202-108">返回值</span><span class="sxs-lookup"><span data-stu-id="3f202-108">Return Value</span></span>  

 <span data-ttu-id="3f202-109">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="3f202-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3f202-110">要求</span><span class="sxs-lookup"><span data-stu-id="3f202-110">Requirements</span></span>  

 <span data-ttu-id="3f202-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="3f202-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3f202-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="3f202-112">See also</span></span>

- [<span data-ttu-id="3f202-113">ISymUnmanagedScope 接口</span><span class="sxs-lookup"><span data-stu-id="3f202-113">ISymUnmanagedScope Interface</span></span>](isymunmanagedscope-interface.md)
- [<span data-ttu-id="3f202-114">GetEndOffset 方法</span><span class="sxs-lookup"><span data-stu-id="3f202-114">GetEndOffset Method</span></span>](isymunmanagedscope-getendoffset-method.md)
