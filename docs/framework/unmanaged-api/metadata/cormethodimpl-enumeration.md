---
description: 了解详细信息： CorMethodImpl 枚举
title: CorMethodImpl 枚举
ms.date: 03/30/2017
api_name:
- CorMethodImpl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorMethodImpl
helpviewer_keywords:
- CorMethodImpl enumeration [.NET Framework metadata]
ms.assetid: ffbb3caf-20da-4a4b-8983-77376e72b990
topic_type:
- apiref
ms.openlocfilehash: 157db81a72742f1f2aae7e95249b819b2396ef4b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784387"
---
# <a name="cormethodimpl-enumeration"></a><span data-ttu-id="f3f81-103">CorMethodImpl 枚举</span><span class="sxs-lookup"><span data-stu-id="f3f81-103">CorMethodImpl Enumeration</span></span>

<span data-ttu-id="f3f81-104">包含一些值，用于描述方法实现功能。</span><span class="sxs-lookup"><span data-stu-id="f3f81-104">Contains values that describe method implementation features.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f3f81-105">语法</span><span class="sxs-lookup"><span data-stu-id="f3f81-105">Syntax</span></span>  
  
```cpp  
typedef enum CorMethodImpl {  
  
    miCodeTypeMask      =   0x0003,  
    miIL                =   0x0000,  
    miNative            =   0x0001,  
    miOPTIL             =   0x0002,  
    miRuntime           =   0x0003,  
  
    miManagedMask       =   0x0004,  
    miUnmanaged         =   0x0004,  
    miManaged           =   0x0000,  
  
    miForwardRef        =   0x0010,  
    miPreserveSig       =   0x0080,  
  
    miInternalCall      =   0x1000,  
    miSynchronized      =   0x0020,  
    miNoInlining        =   0x0008,  
    miAggressiveInlining =  0x0100,  
    miNoOptimization     =  0x0040,  
    miMaxMethodImplVal  =   0xffff  
  
} CorMethodImpl;  
```  
  
## <a name="members"></a><span data-ttu-id="f3f81-106">成员</span><span class="sxs-lookup"><span data-stu-id="f3f81-106">Members</span></span>  
  
|<span data-ttu-id="f3f81-107">成员</span><span class="sxs-lookup"><span data-stu-id="f3f81-107">Member</span></span>|<span data-ttu-id="f3f81-108">说明</span><span class="sxs-lookup"><span data-stu-id="f3f81-108">Description</span></span>|  
|------------|-----------------|  
|`miCodeTypeMask`|<span data-ttu-id="f3f81-109">描述代码类型的标志。</span><span class="sxs-lookup"><span data-stu-id="f3f81-109">Flags that describe code type.</span></span>|  
|`miIL`|<span data-ttu-id="f3f81-110">指定方法实现为 Microsoft 中间语言 (MSIL) 。</span><span class="sxs-lookup"><span data-stu-id="f3f81-110">Specifies that the method implementation is Microsoft intermediate language (MSIL).</span></span>|  
|`miNative`|<span data-ttu-id="f3f81-111">指定方法实现为本机。</span><span class="sxs-lookup"><span data-stu-id="f3f81-111">Specifies that the method implementation is native.</span></span>|  
|`miOPTIL`|<span data-ttu-id="f3f81-112">指定方法实现为 OPTIL。</span><span class="sxs-lookup"><span data-stu-id="f3f81-112">Specifies that the method implementation is OPTIL.</span></span>|  
|`miRuntime`|<span data-ttu-id="f3f81-113">指定方法实现由公共语言运行时提供。</span><span class="sxs-lookup"><span data-stu-id="f3f81-113">Specifies that the method implementation is provided by the common language runtime.</span></span>|  
|`miManagedMask`|<span data-ttu-id="f3f81-114">指示代码是托管代码还是非托管代码的标志。</span><span class="sxs-lookup"><span data-stu-id="f3f81-114">Flags that indicate whether the code is managed or unmanaged.</span></span>|  
|`miUnmanaged`|<span data-ttu-id="f3f81-115">指定方法实现是不受管理的。</span><span class="sxs-lookup"><span data-stu-id="f3f81-115">Specifies that the method implementation is unmanaged.</span></span>|  
|`miManaged`|<span data-ttu-id="f3f81-116">指定方法实现是托管的。</span><span class="sxs-lookup"><span data-stu-id="f3f81-116">Specifies that the method implementation is managed.</span></span>|  
|`miForwardRef`|<span data-ttu-id="f3f81-117">指定定义方法。</span><span class="sxs-lookup"><span data-stu-id="f3f81-117">Specifies that the method is defined.</span></span> <span data-ttu-id="f3f81-118">此标志主要用于合并方案。</span><span class="sxs-lookup"><span data-stu-id="f3f81-118">This flag is used primarily in merge scenarios.</span></span>|  
|`miPreserveSig`|<span data-ttu-id="f3f81-119">指定方法签名不能用于 HRESULT 转换。</span><span class="sxs-lookup"><span data-stu-id="f3f81-119">Specifies that the method signature cannot be mangled for an HRESULT conversion.</span></span>|  
|`miInternalCall`|<span data-ttu-id="f3f81-120">保留供公共语言运行时内部使用。</span><span class="sxs-lookup"><span data-stu-id="f3f81-120">Reserved for internal use by the common language runtime.</span></span>|  
|`miSynchronized`|<span data-ttu-id="f3f81-121">指定方法是通过其主体单线程的。</span><span class="sxs-lookup"><span data-stu-id="f3f81-121">Specifies that the method is single-threaded through its body.</span></span>|  
|`miNoInlining`|<span data-ttu-id="f3f81-122">指定方法不能内联。</span><span class="sxs-lookup"><span data-stu-id="f3f81-122">Specifies that the method cannot be inlined.</span></span>|  
|`miAggressiveInlining`|<span data-ttu-id="f3f81-123">指定方法应尽可能内联。</span><span class="sxs-lookup"><span data-stu-id="f3f81-123">Specifies that the method should be inlined if possible.</span></span>|  
|`miNoOptimization`|<span data-ttu-id="f3f81-124">指定不应优化方法。</span><span class="sxs-lookup"><span data-stu-id="f3f81-124">Specifies that the method should not be optimized.</span></span>|  
|`miMaxMethodImplVal`|<span data-ttu-id="f3f81-125">的最大有效值 `CorMethodImpl` 。</span><span class="sxs-lookup"><span data-stu-id="f3f81-125">The maximum valid value for a `CorMethodImpl`.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f3f81-126">要求</span><span class="sxs-lookup"><span data-stu-id="f3f81-126">Requirements</span></span>  

 <span data-ttu-id="f3f81-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f3f81-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f3f81-128">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="f3f81-128">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="f3f81-129">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f3f81-129">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f3f81-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="f3f81-130">See also</span></span>

- [<span data-ttu-id="f3f81-131">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="f3f81-131">Metadata Enumerations</span></span>](metadata-enumerations.md)
