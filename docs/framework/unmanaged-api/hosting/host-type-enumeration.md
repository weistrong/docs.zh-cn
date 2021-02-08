---
description: 了解详细信息： HOST_TYPE 枚举
title: HOST_TYPE 枚举
ms.date: 03/30/2017
api_name:
- HOST_TYPE
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- HOST_TYPE
helpviewer_keywords:
- HOST_TYPE enumeration [.NET Framework hosting]
ms.assetid: 51f848be-84c5-4036-9839-c762c576bbf5
topic_type:
- apiref
ms.openlocfilehash: 6a0baf3050f99885953ddec06342cbe19accfef3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785232"
---
# <a name="host_type-enumeration"></a><span data-ttu-id="acbec-103">HOST_TYPE 枚举</span><span class="sxs-lookup"><span data-stu-id="acbec-103">HOST_TYPE Enumeration</span></span>

<span data-ttu-id="acbec-104">包含的值用于指定启动应用程序的主机的类型。</span><span class="sxs-lookup"><span data-stu-id="acbec-104">Contains values that specify the type of host that is launching an application.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="acbec-105">语法</span><span class="sxs-lookup"><span data-stu-id="acbec-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    HOST_TYPE_DEFAULT     = 0x0,  
    HOST_TYPE_APPLAUNCH   = 0x1,  
    HOST_TYPE_CORFLAG     = 0x2  
} HOST_TYPE;  
```  
  
## <a name="members"></a><span data-ttu-id="acbec-106">成员</span><span class="sxs-lookup"><span data-stu-id="acbec-106">Members</span></span>  
  
|<span data-ttu-id="acbec-107">成员</span><span class="sxs-lookup"><span data-stu-id="acbec-107">Member</span></span>|<span data-ttu-id="acbec-108">说明</span><span class="sxs-lookup"><span data-stu-id="acbec-108">Description</span></span>|  
|------------|-----------------|  
|`HOST_TYPE_APPLAUNCH`|<span data-ttu-id="acbec-109">启动 AppLaunch.exe 的应用程序。</span><span class="sxs-lookup"><span data-stu-id="acbec-109">Launch the application from AppLaunch.exe.</span></span><br /><br /> <span data-ttu-id="acbec-110">将此值用于部分受信任的应用程序。</span><span class="sxs-lookup"><span data-stu-id="acbec-110">Use this value for partially-trusted applications.</span></span>|  
|`HOST_TYPE_CORFLAG`|<span data-ttu-id="acbec-111">直接启动该应用程序。</span><span class="sxs-lookup"><span data-stu-id="acbec-111">Launch the application directly.</span></span> <span data-ttu-id="acbec-112">也就是说，从它自己的 .exe 文件启动该应用程序。</span><span class="sxs-lookup"><span data-stu-id="acbec-112">That is, launch the application from its own .exe file.</span></span><br /><br /> <span data-ttu-id="acbec-113">将此值用于完全受信任的应用程序。</span><span class="sxs-lookup"><span data-stu-id="acbec-113">Use this value for fully-trusted applications.</span></span>|  
|`HOST_TYPE_DEFAULT`|<span data-ttu-id="acbec-114">与 HOST_TYPE_APPLAUNCH 相同。</span><span class="sxs-lookup"><span data-stu-id="acbec-114">Same as HOST_TYPE_APPLAUNCH.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="acbec-115">要求</span><span class="sxs-lookup"><span data-stu-id="acbec-115">Requirements</span></span>  

 <span data-ttu-id="acbec-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="acbec-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="acbec-117">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="acbec-117">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="acbec-118">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="acbec-118">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="acbec-119">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="acbec-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="acbec-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="acbec-120">See also</span></span>

- [<span data-ttu-id="acbec-121">承载枚举</span><span class="sxs-lookup"><span data-stu-id="acbec-121">Hosting Enumerations</span></span>](hosting-enumerations.md)
