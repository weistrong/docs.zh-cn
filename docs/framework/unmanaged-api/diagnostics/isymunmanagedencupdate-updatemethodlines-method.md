---
description: 了解详细信息： ISymUnmanagedENCUpdate：： UpdateMethodLines 方法
title: ISymUnmanagedENCUpdate::UpdateMethodLines 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedENCUpdate.UpdateMethodLines
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedENCUpdate::UpdateMethodLines
helpviewer_keywords:
- UpdateMethodLines method [.NET Framework debugging]
- ISymUnmanagedENCUpdate::UpdateMethodLines method [.NET Framework debugging]
ms.assetid: 275ef87b-0b53-49f9-af6b-58506335dc06
topic_type:
- apiref
ms.openlocfilehash: 6174f3aa980ccf2cdc07720e3aa90b7bb74a77af
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99710057"
---
# <a name="isymunmanagedencupdateupdatemethodlines-method"></a><span data-ttu-id="ac334-103">ISymUnmanagedENCUpdate::UpdateMethodLines 方法</span><span class="sxs-lookup"><span data-stu-id="ac334-103">ISymUnmanagedENCUpdate::UpdateMethodLines Method</span></span>

<span data-ttu-id="ac334-104">允许更新尚未重新编译但行已单独移动的方法的行信息。</span><span class="sxs-lookup"><span data-stu-id="ac334-104">Allows updating the line information for a method that has not been recompiled, but whose lines have moved independently.</span></span> <span data-ttu-id="ac334-105">允许每个语句的增量。</span><span class="sxs-lookup"><span data-stu-id="ac334-105">A delta for each statement is allowed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ac334-106">语法</span><span class="sxs-lookup"><span data-stu-id="ac334-106">Syntax</span></span>  
  
```cpp  
HRESULT UpdateMethodLines(  
    [in]  mdMethodDef  mdMethodToken,  
    [in, size_is(cDeltas)] INT32*  pDeltas,  
    [in]  ULONG        cDeltas);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ac334-107">参数</span><span class="sxs-lookup"><span data-stu-id="ac334-107">Parameters</span></span>  

 `mdMethodToken`  
 <span data-ttu-id="ac334-108">中方法标记的元数据。</span><span class="sxs-lookup"><span data-stu-id="ac334-108">[in] The metadata of the method token.</span></span>  
  
 `pDeltas`  
 <span data-ttu-id="ac334-109">中 `INT32` 值的数组，指示方法中的每个序列点的增量。</span><span class="sxs-lookup"><span data-stu-id="ac334-109">[in] An array of `INT32` values that indicates deltas for each sequence point in the method.</span></span>  
  
 `cDeltas`  
 <span data-ttu-id="ac334-110">中一个 `ULONG` 包含参数大小的 `pDeltas` 。</span><span class="sxs-lookup"><span data-stu-id="ac334-110">[in] A `ULONG` containing the size of the `pDeltas` parameter.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ac334-111">返回值</span><span class="sxs-lookup"><span data-stu-id="ac334-111">Return Value</span></span>  

 <span data-ttu-id="ac334-112">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="ac334-112">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ac334-113">要求</span><span class="sxs-lookup"><span data-stu-id="ac334-113">Requirements</span></span>  

 <span data-ttu-id="ac334-114">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="ac334-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ac334-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="ac334-115">See also</span></span>

- [<span data-ttu-id="ac334-116">ISymUnmanagedENCUpdate 接口</span><span class="sxs-lookup"><span data-stu-id="ac334-116">ISymUnmanagedENCUpdate Interface</span></span>](isymunmanagedencupdate-interface.md)
