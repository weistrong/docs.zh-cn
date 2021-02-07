---
description: 了解详细信息： ISymUnmanagedWriter3：： OpenMethod2 方法
title: ISymUnmanagedWriter3::OpenMethod2 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter3.OpenMethod2
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter3::OpenMethod2
helpviewer_keywords:
- ISymUnmanagedWriter3::OpenMethod2 method [.NET Framework debugging]
- OpenMethod2 method [.NET Framework debugging]
ms.assetid: 025e358c-448f-4423-a2f2-57acf437c8a5
topic_type:
- apiref
ms.openlocfilehash: 7e76be03598599a6498ed45bc3799c6d6f21e088
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761689"
---
# <a name="isymunmanagedwriter3openmethod2-method"></a><span data-ttu-id="d15c7-103">ISymUnmanagedWriter3::OpenMethod2 方法</span><span class="sxs-lookup"><span data-stu-id="d15c7-103">ISymUnmanagedWriter3::OpenMethod2 Method</span></span>

<span data-ttu-id="d15c7-104">打开方法并在图像中提供其实际节偏移量。</span><span class="sxs-lookup"><span data-stu-id="d15c7-104">Opens a method and provides its real section offset in the image.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d15c7-105">语法</span><span class="sxs-lookup"><span data-stu-id="d15c7-105">Syntax</span></span>  
  
```cpp  
HRESULT OpenMethod2(
    [in] mdMethodDef method,  
    [in] ULONG32 isect,  
    [in] ULONG32 offset);  
```  
  
## <a name="parameters"></a><span data-ttu-id="d15c7-106">参数</span><span class="sxs-lookup"><span data-stu-id="d15c7-106">Parameters</span></span>  

 `method`  
 <span data-ttu-id="d15c7-107">中要打开的方法的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="d15c7-107">[in] The metadata token for the method to be opened.</span></span>  
  
 `isect`  
 <span data-ttu-id="d15c7-108">中图像中的节偏移量。</span><span class="sxs-lookup"><span data-stu-id="d15c7-108">[in] The section offset in the image.</span></span>  
  
 `offset`  
 <span data-ttu-id="d15c7-109">中图像中的偏移量。</span><span class="sxs-lookup"><span data-stu-id="d15c7-109">[in] The offset in the image.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d15c7-110">返回值</span><span class="sxs-lookup"><span data-stu-id="d15c7-110">Return Value</span></span>  

 <span data-ttu-id="d15c7-111">如果该方法成功，则 S_OK;否则，E_FAIL 或其他一些错误代码。</span><span class="sxs-lookup"><span data-stu-id="d15c7-111">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d15c7-112">要求</span><span class="sxs-lookup"><span data-stu-id="d15c7-112">Requirements</span></span>  

 <span data-ttu-id="d15c7-113">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="d15c7-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d15c7-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="d15c7-114">See also</span></span>

- [<span data-ttu-id="d15c7-115">ISymUnmanagedWriter3 接口</span><span class="sxs-lookup"><span data-stu-id="d15c7-115">ISymUnmanagedWriter3 Interface</span></span>](isymunmanagedwriter3-interface.md)
- [<span data-ttu-id="d15c7-116">OpenMethod 方法</span><span class="sxs-lookup"><span data-stu-id="d15c7-116">OpenMethod Method</span></span>](isymunmanagedwriter-openmethod-method.md)
