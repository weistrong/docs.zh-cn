---
description: 了解详细信息： COR_PRF_STATIC_TYPE 枚举
title: COR_PRF_STATIC_TYPE 枚举
ms.date: 03/30/2017
api_name:
- COR_PRF_STATIC_TYPE
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- COR_PRF_STATIC_TYPE
helpviewer_keywords:
- COR_PRF_STATIC_TYPE enumeration [.NET Framework profiling]
ms.assetid: 441d7809-5b65-41a5-ba64-2910a8008315
topic_type:
- apiref
ms.openlocfilehash: b7171fe4e9c536d94109d46ae6cad9201a15bab9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789029"
---
# <a name="cor_prf_static_type-enumeration"></a><span data-ttu-id="5590a-103">COR_PRF_STATIC_TYPE 枚举</span><span class="sxs-lookup"><span data-stu-id="5590a-103">COR_PRF_STATIC_TYPE Enumeration</span></span>

<span data-ttu-id="5590a-104">指示字段是否为静态的，并在字段为静态字段时指示应用于该字段的静态质量。</span><span class="sxs-lookup"><span data-stu-id="5590a-104">Indicates whether a field is static and, if so, the static quality that applies to the field.</span></span> <span data-ttu-id="5590a-105">可以使用按位 "或" 运算组合这些值，以指示该字段具有多个不同的静态质量。</span><span class="sxs-lookup"><span data-stu-id="5590a-105">These values can be combined using the bitwise OR operation to indicate that the field has multiple, different static qualities.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5590a-106">语法</span><span class="sxs-lookup"><span data-stu-id="5590a-106">Syntax</span></span>  
  
```cpp  
typedef enum {  
    COR_PRF_FIELD_NOT_A_STATIC = 0x0,  
    COR_PRF_FIELD_APP_DOMAIN_STATIC = 0x1,  
    COR_PRF_FIELD_THREAD_STATIC = 0x2,  
    COR_PRF_FIELD_CONTEXT_STATIC = 0x4,  
    COR_PRF_FIELD_RVA_STATIC = 0x8  
} COR_PRF_STATIC_TYPE;  
```  
  
## <a name="members"></a><span data-ttu-id="5590a-107">成员</span><span class="sxs-lookup"><span data-stu-id="5590a-107">Members</span></span>  
  
|<span data-ttu-id="5590a-108">成员</span><span class="sxs-lookup"><span data-stu-id="5590a-108">Member</span></span>|<span data-ttu-id="5590a-109">说明</span><span class="sxs-lookup"><span data-stu-id="5590a-109">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_FIELD_NOT_A_STATIC`|<span data-ttu-id="5590a-110">此字段不是静态的。</span><span class="sxs-lookup"><span data-stu-id="5590a-110">The field is not static.</span></span>|  
|`COR_PRF_FIELD_APP_DOMAIN_STATIC`|<span data-ttu-id="5590a-111">此字段为应用程序域静态。</span><span class="sxs-lookup"><span data-stu-id="5590a-111">The field is application domain-static.</span></span>|  
|`COR_PRF_FIELD_THREAD_STATIC`|<span data-ttu-id="5590a-112">此字段是线程静态的。</span><span class="sxs-lookup"><span data-stu-id="5590a-112">The field is thread-static.</span></span>|  
|`COR_PRF_FIELD_CONTEXT_STATIC`|<span data-ttu-id="5590a-113">此字段是上下文静态的。</span><span class="sxs-lookup"><span data-stu-id="5590a-113">The field is context-static.</span></span>|  
|`COR_PRF_FIELD_RVA_STATIC`|<span data-ttu-id="5590a-114">此字段是相对虚拟地址 (RVA) 静态。</span><span class="sxs-lookup"><span data-stu-id="5590a-114">The field is relative virtual address (RVA)-static.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5590a-115">要求</span><span class="sxs-lookup"><span data-stu-id="5590a-115">Requirements</span></span>  

 <span data-ttu-id="5590a-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5590a-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5590a-117">**头文件：** CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="5590a-117">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="5590a-118">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="5590a-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="5590a-119">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5590a-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5590a-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="5590a-120">See also</span></span>

- [<span data-ttu-id="5590a-121">分析枚举</span><span class="sxs-lookup"><span data-stu-id="5590a-121">Profiling Enumerations</span></span>](profiling-enumerations.md)
