---
description: 了解详细信息： ICorDebugMemoryBuffer：： GetStartAddress 方法
title: ICorDebugMemoryBuffer::GetStartAddress 方法
ms.date: 03/30/2017
ms.assetid: f804d9ab-8c88-44f0-b278-5fcca7f87726
ms.openlocfilehash: 46720d70b8a1019e712b577b24dec5d4c3d5a31d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99722706"
---
# <a name="icordebugmemorybuffergetstartaddress-method"></a><span data-ttu-id="6d801-103">ICorDebugMemoryBuffer::GetStartAddress 方法</span><span class="sxs-lookup"><span data-stu-id="6d801-103">ICorDebugMemoryBuffer::GetStartAddress Method</span></span>

<span data-ttu-id="6d801-104">获取内存缓冲区的起始地址。</span><span class="sxs-lookup"><span data-stu-id="6d801-104">Gets the starting address of the memory buffer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6d801-105">语法</span><span class="sxs-lookup"><span data-stu-id="6d801-105">Syntax</span></span>  
  
```cpp  
HRESULT GetStartAddress(  
   [out] LPCVOID *address  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="6d801-106">参数</span><span class="sxs-lookup"><span data-stu-id="6d801-106">Parameters</span></span>  

 `address`  
 <span data-ttu-id="6d801-107">[out] 指向内存缓冲区起始地址的指针。</span><span class="sxs-lookup"><span data-stu-id="6d801-107">[out] A pointer to the starting address of the memory buffer.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6d801-108">备注</span><span class="sxs-lookup"><span data-stu-id="6d801-108">Remarks</span></span>  
  
> [!WARNING]
> <span data-ttu-id="6d801-109">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="6d801-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6d801-110">要求</span><span class="sxs-lookup"><span data-stu-id="6d801-110">Requirements</span></span>  

 <span data-ttu-id="6d801-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6d801-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6d801-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="6d801-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="6d801-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="6d801-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="6d801-114">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6d801-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6d801-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="6d801-115">See also</span></span>

- [<span data-ttu-id="6d801-116">ICorDebugMemoryBuffer 接口</span><span class="sxs-lookup"><span data-stu-id="6d801-116">ICorDebugMemoryBuffer Interface</span></span>](icordebugmemorybuffer-interface.md)
- [<span data-ttu-id="6d801-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="6d801-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
