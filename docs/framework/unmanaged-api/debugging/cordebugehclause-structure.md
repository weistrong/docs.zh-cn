---
description: 了解详细信息： CorDebugEHClause 结构
title: CorDebugEHClause 结构
ms.date: 03/30/2017
dev_langs:
- cpp
api_name:
- CorDebugEHClause
api_location:
- mscordbi.dll
api_type:
- COM
ms.assetid: 0e350a1b-6997-46d0-bfc5-962a5011ef43
topic_type:
- apiref
ms.openlocfilehash: ecb00e2a110719ab82de32fb1f1c861e2033a528
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801665"
---
# <a name="cordebugehclause-structure"></a><span data-ttu-id="9dd1d-103">CorDebugEHClause 结构</span><span class="sxs-lookup"><span data-stu-id="9dd1d-103">CorDebugEHClause Structure</span></span>

<span data-ttu-id="9dd1d-104">[仅在 .NET Framework 4.5.2 及更高版本中受支持]</span><span class="sxs-lookup"><span data-stu-id="9dd1d-104">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="9dd1d-105">表示给定的一段中间语言 (IL) 代码的异常处理 (EH) 子句。</span><span class="sxs-lookup"><span data-stu-id="9dd1d-105">Represents an exception handling (EH) clause for a given piece of intermediate language (IL) code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9dd1d-106">语法</span><span class="sxs-lookup"><span data-stu-id="9dd1d-106">Syntax</span></span>  
  
```cpp
typedef struct _CorDebugEHClause {  
   ULONG32 Flags;  
   ULONG32 TryOffset;  
   ULONG32 TryLength;  
   ULONG32 HandlerOffset;  
   ULONG32 HandlerLength;  
   ULONG32 ClassToken;  
   ULONG32 FilterOffset;  
} CorDebugEHClause;  
```  
  
## <a name="members"></a><span data-ttu-id="9dd1d-107">成员</span><span class="sxs-lookup"><span data-stu-id="9dd1d-107">Members</span></span>  
  
|<span data-ttu-id="9dd1d-108">成员</span><span class="sxs-lookup"><span data-stu-id="9dd1d-108">Member</span></span>|<span data-ttu-id="9dd1d-109">说明</span><span class="sxs-lookup"><span data-stu-id="9dd1d-109">Description</span></span>|  
|------------|-----------------|  
|`Flags`|<span data-ttu-id="9dd1d-110">描述 EH 子句中的异常信息的位字段。</span><span class="sxs-lookup"><span data-stu-id="9dd1d-110">A bit field that describes the exception information in the EH clause.</span></span> <span data-ttu-id="9dd1d-111">有关详细信息，请参见“备注”部分。</span><span class="sxs-lookup"><span data-stu-id="9dd1d-111">For more information, see the Remarks section.</span></span>|  
|`TryOffset`|<span data-ttu-id="9dd1d-112">方法主体开头的 `try` 块的偏移量（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="9dd1d-112">The offset, in bytes, of the `try` block from the start of the method body.</span></span>|  
|`TryLength`|<span data-ttu-id="9dd1d-113">`try` 块的长度（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="9dd1d-113">The length, in bytes, of the `try` block.</span></span>|  
|`HandlerOffset`|<span data-ttu-id="9dd1d-114">此 `try` 块的处理程序的位置。</span><span class="sxs-lookup"><span data-stu-id="9dd1d-114">The location of the handler for this `try` block.</span></span>|  
|`HandlerLength`|<span data-ttu-id="9dd1d-115">处理程序代码的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="9dd1d-115">The size of the handler code in bytes.</span></span>|  
|`ClassToken`|<span data-ttu-id="9dd1d-116">基于类型的异常处理程序的元数据标记。</span><span class="sxs-lookup"><span data-stu-id="9dd1d-116">The metadata token for a type-based exception handler.</span></span>|  
|`FilterOffset`|<span data-ttu-id="9dd1d-117">基于筛选器的异常处理程序的方法主体开头的偏移量（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="9dd1d-117">The offset, in bytes, from the start of the method body for a filter-based exception handler.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9dd1d-118">备注</span><span class="sxs-lookup"><span data-stu-id="9dd1d-118">Remarks</span></span>  

 <span data-ttu-id="9dd1d-119">`CoreDebugEHClause` [GetEHClauses](icordebugilcode-getehclauses-method.md)方法返回值的数组。</span><span class="sxs-lookup"><span data-stu-id="9dd1d-119">An array of `CoreDebugEHClause` values is returned by the [GetEHClauses](icordebugilcode-getehclauses-method.md) method.</span></span>  
  
 <span data-ttu-id="9dd1d-120">EH 子句信息由 CLI 规范定义。</span><span class="sxs-lookup"><span data-stu-id="9dd1d-120">The EH clause information is defined by the CLI specification.</span></span> <span data-ttu-id="9dd1d-121">有关详细信息，请参阅 [标准 ECMA-355：公共语言基础结构 (CLI) ，第6版](https://www.ecma-international.org/publications/standards/Ecma-335.htm)。</span><span class="sxs-lookup"><span data-stu-id="9dd1d-121">For more information, see [Standard ECMA-355: Common Language Infrastructure (CLI), 6th Edition](https://www.ecma-international.org/publications/standards/Ecma-335.htm).</span></span>  
  
 <span data-ttu-id="9dd1d-122">`flags` 字段可以包含以下标志。</span><span class="sxs-lookup"><span data-stu-id="9dd1d-122">The `flags` field can contain the following flags.</span></span> <span data-ttu-id="9dd1d-123">请注意，它们不会在 CorDebug.idl 或 CorDebug.h 中定义。</span><span class="sxs-lookup"><span data-stu-id="9dd1d-123">Note that they are not defined in CorDebug.idl or CorDebug.h.</span></span>  
  
|<span data-ttu-id="9dd1d-124">标志</span><span class="sxs-lookup"><span data-stu-id="9dd1d-124">Flag</span></span>|<span data-ttu-id="9dd1d-125">值</span><span class="sxs-lookup"><span data-stu-id="9dd1d-125">Value</span></span>|<span data-ttu-id="9dd1d-126">说明</span><span class="sxs-lookup"><span data-stu-id="9dd1d-126">Description</span></span>|  
|----------|-----------|-----------------|  
|`COR_ILEXCEPTION_CLAUSE_EXCEPTION`|<span data-ttu-id="9dd1d-127">0x00000000</span><span class="sxs-lookup"><span data-stu-id="9dd1d-127">0x00000000</span></span>|<span data-ttu-id="9dd1d-128">键入的异常子句。</span><span class="sxs-lookup"><span data-stu-id="9dd1d-128">A typed exception clause.</span></span>|  
|`COR_ILEXCEPTION_CLAUSE_FILTER`|<span data-ttu-id="9dd1d-129">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9dd1d-129">0x00000001</span></span>|<span data-ttu-id="9dd1d-130">异常筛选器和处理程序子句。</span><span class="sxs-lookup"><span data-stu-id="9dd1d-130">An exception filter and handler clause.</span></span>|  
|`COR_ILEXCEPTION_CLAUSE_FINALLY`|<span data-ttu-id="9dd1d-131">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9dd1d-131">0x00000002</span></span>|<span data-ttu-id="9dd1d-132">`finally` 子句。</span><span class="sxs-lookup"><span data-stu-id="9dd1d-132">A `finally` clause.</span></span>|  
|`COR_ILEXCEPTION_CLAUSE_FAULT`|<span data-ttu-id="9dd1d-133">0x00000004</span><span class="sxs-lookup"><span data-stu-id="9dd1d-133">0x00000004</span></span>|<span data-ttu-id="9dd1d-134">Fault 子句（仅当引发异常时才调用的 `finally` 子句）。</span><span class="sxs-lookup"><span data-stu-id="9dd1d-134">A fault clause (a `finally` clause that is called only when an exception is thrown).</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="9dd1d-135">要求</span><span class="sxs-lookup"><span data-stu-id="9dd1d-135">Requirements</span></span>  

 <span data-ttu-id="9dd1d-136">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9dd1d-136">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9dd1d-137">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="9dd1d-137">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9dd1d-138">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9dd1d-138">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9dd1d-139">**.NET Framework 版本：**[!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9dd1d-139">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9dd1d-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="9dd1d-140">See also</span></span>

- [<span data-ttu-id="9dd1d-141">GetEHClauses 方法</span><span class="sxs-lookup"><span data-stu-id="9dd1d-141">GetEHClauses Method</span></span>](icordebugilcode-getehclauses-method.md)
- [<span data-ttu-id="9dd1d-142">调试结构</span><span class="sxs-lookup"><span data-stu-id="9dd1d-142">Debugging Structures</span></span>](debugging-structures.md)
