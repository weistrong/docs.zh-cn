---
description: 了解详细信息： CorMethodAttr 枚举
title: CorMethodAttr 枚举
ms.date: 03/30/2017
api_name:
- CorMethodAttr
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorMethodAttr
helpviewer_keywords:
- CorMethodAttr enumeration [.NET Framework metadata]
ms.assetid: 4e0c3521-e54d-43c1-9857-cc76b49b8ffc
topic_type:
- apiref
ms.openlocfilehash: 4050235675f4b237b184d31378a614a0613ab3df
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99784374"
---
# <a name="cormethodattr-enumeration"></a><span data-ttu-id="ee545-103">CorMethodAttr 枚举</span><span class="sxs-lookup"><span data-stu-id="ee545-103">CorMethodAttr Enumeration</span></span>

<span data-ttu-id="ee545-104">包含描述方法功能的值。</span><span class="sxs-lookup"><span data-stu-id="ee545-104">Contains values that describe the features of a method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ee545-105">语法</span><span class="sxs-lookup"><span data-stu-id="ee545-105">Syntax</span></span>  
  
```cpp  
typedef enum CorMethodAttr {  
  
    mdMemberAccessMask          =   0x0007,  
    mdPrivateScope              =   0x0000,  
    mdPrivate                   =   0x0001,  
    mdFamANDAssem               =   0x0002,  
    mdAssem                     =   0x0003,  
    mdFamily                    =   0x0004,  
    mdFamORAssem                =   0x0005,  
    mdPublic                    =   0x0006,  
  
    mdStatic                    =   0x0010,  
    mdFinal                     =   0x0020,  
    mdVirtual                   =   0x0040,  
    mdHideBySig                 =   0x0080,  
  
    mdVtableLayoutMask          =   0x0100,  
    mdReuseSlot                 =   0x0000,  
    mdNewSlot                   =   0x0100,  
  
    mdCheckAccessOnOverride     =   0x0200,  
    mdAbstract                  =   0x0400,  
    mdSpecialName               =   0x0800,  
  
    mdPinvokeImpl               =   0x2000,  
    mdUnmanagedExport           =   0x0008,  
  
    mdReservedMask              =   0xd000,  
    mdRTSpecialName             =   0x1000,  
    mdHasSecurity               =   0x4000,  
    mdRequireSecObject          =   0x8000,  
  
} CorMethodAttr;  
```  
  
## <a name="members"></a><span data-ttu-id="ee545-106">成员</span><span class="sxs-lookup"><span data-stu-id="ee545-106">Members</span></span>  
  
|<span data-ttu-id="ee545-107">成员</span><span class="sxs-lookup"><span data-stu-id="ee545-107">Member</span></span>|<span data-ttu-id="ee545-108">说明</span><span class="sxs-lookup"><span data-stu-id="ee545-108">Description</span></span>|  
|------------|-----------------|  
|`mdMemberAccessMask`|<span data-ttu-id="ee545-109">指定成员访问。</span><span class="sxs-lookup"><span data-stu-id="ee545-109">Specifies member access.</span></span>|  
|`mdPrivateScope`|<span data-ttu-id="ee545-110">指定不能引用成员。</span><span class="sxs-lookup"><span data-stu-id="ee545-110">Specifies that the member cannot be referenced.</span></span>|  
|`mdPrivate`|<span data-ttu-id="ee545-111">指定只能由父类型访问成员。</span><span class="sxs-lookup"><span data-stu-id="ee545-111">Specifies that the member is accessible only by the parent type.</span></span>|  
|`mdFamANDAssem`|<span data-ttu-id="ee545-112">指定该成员只能由此程序集中的子类型访问。</span><span class="sxs-lookup"><span data-stu-id="ee545-112">Specifies that the member is accessible by subtypes only in this assembly.</span></span>|  
|`mdAssem`|<span data-ttu-id="ee545-113">指定该成员由程序集中的任何人 accessibly。</span><span class="sxs-lookup"><span data-stu-id="ee545-113">Specifies that the member is accessibly by anyone in the assembly.</span></span>|  
|`mdFamily`|<span data-ttu-id="ee545-114">指定成员只能由类型和子类型访问。</span><span class="sxs-lookup"><span data-stu-id="ee545-114">Specifies that the member is accessible only by type and subtypes.</span></span>|  
|`mdFamORAssem`|<span data-ttu-id="ee545-115">指定成员可由派生类和其程序集中的其他类型访问。</span><span class="sxs-lookup"><span data-stu-id="ee545-115">Specifies that the member is accessible by derived classes and by other types in its assembly.</span></span>|  
|`mdPublic`|<span data-ttu-id="ee545-116">指定成员可由对范围具有访问权限的所有类型进行访问。</span><span class="sxs-lookup"><span data-stu-id="ee545-116">Specifies that the member is accessible by all types with access to the scope.</span></span>|  
|`mdStatic`|<span data-ttu-id="ee545-117">指定将成员定义为类型的一部分而不是实例的成员。</span><span class="sxs-lookup"><span data-stu-id="ee545-117">Specifies that the member is defined as part of the type rather than as a member of an instance.</span></span>|  
|`mdFinal`|<span data-ttu-id="ee545-118">指定该方法不能被重写。</span><span class="sxs-lookup"><span data-stu-id="ee545-118">Specifies that the method cannot be overridden.</span></span>|  
|`mdVirtual`|<span data-ttu-id="ee545-119">指定可以重写方法。</span><span class="sxs-lookup"><span data-stu-id="ee545-119">Specifies that the method can be overridden.</span></span>|  
|`mdHideBySig`|<span data-ttu-id="ee545-120">指定该方法按名称和签名隐藏，而不是按名称隐藏。</span><span class="sxs-lookup"><span data-stu-id="ee545-120">Specifies that the method hides by name and signature, rather than just by name.</span></span>|  
|`mdVtableLayoutMask`|<span data-ttu-id="ee545-121">指定虚拟表布局。</span><span class="sxs-lookup"><span data-stu-id="ee545-121">Specifies virtual table layout.</span></span>|  
|`mdReuseSlot`|<span data-ttu-id="ee545-122">指定重复使用用于虚拟表中此方法的槽。</span><span class="sxs-lookup"><span data-stu-id="ee545-122">Specifies that the slot used for this method in the virtual table be reused.</span></span> <span data-ttu-id="ee545-123">这是默认设置。</span><span class="sxs-lookup"><span data-stu-id="ee545-123">This is the default.</span></span>|  
|`mdNewSlot`|<span data-ttu-id="ee545-124">指定方法始终获取虚拟表中的新槽。</span><span class="sxs-lookup"><span data-stu-id="ee545-124">Specifies that the method always gets a new slot in the virtual table.</span></span>|  
|`mdCheckAccessOnOverride`|<span data-ttu-id="ee545-125">指定方法可以由其可见的相同类型重写。</span><span class="sxs-lookup"><span data-stu-id="ee545-125">Specifies that the method can be overridden by the same types to which it is visible.</span></span>|  
|`mdAbstract`|<span data-ttu-id="ee545-126">指定未实现该方法。</span><span class="sxs-lookup"><span data-stu-id="ee545-126">Specifies that the method is not implemented.</span></span>|  
|`mdSpecialName`|<span data-ttu-id="ee545-127">指定该方法是特殊方法，其名称描述了操作方法。</span><span class="sxs-lookup"><span data-stu-id="ee545-127">Specifies that the method is special, and that its name describes how.</span></span>|  
|`mdPinvokeImpl`|<span data-ttu-id="ee545-128">指定使用 PInvoke 转发方法实现。</span><span class="sxs-lookup"><span data-stu-id="ee545-128">Specifies that the method implementation is forwarded using PInvoke.</span></span>|  
|`mdUnmanagedExport`|<span data-ttu-id="ee545-129">指定方法是导出到非托管代码的托管方法。</span><span class="sxs-lookup"><span data-stu-id="ee545-129">Specifies that the method is a managed method exported to unmanaged code.</span></span>|  
|`mdReservedMask`|<span data-ttu-id="ee545-130">保留供公共语言运行时内部使用。</span><span class="sxs-lookup"><span data-stu-id="ee545-130">Reserved for internal use by the common language runtime.</span></span>|  
|`mdRTSpecialName`|<span data-ttu-id="ee545-131">指定公共语言运行时应检查方法名称的编码。</span><span class="sxs-lookup"><span data-stu-id="ee545-131">Specifies that the common language runtime should check the encoding of the method name.</span></span>|  
|`mdHasSecurity`|<span data-ttu-id="ee545-132">指定该方法具有与之关联的安全性。</span><span class="sxs-lookup"><span data-stu-id="ee545-132">Specifies that the method has security associated with it.</span></span>|  
|`mdRequireSecObject`|<span data-ttu-id="ee545-133">指定该方法调用另一个包含安全代码的方法。</span><span class="sxs-lookup"><span data-stu-id="ee545-133">Specifies that the method calls another method containing security code.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ee545-134">要求</span><span class="sxs-lookup"><span data-stu-id="ee545-134">Requirements</span></span>  

 <span data-ttu-id="ee545-135">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ee545-135">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ee545-136">**标头：** Corhdr。h</span><span class="sxs-lookup"><span data-stu-id="ee545-136">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="ee545-137">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ee545-137">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ee545-138">请参阅</span><span class="sxs-lookup"><span data-stu-id="ee545-138">See also</span></span>

- [<span data-ttu-id="ee545-139">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="ee545-139">Metadata Enumerations</span></span>](metadata-enumerations.md)
