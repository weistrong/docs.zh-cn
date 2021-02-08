---
description: 了解详细信息： ISymUnmanagedAsyncMethodPropertiesWriter：:D efineAsyncStepInfo 方法
title: ISymUnmanagedAsyncMethodPropertiesWriter::DefineAsyncStepInfo 方法
ms.date: 03/30/2017
ms.assetid: f738a6ed-7cd9-4106-a5cd-355481e5771c
ms.openlocfilehash: f95436b10041ae5bfd56ca080a9b8ce70748022c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790238"
---
# <a name="isymunmanagedasyncmethodpropertieswriterdefineasyncstepinfo-method"></a><span data-ttu-id="adc30-103">ISymUnmanagedAsyncMethodPropertiesWriter::DefineAsyncStepInfo 方法</span><span class="sxs-lookup"><span data-stu-id="adc30-103">ISymUnmanagedAsyncMethodPropertiesWriter::DefineAsyncStepInfo Method</span></span>

<span data-ttu-id="adc30-104">在当前方法中定义一组异步等待操作。</span><span class="sxs-lookup"><span data-stu-id="adc30-104">Define a group of async await operations in the current method.</span></span>  
  
 <span data-ttu-id="adc30-105">每个 yield 偏移均与 await 的返回指令匹配，确定潜在的收益率。</span><span class="sxs-lookup"><span data-stu-id="adc30-105">Each yield offset matches an await's return instruction, identifying a potential yield.</span></span> <span data-ttu-id="adc30-106">每个 `breakpointMethod` / `breakpointOffset` 对都告诉我们异步操作将恢复到的位置，这可能在不同的方法中。</span><span class="sxs-lookup"><span data-stu-id="adc30-106">Each `breakpointMethod`/`breakpointOffset` pair tells us where the asynchronous operation will resume which could be in a different method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="adc30-107">语法</span><span class="sxs-lookup"><span data-stu-id="adc30-107">Syntax</span></span>  
  
```idl  
HRESULT DefineAsyncStepInfo(    [in] ULONG32 count,    [in, size_is(count)] ULONG32 yieldOffsets[],    [in, size_is(count)] ULONG32 breakpointOffset[],     [in, size_is(count)] mdToken breakpointMethod[]);  
```  
  
## <a name="parameters"></a><span data-ttu-id="adc30-108">参数</span><span class="sxs-lookup"><span data-stu-id="adc30-108">Parameters</span></span>  
  
|<span data-ttu-id="adc30-109">参数</span><span class="sxs-lookup"><span data-stu-id="adc30-109">Parameter</span></span>|<span data-ttu-id="adc30-110">说明</span><span class="sxs-lookup"><span data-stu-id="adc30-110">Description</span></span>|  
|---------------|-----------------|  
|`count`||  
|`yieldOffsets`||  
|`breakpointOffset`||  
|`breakpointMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="adc30-111">返回值</span><span class="sxs-lookup"><span data-stu-id="adc30-111">Return Value</span></span>  

 <span data-ttu-id="adc30-112">返回 `HRESULT`。</span><span class="sxs-lookup"><span data-stu-id="adc30-112">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="adc30-113">要求</span><span class="sxs-lookup"><span data-stu-id="adc30-113">Requirements</span></span>  

 <span data-ttu-id="adc30-114">**标头：** CorSym，CorSym</span><span class="sxs-lookup"><span data-stu-id="adc30-114">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="adc30-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="adc30-115">See also</span></span>

- [<span data-ttu-id="adc30-116">ISymUnmanagedAsyncMethodPropertiesWriter 接口</span><span class="sxs-lookup"><span data-stu-id="adc30-116">ISymUnmanagedAsyncMethodPropertiesWriter Interface</span></span>](isymunmanagedasyncmethodpropertieswriter-interface.md)
