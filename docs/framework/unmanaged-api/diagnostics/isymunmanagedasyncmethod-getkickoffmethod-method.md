---
description: 了解详细信息： ISymUnmanagedAsyncMethod：： GetKickoffMethod 方法
title: ISymUnmanagedAsyncMethod::GetKickoffMethod 方法
ms.date: 03/30/2017
ms.assetid: ba084444-9e68-4cde-9388-54b950670987
ms.openlocfilehash: c763109ac8556fd7941675f98879c6a1792e8bc4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790290"
---
# <a name="isymunmanagedasyncmethodgetkickoffmethod-method"></a><span data-ttu-id="a03cc-103">ISymUnmanagedAsyncMethod::GetKickoffMethod 方法</span><span class="sxs-lookup"><span data-stu-id="a03cc-103">ISymUnmanagedAsyncMethod::GetKickoffMethod Method</span></span>

<span data-ttu-id="a03cc-104">请参阅 [DefineKickoffMethod 方法](isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md)。</span><span class="sxs-lookup"><span data-stu-id="a03cc-104">See [DefineKickoffMethod Method](isymunmanagedasyncmethodpropertieswriter-definekickoffmethod-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a03cc-105">语法</span><span class="sxs-lookup"><span data-stu-id="a03cc-105">Syntax</span></span>  
  
```idl  
HRESULT GetKickoffMethod(    [out, retval] mdToken* kickoffMethod);  
```  
  
## <a name="parameters"></a><span data-ttu-id="a03cc-106">参数</span><span class="sxs-lookup"><span data-stu-id="a03cc-106">Parameters</span></span>  
  
|<span data-ttu-id="a03cc-107">参数</span><span class="sxs-lookup"><span data-stu-id="a03cc-107">Parameter</span></span>|<span data-ttu-id="a03cc-108">说明</span><span class="sxs-lookup"><span data-stu-id="a03cc-108">Description</span></span>|  
|---------------|-----------------|  
|`kickoffMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="a03cc-109">返回值</span><span class="sxs-lookup"><span data-stu-id="a03cc-109">Return Value</span></span>  

 <span data-ttu-id="a03cc-110">返回 `HRESULT`。</span><span class="sxs-lookup"><span data-stu-id="a03cc-110">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a03cc-111">要求</span><span class="sxs-lookup"><span data-stu-id="a03cc-111">Requirements</span></span>  

 <span data-ttu-id="a03cc-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="a03cc-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a03cc-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="a03cc-113">See also</span></span>

- [<span data-ttu-id="a03cc-114">ISymUnmanagedAsyncMethod 接口</span><span class="sxs-lookup"><span data-stu-id="a03cc-114">ISymUnmanagedAsyncMethod Interface</span></span>](isymunmanagedasyncmethod-interface.md)
