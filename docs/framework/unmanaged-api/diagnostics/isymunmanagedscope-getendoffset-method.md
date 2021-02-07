---
description: 了解详细信息： ISymUnmanagedScope：： GetEndOffset 方法
title: ISymUnmanagedScope::GetEndOffset 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetEndOffset
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetEndOffset
helpviewer_keywords:
- ISymUnmanagedScope::GetEndOffset method [.NET Framework debugging]
- GetEndOffset method, ISymUnmanagedScope interface [.NET Framework debugging]
ms.assetid: 1d0b15c9-8059-435f-9fce-346a08b9bd36
topic_type:
- apiref
ms.openlocfilehash: ac95b98bb87fbf3dc3b42b5a2e5413f76dfffa34
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763471"
---
# <a name="isymunmanagedscopegetendoffset-method"></a><span data-ttu-id="9d1ff-103">ISymUnmanagedScope::GetEndOffset 方法</span><span class="sxs-lookup"><span data-stu-id="9d1ff-103">ISymUnmanagedScope::GetEndOffset Method</span></span>

<span data-ttu-id="9d1ff-104">获取此范围的结束偏移量。</span><span class="sxs-lookup"><span data-stu-id="9d1ff-104">Gets the end offset for this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9d1ff-105">语法</span><span class="sxs-lookup"><span data-stu-id="9d1ff-105">Syntax</span></span>  
  
```cpp  
HRESULT GetEndOffset(  
    [out, retval] ULONG32* pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9d1ff-106">参数</span><span class="sxs-lookup"><span data-stu-id="9d1ff-106">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="9d1ff-107">弄指向的指针 `ULONG32` ，该指针接收结束偏移量。</span><span class="sxs-lookup"><span data-stu-id="9d1ff-107">[out] A pointer to a `ULONG32` that receives the end offset.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9d1ff-108">返回值</span><span class="sxs-lookup"><span data-stu-id="9d1ff-108">Return Value</span></span>  

 <span data-ttu-id="9d1ff-109">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="9d1ff-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9d1ff-110">要求</span><span class="sxs-lookup"><span data-stu-id="9d1ff-110">Requirements</span></span>  

 <span data-ttu-id="9d1ff-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="9d1ff-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9d1ff-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="9d1ff-112">See also</span></span>

- [<span data-ttu-id="9d1ff-113">ISymUnmanagedScope 接口</span><span class="sxs-lookup"><span data-stu-id="9d1ff-113">ISymUnmanagedScope Interface</span></span>](isymunmanagedscope-interface.md)
- [<span data-ttu-id="9d1ff-114">GetStartOffset 方法</span><span class="sxs-lookup"><span data-stu-id="9d1ff-114">GetStartOffset Method</span></span>](isymunmanagedscope-getstartoffset-method.md)
