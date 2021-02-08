---
description: 了解详细信息： ICLRDataEnumMemoryRegionsCallback：： EnumMemoryRegion 方法
title: ICLRDataEnumMemoryRegionsCallback::EnumMemoryRegion 方法
ms.date: 03/30/2017
api_name:
- ICLRDataEnumMemoryRegionsCallback.EnumMemoryRegion
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataEnumMemoryRegionsCallback::EnumMemoryRegion
helpviewer_keywords:
- EnumMemoryRegion method [.NET Framework debugging]
- ICLRDataEnumMemoryRegionsCallback::EnumMemoryRegion method [.NET Framework debugging]
ms.assetid: 9bb93fab-57e8-4f9a-9ef3-1794504fa896
topic_type:
- apiref
ms.openlocfilehash: 733911f71898ea7019a0b8d854fb1c1bf61a2474
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801392"
---
# <a name="iclrdataenummemoryregionscallbackenummemoryregion-method"></a><span data-ttu-id="e2909-103">ICLRDataEnumMemoryRegionsCallback::EnumMemoryRegion 方法</span><span class="sxs-lookup"><span data-stu-id="e2909-103">ICLRDataEnumMemoryRegionsCallback::EnumMemoryRegion Method</span></span>

<span data-ttu-id="e2909-104">由 [ICLRDataEnumMemoryRegions：： EnumMemoryRegions](iclrdataenummemoryregions-enummemoryregions-method.md) 调用，以向调试器报告尝试枚举指定的内存区域的结果。</span><span class="sxs-lookup"><span data-stu-id="e2909-104">Called by [ICLRDataEnumMemoryRegions::EnumMemoryRegions](iclrdataenummemoryregions-enummemoryregions-method.md) to report to the debugger the result of an attempt to enumerate a specified region of memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e2909-105">语法</span><span class="sxs-lookup"><span data-stu-id="e2909-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumMemoryRegion (  
    [in] CLRDATA_ADDRESS  address,  
    [in] ULONG32          size  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e2909-106">参数</span><span class="sxs-lookup"><span data-stu-id="e2909-106">Parameters</span></span>  

 `address`  
 <span data-ttu-id="e2909-107">中要枚举的内存区域的起始地址。</span><span class="sxs-lookup"><span data-stu-id="e2909-107">[in] The starting address of the memory region that was to be enumerated.</span></span>  
  
 `size`  
 <span data-ttu-id="e2909-108">中内存区域的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="e2909-108">[in] The size, in bytes, of the memory region.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e2909-109">备注</span><span class="sxs-lookup"><span data-stu-id="e2909-109">Remarks</span></span>  

 <span data-ttu-id="e2909-110">`ICLRDataEnumMemoryRegions::EnumMemoryRegions`此方法将在每次尝试枚举内存区域后调用此回调方法。</span><span class="sxs-lookup"><span data-stu-id="e2909-110">The `ICLRDataEnumMemoryRegions::EnumMemoryRegions` method will call this callback method after each attempt to enumerate a memory region.</span></span> <span data-ttu-id="e2909-111">即使此方法返回一个指示失败的 HRESULT，枚举也将继续。</span><span class="sxs-lookup"><span data-stu-id="e2909-111">The enumeration will continue even if this method returns an HRESULT indicating failure.</span></span>  
  
 <span data-ttu-id="e2909-112">此回调报告的区域可能是重复区域或重叠区域。</span><span class="sxs-lookup"><span data-stu-id="e2909-112">Regions reported by this callback may be duplicates or overlapping regions.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e2909-113">要求</span><span class="sxs-lookup"><span data-stu-id="e2909-113">Requirements</span></span>  

 <span data-ttu-id="e2909-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e2909-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e2909-115">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="e2909-115">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="e2909-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e2909-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e2909-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e2909-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e2909-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="e2909-118">See also</span></span>

- [<span data-ttu-id="e2909-119">ICLRDataEnumMemoryRegionsCallback 接口</span><span class="sxs-lookup"><span data-stu-id="e2909-119">ICLRDataEnumMemoryRegionsCallback Interface</span></span>](iclrdataenummemoryregionscallback-interface.md)
