---
description: 了解详细信息： CorAttributeTargets 枚举
title: CorAttributeTargets 枚举
ms.date: 03/30/2017
api_name:
- CorAttributeTargets
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorAttributeTargets
helpviewer_keywords:
- CorAttributeTargets enumeration [.NET Framework metadata]
ms.assetid: 694c0fa0-7011-41a9-9dfd-f0e16ea574b5
topic_type:
- apiref
ms.openlocfilehash: 6f80df31b9da8591fac3d979ede1e9bf0f8ecfc4
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678483"
---
# <a name="corattributetargets-enumeration"></a><span data-ttu-id="946a3-103">CorAttributeTargets 枚举</span><span class="sxs-lookup"><span data-stu-id="946a3-103">CorAttributeTargets Enumeration</span></span>

<span data-ttu-id="946a3-104">指定可应用属性的应用程序元素。</span><span class="sxs-lookup"><span data-stu-id="946a3-104">Specifies the application elements on which it is valid to apply an attribute.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="946a3-105">语法</span><span class="sxs-lookup"><span data-stu-id="946a3-105">Syntax</span></span>  
  
```cpp  
typedef enum CorAttributeTargets  
{  
    catAssembly            = 0x0001,  
    catModule              = 0x0002,  
    catClass               = 0x0004,  
    catStruct              = 0x0008,  
    catEnum                = 0x0010,  
    catConstructor         = 0x0020,  
    catMethod              = 0x0040,  
    catProperty            = 0x0080,  
    catField               = 0x0100,  
    catEvent               = 0x0200,  
    catInterface           = 0x0400,  
    catParameter           = 0x0800,  
    catDelegate            = 0x1000,  
    catGenericParameter    = 0x4000,  
  
    catAll                 =
        catAssembly | catModule | catClass | catStruct |
        catEnum | catConstructor | catMethod | catProperty |
        catField | catEvent | catInterface | catParameter |
        catDelegate | catGenericParameter,  
  
    catClassMembers        =
        catClass | catStruct | catEnum | catConstructor |
        catMethod | catProperty | catField | catEvent |
        catDelegate | catInterface  
  
} CorAttributeTargets;  
```  
  
## <a name="members"></a><span data-ttu-id="946a3-106">成员</span><span class="sxs-lookup"><span data-stu-id="946a3-106">Members</span></span>  
  
|<span data-ttu-id="946a3-107">成员</span><span class="sxs-lookup"><span data-stu-id="946a3-107">Member</span></span>|<span data-ttu-id="946a3-108">说明</span><span class="sxs-lookup"><span data-stu-id="946a3-108">Description</span></span>|  
|------------|-----------------|  
|`catAssembly`|<span data-ttu-id="946a3-109">可以对程序集应用属性。</span><span class="sxs-lookup"><span data-stu-id="946a3-109">Attribute can be applied to an assembly.</span></span>|  
|`catModule`|<span data-ttu-id="946a3-110">特性可应用到可移植的可执行文件 ( .dll 或 .exe) 模块。</span><span class="sxs-lookup"><span data-stu-id="946a3-110">Attribute can be applied to a portable executable (.dll or .exe) module.</span></span>|  
|`catClass`|<span data-ttu-id="946a3-111">可以对类应用属性。</span><span class="sxs-lookup"><span data-stu-id="946a3-111">Attribute can be applied to a class.</span></span>|  
|`catStruct`|<span data-ttu-id="946a3-112">可以对结构应用属性，即值类型。</span><span class="sxs-lookup"><span data-stu-id="946a3-112">Attribute can be applied to a structure; that is, a value type.</span></span>|  
|`catEnum`|<span data-ttu-id="946a3-113">可以对枚举应用属性。</span><span class="sxs-lookup"><span data-stu-id="946a3-113">Attribute can be applied to an enumeration.</span></span>|  
|`catConstructor`|<span data-ttu-id="946a3-114">可以对构造函数应用属性。</span><span class="sxs-lookup"><span data-stu-id="946a3-114">Attribute can be applied to a constructor.</span></span>|  
|`catMethod`|<span data-ttu-id="946a3-115">可以对方法应用属性。</span><span class="sxs-lookup"><span data-stu-id="946a3-115">Attribute can be applied to a method.</span></span>|  
|`catProperty`|<span data-ttu-id="946a3-116">可以对属性 (Property) 应用属性 (Attribute)。</span><span class="sxs-lookup"><span data-stu-id="946a3-116">Attribute can be applied to a property.</span></span>|  
|`catField`|<span data-ttu-id="946a3-117">可以对字段应用属性。</span><span class="sxs-lookup"><span data-stu-id="946a3-117">Attribute can be applied to a field.</span></span>|  
|`catEvent`|<span data-ttu-id="946a3-118">可以对事件应用属性。</span><span class="sxs-lookup"><span data-stu-id="946a3-118">Attribute can be applied to an event.</span></span>|  
|`catInterface`|<span data-ttu-id="946a3-119">可以对接口应用属性。</span><span class="sxs-lookup"><span data-stu-id="946a3-119">Attribute can be applied to an interface.</span></span>|  
|`catParameter`|<span data-ttu-id="946a3-120">可以对参数应用属性。</span><span class="sxs-lookup"><span data-stu-id="946a3-120">Attribute can be applied to a parameter.</span></span>|  
|`catDelegate`|<span data-ttu-id="946a3-121">可以对委托应用属性。</span><span class="sxs-lookup"><span data-stu-id="946a3-121">Attribute can be applied to a delegate.</span></span>|  
|`catGenericParameter`|<span data-ttu-id="946a3-122">可以对泛型参数应用属性。</span><span class="sxs-lookup"><span data-stu-id="946a3-122">Attribute can be applied to a generic parameter.</span></span>|  
|`catAll`|<span data-ttu-id="946a3-123">可以对任何应用程序元素应用属性。</span><span class="sxs-lookup"><span data-stu-id="946a3-123">Attribute can be applied to any application element.</span></span>|  
|`catClassMembers`|<span data-ttu-id="946a3-124">特性可应用于类的成员。</span><span class="sxs-lookup"><span data-stu-id="946a3-124">Attribute can be applied to a member of a class.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="946a3-125">备注</span><span class="sxs-lookup"><span data-stu-id="946a3-125">Remarks</span></span>  

 <span data-ttu-id="946a3-126">`CorAttributeTargets`枚举值可以与按位 "或" 运算组合在一起，以获取首选组合。</span><span class="sxs-lookup"><span data-stu-id="946a3-126">The `CorAttributeTargets` enumeration values can be combined with a bitwise OR operation to get the preferred combination.</span></span>  
  
 <span data-ttu-id="946a3-127">等效 `CorAttributeTargets` 托管 <xref:System.AttributeTargets?displayProperty=nameWithType> 枚举。</span><span class="sxs-lookup"><span data-stu-id="946a3-127">The `CorAttributeTargets` parallels the managed <xref:System.AttributeTargets?displayProperty=nameWithType> enumeration.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="946a3-128">要求</span><span class="sxs-lookup"><span data-stu-id="946a3-128">Requirements</span></span>  

 <span data-ttu-id="946a3-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="946a3-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="946a3-130">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="946a3-130">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="946a3-131">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="946a3-131">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="946a3-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="946a3-132">See also</span></span>

- [<span data-ttu-id="946a3-133">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="946a3-133">Metadata Enumerations</span></span>](metadata-enumerations.md)
