---
description: 了解详细信息： ICLRDataTarget2 接口
title: ICLRDataTarget2 接口
ms.date: 03/30/2017
api_name:
- ICLRDataTarget2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget2
helpviewer_keywords:
- ICLRDataTarget2 interface [.NET Framework debugging]
ms.assetid: 94249397-861b-4294-a538-cf01466a66d3
topic_type:
- apiref
ms.openlocfilehash: 9ba6d11ea043d3b6ba85544b47e063f585854af8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794840"
---
# <a name="iclrdatatarget2-interface"></a><span data-ttu-id="a6734-103">ICLRDataTarget2 接口</span><span class="sxs-lookup"><span data-stu-id="a6734-103">ICLRDataTarget2 Interface</span></span>

<span data-ttu-id="a6734-104">数据访问服务层用于处理目标进程中的虚拟内存区域的 [ICLRDataTarget](iclrdatatarget-interface.md) 的子类。</span><span class="sxs-lookup"><span data-stu-id="a6734-104">A subclass of [ICLRDataTarget](iclrdatatarget-interface.md) that is used by the data access services layer to manipulate virtual memory regions in the target process.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="a6734-105">方法</span><span class="sxs-lookup"><span data-stu-id="a6734-105">Methods</span></span>  
  
|<span data-ttu-id="a6734-106">方法</span><span class="sxs-lookup"><span data-stu-id="a6734-106">Method</span></span>|<span data-ttu-id="a6734-107">说明</span><span class="sxs-lookup"><span data-stu-id="a6734-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="a6734-108">AllocVirtual 方法</span><span class="sxs-lookup"><span data-stu-id="a6734-108">AllocVirtual Method</span></span>](iclrdatatarget2-allocvirtual-method.md)|<span data-ttu-id="a6734-109">在目标进程的地址空间中分配内存。</span><span class="sxs-lookup"><span data-stu-id="a6734-109">Allocates memory in the address space of the target process.</span></span>|  
|[<span data-ttu-id="a6734-110">FreeVirtual 方法</span><span class="sxs-lookup"><span data-stu-id="a6734-110">FreeVirtual Method</span></span>](iclrdatatarget2-freevirtual-method.md)|<span data-ttu-id="a6734-111">释放以前在目标进程的地址空间中分配的内存。</span><span class="sxs-lookup"><span data-stu-id="a6734-111">Frees memory that was previously allocated in the address space of the target process.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="a6734-112">备注</span><span class="sxs-lookup"><span data-stu-id="a6734-112">Remarks</span></span>  

 <span data-ttu-id="a6734-113">API 客户端（即调试器）必须针对特定的目标进程实现此接口。</span><span class="sxs-lookup"><span data-stu-id="a6734-113">The API client (that is, the debugger) must implement this interface as appropriate for the particular target process.</span></span> <span data-ttu-id="a6734-114">例如，活动进程的实现将不同于内存转储的。</span><span class="sxs-lookup"><span data-stu-id="a6734-114">For example, a live process would have an implementation different from that of a memory dump.</span></span> <span data-ttu-id="a6734-115">目标可能不支持对其内存区域的修改。</span><span class="sxs-lookup"><span data-stu-id="a6734-115">The target may not support modification of its memory regions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a6734-116">要求</span><span class="sxs-lookup"><span data-stu-id="a6734-116">Requirements</span></span>  

 <span data-ttu-id="a6734-117">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a6734-117">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a6734-118">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="a6734-118">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="a6734-119">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a6734-119">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a6734-120">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a6734-120">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a6734-121">请参阅</span><span class="sxs-lookup"><span data-stu-id="a6734-121">See also</span></span>

- [<span data-ttu-id="a6734-122">ICLRDataTarget 接口</span><span class="sxs-lookup"><span data-stu-id="a6734-122">ICLRDataTarget Interface</span></span>](iclrdatatarget-interface.md)
- [<span data-ttu-id="a6734-123">调试接口</span><span class="sxs-lookup"><span data-stu-id="a6734-123">Debugging Interfaces</span></span>](debugging-interfaces.md)
