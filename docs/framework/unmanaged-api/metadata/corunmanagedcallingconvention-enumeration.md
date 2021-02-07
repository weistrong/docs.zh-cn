---
description: 了解详细信息： CorUnmanagedCallingConvention 枚举
title: CorUnmanagedCallingConvention 枚举
ms.date: 03/30/2017
api_name:
- CorUnmanagedCallingConvention
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorUnmanagedCallingConvention
helpviewer_keywords:
- CorUnmanagedCallingConvention enumeration [.NET Framework metadata]
ms.assetid: 83058790-160b-4703-a5eb-74b66acbdfa9
topic_type:
- apiref
ms.openlocfilehash: a4b5c70b7dcb4750d641540662941ed3cc08c94b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99707288"
---
# <a name="corunmanagedcallingconvention-enumeration"></a><span data-ttu-id="6bf88-103">CorUnmanagedCallingConvention 枚举</span><span class="sxs-lookup"><span data-stu-id="6bf88-103">CorUnmanagedCallingConvention Enumeration</span></span>

<span data-ttu-id="6bf88-104">指定非托管代码的调用约定。</span><span class="sxs-lookup"><span data-stu-id="6bf88-104">Specifies the calling conventions for unmanaged code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6bf88-105">语法</span><span class="sxs-lookup"><span data-stu-id="6bf88-105">Syntax</span></span>  
  
```cpp  
typedef enum CorUnmanagedCallingConvention {  
  
    IMAGE_CEE_UNMANAGED_CALLCONV_C         = 0x1,  
    IMAGE_CEE_UNMANAGED_CALLCONV_STDCALL   = 0x2,  
    IMAGE_CEE_UNMANAGED_CALLCONV_THISCALL  = 0x3,  
    IMAGE_CEE_UNMANAGED_CALLCONV_FASTCALL  = 0x4,  
  
    IMAGE_CEE_CS_CALLCONV_C                = 0x1,  
    IMAGE_CEE_CS_CALLCONV_STDCALL          = 0x2,  
    IMAGE_CEE_CS_CALLCONV_THISCALL         = 0x3,  
    IMAGE_CEE_CS_CALLCONV_FASTCALL         = 0x4  
  
} CorUnmanagedCallingConvention;  
```  
  
## <a name="members"></a><span data-ttu-id="6bf88-106">成员</span><span class="sxs-lookup"><span data-stu-id="6bf88-106">Members</span></span>  
  
|<span data-ttu-id="6bf88-107">成员</span><span class="sxs-lookup"><span data-stu-id="6bf88-107">Member</span></span>|<span data-ttu-id="6bf88-108">说明</span><span class="sxs-lookup"><span data-stu-id="6bf88-108">Description</span></span>|  
|------------|-----------------|  
|`IMAGE_CEE_UNMANAGED_CALLCONV_C`|<span data-ttu-id="6bf88-109">C 语言调用约定。</span><span class="sxs-lookup"><span data-stu-id="6bf88-109">The C language calling convention.</span></span>|  
|`IMAGE_CEE_UNMANAGED_CALLCONV_STDCALL`|<span data-ttu-id="6bf88-110">标准调用约定。</span><span class="sxs-lookup"><span data-stu-id="6bf88-110">The standard calling convention.</span></span>|  
|`IMAGE_CEE_UNMANAGED_CALLCONV_THISCALL`|<span data-ttu-id="6bf88-111">"This" 调用约定。</span><span class="sxs-lookup"><span data-stu-id="6bf88-111">The "this" calling convention.</span></span>|  
|`IMAGE_CEE_UNMANAGED_CALLCONV_FASTCALL`|<span data-ttu-id="6bf88-112">"Fast" 调用约定。</span><span class="sxs-lookup"><span data-stu-id="6bf88-112">The "fast" calling convention.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_C`|<span data-ttu-id="6bf88-113">未使用。</span><span class="sxs-lookup"><span data-stu-id="6bf88-113">Not used.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_STDCALL`|<span data-ttu-id="6bf88-114">未使用。</span><span class="sxs-lookup"><span data-stu-id="6bf88-114">Not used.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_THISCALL`|<span data-ttu-id="6bf88-115">未使用。</span><span class="sxs-lookup"><span data-stu-id="6bf88-115">Not used.</span></span>|  
|`IMAGE_CEE_CS_CALLCONV_FASTCALL`|<span data-ttu-id="6bf88-116">未使用。</span><span class="sxs-lookup"><span data-stu-id="6bf88-116">Not used.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6bf88-117">备注</span><span class="sxs-lookup"><span data-stu-id="6bf88-117">Remarks</span></span>  

 <span data-ttu-id="6bf88-118">CLR 不支持 .NET Framework 版本1.0 中的 "fast" 调用约定。</span><span class="sxs-lookup"><span data-stu-id="6bf88-118">The CLR does not support the "fast" calling convention in the .NET Framework version 1.0.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="6bf88-119">要求</span><span class="sxs-lookup"><span data-stu-id="6bf88-119">Requirements</span></span>  

 <span data-ttu-id="6bf88-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="6bf88-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="6bf88-121">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="6bf88-121">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="6bf88-122">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="6bf88-122">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6bf88-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="6bf88-123">See also</span></span>

- [<span data-ttu-id="6bf88-124">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="6bf88-124">Metadata Enumerations</span></span>](metadata-enumerations.md)
