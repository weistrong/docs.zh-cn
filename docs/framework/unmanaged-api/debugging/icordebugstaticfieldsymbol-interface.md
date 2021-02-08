---
description: 了解详细信息： ICorDebugStaticFieldSymbol 接口
title: ICorDebugStaticFieldSymbol 接口
ms.date: 03/30/2017
ms.assetid: c0b93609-631e-4b15-878a-189ede922631
ms.openlocfilehash: 3aa9c98cef4cdc7edc519b06b6cf9b4b2192b4e5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794671"
---
# <a name="icordebugstaticfieldsymbol-interface"></a><span data-ttu-id="566ee-103">ICorDebugStaticFieldSymbol 接口</span><span class="sxs-lookup"><span data-stu-id="566ee-103">ICorDebugStaticFieldSymbol Interface</span></span>

<span data-ttu-id="566ee-104">表示某个静态字段的调试符号信息。</span><span class="sxs-lookup"><span data-stu-id="566ee-104">Represents the debug symbol information for a static field.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="566ee-105">方法</span><span class="sxs-lookup"><span data-stu-id="566ee-105">Methods</span></span>  
  
|<span data-ttu-id="566ee-106">方法</span><span class="sxs-lookup"><span data-stu-id="566ee-106">Method</span></span>|<span data-ttu-id="566ee-107">说明</span><span class="sxs-lookup"><span data-stu-id="566ee-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="566ee-108">GetAddress 方法</span><span class="sxs-lookup"><span data-stu-id="566ee-108">GetAddress Method</span></span>](icordebugstaticfieldsymbol-getaddress-method.md)|<span data-ttu-id="566ee-109">获取静态字段的地址。</span><span class="sxs-lookup"><span data-stu-id="566ee-109">Gets the address of the static field.</span></span>|  
|[<span data-ttu-id="566ee-110">GetName 方法</span><span class="sxs-lookup"><span data-stu-id="566ee-110">GetName Method</span></span>](icordebugstaticfieldsymbol-getname-method.md)|<span data-ttu-id="566ee-111">获取静态字段的名称。</span><span class="sxs-lookup"><span data-stu-id="566ee-111">Gets the name of the static field.</span></span>|  
|[<span data-ttu-id="566ee-112">GetSize 方法</span><span class="sxs-lookup"><span data-stu-id="566ee-112">GetSize Method</span></span>](icordebugstaticfieldsymbol-getsize-method.md)|<span data-ttu-id="566ee-113">获取静态字段的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="566ee-113">Gets the size in bytes of the static field.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="566ee-114">备注</span><span class="sxs-lookup"><span data-stu-id="566ee-114">Remarks</span></span>  

 <span data-ttu-id="566ee-115">`ICorDebugStaticFieldSymbol` 接口用于检索某个静态字段的调试符号信息。</span><span class="sxs-lookup"><span data-stu-id="566ee-115">The `ICorDebugStaticFieldSymbol` interface is used to retrieve the debug symbol information for a static field.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="566ee-116">此接口仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="566ee-116">This interface is available with .NET Native only.</span></span> <span data-ttu-id="566ee-117">如果在 .NET Native 外为 ICorDebug 方案实现此接口，则公共语言运行时将忽略此接口。</span><span class="sxs-lookup"><span data-stu-id="566ee-117">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="566ee-118">要求</span><span class="sxs-lookup"><span data-stu-id="566ee-118">Requirements</span></span>  

 <span data-ttu-id="566ee-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="566ee-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="566ee-120">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="566ee-120">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="566ee-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="566ee-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="566ee-122">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="566ee-122">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="566ee-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="566ee-123">See also</span></span>

- [<span data-ttu-id="566ee-124">ICorDebugInstanceFieldSymbol 接口</span><span class="sxs-lookup"><span data-stu-id="566ee-124">ICorDebugInstanceFieldSymbol Interface</span></span>](icordebuginstancefieldsymbol-interface.md)
- [<span data-ttu-id="566ee-125">调试接口</span><span class="sxs-lookup"><span data-stu-id="566ee-125">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="566ee-126">调试</span><span class="sxs-lookup"><span data-stu-id="566ee-126">Debugging</span></span>](index.md)
