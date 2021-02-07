---
description: 了解详细信息： CeeSectionRelocExtra 联合
title: CeeSectionRelocExtra 联合
ms.date: 03/30/2017
api_name:
- CeeSectionRelocExtra Union
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CeeSectionRelocExtra
helpviewer_keywords:
- CeeSectionRelocExtra union [.NET Framework metadata]
ms.assetid: d9568cf6-7f98-4cd6-ab36-0a2bd509afcc
topic_type:
- apiref
ms.openlocfilehash: 40001c1a0772e24633f4232da8e7817f3747f8ea
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678843"
---
# <a name="ceesectionrelocextra-union"></a><span data-ttu-id="7b54b-103">CeeSectionRelocExtra 联合</span><span class="sxs-lookup"><span data-stu-id="7b54b-103">CeeSectionRelocExtra Union</span></span>

<span data-ttu-id="7b54b-104">表示 [ICeeGen](iceegen-interface.md) 接口用于重定位节的地址偏移量。</span><span class="sxs-lookup"><span data-stu-id="7b54b-104">Represents an address offset that is used by the [ICeeGen](iceegen-interface.md) interface to relocate a section.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7b54b-105">语法</span><span class="sxs-lookup"><span data-stu-id="7b54b-105">Syntax</span></span>  
  
```cpp  
typedef union  {  
    USHORT highAdj;  
} CeeSectionRelocExtra;  
```  
  
## <a name="members"></a><span data-ttu-id="7b54b-106">成员</span><span class="sxs-lookup"><span data-stu-id="7b54b-106">Members</span></span>  
  
|<span data-ttu-id="7b54b-107">成员</span><span class="sxs-lookup"><span data-stu-id="7b54b-107">Member</span></span>|<span data-ttu-id="7b54b-108">说明</span><span class="sxs-lookup"><span data-stu-id="7b54b-108">Description</span></span>|  
|------------|-----------------|  
|`highAdj`|<span data-ttu-id="7b54b-109">部分的大小上限。</span><span class="sxs-lookup"><span data-stu-id="7b54b-109">The upper address adjustment for the section.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="7b54b-110">要求</span><span class="sxs-lookup"><span data-stu-id="7b54b-110">Requirements</span></span>  

 <span data-ttu-id="7b54b-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="7b54b-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7b54b-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="7b54b-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="7b54b-113">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7b54b-113">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="7b54b-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7b54b-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7b54b-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="7b54b-115">See also</span></span>

- [<span data-ttu-id="7b54b-116">元数据联合</span><span class="sxs-lookup"><span data-stu-id="7b54b-116">Metadata Unions</span></span>](metadata-unions.md)
