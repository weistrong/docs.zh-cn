---
description: 了解详细信息： ICorDebugMemoryBuffer 接口
title: ICorDebugMemoryBuffer 接口
ms.date: 03/30/2017
ms.assetid: 85dc2d65-3657-4b93-9f23-9feaa95d37ff
ms.openlocfilehash: 94eeb0f31c0e1c053fabbd556768fa65dda2d328
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754012"
---
# <a name="icordebugmemorybuffer-interface"></a><span data-ttu-id="02499-103">ICorDebugMemoryBuffer 接口</span><span class="sxs-lookup"><span data-stu-id="02499-103">ICorDebugMemoryBuffer Interface</span></span>

<span data-ttu-id="02499-104">表示内存中缓冲区。</span><span class="sxs-lookup"><span data-stu-id="02499-104">Represents an in-memory buffer.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="02499-105">方法</span><span class="sxs-lookup"><span data-stu-id="02499-105">Methods</span></span>  
  
|<span data-ttu-id="02499-106">方法</span><span class="sxs-lookup"><span data-stu-id="02499-106">Method</span></span>|<span data-ttu-id="02499-107">说明</span><span class="sxs-lookup"><span data-stu-id="02499-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="02499-108">GetSize 方法</span><span class="sxs-lookup"><span data-stu-id="02499-108">GetSize Method</span></span>](icordebugmemorybuffer-getsize-method.md)|<span data-ttu-id="02499-109">获取内存缓冲区的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="02499-109">Gets the size of the memory buffer in bytes.</span></span>|  
|[<span data-ttu-id="02499-110">GetStartAddress 方法</span><span class="sxs-lookup"><span data-stu-id="02499-110">GetStartAddress Method</span></span>](icordebugmemorybuffer-getstartaddress-method.md)|<span data-ttu-id="02499-111">获取内存缓冲区的起始地址。</span><span class="sxs-lookup"><span data-stu-id="02499-111">Gets the starting address of the memory buffer.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="02499-112">备注</span><span class="sxs-lookup"><span data-stu-id="02499-112">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="02499-113">此接口仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="02499-113">This interface is available with .NET Native only.</span></span> <span data-ttu-id="02499-114">如果在 .NET Native 外为 ICorDebug 方案实现此接口，则公共语言运行时将忽略此接口。</span><span class="sxs-lookup"><span data-stu-id="02499-114">If you implement this interface for ICorDebug scenarios outside of .NET Native, the common language runtime will ignore this interface.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="02499-115">要求</span><span class="sxs-lookup"><span data-stu-id="02499-115">Requirements</span></span>  

 <span data-ttu-id="02499-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="02499-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="02499-117">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="02499-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="02499-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="02499-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="02499-119">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="02499-119">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="02499-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="02499-120">See also</span></span>

- [<span data-ttu-id="02499-121">调试接口</span><span class="sxs-lookup"><span data-stu-id="02499-121">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="02499-122">调试</span><span class="sxs-lookup"><span data-stu-id="02499-122">Debugging</span></span>](index.md)
