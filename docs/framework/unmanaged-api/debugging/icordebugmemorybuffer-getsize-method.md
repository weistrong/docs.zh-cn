---
description: 了解详细信息： ICorDebugMemoryBuffer：： GetSize 方法
title: ICorDebugMemoryBuffer::GetSize 方法
ms.date: 03/30/2017
ms.assetid: 9ffd5482-268e-4680-9fd1-bfb0b7d66450
ms.openlocfilehash: 7de23dd13a1e0ef841145e3845d7d0052ce3ef9a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99754035"
---
# <a name="icordebugmemorybuffergetsize-method"></a><span data-ttu-id="18293-103">ICorDebugMemoryBuffer::GetSize 方法</span><span class="sxs-lookup"><span data-stu-id="18293-103">ICorDebugMemoryBuffer::GetSize Method</span></span>

<span data-ttu-id="18293-104">获取内存缓冲区的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="18293-104">Gets the size of the memory buffer in bytes.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="18293-105">语法</span><span class="sxs-lookup"><span data-stu-id="18293-105">Syntax</span></span>  
  
```cpp  
HRESULT GetSize(  
   [out] ULONG32 *pcbBufferLength  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="18293-106">参数</span><span class="sxs-lookup"><span data-stu-id="18293-106">Parameters</span></span>  

 `pcbBufferLength`  
 <span data-ttu-id="18293-107">[out] 指向内存缓冲区大小的指针。</span><span class="sxs-lookup"><span data-stu-id="18293-107">[out] A pointer to the size of the memory buffer.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="18293-108">备注</span><span class="sxs-lookup"><span data-stu-id="18293-108">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="18293-109">此方法仅适用于 .NET Native。</span><span class="sxs-lookup"><span data-stu-id="18293-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="18293-110">要求</span><span class="sxs-lookup"><span data-stu-id="18293-110">Requirements</span></span>  

 <span data-ttu-id="18293-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="18293-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="18293-112">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="18293-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="18293-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="18293-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="18293-114">**.NET Framework 版本：**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="18293-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="18293-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="18293-115">See also</span></span>

- [<span data-ttu-id="18293-116">ICorDebugMemoryBuffer 接口</span><span class="sxs-lookup"><span data-stu-id="18293-116">ICorDebugMemoryBuffer Interface</span></span>](icordebugmemorybuffer-interface.md)
- [<span data-ttu-id="18293-117">调试接口</span><span class="sxs-lookup"><span data-stu-id="18293-117">Debugging Interfaces</span></span>](debugging-interfaces.md)
