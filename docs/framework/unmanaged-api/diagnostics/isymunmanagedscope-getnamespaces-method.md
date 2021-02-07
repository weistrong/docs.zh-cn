---
description: 了解详细信息： ISymUnmanagedScope：： GetNamespaces 方法
title: ISymUnmanagedScope::GetNamespaces 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetNamespaces
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetNamespaces
helpviewer_keywords:
- GetNamespaces method, ISymUnmanagedScope interface [.NET Framework debugging]
- ISymUnmanagedScope::GetNamespaces method [.NET Framework debugging]
ms.assetid: c44b0440-04bd-460a-84fb-41afecf44503
topic_type:
- apiref
ms.openlocfilehash: 39b6507845e911cafc9b9ab38f7b67cdf1fdf2c5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763340"
---
# <a name="isymunmanagedscopegetnamespaces-method"></a><span data-ttu-id="57f31-103">ISymUnmanagedScope::GetNamespaces 方法</span><span class="sxs-lookup"><span data-stu-id="57f31-103">ISymUnmanagedScope::GetNamespaces Method</span></span>

<span data-ttu-id="57f31-104">获取正在此范围内使用的命名空间。</span><span class="sxs-lookup"><span data-stu-id="57f31-104">Gets the namespaces that are being used within this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="57f31-105">语法</span><span class="sxs-lookup"><span data-stu-id="57f31-105">Syntax</span></span>  
  
```cpp  
HRESULT GetNamespaces(  
    [in]  ULONG32  cNameSpaces,  
    [out] ULONG32  *pcNameSpaces,  
    [out, size_is(cNameSpaces),  
        length_is(*pcNameSpaces)]  
        ISymUnmanagedNamespace* namespaces[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="57f31-106">参数</span><span class="sxs-lookup"><span data-stu-id="57f31-106">Parameters</span></span>  

 `cNameSpaces`  
 <span data-ttu-id="57f31-107">[in] `namespaces` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="57f31-107">[in] The size of the `namespaces` array.</span></span>  
  
 `pcNameSpaces`  
 <span data-ttu-id="57f31-108">弄指向的指针 `ULONG32` ，该指针接收包含命名空间所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="57f31-108">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the namespaces.</span></span>  
  
 `namespaces`  
 <span data-ttu-id="57f31-109">弄接收命名空间的数组。</span><span class="sxs-lookup"><span data-stu-id="57f31-109">[out] The array that receives the namespaces.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="57f31-110">返回值</span><span class="sxs-lookup"><span data-stu-id="57f31-110">Return Value</span></span>  

 <span data-ttu-id="57f31-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="57f31-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="57f31-112">要求</span><span class="sxs-lookup"><span data-stu-id="57f31-112">Requirements</span></span>  

 <span data-ttu-id="57f31-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="57f31-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="57f31-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="57f31-114">See also</span></span>

- [<span data-ttu-id="57f31-115">ISymUnmanagedScope 接口</span><span class="sxs-lookup"><span data-stu-id="57f31-115">ISymUnmanagedScope Interface</span></span>](isymunmanagedscope-interface.md)
