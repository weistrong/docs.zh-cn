---
description: 了解详细信息： ISymUnmanagedReader：： GetVariables 方法
title: ISymUnmanagedReader::GetVariables 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetVariables
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetVariables
helpviewer_keywords:
- ISymUnmanagedReader::GetVariables method [.NET Framework debugging]
- GetVariables method, ISymUnmanagedReader interface [.NET Framework debugging]
ms.assetid: 16dc49cb-2c60-4ac8-9c35-020e9afba3f8
topic_type:
- apiref
ms.openlocfilehash: 93208e6c5c65c4c770c533b7ea72de513451d97d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99763899"
---
# <a name="isymunmanagedreadergetvariables-method"></a><span data-ttu-id="3df23-103">ISymUnmanagedReader::GetVariables 方法</span><span class="sxs-lookup"><span data-stu-id="3df23-103">ISymUnmanagedReader::GetVariables Method</span></span>

<span data-ttu-id="3df23-104">在给定父和名称的情况下，返回非局部变量。</span><span class="sxs-lookup"><span data-stu-id="3df23-104">Returns a non-local variable, given its parent and name.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3df23-105">语法</span><span class="sxs-lookup"><span data-stu-id="3df23-105">Syntax</span></span>  
  
```cpp  
HRESULT GetVariables (  
    [in]  mdToken  parent,  
    [in]  ULONG32  cVars,  
    [out] ULONG32  *pcVars,  
    [out, size_is (cVars),  
        length_is (*pcVars)] ISymUnmanagedVariable *pVars[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3df23-106">参数</span><span class="sxs-lookup"><span data-stu-id="3df23-106">Parameters</span></span>  

 `parent`  
 <span data-ttu-id="3df23-107">中变量的父级。</span><span class="sxs-lookup"><span data-stu-id="3df23-107">[in] The parent of the variable.</span></span>  
  
 `cVars`  
 <span data-ttu-id="3df23-108">[in] `pVars` 数组的大小。</span><span class="sxs-lookup"><span data-stu-id="3df23-108">[in] The size of the `pVars` array.</span></span>  
  
 `pcVars`  
 <span data-ttu-id="3df23-109">弄指向一个变量的指针，该变量接收返回的变量数 `pVars` 。</span><span class="sxs-lookup"><span data-stu-id="3df23-109">[out] A pointer to the variable that receives the number of variables returned in `pVars`.</span></span>  
  
 `pVars`  
 <span data-ttu-id="3df23-110">弄指向接收变量的变量的指针。</span><span class="sxs-lookup"><span data-stu-id="3df23-110">[out] A pointer to the variable that receives the variables.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3df23-111">返回值</span><span class="sxs-lookup"><span data-stu-id="3df23-111">Return Value</span></span>  

 <span data-ttu-id="3df23-112">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="3df23-112">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3df23-113">要求</span><span class="sxs-lookup"><span data-stu-id="3df23-113">Requirements</span></span>  

 <span data-ttu-id="3df23-114">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="3df23-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3df23-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="3df23-115">See also</span></span>

- [<span data-ttu-id="3df23-116">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="3df23-116">ISymUnmanagedReader Interface</span></span>](isymunmanagedreader-interface.md)
