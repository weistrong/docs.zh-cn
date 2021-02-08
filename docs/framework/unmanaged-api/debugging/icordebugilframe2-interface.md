---
description: 了解详细信息： ICorDebugILFrame2 接口
title: ICorDebugILFrame2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugILFrame2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugILFrame2
helpviewer_keywords:
- ICorDebugILFrame2 interface [.NET Framework debugging]
ms.assetid: f94b9d53-d8f8-4424-a95e-53a1bfd26e4a
topic_type:
- apiref
ms.openlocfilehash: 8379fda39a210e1df902dab3ac85132f04aee5fc
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99791304"
---
# <a name="icordebugilframe2-interface"></a><span data-ttu-id="89f76-103">ICorDebugILFrame2 接口</span><span class="sxs-lookup"><span data-stu-id="89f76-103">ICorDebugILFrame2 Interface</span></span>

<span data-ttu-id="89f76-104">ICorDebugILFrame 接口的逻辑扩展。</span><span class="sxs-lookup"><span data-stu-id="89f76-104">A logical extension of the ICorDebugILFrame interface.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="89f76-105">方法</span><span class="sxs-lookup"><span data-stu-id="89f76-105">Methods</span></span>  
  
|<span data-ttu-id="89f76-106">方法</span><span class="sxs-lookup"><span data-stu-id="89f76-106">Method</span></span>|<span data-ttu-id="89f76-107">说明</span><span class="sxs-lookup"><span data-stu-id="89f76-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="89f76-108">EnumerateTypeParameters 方法</span><span class="sxs-lookup"><span data-stu-id="89f76-108">EnumerateTypeParameters Method</span></span>](icordebugilframe2-enumeratetypeparameters-method.md)|<span data-ttu-id="89f76-109">获取一个 ICorDebugTypeEnum 对象，该对象包含 <xref:System.Type> 此帧中的参数。</span><span class="sxs-lookup"><span data-stu-id="89f76-109">Gets an ICorDebugTypeEnum object that contains the <xref:System.Type> parameters in this frame.</span></span>|  
|[<span data-ttu-id="89f76-110">RemapFunction 方法</span><span class="sxs-lookup"><span data-stu-id="89f76-110">RemapFunction Method</span></span>](icordebugilframe2-remapfunction-method.md)|<span data-ttu-id="89f76-111">通过指定新的 MSIL 偏移量重新映射编辑的函数。</span><span class="sxs-lookup"><span data-stu-id="89f76-111">Remaps an edited function by specifying the new MSIL offset.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="89f76-112">备注</span><span class="sxs-lookup"><span data-stu-id="89f76-112">Remarks</span></span>  
  
> [!NOTE]
> <span data-ttu-id="89f76-113">此接口不支持跨计算机或跨进程远程调用。</span><span class="sxs-lookup"><span data-stu-id="89f76-113">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="89f76-114">要求</span><span class="sxs-lookup"><span data-stu-id="89f76-114">Requirements</span></span>  

 <span data-ttu-id="89f76-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="89f76-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="89f76-116">**标头**：CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="89f76-116">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="89f76-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="89f76-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="89f76-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="89f76-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="89f76-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="89f76-119">See also</span></span>

- [<span data-ttu-id="89f76-120">调试接口</span><span class="sxs-lookup"><span data-stu-id="89f76-120">Debugging Interfaces</span></span>](debugging-interfaces.md)
