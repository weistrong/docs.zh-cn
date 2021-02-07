---
description: 了解详细信息： ISymUnmanagedWriter5：： CloseMapTokensToSourceSpans 方法
title: ISymUnmanagedWriter5::CloseMapTokensToSourceSpans 方法
ms.date: 03/30/2017
ms.assetid: f8a0c0a2-a11d-436c-aa85-bc110215cfd6
ms.openlocfilehash: 687a853441a4406c2eb0a9c4b3d5d59df3575e1d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761650"
---
# <a name="isymunmanagedwriter5closemaptokenstosourcespans-method"></a><span data-ttu-id="4459a-103">ISymUnmanagedWriter5::CloseMapTokensToSourceSpans 方法</span><span class="sxs-lookup"><span data-stu-id="4459a-103">ISymUnmanagedWriter5::CloseMapTokensToSourceSpans Method</span></span>

<span data-ttu-id="4459a-104">关闭 "特定自定义数据" 部分以获取令牌到源范围的映射信息。</span><span class="sxs-lookup"><span data-stu-id="4459a-104">Close the special custom data section for token-to-source span mapping information.</span></span> <span data-ttu-id="4459a-105">关闭后，不能再添加映射信息。</span><span class="sxs-lookup"><span data-stu-id="4459a-105">After it is closed, no more mapping information can be added.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4459a-106">语法</span><span class="sxs-lookup"><span data-stu-id="4459a-106">Syntax</span></span>  
  
```idl  
HRESULT CloseMapTokensToSourceSpans();  
```  
  
## <a name="return-value"></a><span data-ttu-id="4459a-107">返回值</span><span class="sxs-lookup"><span data-stu-id="4459a-107">Return Value</span></span>  

 <span data-ttu-id="4459a-108">返回 `HRESULT`。</span><span class="sxs-lookup"><span data-stu-id="4459a-108">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4459a-109">要求</span><span class="sxs-lookup"><span data-stu-id="4459a-109">Requirements</span></span>  

 <span data-ttu-id="4459a-110">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="4459a-110">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4459a-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="4459a-111">See also</span></span>

- [<span data-ttu-id="4459a-112">ISymUnmanagedWriter5 接口</span><span class="sxs-lookup"><span data-stu-id="4459a-112">ISymUnmanagedWriter5 Interface</span></span>](isymunmanagedwriter5-interface.md)
