---
description: 了解详细信息： ICorDebugMetaDataLocator 接口
title: ICorDebugMetaDataLocator 接口
ms.date: 03/30/2017
api_name:
- ICorDebugMetaDataLocator
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugMetaDataLocator
helpviewer_keywords:
- ICorDebugMetaDataLocator interface [.NET Framework debugging]
ms.assetid: 287f5ecd-863f-4090-a615-077859f0257b
topic_type:
- apiref
ms.openlocfilehash: 7b87527d4d0b98fc97631fb47184665daaf39edb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790823"
---
# <a name="icordebugmetadatalocator-interface"></a><span data-ttu-id="0fca1-103">ICorDebugMetaDataLocator 接口</span><span class="sxs-lookup"><span data-stu-id="0fca1-103">ICorDebugMetaDataLocator Interface</span></span>

<span data-ttu-id="0fca1-104">向调试器提供元数据信息。</span><span class="sxs-lookup"><span data-stu-id="0fca1-104">Provides metadata information to the debugger.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="0fca1-105">方法</span><span class="sxs-lookup"><span data-stu-id="0fca1-105">Methods</span></span>  
  
|<span data-ttu-id="0fca1-106">方法</span><span class="sxs-lookup"><span data-stu-id="0fca1-106">Method</span></span>|<span data-ttu-id="0fca1-107">说明</span><span class="sxs-lookup"><span data-stu-id="0fca1-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="0fca1-108">GetMetaData 方法</span><span class="sxs-lookup"><span data-stu-id="0fca1-108">GetMetaData Method</span></span>](icordebugmetadatalocator-getmetadata-method.md)|<span data-ttu-id="0fca1-109">要求调试器返回模块（完成该调试器请求的操作需要其元数据）的完整路径。</span><span class="sxs-lookup"><span data-stu-id="0fca1-109">Asks the debugger to return the full path to a module whose metadata is needed to complete an operation the debugger requested.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0fca1-110">备注</span><span class="sxs-lookup"><span data-stu-id="0fca1-110">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="0fca1-111">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="0fca1-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0fca1-112">要求</span><span class="sxs-lookup"><span data-stu-id="0fca1-112">Requirements</span></span>  

 <span data-ttu-id="0fca1-113">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="0fca1-113">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0fca1-114">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="0fca1-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0fca1-115">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0fca1-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0fca1-116">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0fca1-116">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0fca1-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="0fca1-117">See also</span></span>

- [<span data-ttu-id="0fca1-118">调试接口</span><span class="sxs-lookup"><span data-stu-id="0fca1-118">Debugging Interfaces</span></span>](debugging-interfaces.md)
- [<span data-ttu-id="0fca1-119">调试</span><span class="sxs-lookup"><span data-stu-id="0fca1-119">Debugging</span></span>](index.md)
