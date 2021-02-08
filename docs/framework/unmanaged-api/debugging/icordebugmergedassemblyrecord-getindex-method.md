---
description: 了解详细信息： ICorDebugMergedAssemblyRecord：： GetIndex 方法
title: ICorDebugMergedAssemblyRecord::GetIndex 方法
ms.date: 03/30/2017
ms.assetid: 98701444-b9bc-4978-9548-89ac3394147d
ms.openlocfilehash: f3a51c5ed5edacc9678c965ac385d0969e2ee8a7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801106"
---
# <a name="icordebugmergedassemblyrecordgetindex-method"></a><span data-ttu-id="94d6b-103">ICorDebugMergedAssemblyRecord::GetIndex 方法</span><span class="sxs-lookup"><span data-stu-id="94d6b-103">ICorDebugMergedAssemblyRecord::GetIndex Method</span></span>

<span data-ttu-id="94d6b-104">获取程序集的前缀索引。</span><span class="sxs-lookup"><span data-stu-id="94d6b-104">Gets the assembly's prefix index.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="94d6b-105">语法</span><span class="sxs-lookup"><span data-stu-id="94d6b-105">Syntax</span></span>  
  
```cpp  
HRESULT GetIndex(  
   [out] ULONG32 *pIndex  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="94d6b-106">参数</span><span class="sxs-lookup"><span data-stu-id="94d6b-106">Parameters</span></span>  

 `pIndex`  
 <span data-ttu-id="94d6b-107">[out] 指向前缀索引的指针。</span><span class="sxs-lookup"><span data-stu-id="94d6b-107">[out] A pointer to the prefix index.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="94d6b-108">备注</span><span class="sxs-lookup"><span data-stu-id="94d6b-108">Remarks</span></span>  

 <span data-ttu-id="94d6b-109">前缀索引用于防止合并的元数据类型名称出现名称冲突。</span><span class="sxs-lookup"><span data-stu-id="94d6b-109">The prefix index is used to prevent name collisions in the merged metadata type names.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="94d6b-110">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="94d6b-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="94d6b-111">要求</span><span class="sxs-lookup"><span data-stu-id="94d6b-111">Requirements</span></span>  

 <span data-ttu-id="94d6b-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="94d6b-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="94d6b-113">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="94d6b-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="94d6b-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="94d6b-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="94d6b-115">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="94d6b-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="94d6b-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="94d6b-116">See also</span></span>

- [<span data-ttu-id="94d6b-117">ICorDebugMergedAssemblyRecord 接口</span><span class="sxs-lookup"><span data-stu-id="94d6b-117">ICorDebugMergedAssemblyRecord Interface</span></span>](icordebugmergedassemblyrecord-interface.md)
- [<span data-ttu-id="94d6b-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="94d6b-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
