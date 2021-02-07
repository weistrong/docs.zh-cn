---
description: 了解详细信息： ISymUnmanagedScope：： GetParent 方法
title: ISymUnmanagedScope::GetParent 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetParent
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetParent
helpviewer_keywords:
- GetParent method [.NET Framework debugging]
- ISymUnmanagedScope::GetParent method [.NET Framework debugging]
ms.assetid: c7963c87-6ec5-49b3-a5cd-e0fe0c43f9b4
topic_type:
- apiref
ms.openlocfilehash: c6a056c828bfaefd171ef3f0c546d93d30fb6863
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763327"
---
# <a name="isymunmanagedscopegetparent-method"></a><span data-ttu-id="cd9c3-103">ISymUnmanagedScope::GetParent 方法</span><span class="sxs-lookup"><span data-stu-id="cd9c3-103">ISymUnmanagedScope::GetParent Method</span></span>

<span data-ttu-id="cd9c3-104">获取此范围的父范围。</span><span class="sxs-lookup"><span data-stu-id="cd9c3-104">Gets the parent scope of this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="cd9c3-105">语法</span><span class="sxs-lookup"><span data-stu-id="cd9c3-105">Syntax</span></span>  
  
```cpp  
HRESULT GetParent(  
    [out, retval] ISymUnmanagedScope** pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="cd9c3-106">参数</span><span class="sxs-lookup"><span data-stu-id="cd9c3-106">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="cd9c3-107">弄指向返回的 [ISymUnmanagedScope](isymunmanagedscope-interface.md) 接口的指针。</span><span class="sxs-lookup"><span data-stu-id="cd9c3-107">[out] A pointer to the returned [ISymUnmanagedScope](isymunmanagedscope-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="cd9c3-108">返回值</span><span class="sxs-lookup"><span data-stu-id="cd9c3-108">Return Value</span></span>  

 <span data-ttu-id="cd9c3-109">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="cd9c3-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="cd9c3-110">要求</span><span class="sxs-lookup"><span data-stu-id="cd9c3-110">Requirements</span></span>  

 <span data-ttu-id="cd9c3-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="cd9c3-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cd9c3-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="cd9c3-112">See also</span></span>

- [<span data-ttu-id="cd9c3-113">ISymUnmanagedScope 接口</span><span class="sxs-lookup"><span data-stu-id="cd9c3-113">ISymUnmanagedScope Interface</span></span>](isymunmanagedscope-interface.md)
- [<span data-ttu-id="cd9c3-114">GetChildren 方法</span><span class="sxs-lookup"><span data-stu-id="cd9c3-114">GetChildren Method</span></span>](isymunmanagedscope-getchildren-method.md)
