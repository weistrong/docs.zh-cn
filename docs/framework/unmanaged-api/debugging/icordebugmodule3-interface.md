---
description: 了解详细信息： ICorDebugModule3 接口
title: ICorDebugModule3 接口
ms.date: 03/30/2017
api_name:
- ICorDebugModule3
api_location:
- CorDebug.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule3
helpviewer_keywords:
- ICorDebugModule3 interface [.NET Framework debugging]
ms.assetid: 0b69f945-263a-4e11-8512-89d27f6ea296
topic_type:
- apiref
ms.openlocfilehash: 5b47cffb267ab97de2cd225aca2998962ba66d99
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790758"
---
# <a name="icordebugmodule3-interface"></a><span data-ttu-id="8ffb8-103">ICorDebugModule3 接口</span><span class="sxs-lookup"><span data-stu-id="8ffb8-103">ICorDebugModule3 Interface</span></span>

<span data-ttu-id="8ffb8-104">为动态模块创建符号读取器。</span><span class="sxs-lookup"><span data-stu-id="8ffb8-104">Creates a symbol reader for a dynamic module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8ffb8-105">语法</span><span class="sxs-lookup"><span data-stu-id="8ffb8-105">Syntax</span></span>  
  
```cpp  
interface ICorDebugModule3 : IUnknown  
{  
    HRESULT CreateReaderForInMemorySymbols  
      (  
      [in] REFIID riid,  
      [out][iid_is(riid)] void **  ppObj  
      );  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="8ffb8-106">方法</span><span class="sxs-lookup"><span data-stu-id="8ffb8-106">Methods</span></span>  
  
|<span data-ttu-id="8ffb8-107">方法</span><span class="sxs-lookup"><span data-stu-id="8ffb8-107">Method</span></span>|<span data-ttu-id="8ffb8-108">说明</span><span class="sxs-lookup"><span data-stu-id="8ffb8-108">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="8ffb8-109">ICorDebugModule3::CreateReaderForInMemorySymbols 方法</span><span class="sxs-lookup"><span data-stu-id="8ffb8-109">ICorDebugModule3::CreateReaderForInMemorySymbols Method</span></span>](icordebugmodule3-createreaderforinmemorysymbols-method.md)|<span data-ttu-id="8ffb8-110"> (通常为动态模块的 [ISymUnmanagedReader 接口](../diagnostics/isymunmanagedreader-interface.md)) 创建符号读取器。</span><span class="sxs-lookup"><span data-stu-id="8ffb8-110">Creates a symbol reader (typically [ISymUnmanagedReader Interface](../diagnostics/isymunmanagedreader-interface.md)) for a dynamic module.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="8ffb8-111">备注</span><span class="sxs-lookup"><span data-stu-id="8ffb8-111">Remarks</span></span>  

 <span data-ttu-id="8ffb8-112">此接口以逻辑方式扩展了 "ICorDebugModule" 和 "ICorDebugModule2" 接口。</span><span class="sxs-lookup"><span data-stu-id="8ffb8-112">This interface logically extends the "ICorDebugModule" and "ICorDebugModule2" interfaces.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="8ffb8-113">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="8ffb8-113">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8ffb8-114">要求</span><span class="sxs-lookup"><span data-stu-id="8ffb8-114">Requirements</span></span>  

 <span data-ttu-id="8ffb8-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="8ffb8-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8ffb8-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="8ffb8-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8ffb8-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8ffb8-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8ffb8-118">**.NET Framework 版本：** 4.5、4、3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="8ffb8-118">**.NET Framework Versions:** 4.5, 4, 3.5 SP1</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8ffb8-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="8ffb8-119">See also</span></span>

- [<span data-ttu-id="8ffb8-120">ICorDebugRemoteTarget 接口</span><span class="sxs-lookup"><span data-stu-id="8ffb8-120">ICorDebugRemoteTarget Interface</span></span>](icordebugremotetarget-interface.md)
- [<span data-ttu-id="8ffb8-121">ICorDebug 接口</span><span class="sxs-lookup"><span data-stu-id="8ffb8-121">ICorDebug Interface</span></span>](icordebug-interface.md)

- [<span data-ttu-id="8ffb8-122">调试接口</span><span class="sxs-lookup"><span data-stu-id="8ffb8-122">Debugging Interfaces</span></span>](debugging-interfaces.md)
