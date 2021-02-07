---
description: 了解详细信息： ISymUnmanagedAsyncMethod：： GetAsyncStepInfo 方法
title: ISymUnmanagedAsyncMethod::GetAsyncStepInfo 方法
ms.date: 03/30/2017
ms.assetid: 3ef5b4b8-4ac7-4906-849b-f932c5e3db07
ms.openlocfilehash: dc255323f103b3422b927b0489402b24767dcd92
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99737839"
---
# <a name="isymunmanagedasyncmethodgetasyncstepinfo-method"></a><span data-ttu-id="0804d-103">ISymUnmanagedAsyncMethod::GetAsyncStepInfo 方法</span><span class="sxs-lookup"><span data-stu-id="0804d-103">ISymUnmanagedAsyncMethod::GetAsyncStepInfo Method</span></span>

<span data-ttu-id="0804d-104">请参阅 [DefineAsyncStepInfo 方法](isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md)。</span><span class="sxs-lookup"><span data-stu-id="0804d-104">See [DefineAsyncStepInfo Method](isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0804d-105">语法</span><span class="sxs-lookup"><span data-stu-id="0804d-105">Syntax</span></span>  
  
```idl  
HRESULT GetAsyncStepInfo(    [in] ULONG32 cStepInfo,    [out] ULONG32 *pcStepInfo,    [in, size_is(cStepInfo)] ULONG32 yieldOffsets[],    [in, size_is(cStepInfo)] ULONG32 breakpointOffset[],    [in, size_is(cStepInfo)] mdToken breakpointMethod[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="0804d-106">参数</span><span class="sxs-lookup"><span data-stu-id="0804d-106">Parameters</span></span>  
  
|<span data-ttu-id="0804d-107">参数</span><span class="sxs-lookup"><span data-stu-id="0804d-107">Parameter</span></span>|<span data-ttu-id="0804d-108">说明</span><span class="sxs-lookup"><span data-stu-id="0804d-108">Description</span></span>|  
|---------------|-----------------|  
|`cStepInfo`||  
|`pcStepInfo`||  
|`yieldOffsets`||  
|`breakpointOffset`||  
|`breakpointMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="0804d-109">返回值</span><span class="sxs-lookup"><span data-stu-id="0804d-109">Return Value</span></span>  

 <span data-ttu-id="0804d-110">返回 `HRESULT`。</span><span class="sxs-lookup"><span data-stu-id="0804d-110">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0804d-111">要求</span><span class="sxs-lookup"><span data-stu-id="0804d-111">Requirements</span></span>  

 <span data-ttu-id="0804d-112">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="0804d-112">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0804d-113">请参阅</span><span class="sxs-lookup"><span data-stu-id="0804d-113">See also</span></span>

- [<span data-ttu-id="0804d-114">ISymUnmanagedAsyncMethod 接口</span><span class="sxs-lookup"><span data-stu-id="0804d-114">ISymUnmanagedAsyncMethod Interface</span></span>](isymunmanagedasyncmethod-interface.md)
