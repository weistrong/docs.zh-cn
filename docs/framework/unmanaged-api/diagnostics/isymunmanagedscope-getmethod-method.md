---
description: 了解详细信息： ISymUnmanagedScope：： GetMethod 方法
title: ISymUnmanagedScope::GetMethod 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetMethod
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetMethod
helpviewer_keywords:
- GetMethod method, ISymUnmanagedScope interface [.NET Framework debugging]
- ISymUnmanagedScope::GetMethod method [.NET Framework debugging]
ms.assetid: a61866ee-221a-45b9-a1b7-395825b77872
topic_type:
- apiref
ms.openlocfilehash: 7dfc5f41d849d47bfaf600e40a7ccc9dd45da676
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763392"
---
# <a name="isymunmanagedscopegetmethod-method"></a><span data-ttu-id="6bc13-103">ISymUnmanagedScope::GetMethod 方法</span><span class="sxs-lookup"><span data-stu-id="6bc13-103">ISymUnmanagedScope::GetMethod Method</span></span>

<span data-ttu-id="6bc13-104">获取包含此范围的方法。</span><span class="sxs-lookup"><span data-stu-id="6bc13-104">Gets the method that contains this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6bc13-105">语法</span><span class="sxs-lookup"><span data-stu-id="6bc13-105">Syntax</span></span>  
  
```cpp  
HRESULT GetMethod(  
    [out, retval] ISymUnmanagedMethod** pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6bc13-106">参数</span><span class="sxs-lookup"><span data-stu-id="6bc13-106">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="6bc13-107">弄指向返回的 [ISymUnmanagedMethod](isymunmanagedmethod-interface.md) 接口的指针。</span><span class="sxs-lookup"><span data-stu-id="6bc13-107">[out] A pointer to the returned [ISymUnmanagedMethod](isymunmanagedmethod-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="6bc13-108">返回值</span><span class="sxs-lookup"><span data-stu-id="6bc13-108">Return Value</span></span>  

 <span data-ttu-id="6bc13-109">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="6bc13-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6bc13-110">要求</span><span class="sxs-lookup"><span data-stu-id="6bc13-110">Requirements</span></span>  

 <span data-ttu-id="6bc13-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="6bc13-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6bc13-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="6bc13-112">See also</span></span>

- [<span data-ttu-id="6bc13-113">ISymUnmanagedScope 接口</span><span class="sxs-lookup"><span data-stu-id="6bc13-113">ISymUnmanagedScope Interface</span></span>](isymunmanagedscope-interface.md)
