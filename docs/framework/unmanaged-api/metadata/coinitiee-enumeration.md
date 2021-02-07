---
description: 了解详细信息： COINITIEE 枚举
title: COINITIEE 枚举
ms.date: 03/30/2017
api_name:
- COINITIEE
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- COINITIEE
helpviewer_keywords:
- COINITIEE enumeration [.NET Framework metadata]
ms.assetid: 64264238-3b68-4bac-a887-36b552426a6c
topic_type:
- apiref
ms.openlocfilehash: c17980582903a29cdfe33c64200c31f29ddeb17c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678583"
---
# <a name="coinitiee-enumeration"></a><span data-ttu-id="210c8-103">COINITIEE 枚举</span><span class="sxs-lookup"><span data-stu-id="210c8-103">COINITIEE Enumeration</span></span>

<span data-ttu-id="210c8-104">指定初始化公共语言运行时 [CoInitializeEE](../hosting/coinitializeee-function.md) 使用的常量。</span><span class="sxs-lookup"><span data-stu-id="210c8-104">Specifies constants used by [CoInitializeEE](../hosting/coinitializeee-function.md) when initializing the common language runtime.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="210c8-105">语法</span><span class="sxs-lookup"><span data-stu-id="210c8-105">Syntax</span></span>  
  
```cpp  
typedef enum tagCOINITEE {  
   COINITEE_DEFAULT = 0x0,  
   COINITEE_DLL     = 0x1,  
   COINITEE_MAIN    = 0x2  
} COINITIEE;  
```  
  
## <a name="members"></a><span data-ttu-id="210c8-106">成员</span><span class="sxs-lookup"><span data-stu-id="210c8-106">Members</span></span>  
  
|<span data-ttu-id="210c8-107">成员</span><span class="sxs-lookup"><span data-stu-id="210c8-107">Member</span></span>|<span data-ttu-id="210c8-108">说明</span><span class="sxs-lookup"><span data-stu-id="210c8-108">Description</span></span>|  
|------------|-----------------|  
|`COINITEE_DEFAULT`|<span data-ttu-id="210c8-109">默认初始化模式。</span><span class="sxs-lookup"><span data-stu-id="210c8-109">Default initialization mode.</span></span> <span data-ttu-id="210c8-110">这将初始化运行时并创建默认值 <xref:System.AppDomain> 。</span><span class="sxs-lookup"><span data-stu-id="210c8-110">This initializes the runtime and creates the default <xref:System.AppDomain>.</span></span>|  
|`COINITEE_DLL`|<span data-ttu-id="210c8-111">初始化以运行托管 DLL。</span><span class="sxs-lookup"><span data-stu-id="210c8-111">Initializes to run a managed DLL.</span></span>|  
|`COINITEE_MAIN`|<span data-ttu-id="210c8-112">初始化以运行托管 EXE。</span><span class="sxs-lookup"><span data-stu-id="210c8-112">Initializes to run a managed EXE.</span></span> <span data-ttu-id="210c8-113">这将初始化运行时，但不会创建默认值 <xref:System.AppDomain> ，该默认值是在输入 EXE 的主例程之后创建的。</span><span class="sxs-lookup"><span data-stu-id="210c8-113">This initializes the runtime but does not create the default <xref:System.AppDomain>, which is created after entering the main routine of the EXE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="210c8-114">要求</span><span class="sxs-lookup"><span data-stu-id="210c8-114">Requirements</span></span>  

 <span data-ttu-id="210c8-115">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="210c8-115">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="210c8-116">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="210c8-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="210c8-117">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="210c8-117">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="210c8-118">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="210c8-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="210c8-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="210c8-119">See also</span></span>

- [<span data-ttu-id="210c8-120">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="210c8-120">Metadata Enumerations</span></span>](metadata-enumerations.md)
