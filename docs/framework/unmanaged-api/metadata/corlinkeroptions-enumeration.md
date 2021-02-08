---
description: 了解详细信息： CorLinkerOptions 枚举
title: CorLinkerOptions 枚举
ms.date: 03/30/2017
api_name:
- CorLinkerOptions
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorLinkerOptions
helpviewer_keywords:
- CorLinkerOptions enumeration [.NET Framework metadata]
ms.assetid: a656aad6-cc7e-4994-8251-004a6a45e18f
topic_type:
- apiref
ms.openlocfilehash: 40f8ba6382fc937a072e01f9b3f6f89056f628db
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784426"
---
# <a name="corlinkeroptions-enumeration"></a><span data-ttu-id="68819-103">CorLinkerOptions 枚举</span><span class="sxs-lookup"><span data-stu-id="68819-103">CorLinkerOptions Enumeration</span></span>

<span data-ttu-id="68819-104">指定用于选择元数据链接器的选项的标志。</span><span class="sxs-lookup"><span data-stu-id="68819-104">Specifies flags to select options for the metadata linker.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="68819-105">语法</span><span class="sxs-lookup"><span data-stu-id="68819-105">Syntax</span></span>  
  
```cpp  
typedef enum CorLinkerOptions {  
    MDAssembly          = 0x00000000,  
    MDNetModule         = 0x00000001,  
} CorLinkerOptions;  
```  
  
## <a name="members"></a><span data-ttu-id="68819-106">成员</span><span class="sxs-lookup"><span data-stu-id="68819-106">Members</span></span>  
  
|<span data-ttu-id="68819-107">成员</span><span class="sxs-lookup"><span data-stu-id="68819-107">Member</span></span>|<span data-ttu-id="68819-108">说明</span><span class="sxs-lookup"><span data-stu-id="68819-108">Description</span></span>|  
|------------|-----------------|  
|`MDAssembly`|<span data-ttu-id="68819-109">不保留私有类型和全局函数。</span><span class="sxs-lookup"><span data-stu-id="68819-109">The private types and global functions are not preserved.</span></span>|  
|`MDNetModule`|<span data-ttu-id="68819-110">私有类型和全局函数会被保留。</span><span class="sxs-lookup"><span data-stu-id="68819-110">The private types and global functions are preserved.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="68819-111">要求</span><span class="sxs-lookup"><span data-stu-id="68819-111">Requirements</span></span>  

 <span data-ttu-id="68819-112">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="68819-112">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="68819-113">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="68819-113">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="68819-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="68819-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="68819-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="68819-115">See also</span></span>

- [<span data-ttu-id="68819-116">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="68819-116">Metadata Enumerations</span></span>](metadata-enumerations.md)
