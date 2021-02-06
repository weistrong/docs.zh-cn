---
description: 了解详细信息： CLRDataEnumMemoryFlags 枚举
title: CLRDataEnumMemoryFlags 枚举
ms.date: 03/30/2017
api_name:
- CLRDataEnumMemoryFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CLRDataEnumMemoryFlags
helpviewer_keywords:
- CLRDataEnumMemoryFlags enumeration [.NET Framework debugging]
ms.assetid: e249f9fc-e24a-4506-903c-92781f6eab7c
topic_type:
- apiref
ms.openlocfilehash: 3522649c59177de8295416ce260c374df605efb3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99662216"
---
# <a name="clrdataenummemoryflags-enumeration"></a><span data-ttu-id="3c2e2-103">CLRDataEnumMemoryFlags 枚举</span><span class="sxs-lookup"><span data-stu-id="3c2e2-103">CLRDataEnumMemoryFlags Enumeration</span></span>

<span data-ttu-id="3c2e2-104">指示对 [ICLRDataEnumMemoryRegions：： EnumMemoryRegions](iclrdataenummemoryregions-enummemoryregions-method.md) 方法的调用应包括哪些内存区域。</span><span class="sxs-lookup"><span data-stu-id="3c2e2-104">Indicates which memory regions a call to the [ICLRDataEnumMemoryRegions::EnumMemoryRegions](iclrdataenummemoryregions-enummemoryregions-method.md) method should include.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3c2e2-105">语法</span><span class="sxs-lookup"><span data-stu-id="3c2e2-105">Syntax</span></span>  
  
```cpp  
typedef enum CLRDataEnumMemoryFlags {  
    CLRDATA_ENUM_MEM_DEFAULT  = 0x0,  
    CLRDATA_ENUM_MEM_MINI     = CLRDATA_ENUM_MEM_DEFAULT,  
    CLRDATA_ENUM_MEM_HEAP     = 0x1  
} CLRDataEnumMemoryFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="3c2e2-106">成员</span><span class="sxs-lookup"><span data-stu-id="3c2e2-106">Members</span></span>  
  
|<span data-ttu-id="3c2e2-107">成员</span><span class="sxs-lookup"><span data-stu-id="3c2e2-107">Member</span></span>|<span data-ttu-id="3c2e2-108">说明</span><span class="sxs-lookup"><span data-stu-id="3c2e2-108">Description</span></span>|  
|------------|-----------------|  
|`CLRDATA_ENUM_MEM_DEFAULT`|<span data-ttu-id="3c2e2-109">小型转储，即稀疏内存转储。</span><span class="sxs-lookup"><span data-stu-id="3c2e2-109">A minidump, that is, a sparse memory dump.</span></span>|  
|`CLRDATA_ENUM_MEM_HEAP`|<span data-ttu-id="3c2e2-110">完整堆转储。</span><span class="sxs-lookup"><span data-stu-id="3c2e2-110">A full heap dump.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="3c2e2-111">要求</span><span class="sxs-lookup"><span data-stu-id="3c2e2-111">Requirements</span></span>  

 <span data-ttu-id="3c2e2-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3c2e2-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3c2e2-113">**标头：** ClrData，ClrData</span><span class="sxs-lookup"><span data-stu-id="3c2e2-113">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="3c2e2-114">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3c2e2-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3c2e2-115">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3c2e2-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3c2e2-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="3c2e2-116">See also</span></span>

- [<span data-ttu-id="3c2e2-117">调试枚举</span><span class="sxs-lookup"><span data-stu-id="3c2e2-117">Debugging Enumerations</span></span>](debugging-enumerations.md)
