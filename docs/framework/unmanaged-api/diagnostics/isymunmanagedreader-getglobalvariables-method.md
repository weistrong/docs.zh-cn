---
description: 了解详细信息： ISymUnmanagedReader：： GetGlobalVariables 方法
title: ISymUnmanagedReader::GetGlobalVariables 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedReader.GetGlobalVariables
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedReader::GetGlobalVariables
helpviewer_keywords:
- GetGlobalVariables method [.NET Framework debugging]
- ISymUnmanagedReader::GetGlobalVariables method [.NET Framework debugging]
ms.assetid: a2dd5098-3e58-4be5-b7a2-e4160b3b505a
topic_type:
- apiref
ms.openlocfilehash: 2b017d2a5746942f701cf79d3d29f1eb571dceab
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689646"
---
# <a name="isymunmanagedreadergetglobalvariables-method"></a><span data-ttu-id="d1052-103">ISymUnmanagedReader::GetGlobalVariables 方法</span><span class="sxs-lookup"><span data-stu-id="d1052-103">ISymUnmanagedReader::GetGlobalVariables Method</span></span>

<span data-ttu-id="d1052-104">返回所有全局变量。</span><span class="sxs-lookup"><span data-stu-id="d1052-104">Returns all global variables.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d1052-105">语法</span><span class="sxs-lookup"><span data-stu-id="d1052-105">Syntax</span></span>  
  
```cpp  
HRESULT GetGlobalVariables(  
    [in]  ULONG32  cVars,  
    [out] ULONG32  *pcVars,  
    [out, size_is(cVars),  
        length_is(*pcVars)] ISymUnmanagedVariable *pVars[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d1052-106">参数</span><span class="sxs-lookup"><span data-stu-id="d1052-106">Parameters</span></span>  

 `cVars`  
 <span data-ttu-id="d1052-107">中所指向的缓冲区的长度 `pcVars` 。</span><span class="sxs-lookup"><span data-stu-id="d1052-107">[in] The length of the buffer pointed to by `pcVars`.</span></span>  
  
 `pcVars`  
 <span data-ttu-id="d1052-108">弄指向的指针 `ULONG32` ，该指针接收包含变量所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="d1052-108">[out] A pointer to a `ULONG32` that receives the size of the buffer required to contain the variables.</span></span>  
  
 `pVars`  
 <span data-ttu-id="d1052-109">弄包含变量的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="d1052-109">[out] A buffer that contains the variables.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d1052-110">返回值</span><span class="sxs-lookup"><span data-stu-id="d1052-110">Return Value</span></span>  

 <span data-ttu-id="d1052-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="d1052-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d1052-112">要求</span><span class="sxs-lookup"><span data-stu-id="d1052-112">Requirements</span></span>  

 <span data-ttu-id="d1052-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="d1052-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d1052-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="d1052-114">See also</span></span>

- [<span data-ttu-id="d1052-115">ISymUnmanagedReader 接口</span><span class="sxs-lookup"><span data-stu-id="d1052-115">ISymUnmanagedReader Interface</span></span>](isymunmanagedreader-interface.md)
