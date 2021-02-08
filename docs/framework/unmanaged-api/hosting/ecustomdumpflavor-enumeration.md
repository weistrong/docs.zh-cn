---
description: 了解详细信息： ECustomDumpFlavor 枚举
title: ECustomDumpFlavor 枚举
ms.date: 03/30/2017
api_name:
- ECustomDumpFlavor
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ECustomDumpFlavor
helpviewer_keywords:
- ECustomDumpFlavor enumeration [.NET Framework hosting]
ms.assetid: b39b3320-fac7-41f1-9a03-ab6fb0cd89c7
topic_type:
- apiref
ms.openlocfilehash: 3ef118368fc827472bdaacb0b03d8c2011275056
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785518"
---
# <a name="ecustomdumpflavor-enumeration"></a><span data-ttu-id="7f90d-103">ECustomDumpFlavor 枚举</span><span class="sxs-lookup"><span data-stu-id="7f90d-103">ECustomDumpFlavor Enumeration</span></span>

<span data-ttu-id="7f90d-104">包含一些值，这些值指示在报告错误时要包含在堆转储的自定义子集中的项。</span><span class="sxs-lookup"><span data-stu-id="7f90d-104">Contains values that indicate which items to include in a custom subset of a heap dump when reporting errors.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7f90d-105">语法</span><span class="sxs-lookup"><span data-stu-id="7f90d-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    DUMP_FLAVOR_Mini            = 1,  
    DUMP_FLAVOR_NonHeapCLRState = 2  
} ECustomDumpFlavor;  
```  
  
## <a name="members"></a><span data-ttu-id="7f90d-106">成员</span><span class="sxs-lookup"><span data-stu-id="7f90d-106">Members</span></span>  
  
|<span data-ttu-id="7f90d-107">成员</span><span class="sxs-lookup"><span data-stu-id="7f90d-107">Member</span></span>|<span data-ttu-id="7f90d-108">说明</span><span class="sxs-lookup"><span data-stu-id="7f90d-108">Description</span></span>|  
|------------|-----------------|  
|`DUMP_FLAVOR_Mini`|<span data-ttu-id="7f90d-109">指定自定义堆转储应作为小型转储开始，并包含传递给同一方法的任何 [CustomDumpItem](customdumpitem-structure.md) 实例指定的额外数据。</span><span class="sxs-lookup"><span data-stu-id="7f90d-109">Specifies that the custom heap dump should start as a minidump and include extra data specified by any [CustomDumpItem](customdumpitem-structure.md) instances passed to the same method.</span></span>|  
|`DUMP_FLAVOR_NonHeapCLRState`|<span data-ttu-id="7f90d-110">指定自定义堆转储应收集未动态分配的所有运行时状态数据。</span><span class="sxs-lookup"><span data-stu-id="7f90d-110">Specifies that the custom heap dump should gather all run-time state data that was not dynamically allocated.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="7f90d-111">备注</span><span class="sxs-lookup"><span data-stu-id="7f90d-111">Remarks</span></span>  

 <span data-ttu-id="7f90d-112">类型的参数 `ECustomDumpFlavor` 传递给 [ICLRErrorReportingManager：： BeginCustomDump](iclrerrorreportingmanager-begincustomdump-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="7f90d-112">A parameter of type `ECustomDumpFlavor` is passed to the [ICLRErrorReportingManager::BeginCustomDump](iclrerrorreportingmanager-begincustomdump-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7f90d-113">要求</span><span class="sxs-lookup"><span data-stu-id="7f90d-113">Requirements</span></span>  

 <span data-ttu-id="7f90d-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7f90d-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7f90d-115">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="7f90d-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="7f90d-116">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7f90d-116">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="7f90d-117">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7f90d-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7f90d-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="7f90d-118">See also</span></span>

- [<span data-ttu-id="7f90d-119">ECustomDumpItemKind 枚举</span><span class="sxs-lookup"><span data-stu-id="7f90d-119">ECustomDumpItemKind Enumeration</span></span>](ecustomdumpitemkind-enumeration.md)
- [<span data-ttu-id="7f90d-120">ICLRErrorReportingManager 接口</span><span class="sxs-lookup"><span data-stu-id="7f90d-120">ICLRErrorReportingManager Interface</span></span>](iclrerrorreportingmanager-interface.md)
- [<span data-ttu-id="7f90d-121">承载枚举</span><span class="sxs-lookup"><span data-stu-id="7f90d-121">Hosting Enumerations</span></span>](hosting-enumerations.md)
