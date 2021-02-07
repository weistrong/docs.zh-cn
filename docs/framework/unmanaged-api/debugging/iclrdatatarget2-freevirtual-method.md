---
description: 了解详细信息： ICLRDataTarget2：： FreeVirtual 方法
title: ICLRDataTarget2::FreeVirtual 方法
ms.date: 03/30/2017
api_name:
- ICLRDataTarget2.FreeVirtual
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataTarget2::FreeVirtual
helpviewer_keywords:
- ICLRDataTarget::FreeVirtual method [.NET Framework debugging]
- FreeVirtual method [.NET Framework debugging]
ms.assetid: 26fb69f8-1467-4711-bd24-cb117c63938f
topic_type:
- apiref
ms.openlocfilehash: ef4048f421fcdc7d284663036f8cc9f2614f4e13
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99729241"
---
# <a name="iclrdatatarget2freevirtual-method"></a><span data-ttu-id="590f4-103">ICLRDataTarget2::FreeVirtual 方法</span><span class="sxs-lookup"><span data-stu-id="590f4-103">ICLRDataTarget2::FreeVirtual Method</span></span>

<span data-ttu-id="590f4-104">由公共语言运行时 (CLR) 数据访问服务调用，以释放以前在目标进程的地址空间中分配的内存。</span><span class="sxs-lookup"><span data-stu-id="590f4-104">Called by the common language runtime (CLR) data access services to free memory that was previously allocated in the address space of the target process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="590f4-105">语法</span><span class="sxs-lookup"><span data-stu-id="590f4-105">Syntax</span></span>  
  
```cpp  
HRESULT FreeVirtual(  
    [in] CLRDATA_ADDRESS addr,  
    [in] ULONG32 size,  
    [in] ULONG32 typeFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="590f4-106">参数</span><span class="sxs-lookup"><span data-stu-id="590f4-106">Parameters</span></span>  

 `addr`  
 <span data-ttu-id="590f4-107">中一个 `CLRDATA_ADDRESS` 值，该值指定要释放的内存的起始地址。</span><span class="sxs-lookup"><span data-stu-id="590f4-107">[in] A `CLRDATA_ADDRESS` value that specifies the starting address of the memory to be freed.</span></span>  
  
 `size`  
 <span data-ttu-id="590f4-108">中要释放的内存的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="590f4-108">[in] The size, in bytes, of the memory to be freed.</span></span>  
  
 `typeFlags`  
 <span data-ttu-id="590f4-109">中控制释放内存的标志。</span><span class="sxs-lookup"><span data-stu-id="590f4-109">[in] Flags that control the freeing of memory.</span></span> <span data-ttu-id="590f4-110">请参阅 Win32 `VirtualFree` 函数。</span><span class="sxs-lookup"><span data-stu-id="590f4-110">See the Win32 `VirtualFree` function.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="590f4-111">备注</span><span class="sxs-lookup"><span data-stu-id="590f4-111">Remarks</span></span>  

 <span data-ttu-id="590f4-112">`FreeVirtual`方法用作 Win32 函数的逻辑包装 `VirtualFree` 。</span><span class="sxs-lookup"><span data-stu-id="590f4-112">The `FreeVirtual` method serves as a logical wrapper for the Win32 `VirtualFree` function.</span></span>  
  
 <span data-ttu-id="590f4-113">此方法由调试应用程序的编写器实现。</span><span class="sxs-lookup"><span data-stu-id="590f4-113">This method is implemented by the writer of the debugging application.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="590f4-114">要求</span><span class="sxs-lookup"><span data-stu-id="590f4-114">Requirements</span></span>  

 <span data-ttu-id="590f4-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="590f4-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="590f4-116">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="590f4-116">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="590f4-117">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="590f4-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="590f4-118">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="590f4-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="590f4-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="590f4-119">See also</span></span>

- [<span data-ttu-id="590f4-120">ICLRDataTarget2 接口</span><span class="sxs-lookup"><span data-stu-id="590f4-120">ICLRDataTarget2 Interface</span></span>](iclrdatatarget2-interface.md)
- [<span data-ttu-id="590f4-121">AllocVirtual 方法</span><span class="sxs-lookup"><span data-stu-id="590f4-121">AllocVirtual Method</span></span>](iclrdatatarget2-allocvirtual-method.md)
