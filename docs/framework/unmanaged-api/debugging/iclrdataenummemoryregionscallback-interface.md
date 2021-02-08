---
description: 了解详细信息： ICLRDataEnumMemoryRegionsCallback 接口
title: ICLRDataEnumMemoryRegionsCallback 接口
ms.date: 03/30/2017
api_name:
- ICLRDataEnumMemoryRegionsCallback
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataEnumMemoryRegionsCallback
helpviewer_keywords:
- ICLRDataEnumMemoryRegionsCallback interface [.NET Framework debugging]
ms.assetid: 3f1af8b0-8478-48e0-a7ec-3e90e0b97649
topic_type:
- apiref
ms.openlocfilehash: 863192844c4d4d8a35d1e73d38adea3a513bc944
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99801366"
---
# <a name="iclrdataenummemoryregionscallback-interface"></a><span data-ttu-id="fc150-103">ICLRDataEnumMemoryRegionsCallback 接口</span><span class="sxs-lookup"><span data-stu-id="fc150-103">ICLRDataEnumMemoryRegionsCallback Interface</span></span>

<span data-ttu-id="fc150-104">为 [ICLRDataEnumMemoryRegions：： EnumMemoryRegions](iclrdataenummemoryregions-enummemoryregions-method.md) 提供回调方法，以便向调试器报告尝试枚举指定的内存区域的结果。</span><span class="sxs-lookup"><span data-stu-id="fc150-104">Provides a callback method for [ICLRDataEnumMemoryRegions::EnumMemoryRegions](iclrdataenummemoryregions-enummemoryregions-method.md) to report to the debugger the result of an attempt to enumerate a specified region of memory.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="fc150-105">方法</span><span class="sxs-lookup"><span data-stu-id="fc150-105">Methods</span></span>  
  
|<span data-ttu-id="fc150-106">方法</span><span class="sxs-lookup"><span data-stu-id="fc150-106">Method</span></span>|<span data-ttu-id="fc150-107">说明</span><span class="sxs-lookup"><span data-stu-id="fc150-107">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="fc150-108">EnumMemoryRegion 方法</span><span class="sxs-lookup"><span data-stu-id="fc150-108">EnumMemoryRegion Method</span></span>](iclrdataenummemoryregionscallback-enummemoryregion-method.md)|<span data-ttu-id="fc150-109">由调用 `ICLRDataEnumMemoryRegions::EnumMemoryRegions` ，以向调试器报告尝试枚举指定的内存区域的结果。</span><span class="sxs-lookup"><span data-stu-id="fc150-109">Called by `ICLRDataEnumMemoryRegions::EnumMemoryRegions` to report to the debugger the result of an attempt to enumerate a specified region of memory.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="fc150-110">要求</span><span class="sxs-lookup"><span data-stu-id="fc150-110">Requirements</span></span>  

 <span data-ttu-id="fc150-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="fc150-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fc150-112">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="fc150-112">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="fc150-113">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="fc150-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="fc150-114">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fc150-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fc150-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="fc150-115">See also</span></span>

- [<span data-ttu-id="fc150-116">调试接口</span><span class="sxs-lookup"><span data-stu-id="fc150-116">Debugging Interfaces</span></span>](debugging-interfaces.md)
