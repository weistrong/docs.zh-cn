---
description: 了解详细信息： COR_NATIVE_LINK 结构
title: COR_NATIVE_LINK 结构
ms.date: 03/30/2017
api_name:
- COR_NATIVE_LINK
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- COR_NATIVE_LINK
helpviewer_keywords:
- COR_NATIVE_LINK structure [.NET Framework metadata]
ms.assetid: 6ef78d3c-1c69-4141-b687-dcb065b7a74d
topic_type:
- apiref
ms.openlocfilehash: 09c715af698a0614fd4a9a17679df6908a1497a6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678570"
---
# <a name="cor_native_link-structure"></a><span data-ttu-id="b1f56-103">COR_NATIVE_LINK 结构</span><span class="sxs-lookup"><span data-stu-id="b1f56-103">COR_NATIVE_LINK Structure</span></span>

<span data-ttu-id="b1f56-104">包含用于链接本机代码的信息。</span><span class="sxs-lookup"><span data-stu-id="b1f56-104">Contains information that is used to link native code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b1f56-105">语法</span><span class="sxs-lookup"><span data-stu-id="b1f56-105">Syntax</span></span>  
  
```cpp  
typedef struct
{  
    BYTE        m_linkType;  
    BYTE        m_flags;  
    mdMemberRef m_entryPoint;  
} COR_NATIVE_LINK;  
```  
  
## <a name="members"></a><span data-ttu-id="b1f56-106">成员</span><span class="sxs-lookup"><span data-stu-id="b1f56-106">Members</span></span>  
  
|<span data-ttu-id="b1f56-107">成员</span><span class="sxs-lookup"><span data-stu-id="b1f56-107">Member</span></span>|<span data-ttu-id="b1f56-108">说明</span><span class="sxs-lookup"><span data-stu-id="b1f56-108">Description</span></span>|  
|------------|-----------------|  
|`m_linkType`|<span data-ttu-id="b1f56-109">要在本机代码中链接的类型。</span><span class="sxs-lookup"><span data-stu-id="b1f56-109">The type to be linked in native code.</span></span> <span data-ttu-id="b1f56-110">此值为 [CorNativeLinkType](cornativelinktype-enumeration.md) 值之一。</span><span class="sxs-lookup"><span data-stu-id="b1f56-110">This value is one of the [CorNativeLinkType](cornativelinktype-enumeration.md) values.</span></span>|  
|`m_flags`|<span data-ttu-id="b1f56-111">链接本机代码时链接器使用的标志。</span><span class="sxs-lookup"><span data-stu-id="b1f56-111">Flags used by the linker when linking native code.</span></span> <span data-ttu-id="b1f56-112">此值为 [CorNativeLinkFlags](cornativelinkflags-enumeration.md) 值之一。</span><span class="sxs-lookup"><span data-stu-id="b1f56-112">This value is one of the [CorNativeLinkFlags](cornativelinkflags-enumeration.md) values.</span></span>|  
|`m_entryPoint`|<span data-ttu-id="b1f56-113">表示入口点的 MemberRef 元数据标记。</span><span class="sxs-lookup"><span data-stu-id="b1f56-113">The MemberRef metadata token that represents the entry point.</span></span> <span data-ttu-id="b1f56-114">格式为 `lib:entrypoint`。</span><span class="sxs-lookup"><span data-stu-id="b1f56-114">The format is `lib:entrypoint`.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b1f56-115">要求</span><span class="sxs-lookup"><span data-stu-id="b1f56-115">Requirements</span></span>  

 <span data-ttu-id="b1f56-116">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b1f56-116">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b1f56-117">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="b1f56-117">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="b1f56-118">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="b1f56-118">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="b1f56-119">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b1f56-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b1f56-120">请参阅</span><span class="sxs-lookup"><span data-stu-id="b1f56-120">See also</span></span>

- [<span data-ttu-id="b1f56-121">元数据结构</span><span class="sxs-lookup"><span data-stu-id="b1f56-121">Metadata Structures</span></span>](metadata-structures.md)
- [<span data-ttu-id="b1f56-122">CorNativeLinkType 枚举</span><span class="sxs-lookup"><span data-stu-id="b1f56-122">CorNativeLinkType Enumeration</span></span>](cornativelinktype-enumeration.md)
- [<span data-ttu-id="b1f56-123">CorNativeLinkFlags 枚举</span><span class="sxs-lookup"><span data-stu-id="b1f56-123">CorNativeLinkFlags Enumeration</span></span>](cornativelinkflags-enumeration.md)
