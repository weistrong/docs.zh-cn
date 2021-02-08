---
description: 了解详细信息： WriteableMetadataUpdateMode 枚举
title: WriteableMetadataUpdateMode 枚举
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- WriteableMetadataUpdateMode
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 6758f4d3-6bc7-4c99-8582-e9be00566784
topic_type:
- apiref
ms.openlocfilehash: b8136963e315c429643bd0ebf4bdb509d5173bec
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800508"
---
# <a name="writeablemetadataupdatemode-enumeration"></a><span data-ttu-id="f0a15-103">WriteableMetadataUpdateMode 枚举</span><span class="sxs-lookup"><span data-stu-id="f0a15-103">WriteableMetadataUpdateMode Enumeration</span></span>

<span data-ttu-id="f0a15-104">[仅在 .NET Framework 4.5.2 及更高版本中受支持]</span><span class="sxs-lookup"><span data-stu-id="f0a15-104">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="f0a15-105">提供用于指定元数据的内存中更新对调试器是否可见的值。</span><span class="sxs-lookup"><span data-stu-id="f0a15-105">Provides values that specify whether in-memory updates to metadata are visible to a debugger.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f0a15-106">语法</span><span class="sxs-lookup"><span data-stu-id="f0a15-106">Syntax</span></span>  
  
```cpp
typedef enum WriteableMetadataUpdateMode {  
   LegacyCompatPolicy,  
   AlwaysShowUpdates  
} WriteableMetadataUpdateMode;  
```  
  
## <a name="members"></a><span data-ttu-id="f0a15-107">成员</span><span class="sxs-lookup"><span data-stu-id="f0a15-107">Members</span></span>  
  
|<span data-ttu-id="f0a15-108">成员名称</span><span class="sxs-lookup"><span data-stu-id="f0a15-108">Member name</span></span>|<span data-ttu-id="f0a15-109">描述</span><span class="sxs-lookup"><span data-stu-id="f0a15-109">Description</span></span>|  
|-----------------|-----------------|  
|`LegacyCompatPolicy`|<span data-ttu-id="f0a15-110">当使元数据的内存中更新可见时，保持与 .NET Framework 早期版本的兼容性。</span><span class="sxs-lookup"><span data-stu-id="f0a15-110">Maintain compatibility with previous versions of the .NET Framework when making in-memory updates to metadata visible.</span></span> <span data-ttu-id="f0a15-111">有关详细信息，请参阅备注部分。</span><span class="sxs-lookup"><span data-stu-id="f0a15-111">See the Remarks section for more information.</span></span>|  
|`AlwaysShowUpdates`|<span data-ttu-id="f0a15-112">使元数据的内存中更新对调试器可见。</span><span class="sxs-lookup"><span data-stu-id="f0a15-112">Make in-memory updates to metadata visible to the debugger.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f0a15-113">备注</span><span class="sxs-lookup"><span data-stu-id="f0a15-113">Remarks</span></span>  

 <span data-ttu-id="f0a15-114">枚举的成员 `WriteableMetadataUpdateMode` 可以传递给 [SetWriteableMetadataUpdateMode](icordebugprocess7-setwriteablemetadataupdatemode-method.md) 方法，以控制目标进程中元数据的内存中更新对调试器是否可见。</span><span class="sxs-lookup"><span data-stu-id="f0a15-114">A member of the `WriteableMetadataUpdateMode` enumeration can be passed to the [SetWriteableMetadataUpdateMode](icordebugprocess7-setwriteablemetadataupdatemode-method.md) method to control whether in-memory updates to metadata in the target process are visible to the debugger.</span></span>  
  
 <span data-ttu-id="f0a15-115">`LegacyCompatPolicy` 选项将强制执行与 4.5.2 之前的 .NET Framework 版本相同的行为。</span><span class="sxs-lookup"><span data-stu-id="f0a15-115">The `LegacyCompatPolicy` option enforces the same behavior as in versions of the .NET Framework before 4.5.2.</span></span> <span data-ttu-id="f0a15-116">这通常代表更新中的元数据不可见。</span><span class="sxs-lookup"><span data-stu-id="f0a15-116">This often means that metadata from updates is not visible.</span></span> <span data-ttu-id="f0a15-117">但是，对大量调试方法的调用会隐式强迫调试器使更新变得可见。</span><span class="sxs-lookup"><span data-stu-id="f0a15-117">However, calls to a number of debugging methods implicitly coerce the debugger to make updates visible.</span></span> <span data-ttu-id="f0a15-118">例如，如果调试器传递了 [ICorDebugILFrame：： GetLocalVariable](icordebugilframe-getlocalvariable-method.md) ，而该方法的原始元数据中找不到该变量的索引，则该模块的所有元数据将更新为与该进程的当前状态匹配的快照。</span><span class="sxs-lookup"><span data-stu-id="f0a15-118">For example, if the debugger passes [ICorDebugILFrame::GetLocalVariable](icordebugilframe-getlocalvariable-method.md) the index of a variable not found in the method's original metadata, all metadata for the module is updated to a snapshot matching the current state of the process.</span></span> <span data-ttu-id="f0a15-119">也就是说，借助 `LegacyCompatPolicy` 选项，调试器可能看不见任何可用的元数据更新，或者可能看见一些或者所有可用的元数据更新，具体取决于它使用非托管调试 API 的其他部分的方式。</span><span class="sxs-lookup"><span data-stu-id="f0a15-119">In other words, with the `LegacyCompatPolicy` option, the debugger might see none, some, or all of the available metadata updates, depending on how it uses other parts of the unmanaged debugging API.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f0a15-120">要求</span><span class="sxs-lookup"><span data-stu-id="f0a15-120">Requirements</span></span>  

 <span data-ttu-id="f0a15-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f0a15-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f0a15-122">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f0a15-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f0a15-123">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f0a15-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f0a15-124">**.NET Framework 版本：**[!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f0a15-124">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f0a15-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="f0a15-125">See also</span></span>

- [<span data-ttu-id="f0a15-126">调试枚举</span><span class="sxs-lookup"><span data-stu-id="f0a15-126">Debugging Enumerations</span></span>](debugging-enumerations.md)
- [<span data-ttu-id="f0a15-127">SetWriteableMetadataUpdateMode 方法</span><span class="sxs-lookup"><span data-stu-id="f0a15-127">SetWriteableMetadataUpdateMode Method</span></span>](icordebugprocess7-setwriteablemetadataupdatemode-method.md)
