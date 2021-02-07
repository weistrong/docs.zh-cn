---
description: 了解详细信息： ISymUnmanagedMethod：： GetRootScope 方法
title: ISymUnmanagedMethod::GetRootScope 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetRootScope
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetRootScope
helpviewer_keywords:
- ISymUnmanagedMethod::GetRootScope method [.NET Framework debugging]
- GetRootScope method [.NET Framework debugging]
ms.assetid: 7d58caac-2e75-4dfa-9249-32d8a624b247
topic_type:
- apiref
ms.openlocfilehash: b1e490d8e0c5e0d60143202dd0291237685c950f
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99709994"
---
# <a name="isymunmanagedmethodgetrootscope-method"></a><span data-ttu-id="946dd-103">ISymUnmanagedMethod::GetRootScope 方法</span><span class="sxs-lookup"><span data-stu-id="946dd-103">ISymUnmanagedMethod::GetRootScope Method</span></span>

<span data-ttu-id="946dd-104">获取此方法内的根词法范围。</span><span class="sxs-lookup"><span data-stu-id="946dd-104">Gets the root lexical scope within this method.</span></span> <span data-ttu-id="946dd-105">此范围包括整个方法。</span><span class="sxs-lookup"><span data-stu-id="946dd-105">This scope encloses the entire method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="946dd-106">语法</span><span class="sxs-lookup"><span data-stu-id="946dd-106">Syntax</span></span>  
  
```cpp  
HRESULT GetRootScope(  
    [out, retval] ISymUnmanagedScope** pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="946dd-107">参数</span><span class="sxs-lookup"><span data-stu-id="946dd-107">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="946dd-108">弄设置为返回的 [ISymUnmanagedScope](isymunmanagedscope-interface.md) 接口的指针。</span><span class="sxs-lookup"><span data-stu-id="946dd-108">[out] A pointer that is set to the returned [ISymUnmanagedScope](isymunmanagedscope-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="946dd-109">返回值</span><span class="sxs-lookup"><span data-stu-id="946dd-109">Return Value</span></span>  

 <span data-ttu-id="946dd-110">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="946dd-110">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="946dd-111">要求</span><span class="sxs-lookup"><span data-stu-id="946dd-111">Requirements</span></span>  

 <span data-ttu-id="946dd-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="946dd-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="946dd-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="946dd-113">See also</span></span>

- [<span data-ttu-id="946dd-114">ISymUnmanagedMethod 接口</span><span class="sxs-lookup"><span data-stu-id="946dd-114">ISymUnmanagedMethod Interface</span></span>](isymunmanagedmethod-interface.md)
