---
description: 了解详细信息： ICLRDataEnumMemoryRegions：： EnumMemoryRegions 方法
title: ICLRDataEnumMemoryRegions::EnumMemoryRegions 方法
ms.date: 03/30/2017
api_name:
- ICLRDataEnumMemoryRegions.EnumMemoryRegions
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICLRDataEnumMemoryRegions::EnumMemoryRegions
helpviewer_keywords:
- ICLRDataEnumMemoryRegions::EnumMemoryRegions method [.NET Framework debugging]
- EnumMemoryRegions method [.NET Framework debugging]
ms.assetid: 22d2e339-f174-40b5-a478-0b744501566f
topic_type:
- apiref
ms.openlocfilehash: 48887defab38d6ac99c718e14646d39166927438
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785725"
---
# <a name="iclrdataenummemoryregionsenummemoryregions-method"></a><span data-ttu-id="13fe5-103">ICLRDataEnumMemoryRegions::EnumMemoryRegions 方法</span><span class="sxs-lookup"><span data-stu-id="13fe5-103">ICLRDataEnumMemoryRegions::EnumMemoryRegions Method</span></span>

<span data-ttu-id="13fe5-104">枚举指定的内存区域。</span><span class="sxs-lookup"><span data-stu-id="13fe5-104">Enumerates specified areas of memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="13fe5-105">语法</span><span class="sxs-lookup"><span data-stu-id="13fe5-105">Syntax</span></span>  
  
```cpp  
HRESULT EnumMemoryRegions (  
    [in] ICLRDataEnumMemoryRegionsCallback  *callback,  
    [in] ULONG32                            miniDumpFlags,  
    [in] CLRDataEnumMemoryFlags             clrFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="13fe5-106">参数</span><span class="sxs-lookup"><span data-stu-id="13fe5-106">Parameters</span></span>  

 `callback`  
 <span data-ttu-id="13fe5-107">中指向 [ICLRDataEnumMemoryRegionsCallback](iclrdataenummemoryregionscallback-interface.md) 实例的指针，此方法为每个要枚举的内存区域调用此方法，以通知调试器结果。</span><span class="sxs-lookup"><span data-stu-id="13fe5-107">[in] A pointer to an [ICLRDataEnumMemoryRegionsCallback](iclrdataenummemoryregionscallback-interface.md) instance that is called by this method for each memory region being enumerated to notify the debugger of the result.</span></span>  
  
 <span data-ttu-id="13fe5-108">即使回调指示失败，内存区域的枚举仍将继续。</span><span class="sxs-lookup"><span data-stu-id="13fe5-108">The enumeration of memory regions continues even if the callback indicates a failure.</span></span>  
  
 `miniDumpFlags`  
 <span data-ttu-id="13fe5-109">中不使用。</span><span class="sxs-lookup"><span data-stu-id="13fe5-109">[in] Not used.</span></span>  
  
 `clrFlags`  
 <span data-ttu-id="13fe5-110">中 [CLRDataEnumMemoryFlags](clrdataenummemoryflags-enumeration.md) 枚举的一个值，该值指定要枚举的内存区域。</span><span class="sxs-lookup"><span data-stu-id="13fe5-110">[in] A value of the [CLRDataEnumMemoryFlags](clrdataenummemoryflags-enumeration.md) enumeration that specifies the regions of memory to be enumerated.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="13fe5-111">备注</span><span class="sxs-lookup"><span data-stu-id="13fe5-111">Remarks</span></span>  

 <span data-ttu-id="13fe5-112">此方法使用指定的 [ICLRDataEnumMemoryRegionsCallback](iclrdataenummemoryregionscallback-interface.md) 实例将结果通知给调用方。</span><span class="sxs-lookup"><span data-stu-id="13fe5-112">This method uses the specified [ICLRDataEnumMemoryRegionsCallback](iclrdataenummemoryregionscallback-interface.md) instance to notify the caller of results.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="13fe5-113">要求</span><span class="sxs-lookup"><span data-stu-id="13fe5-113">Requirements</span></span>  

 <span data-ttu-id="13fe5-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="13fe5-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="13fe5-115">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="13fe5-115">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="13fe5-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="13fe5-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="13fe5-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="13fe5-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="13fe5-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="13fe5-118">See also</span></span>

- [<span data-ttu-id="13fe5-119">ICLRDataEnumMemoryRegions 接口</span><span class="sxs-lookup"><span data-stu-id="13fe5-119">ICLRDataEnumMemoryRegions Interface</span></span>](iclrdataenummemoryregions-interface.md)
