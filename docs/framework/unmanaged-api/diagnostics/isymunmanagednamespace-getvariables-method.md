---
description: 了解详细信息： ISymUnmanagedNamespace：： GetVariables 方法
title: ISymUnmanagedNamespace::GetVariables 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedNamespace.GetVariables
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedNamespace::GetVariables
helpviewer_keywords:
- ISymUnmanagedNamespace::GetVariables method [.NET Framework debugging]
- GetVariables method, ISymUnmanagedNamespace interface [.NET Framework debugging]
ms.assetid: ea7c1617-f3ce-4220-8288-f2b50eaf0f0f
topic_type:
- apiref
ms.openlocfilehash: 63316bf3ba1e4736d542be3362076c3ae6e95def
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721198"
---
# <a name="isymunmanagednamespacegetvariables-method"></a><span data-ttu-id="508ed-103">ISymUnmanagedNamespace::GetVariables 方法</span><span class="sxs-lookup"><span data-stu-id="508ed-103">ISymUnmanagedNamespace::GetVariables Method</span></span>

<span data-ttu-id="508ed-104">返回在此命名空间中的全局范围内定义的所有变量。</span><span class="sxs-lookup"><span data-stu-id="508ed-104">Returns all variables defined at global scope within this namespace.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="508ed-105">语法</span><span class="sxs-lookup"><span data-stu-id="508ed-105">Syntax</span></span>  
  
```cpp
HRESULT GetVariables(  
    [in]  ULONG32  cVars,  
    [out] ULONG32  *pcVars,  
    [out, size_is(cVars), length_is(*pcVars)]  
        ISymUnmanagedVariable *pVars[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="508ed-106">参数</span><span class="sxs-lookup"><span data-stu-id="508ed-106">Parameters</span></span>  

 `cVars`  
 <span data-ttu-id="508ed-107">中 `ULONG32` 指示数组大小的 `pVars` 。</span><span class="sxs-lookup"><span data-stu-id="508ed-107">[in] A `ULONG32` that indicates the size of the `pVars` array.</span></span>  
  
 `pcVars`  
 <span data-ttu-id="508ed-108">弄指向的指针 `ULONG32` ，该指针接收包含命名空间所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="508ed-108">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the namespaces.</span></span>  
  
 `pVars`  
 <span data-ttu-id="508ed-109">弄指向包含命名空间的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="508ed-109">[out] A pointer to a buffer that contains the namespaces.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="508ed-110">返回值</span><span class="sxs-lookup"><span data-stu-id="508ed-110">Return Value</span></span>  

 <span data-ttu-id="508ed-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="508ed-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="508ed-112">要求</span><span class="sxs-lookup"><span data-stu-id="508ed-112">Requirements</span></span>  

 <span data-ttu-id="508ed-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="508ed-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="508ed-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="508ed-114">See also</span></span>

- [<span data-ttu-id="508ed-115">ISymUnmanagedNamespace 接口</span><span class="sxs-lookup"><span data-stu-id="508ed-115">ISymUnmanagedNamespace Interface</span></span>](isymunmanagednamespace-interface.md)
