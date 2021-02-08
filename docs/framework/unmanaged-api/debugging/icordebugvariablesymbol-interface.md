---
description: 了解详细信息： ICorDebugVariableSymbol 接口
title: ICorDebugVariableSymbol 接口
ms.date: 03/30/2017
ms.assetid: 0e58b85e-69bd-41ff-bedb-8cdc8be6a7a2
ms.openlocfilehash: fa3fc1f318627e9175a3066c3bd3eac00929ea60
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790537"
---
# <a name="icordebugvariablesymbol-interface"></a><span data-ttu-id="11867-103">ICorDebugVariableSymbol 接口</span><span class="sxs-lookup"><span data-stu-id="11867-103">ICorDebugVariableSymbol Interface</span></span>

<span data-ttu-id="11867-104">检索变量的调试符号信息。</span><span class="sxs-lookup"><span data-stu-id="11867-104">Retrieves the debug symbol information for a variable.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="11867-105">方法</span><span class="sxs-lookup"><span data-stu-id="11867-105">Methods</span></span>  
  
|<span data-ttu-id="11867-106">方法</span><span class="sxs-lookup"><span data-stu-id="11867-106">Method</span></span>|<span data-ttu-id="11867-107">说明</span><span class="sxs-lookup"><span data-stu-id="11867-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="11867-108">GetName 方法</span><span class="sxs-lookup"><span data-stu-id="11867-108">GetName Method</span></span>](icordebugvariablesymbol-getname-method.md)|<span data-ttu-id="11867-109">获取变量名。</span><span class="sxs-lookup"><span data-stu-id="11867-109">Gets the name of a variable.</span></span>|  
|[<span data-ttu-id="11867-110">GetSize 方法</span><span class="sxs-lookup"><span data-stu-id="11867-110">GetSize Method</span></span>](icordebugvariablesymbol-getsize-method.md)|<span data-ttu-id="11867-111">获取变量的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="11867-111">Gets the size of a variable in bytes.</span></span>|  
|[<span data-ttu-id="11867-112">GetSlotIndex 方法</span><span class="sxs-lookup"><span data-stu-id="11867-112">GetSlotIndex Method</span></span>](icordebugvariablesymbol-getslotindex-method.md)|<span data-ttu-id="11867-113">获取本地变量的托管槽索引。</span><span class="sxs-lookup"><span data-stu-id="11867-113">Gets the managed slot index of a local variable.</span></span>|  
|[<span data-ttu-id="11867-114">GetValue 方法</span><span class="sxs-lookup"><span data-stu-id="11867-114">GetValue Method</span></span>](icordebugvariablesymbol-getvalue-method.md)|<span data-ttu-id="11867-115">获取作为字节数组的变量的值。</span><span class="sxs-lookup"><span data-stu-id="11867-115">Gets the value of a variable as a byte array.</span></span>|  
|[<span data-ttu-id="11867-116">SetValue 方法</span><span class="sxs-lookup"><span data-stu-id="11867-116">SetValue Method</span></span>](icordebugvariablesymbol-setvalue-method.md)|<span data-ttu-id="11867-117">将字节数组的值分配给变量。</span><span class="sxs-lookup"><span data-stu-id="11867-117">Assigns the value of a byte array to a variable.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="11867-118">备注</span><span class="sxs-lookup"><span data-stu-id="11867-118">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="11867-119">此接口仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="11867-119">This interface is available with .NET Native only.</span></span> <span data-ttu-id="11867-120">如果在 .NET Native 外为 ICorDebug 方案实现此接口，则公共语言运行时将忽略此接口。</span><span class="sxs-lookup"><span data-stu-id="11867-120">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="11867-121">要求</span><span class="sxs-lookup"><span data-stu-id="11867-121">Requirements</span></span>  

 <span data-ttu-id="11867-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="11867-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="11867-123">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="11867-123">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="11867-124">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="11867-124">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="11867-125">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="11867-125">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="11867-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="11867-126">See also</span></span>

- [<span data-ttu-id="11867-127">调试接口</span><span class="sxs-lookup"><span data-stu-id="11867-127">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="11867-128">调试</span><span class="sxs-lookup"><span data-stu-id="11867-128">Debugging</span></span>](index.md)
