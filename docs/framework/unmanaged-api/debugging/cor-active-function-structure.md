---
description: 了解详细信息： COR_ACTIVE_FUNCTION 结构
title: COR_ACTIVE_FUNCTION 结构
ms.date: 03/30/2017
api_name:
- COR_ACTIVE_FUNCTION
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- COR_ACTIVE_FUNCTION
helpviewer_keywords:
- COR_ACTIVE_FUNCTION structure [.NET Framework debugging]
ms.assetid: ed86185f-2152-459c-961f-10c06d62e83f
topic_type:
- apiref
ms.openlocfilehash: 7cc4a314c11ca4e2cdb4fe2b4090c471bcda26d5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99747200"
---
# <a name="cor_active_function-structure"></a><span data-ttu-id="d3657-103">COR_ACTIVE_FUNCTION 结构</span><span class="sxs-lookup"><span data-stu-id="d3657-103">COR_ACTIVE_FUNCTION Structure</span></span>

<span data-ttu-id="d3657-104">包含有关在线程框架中当前处于活动状态的函数的信息。</span><span class="sxs-lookup"><span data-stu-id="d3657-104">Contains information about the functions that are currently active in a thread's frames.</span></span> <span data-ttu-id="d3657-105">此结构由 [ICorDebugThread2：： GetActiveFunctions](icordebugthread2-getactivefunctions-method.md) 方法使用。</span><span class="sxs-lookup"><span data-stu-id="d3657-105">This structure is used by the [ICorDebugThread2::GetActiveFunctions](icordebugthread2-getactivefunctions-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d3657-106">语法</span><span class="sxs-lookup"><span data-stu-id="d3657-106">Syntax</span></span>  
  
```cpp  
typedef struct  _COR_ACTIVE_FUNCTION {  
    ICorDebugAppDomain   *pAppDomain;  
    ICorDebugModule      *pModule;  
    ICorDebugFunction2   *pFunction;  
    ULONG32              ilOffset;  
    ULONG32              flags;  
} COR_ACTIVE_FUNCTION;  
```  
  
## <a name="members"></a><span data-ttu-id="d3657-107">成员</span><span class="sxs-lookup"><span data-stu-id="d3657-107">Members</span></span>  
  
|<span data-ttu-id="d3657-108">成员</span><span class="sxs-lookup"><span data-stu-id="d3657-108">Member</span></span>|<span data-ttu-id="d3657-109">说明</span><span class="sxs-lookup"><span data-stu-id="d3657-109">Description</span></span>|  
|------------|-----------------|  
|`pAppDomain`|<span data-ttu-id="d3657-110">指向字段的应用程序域所有者的指针 `ilOffset` 。</span><span class="sxs-lookup"><span data-stu-id="d3657-110">Pointer to the application domain owner of the `ilOffset` field.</span></span>|  
|`pModule`|<span data-ttu-id="d3657-111">指向字段的模块所有者的指针 `ilOffset` 。</span><span class="sxs-lookup"><span data-stu-id="d3657-111">Pointer to the module owner of the `ilOffset` field.</span></span>|  
|`pFunction`|<span data-ttu-id="d3657-112">指向字段的函数所有者的指针 `ilOffset` 。</span><span class="sxs-lookup"><span data-stu-id="d3657-112">Pointer to the function owner of the `ilOffset` field.</span></span>|  
|`ilOffset`|<span data-ttu-id="d3657-113">Microsoft 中间语言 (MSIL) 帧偏移量。</span><span class="sxs-lookup"><span data-stu-id="d3657-113">The Microsoft intermediate language (MSIL) offset of the frame.</span></span>|  
|`flags`|<span data-ttu-id="d3657-114">保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="d3657-114">Reserved for future extensibility.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d3657-115">要求</span><span class="sxs-lookup"><span data-stu-id="d3657-115">Requirements</span></span>  

 <span data-ttu-id="d3657-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d3657-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d3657-117">**标头：** Cordebug.idl .idl</span><span class="sxs-lookup"><span data-stu-id="d3657-117">**Header:** CorDebug.idl</span></span>  
  
 <span data-ttu-id="d3657-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="d3657-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d3657-119">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d3657-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d3657-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="d3657-120">See also</span></span>

- [<span data-ttu-id="d3657-121">调试结构</span><span class="sxs-lookup"><span data-stu-id="d3657-121">Debugging Structures</span></span>](debugging-structures.md)
- [<span data-ttu-id="d3657-122">调试</span><span class="sxs-lookup"><span data-stu-id="d3657-122">Debugging</span></span>](index.md)
