---
description: 了解详细信息： ICorDebugAssemblyEnum：： Next 方法
title: ICorDebugAssemblyEnum::Next 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAssemblyEnum.Next
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAssemblyEnum::Next method
helpviewer_keywords:
- ICorDebugAssemblyEnum::Next method [.NET Framework debugging]
- Next method, ICorDebugAssemblyEnum interface [.NET Framework debugging]
ms.assetid: b3e7d0c2-3baa-4ef8-8e3f-b865cf252940
topic_type:
- apiref
ms.openlocfilehash: feb77f22ec59fcc0e1b3f5590b7aee4efba13d01
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99772219"
---
# <a name="icordebugassemblyenumnext-method"></a><span data-ttu-id="fec01-103">ICorDebugAssemblyEnum::Next 方法</span><span class="sxs-lookup"><span data-stu-id="fec01-103">ICorDebugAssemblyEnum::Next Method</span></span>

<span data-ttu-id="fec01-104">从当前游标位置开始，从集合中获取指定数目的程序集。</span><span class="sxs-lookup"><span data-stu-id="fec01-104">Gets the specified number of assemblies from the collection, starting at the current cursor position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fec01-105">语法</span><span class="sxs-lookup"><span data-stu-id="fec01-105">Syntax</span></span>  
  
```cpp  
HRESULT Next (  
    [in] ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugAssembly *values[],  
    [out] ULONG *pceltFetched  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="fec01-106">参数</span><span class="sxs-lookup"><span data-stu-id="fec01-106">Parameters</span></span>  

 `celt`  
 <span data-ttu-id="fec01-107">中要检索的程序集的数目。</span><span class="sxs-lookup"><span data-stu-id="fec01-107">[in] The number of assemblies to be retrieved.</span></span>  
  
 `values`  
 <span data-ttu-id="fec01-108">弄指针的数组，其中每个都指向表示程序集的 ICorDebugAssembly 对象。</span><span class="sxs-lookup"><span data-stu-id="fec01-108">[out] An array of pointers, each of which points to an ICorDebugAssembly object that represents an assembly.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="fec01-109">弄一个指针，指向实际返回的程序集的数目。</span><span class="sxs-lookup"><span data-stu-id="fec01-109">[out] A pointer to the number of assemblies actually returned.</span></span> <span data-ttu-id="fec01-110">如果为1，则此值可以为 null `celt` 。</span><span class="sxs-lookup"><span data-stu-id="fec01-110">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fec01-111">要求</span><span class="sxs-lookup"><span data-stu-id="fec01-111">Requirements</span></span>  

 <span data-ttu-id="fec01-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fec01-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fec01-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="fec01-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="fec01-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fec01-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fec01-115">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fec01-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
