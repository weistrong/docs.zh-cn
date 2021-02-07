---
description: 了解详细信息： ICLRDataTarget2：： AllocVirtual 方法
title: ICLRDataTarget2::AllocVirtual 方法
ms.date: 03/30/2017
api_name:
- ICLRDataTarget2.AllocVirtual
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget2::AllocVirtual
helpviewer_keywords:
- ICLRDataTarget2::AllocVirtual method [.NET Framework debugging]
- AllocVirtual method [.NET Framework debugging]
ms.assetid: e3226230-964b-47fb-9f53-d6fdbeda1e9e
topic_type:
- apiref
ms.openlocfilehash: d81474e4067599178285b6fa876919298617919d
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99729323"
---
# <a name="iclrdatatarget2allocvirtual-method"></a><span data-ttu-id="13385-103">ICLRDataTarget2::AllocVirtual 方法</span><span class="sxs-lookup"><span data-stu-id="13385-103">ICLRDataTarget2::AllocVirtual Method</span></span>

<span data-ttu-id="13385-104">由公共语言运行时 (CLR) 数据访问服务调用以在此目标进程的地址空间中分配内存。</span><span class="sxs-lookup"><span data-stu-id="13385-104">Called by the common language runtime (CLR) data access services to allocate memory in the address space of this target process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="13385-105">语法</span><span class="sxs-lookup"><span data-stu-id="13385-105">Syntax</span></span>  
  
```cpp  
HRESULT AllocVirtual(  
    [in] CLRDATA_ADDRESS addr,  
    [in] ULONG32 size,  
    [in] ULONG32 typeFlags,  
    [in] ULONG32 protectFlags,  
    [out] CLRDATA_ADDRESS* virt  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="13385-106">参数</span><span class="sxs-lookup"><span data-stu-id="13385-106">Parameters</span></span>  

 `addr`  
 <span data-ttu-id="13385-107">中一个 `CLRDATA_ADDRESS` 值，该值指定要分配的内存的起始地址。</span><span class="sxs-lookup"><span data-stu-id="13385-107">[in] A `CLRDATA_ADDRESS` value that specifies the requested starting address of the memory to be allocated.</span></span>  
  
 `size`  
 <span data-ttu-id="13385-108">中要分配的内存的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="13385-108">[in] The size, in bytes, of the memory to be allocated.</span></span>  
  
 `typeFlags`  
 <span data-ttu-id="13385-109">中控制内存分配的标志。</span><span class="sxs-lookup"><span data-stu-id="13385-109">[in] Flags that control the allocation of memory.</span></span> <span data-ttu-id="13385-110">请参阅 Win32 `VirtualAlloc` 函数。</span><span class="sxs-lookup"><span data-stu-id="13385-110">See the Win32 `VirtualAlloc` function.</span></span>  
  
 `protectFlags`  
 <span data-ttu-id="13385-111">中已分配内存的保护特性。</span><span class="sxs-lookup"><span data-stu-id="13385-111">[in] The protection attributes for the allocated memory.</span></span> <span data-ttu-id="13385-112">请参阅 Win32 `VirtualAlloc` 函数。</span><span class="sxs-lookup"><span data-stu-id="13385-112">See the Win32 `VirtualAlloc` function.</span></span>  
  
 `virt`  
 <span data-ttu-id="13385-113">弄一个指向值的指针，该 `CLRDATA_ADDRESS` 值指定分配的内存的实际起始地址。</span><span class="sxs-lookup"><span data-stu-id="13385-113">[out] A pointer to a `CLRDATA_ADDRESS` value that specifies the actual starting address of the allocated memory.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="13385-114">备注</span><span class="sxs-lookup"><span data-stu-id="13385-114">Remarks</span></span>  

 <span data-ttu-id="13385-115">`AllocVirtual`方法用作 Win32 函数的逻辑包装 `VirtualAlloc` 。</span><span class="sxs-lookup"><span data-stu-id="13385-115">The `AllocVirtual` method serves as a logical wrapper for the Win32 `VirtualAlloc` function.</span></span>  
  
 <span data-ttu-id="13385-116">此方法由调试应用程序的编写器实现。</span><span class="sxs-lookup"><span data-stu-id="13385-116">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="13385-117">要求</span><span class="sxs-lookup"><span data-stu-id="13385-117">Requirements</span></span>  

 <span data-ttu-id="13385-118">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="13385-118">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="13385-119">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="13385-119">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="13385-120">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="13385-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="13385-121">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="13385-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="13385-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="13385-122">See also</span></span>

- [<span data-ttu-id="13385-123">ICLRDataTarget2 接口</span><span class="sxs-lookup"><span data-stu-id="13385-123">ICLRDataTarget2 Interface</span></span>](iclrdatatarget2-interface.md)
- [<span data-ttu-id="13385-124">FreeVirtual 方法</span><span class="sxs-lookup"><span data-stu-id="13385-124">FreeVirtual Method</span></span>](iclrdatatarget2-freevirtual-method.md)
