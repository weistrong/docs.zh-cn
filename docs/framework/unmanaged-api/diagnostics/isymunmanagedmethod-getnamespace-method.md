---
description: 了解详细信息： ISymUnmanagedMethod：： GetNamespace 方法
title: ISymUnmanagedMethod::GetNamespace 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedMethod.GetNamespace
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedMethod::GetNamespace
helpviewer_keywords:
- ISymUnmanagedMethod::GetNamespace method [.NET Framework debugging]
- GetNamespace method [.NET Framework debugging]
ms.assetid: 7fbbac42-b966-406d-9ae9-67bf3aea74ce
topic_type:
- apiref
ms.openlocfilehash: 8cb211b1047aff31cc4f12d538fee414c578155b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721406"
---
# <a name="isymunmanagedmethodgetnamespace-method"></a><span data-ttu-id="e3e69-103">ISymUnmanagedMethod::GetNamespace 方法</span><span class="sxs-lookup"><span data-stu-id="e3e69-103">ISymUnmanagedMethod::GetNamespace Method</span></span>

<span data-ttu-id="e3e69-104">获取在其中定义此方法的命名空间。</span><span class="sxs-lookup"><span data-stu-id="e3e69-104">Gets the namespace within which this method is defined.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e3e69-105">语法</span><span class="sxs-lookup"><span data-stu-id="e3e69-105">Syntax</span></span>  
  
```cpp  
HRESULT GetNamespace(  
   [out] ISymUnmanagedNamespace  **pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e3e69-106">参数</span><span class="sxs-lookup"><span data-stu-id="e3e69-106">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="e3e69-107">弄设置为返回的 [ISymUnmanagedNamespace](isymunmanagednamespace-interface.md) 接口的指针。</span><span class="sxs-lookup"><span data-stu-id="e3e69-107">[out] A pointer that is set to the returned [ISymUnmanagedNamespace](isymunmanagednamespace-interface.md) interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e3e69-108">返回值</span><span class="sxs-lookup"><span data-stu-id="e3e69-108">Return Value</span></span>  

 <span data-ttu-id="e3e69-109">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="e3e69-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e3e69-110">要求</span><span class="sxs-lookup"><span data-stu-id="e3e69-110">Requirements</span></span>  

 <span data-ttu-id="e3e69-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="e3e69-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e3e69-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="e3e69-112">See also</span></span>

- [<span data-ttu-id="e3e69-113">ISymUnmanagedMethod 接口</span><span class="sxs-lookup"><span data-stu-id="e3e69-113">ISymUnmanagedMethod Interface</span></span>](isymunmanagedmethod-interface.md)
