---
description: 了解详细信息： ICorDebugInstanceFieldSymbol 接口
title: ICorDebugInstanceFieldSymbol 接口
ms.date: 03/30/2017
ms.assetid: a4a8f259-b83a-4425-ae8b-72b067dbc0d9
ms.openlocfilehash: aa47c858ec5b4b0d04b851357fe81c0fc9b2e30a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791127"
---
# <a name="icordebuginstancefieldsymbol-interface"></a><span data-ttu-id="71094-103">ICorDebugInstanceFieldSymbol 接口</span><span class="sxs-lookup"><span data-stu-id="71094-103">ICorDebugInstanceFieldSymbol Interface</span></span>

<span data-ttu-id="71094-104">表示某一实例字段的调试符号信息。</span><span class="sxs-lookup"><span data-stu-id="71094-104">Represents the debug symbol information for an instance field.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="71094-105">方法</span><span class="sxs-lookup"><span data-stu-id="71094-105">Methods</span></span>  
  
|<span data-ttu-id="71094-106">方法</span><span class="sxs-lookup"><span data-stu-id="71094-106">Method</span></span>|<span data-ttu-id="71094-107">说明</span><span class="sxs-lookup"><span data-stu-id="71094-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="71094-108">GetName 方法</span><span class="sxs-lookup"><span data-stu-id="71094-108">GetName Method</span></span>](icordebuginstancefieldsymbol-getname-method.md)|<span data-ttu-id="71094-109">获取实例字段的名称。</span><span class="sxs-lookup"><span data-stu-id="71094-109">Gets the name of the instance field.</span></span>|  
|[<span data-ttu-id="71094-110">GetOffset 方法</span><span class="sxs-lookup"><span data-stu-id="71094-110">GetOffset Method</span></span>](icordebuginstancefieldsymbol-getoffset-method.md)|<span data-ttu-id="71094-111">获取父类中此示例字段的偏移量（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="71094-111">Gets the offset in bytes of this instance field in its parent class.</span></span>|  
|[<span data-ttu-id="71094-112">GetSize 方法</span><span class="sxs-lookup"><span data-stu-id="71094-112">GetSize Method</span></span>](icordebuginstancefieldsymbol-getsize-method.md)|<span data-ttu-id="71094-113">获取实例字段的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="71094-113">Gets the size in bytes of the instance field.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="71094-114">备注</span><span class="sxs-lookup"><span data-stu-id="71094-114">Remarks</span></span>  

 <span data-ttu-id="71094-115">`ICorDebugInstanceFieldSymbol` 接口用于检索实例字段的调试符号信息。</span><span class="sxs-lookup"><span data-stu-id="71094-115">The `ICorDebugInstanceFieldSymbol` interface is used to retrieve the debug symbol information for an instance field.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="71094-116">此接口仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="71094-116">This interface is available with .NET Native only.</span></span> <span data-ttu-id="71094-117">如果在 .NET Native 外为 ICorDebug 方案实现此接口，则公共语言运行时将忽略此接口。</span><span class="sxs-lookup"><span data-stu-id="71094-117">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="71094-118">要求</span><span class="sxs-lookup"><span data-stu-id="71094-118">Requirements</span></span>  

 <span data-ttu-id="71094-119">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="71094-119">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="71094-120">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="71094-120">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="71094-121">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="71094-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="71094-122">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="71094-122">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="71094-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="71094-123">See also</span></span>

- [<span data-ttu-id="71094-124">ICorDebugStaticFieldSymbol 接口</span><span class="sxs-lookup"><span data-stu-id="71094-124">ICorDebugStaticFieldSymbol Interface</span></span>](icordebugstaticfieldsymbol-interface.md)
- [<span data-ttu-id="71094-125">调试接口</span><span class="sxs-lookup"><span data-stu-id="71094-125">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="71094-126">调试</span><span class="sxs-lookup"><span data-stu-id="71094-126">Debugging</span></span>](index.md)
