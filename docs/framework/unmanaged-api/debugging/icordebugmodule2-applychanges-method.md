---
description: 了解详细信息： ICorDebugModule2：： ApplyChanges 方法
title: ICorDebugModule2::ApplyChanges 方法
ms.date: 03/30/2017
api_name:
- ICorDebugModule2.ApplyChanges
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule2::ApplyChanges
helpviewer_keywords:
- ApplyChanges method [.NET Framework debugging]
- ICorDebugModule2::ApplyChanges method [.NET Framework debugging]
ms.assetid: 96fa3406-6a6f-41a1-88c6-d9bc5d1a16d1
topic_type:
- apiref
ms.openlocfilehash: 09cbc395c8d656d1dc27de86305432b26308c885
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99660071"
---
# <a name="icordebugmodule2applychanges-method"></a><span data-ttu-id="72ee2-103">ICorDebugModule2::ApplyChanges 方法</span><span class="sxs-lookup"><span data-stu-id="72ee2-103">ICorDebugModule2::ApplyChanges Method</span></span>

<span data-ttu-id="72ee2-104">将元数据中的更改和 Microsoft 中间语言 (MSIL) 代码中的更改应用到正在运行的进程。</span><span class="sxs-lookup"><span data-stu-id="72ee2-104">Applies the changes in the metadata and the changes in the Microsoft intermediate language (MSIL) code to the running process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="72ee2-105">语法</span><span class="sxs-lookup"><span data-stu-id="72ee2-105">Syntax</span></span>  
  
```cpp  
HRESULT ApplyChanges (  
    [in] ULONG                       cbMetadata,  
    [in, size_is(cbMetadata)] BYTE   pbMetadata[],  
    [in] ULONG                       cbIL,  
    [in, size_is(cbIL)] BYTE         pbIL[]  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="72ee2-106">参数</span><span class="sxs-lookup"><span data-stu-id="72ee2-106">Parameters</span></span>  

 `cbMetadata`  
 <span data-ttu-id="72ee2-107">中增量元数据的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="72ee2-107">[in] Size, in bytes, of the delta metadata.</span></span>  
  
 `pbMetadata`  
 <span data-ttu-id="72ee2-108">中包含增量元数据的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="72ee2-108">[in] Buffer that contains the delta metadata.</span></span> <span data-ttu-id="72ee2-109">缓冲区的地址从 [IMetaDataEmit2：： SaveDeltaToMemory](../metadata/imetadataemit2-savedeltatomemory-method.md) 方法返回。</span><span class="sxs-lookup"><span data-stu-id="72ee2-109">The address of the buffer is returned from the [IMetaDataEmit2::SaveDeltaToMemory](../metadata/imetadataemit2-savedeltatomemory-method.md) method.</span></span>  
  
 <span data-ttu-id="72ee2-110">元数据中 (Rva) 的相对虚拟地址应相对于 MSIL 代码的开头。</span><span class="sxs-lookup"><span data-stu-id="72ee2-110">The relative virtual addresses (RVAs) in the metadata should be relative to the start of the MSIL code.</span></span>  
  
 `cbIL`  
 <span data-ttu-id="72ee2-111">中增量 MSIL 代码的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="72ee2-111">[in] Size, in bytes, of the delta MSIL code.</span></span>  
  
 `pbIL`  
 <span data-ttu-id="72ee2-112">中包含更新的 MSIL 代码的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="72ee2-112">[in] Buffer that contains the updated MSIL code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="72ee2-113">备注</span><span class="sxs-lookup"><span data-stu-id="72ee2-113">Remarks</span></span>  

 <span data-ttu-id="72ee2-114">`pbMetadata`参数采用特殊的增量元数据格式， (为[IMetaDataEmit2：： SaveDeltaToMemory](../metadata/imetadataemit2-savedeltatomemory-method.md)) 输出。</span><span class="sxs-lookup"><span data-stu-id="72ee2-114">The `pbMetadata` parameter is in a special delta metadata format (as output by [IMetaDataEmit2::SaveDeltaToMemory](../metadata/imetadataemit2-savedeltatomemory-method.md)).</span></span> <span data-ttu-id="72ee2-115">`pbMetadata` 采用以前的元数据作为基础，并描述要应用于该基的各个更改。</span><span class="sxs-lookup"><span data-stu-id="72ee2-115">`pbMetadata` takes previous metadata as a base and describes individual changes to apply to that base.</span></span>  
  
 <span data-ttu-id="72ee2-116">与此相反， `pbIL[` ] 参数包含用于已更新方法的新 msil，旨在完全替换该方法的以前的 msil</span><span class="sxs-lookup"><span data-stu-id="72ee2-116">In contrast, the `pbIL[`] parameter contains the new MSIL for the updated method, and is meant to completely replace the previous MSIL for that method</span></span>  
  
 <span data-ttu-id="72ee2-117">当在调试器内存中创建了增量 MSIL 和元数据时，调试器会调用以将 `ApplyChanges` 更改发送到公共语言运行时 (CLR) 。</span><span class="sxs-lookup"><span data-stu-id="72ee2-117">When the delta MSIL and the metadata have been created in the debugger’s memory, the debugger calls `ApplyChanges` to send the changes into the common language runtime (CLR).</span></span> <span data-ttu-id="72ee2-118">运行时将更新其元数据表，将新的 MSIL 置于进程中，并为新的 MSIL 设置实时 (JIT) 编译。</span><span class="sxs-lookup"><span data-stu-id="72ee2-118">The runtime updates its metadata tables, places the new MSIL into the process, and sets up a just-in-time (JIT) compilation of the new MSIL.</span></span> <span data-ttu-id="72ee2-119">应用这些更改后，调试器应调用 [IMetaDataEmit2：： ResetENCLog](../metadata/imetadataemit2-resetenclog-method.md) 来准备下一个编辑会话。</span><span class="sxs-lookup"><span data-stu-id="72ee2-119">When the changes have been applied, the debugger should call [IMetaDataEmit2::ResetENCLog](../metadata/imetadataemit2-resetenclog-method.md) to prepare for the next editing session.</span></span> <span data-ttu-id="72ee2-120">然后，调试器可以继续执行该过程。</span><span class="sxs-lookup"><span data-stu-id="72ee2-120">The debugger may then continue the process.</span></span>  
  
 <span data-ttu-id="72ee2-121">每当调试器 `ApplyChanges` 在具有增量元数据的模块上调用时，它还应在该模块的元数据的所有副本上调用具有相同增量元数据的 [IMetaDataEmit：： ApplyEditAndContinue](../metadata/imetadataemit-applyeditandcontinue-method.md) （用于发出更改的副本除外）。</span><span class="sxs-lookup"><span data-stu-id="72ee2-121">Whenever the debugger calls `ApplyChanges` on a module that has delta metadata, it should also call [IMetaDataEmit::ApplyEditAndContinue](../metadata/imetadataemit-applyeditandcontinue-method.md) with the same delta metadata on all of its copies of that module’s metadata except for the copy used to emit the changes.</span></span> <span data-ttu-id="72ee2-122">如果元数据的副本在某种程度上与实际的元数据不同步，则调试器始终可以丢弃该复制并获取新副本。</span><span class="sxs-lookup"><span data-stu-id="72ee2-122">If a copy of the metadata somehow becomes out-of-sync with the actual metadata, the debugger can always throw away that copy and obtain a new copy.</span></span>  
  
 <span data-ttu-id="72ee2-123">如果该 `ApplyChanges` 方法失败，调试会话将处于无效状态，必须重新启动。</span><span class="sxs-lookup"><span data-stu-id="72ee2-123">If the `ApplyChanges` method fails, the debug session is in an invalid state and must be restarted.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="72ee2-124">要求</span><span class="sxs-lookup"><span data-stu-id="72ee2-124">Requirements</span></span>  

 <span data-ttu-id="72ee2-125">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="72ee2-125">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="72ee2-126">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="72ee2-126">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="72ee2-127">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="72ee2-127">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="72ee2-128">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="72ee2-128">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
