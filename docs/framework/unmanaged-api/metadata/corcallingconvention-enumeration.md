---
description: 了解详细信息： CorCallingConvention 枚举
title: CorCallingConvention 枚举
ms.date: 03/30/2017
api_name:
- CorCallingConvention
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorCallingConvention
helpviewer_keywords:
- CorCallingConvention enumeration [.NET Framework metadata]
ms.assetid: 69156fbf-7219-43bf-b4b8-b13f1a2fcb86
topic_type:
- apiref
ms.openlocfilehash: 2e823fe3566ef7a54f759cd5debbbd7d5dcf3ceb
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678436"
---
# <a name="corcallingconvention-enumeration"></a><span data-ttu-id="f9cd8-103">CorCallingConvention 枚举</span><span class="sxs-lookup"><span data-stu-id="f9cd8-103">CorCallingConvention Enumeration</span></span>

<span data-ttu-id="f9cd8-104">包含一些值，用于描述托管代码中执行的调用约定类型。</span><span class="sxs-lookup"><span data-stu-id="f9cd8-104">Contains values that describe the types of calling conventions that are made in managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f9cd8-105">语法</span><span class="sxs-lookup"><span data-stu-id="f9cd8-105">Syntax</span></span>  
  
```cpp  
typedef enum CorCallingConvention  
{  
    IMAGE_CEE_CS_CALLCONV_DEFAULT       = 0x0,  
  
    IMAGE_CEE_CS_CALLCONV_VARARG        = 0x5,  
    IMAGE_CEE_CS_CALLCONV_FIELD         = 0x6,  
    IMAGE_CEE_CS_CALLCONV_LOCAL_SIG     = 0x7,  
    IMAGE_CEE_CS_CALLCONV_PROPERTY      = 0x8,  
    IMAGE_CEE_CS_CALLCONV_UNMGD         = 0x9,  
    IMAGE_CEE_CS_CALLCONV_GENERICINST   = 0xa,  
    IMAGE_CEE_CS_CALLCONV_NATIVEVARARG  = 0xb,  
    IMAGE_CEE_CS_CALLCONV_MAX           = 0xc,  
  
    IMAGE_CEE_CS_CALLCONV_MASK          = 0x0f,  
    IMAGE_CEE_CS_CALLCONV_HASTHIS       = 0x20,  
    IMAGE_CEE_CS_CALLCONV_EXPLICITTHIS  = 0x40,  
    IMAGE_CEE_CS_CALLCONV_GENERIC       = 0x10  
  
} CorCallingConvention;  
```  
  
## <a name="members"></a><span data-ttu-id="f9cd8-106">成员</span><span class="sxs-lookup"><span data-stu-id="f9cd8-106">Members</span></span>  
  
|<span data-ttu-id="f9cd8-107">成员</span><span class="sxs-lookup"><span data-stu-id="f9cd8-107">Member</span></span>|<span data-ttu-id="f9cd8-108">说明</span><span class="sxs-lookup"><span data-stu-id="f9cd8-108">Description</span></span>|  
|------------|-----------------|  
|`IMAGE_CEE_CS_CALLCONV_DEFAULT`|<span data-ttu-id="f9cd8-109">指示默认调用约定。</span><span class="sxs-lookup"><span data-stu-id="f9cd8-109">Indicates a default calling convention.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_VARARG`|<span data-ttu-id="f9cd8-110">指示该方法采用可变数量的参数。</span><span class="sxs-lookup"><span data-stu-id="f9cd8-110">Indicates that the method takes a variable number of parameters.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_FIELD`|<span data-ttu-id="f9cd8-111">指示调用为字段。</span><span class="sxs-lookup"><span data-stu-id="f9cd8-111">Indicates that the call is to a field.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_LOCAL_SIG`|<span data-ttu-id="f9cd8-112">指示调用为本地方法。</span><span class="sxs-lookup"><span data-stu-id="f9cd8-112">Indicates that the call is to a local method.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_PROPERTY`|<span data-ttu-id="f9cd8-113">指示对属性的调用。</span><span class="sxs-lookup"><span data-stu-id="f9cd8-113">Indicates that the call is to a property.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_UNMGD`|<span data-ttu-id="f9cd8-114">指示调用是非托管的。</span><span class="sxs-lookup"><span data-stu-id="f9cd8-114">Indicates that the call is unmanaged.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_GENERICINST`|<span data-ttu-id="f9cd8-115">指示泛型方法的实例化。</span><span class="sxs-lookup"><span data-stu-id="f9cd8-115">Indicates a generic method instantiation.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_NATIVEVARARG`|<span data-ttu-id="f9cd8-116">指示对采用可变数目的参数的方法进行64位 PInvoke 调用。</span><span class="sxs-lookup"><span data-stu-id="f9cd8-116">Indicates a 64-bit PInvoke call to a method that takes a variable number of parameters.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_MAX`|<span data-ttu-id="f9cd8-117">描述无效的4位值。</span><span class="sxs-lookup"><span data-stu-id="f9cd8-117">Describes an invalid 4-bit value.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_MASK`|<span data-ttu-id="f9cd8-118">指示调用约定由四位底部描述。</span><span class="sxs-lookup"><span data-stu-id="f9cd8-118">Indicates that the calling convention is described by the bottom four bits.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_HASTHIS`|<span data-ttu-id="f9cd8-119">指示上位描述了一个 `this` 参数。</span><span class="sxs-lookup"><span data-stu-id="f9cd8-119">Indicates that the top bit describes a `this` parameter.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_EXPLICITTHIS`|<span data-ttu-id="f9cd8-120">指示 `this` 签名中显式描述了一个参数。</span><span class="sxs-lookup"><span data-stu-id="f9cd8-120">Indicates that a `this` parameter is explicitly described in the signature.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_GENERIC`|<span data-ttu-id="f9cd8-121">指示包含类型参数的显式数目的泛型方法签名。</span><span class="sxs-lookup"><span data-stu-id="f9cd8-121">Indicates a generic method signature with an explicit number of type arguments.</span></span> <span data-ttu-id="f9cd8-122">这优先于普通参数计数。</span><span class="sxs-lookup"><span data-stu-id="f9cd8-122">This precedes an ordinary parameter count.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f9cd8-123">要求</span><span class="sxs-lookup"><span data-stu-id="f9cd8-123">Requirements</span></span>  

 <span data-ttu-id="f9cd8-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f9cd8-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f9cd8-125">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="f9cd8-125">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="f9cd8-126">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f9cd8-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f9cd8-127">请参阅</span><span class="sxs-lookup"><span data-stu-id="f9cd8-127">See also</span></span>

- [<span data-ttu-id="f9cd8-128">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="f9cd8-128">Metadata Enumerations</span></span>](metadata-enumerations.md)
