---
description: 了解详细信息： CustomDumpItem 结构
title: CustomDumpItem 结构
ms.date: 03/30/2017
api_name:
- CustomDumpItem
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CustomDumpItem
helpviewer_keywords:
- CustomDumpItem structure [.NET Framework hosting]
ms.assetid: fd9085ff-7beb-4c38-97f0-037cd8ba4f65
topic_type:
- apiref
ms.openlocfilehash: 9bd7b2bb59675bc01e24dc6e6d0ce524f3d35466
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99716890"
---
# <a name="customdumpitem-structure"></a><span data-ttu-id="68f23-103">CustomDumpItem 结构</span><span class="sxs-lookup"><span data-stu-id="68f23-103">CustomDumpItem Structure</span></span>

<span data-ttu-id="68f23-104">描述要添加到错误报告中的自定义转储的项。</span><span class="sxs-lookup"><span data-stu-id="68f23-104">Describes an item to be added to a custom dump in error reporting.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="68f23-105">语法</span><span class="sxs-lookup"><span data-stu-id="68f23-105">Syntax</span></span>  
  
```cpp  
struct {  
    ECustomDumpItemKind itemKind;
    union {  
        UINT_PTR pReserved;  
    }  
} CustomDumpItem;  
```  
  
## <a name="members"></a><span data-ttu-id="68f23-106">成员</span><span class="sxs-lookup"><span data-stu-id="68f23-106">Members</span></span>  
  
|<span data-ttu-id="68f23-107">成员</span><span class="sxs-lookup"><span data-stu-id="68f23-107">Member</span></span>|<span data-ttu-id="68f23-108">说明</span><span class="sxs-lookup"><span data-stu-id="68f23-108">Description</span></span>|  
|------------|-----------------|  
|`itemKind`|<span data-ttu-id="68f23-109">一个 [ECustomDumpItemKind](ecustomdumpitemkind-enumeration.md) 值，指示要添加的项的类型。</span><span class="sxs-lookup"><span data-stu-id="68f23-109">An [ECustomDumpItemKind](ecustomdumpitemkind-enumeration.md) value that indicates the kind of item to be added.</span></span>|  
|`pReserved`|<span data-ttu-id="68f23-110">当前未使用。</span><span class="sxs-lookup"><span data-stu-id="68f23-110">Not currently used.</span></span> <span data-ttu-id="68f23-111">添加到联合的任何项都必须不大于指针大小。</span><span class="sxs-lookup"><span data-stu-id="68f23-111">Any items added to the union must be no larger than pointer size.</span></span> <span data-ttu-id="68f23-112">如果 `struct` 需要，您必须单独分配并指向它。</span><span class="sxs-lookup"><span data-stu-id="68f23-112">If a `struct` is required, you must allocate it separately and point to it.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="68f23-113">备注</span><span class="sxs-lookup"><span data-stu-id="68f23-113">Remarks</span></span>  

 <span data-ttu-id="68f23-114">[ICLRErrorReportingManager：： BeginCustomDump](iclrerrorreportingmanager-begincustomdump-method.md) 采用类型为的参数 `CustomDumpItem` 。</span><span class="sxs-lookup"><span data-stu-id="68f23-114">[ICLRErrorReportingManager::BeginCustomDump](iclrerrorreportingmanager-begincustomdump-method.md) takes a parameter of type `CustomDumpItem`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="68f23-115">要求</span><span class="sxs-lookup"><span data-stu-id="68f23-115">Requirements</span></span>  

 <span data-ttu-id="68f23-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="68f23-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="68f23-117">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="68f23-117">**Header:** MSCorEE.idl</span></span>  
  
 <span data-ttu-id="68f23-118">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="68f23-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="68f23-119">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="68f23-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="68f23-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="68f23-120">See also</span></span>

- [<span data-ttu-id="68f23-121">承载结构</span><span class="sxs-lookup"><span data-stu-id="68f23-121">Hosting Structures</span></span>](hosting-structures.md)
