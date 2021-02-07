---
description: 了解详细信息： ICorProfilerInfo7：： ReadInMemorySymbols
title: ICorProfilerInfo7：： ReadInMemorySymbols
ms.date: 03/30/2017
api_name:
- ICorProfilerInfo7.ReadInMemorySymbols
api_location:
- CorProf.idl
- CorProf.h
- CorGuids.lib
api_type:
- COM
ms.assetid: 1745a0b9-8332-4777-a670-b549bff3b901
ms.openlocfilehash: 7f1a88d823e7cdfcc89aa140681f61cfbe3f63ec
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99736981"
---
# <a name="icorprofilerinfo7readinmemorysymbols"></a><span data-ttu-id="4987d-103">ICorProfilerInfo7：： ReadInMemorySymbols</span><span class="sxs-lookup"><span data-stu-id="4987d-103">ICorProfilerInfo7::ReadInMemorySymbols</span></span>

<span data-ttu-id="4987d-104">[仅在 .NET Framework 4.6.1 及更高版本中受支持]</span><span class="sxs-lookup"><span data-stu-id="4987d-104">[Supported in the .NET Framework 4.6.1 and later versions]</span></span>  
  
 <span data-ttu-id="4987d-105">从内存中的符号流中读取字节。</span><span class="sxs-lookup"><span data-stu-id="4987d-105">Reads bytes from an in-memory symbol stream.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4987d-106">语法</span><span class="sxs-lookup"><span data-stu-id="4987d-106">Syntax</span></span>  
  
```cpp  
HRESULT ReadInMemorySymbols(  
        [in] ModuleID moduleId,  
        [in] DWORD symbolsReadOffset,  
        [out] BYTE* pSymbolBytes,  
        [in] DWORD countSymbolBytes,  
        [out] DWORD* pCountSymbolBytesRead  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4987d-107">参数</span><span class="sxs-lookup"><span data-stu-id="4987d-107">Parameters</span></span>  

 `moduleId`  
 <span data-ttu-id="4987d-108">中包含内存中流的模块的标识符。</span><span class="sxs-lookup"><span data-stu-id="4987d-108">[in] The identifier of the module containing the in-memory stream.</span></span>  
  
 `symbolsReadOffset`  
 <span data-ttu-id="4987d-109">中内存中流中的偏移量，从此处开始读取字节。</span><span class="sxs-lookup"><span data-stu-id="4987d-109">[in] The offset within the in-memory stream at which to start reading bytes.</span></span>  
  
 `pSymbolBytes`  
 <span data-ttu-id="4987d-110">弄指向数据将复制到的缓冲区的指针。</span><span class="sxs-lookup"><span data-stu-id="4987d-110">[out] A pointer to the buffer to which the data will be copied.</span></span> <span data-ttu-id="4987d-111">缓冲区应有 `countSymbolBytes` 可用空间。</span><span class="sxs-lookup"><span data-stu-id="4987d-111">The buffer should have `countSymbolBytes` of space available.</span></span>  
  
 `countSymbolBytes`  
 <span data-ttu-id="4987d-112">中要复制的字节数。</span><span class="sxs-lookup"><span data-stu-id="4987d-112">[in] The number of bytes to copy.</span></span>  
  
 `pCountSymbolBytesRead`  
 <span data-ttu-id="4987d-113">弄当该方法返回时，包含所读取的实际字节数。</span><span class="sxs-lookup"><span data-stu-id="4987d-113">[out] When the method returns, contains the actual number of bytes read.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4987d-114">返回值</span><span class="sxs-lookup"><span data-stu-id="4987d-114">Return Value</span></span>  

 <span data-ttu-id="4987d-115">`S_OK`如果读取的字节数为非零，则为。</span><span class="sxs-lookup"><span data-stu-id="4987d-115">`S_OK`, if a non-zero number of bytes were read.</span></span>  
  
 <span data-ttu-id="4987d-116">`CORPROF_E_MODULE_IS_DYNAMIC`如果该模块是使用创建的，则为 <xref:System.Reflection.Emit> 。</span><span class="sxs-lookup"><span data-stu-id="4987d-116">`CORPROF_E_MODULE_IS_DYNAMIC`, if the module was created using <xref:System.Reflection.Emit>.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4987d-117">备注</span><span class="sxs-lookup"><span data-stu-id="4987d-117">Remarks</span></span>  

 <span data-ttu-id="4987d-118">此 `ReadInMemorySymbols` 方法尝试 `countSymbolBytes` 从      `symbolsReadOffset` 内存中流内的偏移量开始读取数据。</span><span class="sxs-lookup"><span data-stu-id="4987d-118">The `ReadInMemorySymbols` method attempts to read `countSymbolBytes` of data starting at offset      `symbolsReadOffset` within the in-memory stream.</span></span> <span data-ttu-id="4987d-119">将数据复制到 `pSymbolBytes` ，该数据应具有 `countSymbolBytes` 可用空间。</span><span class="sxs-lookup"><span data-stu-id="4987d-119">The data is copied to `pSymbolBytes`, which is expected to have `countSymbolBytes` of space available.</span></span>     <span data-ttu-id="4987d-120">`pCountSymbolsBytesRead` 包含读取的实际字节数， `countSymbolBytes` 如果已到达流的末尾，则可以小于。</span><span class="sxs-lookup"><span data-stu-id="4987d-120">`pCountSymbolsBytesRead` contains the actual number of bytes read, which may be less than `countSymbolBytes` if the end of the stream is reached.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="4987d-121">当前实现不支持反射。发出。</span><span class="sxs-lookup"><span data-stu-id="4987d-121">The current implementation does not support Reflection.Emit.</span></span> <span data-ttu-id="4987d-122">如果该模块是使用反射创建的，则该方法返回 `CORPROF_E_MODULE_IS_DYNAMIC` 。</span><span class="sxs-lookup"><span data-stu-id="4987d-122">If the module was created by using Reflection.Emit, the method returns `CORPROF_E_MODULE_IS_DYNAMIC`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4987d-123">要求</span><span class="sxs-lookup"><span data-stu-id="4987d-123">Requirements</span></span>  

 <span data-ttu-id="4987d-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4987d-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4987d-125">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="4987d-125">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="4987d-126">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4987d-126">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4987d-127">**.NET Framework 版本：**[!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4987d-127">**.NET Framework Versions:** [!INCLUDE[net_current_v461plus](../../../../includes/net-current-v461plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4987d-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="4987d-128">See also</span></span>

- [<span data-ttu-id="4987d-129">ICorProfilerInfo7 接口</span><span class="sxs-lookup"><span data-stu-id="4987d-129">ICorProfilerInfo7 Interface</span></span>](icorprofilerinfo7-interface.md)
