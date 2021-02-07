---
description: 了解详细信息： ISymUnmanagedScope：： GetLocals 方法
title: ISymUnmanagedScope::GetLocals 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedScope.GetLocals
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedScope::GetLocals
helpviewer_keywords:
- GetLocals method [.NET Framework debugging]
- ISymUnmanagedScope::GetLocals method [.NET Framework debugging]
ms.assetid: 17c45f15-8c44-44da-b070-f902077b36e4
topic_type:
- apiref
ms.openlocfilehash: 6b20d8a79e826be0bd191d46e794f8dad45c4810
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763405"
---
# <a name="isymunmanagedscopegetlocals-method"></a><span data-ttu-id="3fd99-103">ISymUnmanagedScope::GetLocals 方法</span><span class="sxs-lookup"><span data-stu-id="3fd99-103">ISymUnmanagedScope::GetLocals Method</span></span>

<span data-ttu-id="3fd99-104">获取在此范围内定义的局部变量。</span><span class="sxs-lookup"><span data-stu-id="3fd99-104">Gets the local variables defined within this scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3fd99-105">语法</span><span class="sxs-lookup"><span data-stu-id="3fd99-105">Syntax</span></span>  
  
```cpp  
HRESULT GetLocals(  
    [in]  ULONG32  cLocals,  
    [out] ULONG32  *pcLocals,  
    [out, size_is(cLocals),  
        length_is(*pcLocals)] ISymUnmanagedVariable* locals[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3fd99-106">参数</span><span class="sxs-lookup"><span data-stu-id="3fd99-106">Parameters</span></span>  

 `cLocals`  
 <span data-ttu-id="3fd99-107">中 `ULONG32` 指示数组大小的 `locals` 。</span><span class="sxs-lookup"><span data-stu-id="3fd99-107">[in] A `ULONG32` that indicates the size of the `locals` array.</span></span>  
  
 `pcLocals`  
 <span data-ttu-id="3fd99-108">弄指向的指针 `ULONG32` ，该指针接收包含本地变量所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="3fd99-108">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the local variables.</span></span>  
  
 `locals`  
 <span data-ttu-id="3fd99-109">弄接收局部变量的数组。</span><span class="sxs-lookup"><span data-stu-id="3fd99-109">[out] The array that receives the local variables.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3fd99-110">返回值</span><span class="sxs-lookup"><span data-stu-id="3fd99-110">Return Value</span></span>  

 <span data-ttu-id="3fd99-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="3fd99-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3fd99-112">要求</span><span class="sxs-lookup"><span data-stu-id="3fd99-112">Requirements</span></span>  

 <span data-ttu-id="3fd99-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="3fd99-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3fd99-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="3fd99-114">See also</span></span>

- [<span data-ttu-id="3fd99-115">ISymUnmanagedScope 接口</span><span class="sxs-lookup"><span data-stu-id="3fd99-115">ISymUnmanagedScope Interface</span></span>](isymunmanagedscope-interface.md)
