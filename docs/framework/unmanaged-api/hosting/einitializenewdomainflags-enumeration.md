---
description: 了解详细信息： EInitializeNewDomainFlags 枚举
title: EInitializeNewDomainFlags 枚举
ms.date: 03/30/2017
api_name:
- EInitializeNewDomainFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EInitializeNewDomainFlags
helpviewer_keywords:
- EInitializeNewDomainFlags enumeration [.NET Framework hosting]
ms.assetid: 3a120ab2-f5ef-4c9b-8595-d3ed7247c342
ms.openlocfilehash: b856d061e86c0c79b35f842975378307b79a37e7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785459"
---
# <a name="einitializenewdomainflags-enumeration"></a><span data-ttu-id="29849-103">EInitializeNewDomainFlags 枚举</span><span class="sxs-lookup"><span data-stu-id="29849-103">EInitializeNewDomainFlags Enumeration</span></span>

<span data-ttu-id="29849-104">使宿主能够向运行时提供有关应用程序域初始化的信息。</span><span class="sxs-lookup"><span data-stu-id="29849-104">Enables the host to provide the runtime with information about the initialization of an application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="29849-105">语法</span><span class="sxs-lookup"><span data-stu-id="29849-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    eInitializeNewDomainFlags_None              = 0x0000,  
    eInitializeNewDomainFlags_NoSecurityChanges = 0x0002  
} EInitializeNewDomainFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="29849-106">成员</span><span class="sxs-lookup"><span data-stu-id="29849-106">Members</span></span>  
  
|<span data-ttu-id="29849-107">成员</span><span class="sxs-lookup"><span data-stu-id="29849-107">Member</span></span>|<span data-ttu-id="29849-108">说明</span><span class="sxs-lookup"><span data-stu-id="29849-108">Description</span></span>|  
|------------|-----------------|  
|`eInitializeNewDomainFlags_None`|<span data-ttu-id="29849-109">无标志。</span><span class="sxs-lookup"><span data-stu-id="29849-109">No flags.</span></span>|  
|`eInitializeNewDomainFlags_NoSecurityChanges`|<span data-ttu-id="29849-110">通知公共语言运行时 (CLR) 宿主不会在方法中更改应用程序域的安全状态 <xref:System.AppDomainManager.InitializeNewDomain%2A> 。</span><span class="sxs-lookup"><span data-stu-id="29849-110">Informs the common language runtime (CLR) that the host will not make changes to the security state of the application domain in the <xref:System.AppDomainManager.InitializeNewDomain%2A> method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="29849-111">备注</span><span class="sxs-lookup"><span data-stu-id="29849-111">Remarks</span></span>  

 <span data-ttu-id="29849-112">[ICLRDomainManager：： SetAppDomainManagerType](iclrdomainmanager-setappdomainmanagertype-method.md)方法采用类型的参数 `EInitializeNewDomainFlags` 。</span><span class="sxs-lookup"><span data-stu-id="29849-112">The [ICLRDomainManager::SetAppDomainManagerType](iclrdomainmanager-setappdomainmanagertype-method.md) method takes a parameter of type `EInitializeNewDomainFlags`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="29849-113">要求</span><span class="sxs-lookup"><span data-stu-id="29849-113">Requirements</span></span>  

 <span data-ttu-id="29849-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="29849-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="29849-115">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="29849-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="29849-116">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="29849-116">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="29849-117">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="29849-117">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="29849-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="29849-118">See also</span></span>

- [<span data-ttu-id="29849-119">承载枚举</span><span class="sxs-lookup"><span data-stu-id="29849-119">Hosting Enumerations</span></span>](hosting-enumerations.md)
- [<span data-ttu-id="29849-120">SetAppDomainManagerType 方法</span><span class="sxs-lookup"><span data-stu-id="29849-120">SetAppDomainManagerType Method</span></span>](iclrdomainmanager-setappdomainmanagertype-method.md)
