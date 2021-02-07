---
description: 了解详细信息： ISymUnmanagedENCUpdate：： GetLocalVariables 方法
title: ISymUnmanagedENCUpdate::GetLocalVariables 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedENCUpdate.GetLocalVariables
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedENCUpdate::GetLocalVariables
helpviewer_keywords:
- ISymUnmanagedENCUpdate::GetLocalVariables method [.NET Framework debugging]
- GetLocalVariables method [.NET Framework debugging]
ms.assetid: 5c8840be-ffea-447f-9c8d-178f1eaf8d06
topic_type:
- apiref
ms.openlocfilehash: bc034603dd6a09ea78dad789e11ea951d65e839b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99721458"
---
# <a name="isymunmanagedencupdategetlocalvariables-method"></a><span data-ttu-id="c1b23-103">ISymUnmanagedENCUpdate::GetLocalVariables 方法</span><span class="sxs-lookup"><span data-stu-id="c1b23-103">ISymUnmanagedENCUpdate::GetLocalVariables Method</span></span>

<span data-ttu-id="c1b23-104">获取局部变量。</span><span class="sxs-lookup"><span data-stu-id="c1b23-104">Gets the local variables.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c1b23-105">语法</span><span class="sxs-lookup"><span data-stu-id="c1b23-105">Syntax</span></span>  
  
```cpp  
HRESULT GetLocalVariables(  
    [in]  mdMethodDef  mdMethodToken,  
    [in]  ULONG        cLocals,  
    [out, size_is(cLocals), length_is(*pceltFetched)]  
        ISymUnmanagedVariable *rgLocals[],  
    [out] ULONG        *pceltFetched);  
```  
  
## <a name="parameters"></a><span data-ttu-id="c1b23-106">参数</span><span class="sxs-lookup"><span data-stu-id="c1b23-106">Parameters</span></span>  

 `mdMethodToken`  
 <span data-ttu-id="c1b23-107">中方法的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="c1b23-107">[in] The metadata token of the method.</span></span>  
  
 `cLocals`  
 <span data-ttu-id="c1b23-108">中 `ULONG` 指示参数大小的 `rgLocals` 。</span><span class="sxs-lookup"><span data-stu-id="c1b23-108">[in] A `ULONG` that indicates the size of the `rgLocals` parameter.</span></span>  
  
 `rgLocals`  
 <span data-ttu-id="c1b23-109">弄返回的 [ISymUnmanagedVariable](isymunmanagedvariable-interface.md) 实例的数组。</span><span class="sxs-lookup"><span data-stu-id="c1b23-109">[out] The returned array of [ISymUnmanagedVariable](isymunmanagedvariable-interface.md) instances.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="c1b23-110">弄指向的指针 `ULONG` ，该指针接收 `rgLocals` 包含局部变量所需的缓冲区大小。</span><span class="sxs-lookup"><span data-stu-id="c1b23-110">[out] A pointer to a `ULONG` that receives the size of the `rgLocals` buffer required to contain the locals.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c1b23-111">返回值</span><span class="sxs-lookup"><span data-stu-id="c1b23-111">Return Value</span></span>  

 <span data-ttu-id="c1b23-112">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="c1b23-112">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c1b23-113">要求</span><span class="sxs-lookup"><span data-stu-id="c1b23-113">Requirements</span></span>  

 <span data-ttu-id="c1b23-114">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="c1b23-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c1b23-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="c1b23-115">See also</span></span>

- [<span data-ttu-id="c1b23-116">ISymUnmanagedENCUpdate 接口</span><span class="sxs-lookup"><span data-stu-id="c1b23-116">ISymUnmanagedENCUpdate Interface</span></span>](isymunmanagedencupdate-interface.md)
