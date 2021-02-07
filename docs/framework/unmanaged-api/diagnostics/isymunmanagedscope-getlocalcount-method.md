---
description: 了解详细信息： ISymUnmanagedScope：： GetLocalCount 方法
title: ISymUnmanagedScope::GetLocalCount 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetLocalCount
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetLocalCount
helpviewer_keywords:
- GetLocalCount method [.NET Framework debugging]
- ISymUnmanagedScope::GetLocalCount method [.NET Framework debugging]
ms.assetid: 3ede8fb5-f655-4088-8e19-9c53812588a8
topic_type:
- apiref
ms.openlocfilehash: 987d161d273b12810988ef30acb703973098d29c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763432"
---
# <a name="isymunmanagedscopegetlocalcount-method"></a><span data-ttu-id="49545-103">ISymUnmanagedScope::GetLocalCount 方法</span><span class="sxs-lookup"><span data-stu-id="49545-103">ISymUnmanagedScope::GetLocalCount Method</span></span>

<span data-ttu-id="49545-104">获取在此范围内定义的局部变量的计数。</span><span class="sxs-lookup"><span data-stu-id="49545-104">Gets a count of the local variables defined within this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="49545-105">语法</span><span class="sxs-lookup"><span data-stu-id="49545-105">Syntax</span></span>  
  
```cpp  
HRESULT GetLocalCount(  
    [out, retval] ULONG32 *pRetVal);  
```  
  
## <a name="parameters"></a><span data-ttu-id="49545-106">参数</span><span class="sxs-lookup"><span data-stu-id="49545-106">Parameters</span></span>  

 `pRetVal`  
 <span data-ttu-id="49545-107">弄指向的指针 `ULONG32` ，该指针接收局部变量的计数。</span><span class="sxs-lookup"><span data-stu-id="49545-107">[out] A pointer to a `ULONG32` that receives the count of local variables.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="49545-108">返回值</span><span class="sxs-lookup"><span data-stu-id="49545-108">Return Value</span></span>  

 <span data-ttu-id="49545-109">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="49545-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="49545-110">要求</span><span class="sxs-lookup"><span data-stu-id="49545-110">Requirements</span></span>  

 <span data-ttu-id="49545-111">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="49545-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="49545-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="49545-112">See also</span></span>

- [<span data-ttu-id="49545-113">ISymUnmanagedScope 接口</span><span class="sxs-lookup"><span data-stu-id="49545-113">ISymUnmanagedScope Interface</span></span>](isymunmanagedscope-interface.md)
