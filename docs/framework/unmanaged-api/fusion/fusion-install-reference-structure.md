---
description: 了解详细信息： FUSION_INSTALL_REFERENCE 结构
title: FUSION_INSTALL_REFERENCE 结构
ms.date: 03/30/2017
api_name:
- FUSION_INSTALL_REFERENCE
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- FUSION_INSTALL_REFERENCE
helpviewer_keywords:
- FUSION_INSTALL_REFERENCE structure [.NET Framework fusion]
ms.assetid: ae181ec8-36bf-4ed1-9a02-ca27d417c80b
topic_type:
- apiref
ms.openlocfilehash: 4ac3d2f7d36dd017315a8a3ce6d6185e75f9ddc6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761104"
---
# <a name="fusion_install_reference-structure"></a><span data-ttu-id="5160c-103">FUSION_INSTALL_REFERENCE 结构</span><span class="sxs-lookup"><span data-stu-id="5160c-103">FUSION_INSTALL_REFERENCE Structure</span></span>

<span data-ttu-id="5160c-104">表示应用程序对应用程序已安装在全局程序集缓存中的程序集进行的引用。</span><span class="sxs-lookup"><span data-stu-id="5160c-104">Represents a reference that an application makes to an assembly that the application has installed in the global assembly cache.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="5160c-105">语法</span><span class="sxs-lookup"><span data-stu-id="5160c-105">Syntax</span></span>  
  
```cpp  
typedef struct _FUSION_INSTALL_REFERENCE_ {  
    DWORD    cbSize,  
    DWORD    dwFlags,  
    GUID     guidScheme,  
    LPCWSTR  szIdentifier,  
    LPCWSTR  szNonCanonicalData  
} FUSION_INSTALL_REFERENCE, *LPFUSION_INSTALL_REFERENCE;  
```  
  
## <a name="members"></a><span data-ttu-id="5160c-106">成员</span><span class="sxs-lookup"><span data-stu-id="5160c-106">Members</span></span>  
  
|<span data-ttu-id="5160c-107">成员</span><span class="sxs-lookup"><span data-stu-id="5160c-107">Member</span></span>|<span data-ttu-id="5160c-108">说明</span><span class="sxs-lookup"><span data-stu-id="5160c-108">Description</span></span>|  
|------------|-----------------|  
|`cbSize`|<span data-ttu-id="5160c-109">结构的大小（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="5160c-109">The size of the structure in bytes.</span></span>|  
|`dwFlags`|<span data-ttu-id="5160c-110">保留以供将来进行扩展。</span><span class="sxs-lookup"><span data-stu-id="5160c-110">Reserved for future extensibility.</span></span> <span data-ttu-id="5160c-111">此值必须为 0 (零) 。</span><span class="sxs-lookup"><span data-stu-id="5160c-111">This value must be 0 (zero).</span></span>|  
|`guidScheme`|<span data-ttu-id="5160c-112">添加引用的实体。</span><span class="sxs-lookup"><span data-stu-id="5160c-112">The entity that adds the reference.</span></span> <span data-ttu-id="5160c-113">此字段可以具有以下值之一：</span><span class="sxs-lookup"><span data-stu-id="5160c-113">This field can have one of the following values:</span></span><br /><br /> <span data-ttu-id="5160c-114">-FUSION_REFCOUNT_MSI_GUID：程序集由使用 Microsoft Windows Installer 安装的应用程序引用。</span><span class="sxs-lookup"><span data-stu-id="5160c-114">-   FUSION_REFCOUNT_MSI_GUID: The assembly is referenced by an application that was installed using the Microsoft Windows Installer.</span></span> <span data-ttu-id="5160c-115">该 `szIdentifier` 字段设置为 `MSI` ，并且该 `szNonCanonicalData` 字段设置为 `Windows Installer` 。</span><span class="sxs-lookup"><span data-stu-id="5160c-115">The `szIdentifier` field is set to `MSI`, and the `szNonCanonicalData` field is set to `Windows Installer`.</span></span> <span data-ttu-id="5160c-116">此方案用于 Windows 并行程序集。</span><span class="sxs-lookup"><span data-stu-id="5160c-116">This scheme is used for Windows side-by-side assemblies.</span></span><br /><span data-ttu-id="5160c-117">-FUSION_REFCOUNT_UNINSTALL_SUBKEY_GUID：程序集由在 " **添加/删除程序** " 界面中显示的应用程序引用。</span><span class="sxs-lookup"><span data-stu-id="5160c-117">-   FUSION_REFCOUNT_UNINSTALL_SUBKEY_GUID: The assembly is referenced by an application that appears in the **Add/Remove Programs** interface.</span></span> <span data-ttu-id="5160c-118">`szIdentifier`字段提供了用于将应用程序注册到 "**添加/删除程序**" 界面的令牌。</span><span class="sxs-lookup"><span data-stu-id="5160c-118">The `szIdentifier` field provides the token that registers the application with the **Add/Remove Programs** interface.</span></span><br /><span data-ttu-id="5160c-119">-FUSION_REFCOUNT_FILEPATH_GUID：程序集由文件系统中的文件所表示的应用程序引用。</span><span class="sxs-lookup"><span data-stu-id="5160c-119">-   FUSION_REFCOUNT_FILEPATH_GUID: The assembly is referenced by an application that is represented by a file in the file system.</span></span> <span data-ttu-id="5160c-120">`szIdentifier`字段提供此文件的路径。</span><span class="sxs-lookup"><span data-stu-id="5160c-120">The `szIdentifier` field provides the path to this file.</span></span><br /><span data-ttu-id="5160c-121">-FUSION_REFCOUNT_OPAQUE_STRING_GUID：程序集由仅由不透明字符串表示的应用程序引用。</span><span class="sxs-lookup"><span data-stu-id="5160c-121">-   FUSION_REFCOUNT_OPAQUE_STRING_GUID: The assembly is referenced by an application that is represented only by an opaque string.</span></span> <span data-ttu-id="5160c-122">`szIdentifier`字段提供了此不透明字符串。</span><span class="sxs-lookup"><span data-stu-id="5160c-122">The `szIdentifier` field provides this opaque string.</span></span> <span data-ttu-id="5160c-123">删除此值时，全局程序集缓存不会检查不透明引用是否存在。</span><span class="sxs-lookup"><span data-stu-id="5160c-123">The global assembly cache does not check for the existence of opaque references when you remove this value.</span></span><br /><span data-ttu-id="5160c-124">-FUSION_REFCOUNT_OSINSTALL_GUID：保留此值。</span><span class="sxs-lookup"><span data-stu-id="5160c-124">-   FUSION_REFCOUNT_OSINSTALL_GUID: This value is reserved.</span></span>|  
|`szIdentifier`|<span data-ttu-id="5160c-125">标识在全局程序集缓存中安装程序集的应用程序的唯一字符串。</span><span class="sxs-lookup"><span data-stu-id="5160c-125">A unique string that identifies the application that installed the assembly in the global assembly cache.</span></span> <span data-ttu-id="5160c-126">其值取决于字段的值 `guidScheme` 。</span><span class="sxs-lookup"><span data-stu-id="5160c-126">Its value depends upon the value of the `guidScheme` field.</span></span>|  
|`szNonCanonicalData`|<span data-ttu-id="5160c-127">仅由添加了引用的实体识别的字符串。</span><span class="sxs-lookup"><span data-stu-id="5160c-127">A string that is understood only by the entity that adds the reference.</span></span> <span data-ttu-id="5160c-128">全局程序集缓存存储此字符串，但不使用它。</span><span class="sxs-lookup"><span data-stu-id="5160c-128">The global assembly cache stores this string, but does not use it.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="5160c-129">要求</span><span class="sxs-lookup"><span data-stu-id="5160c-129">Requirements</span></span>  

 <span data-ttu-id="5160c-130">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="5160c-130">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="5160c-131">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="5160c-131">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="5160c-132">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="5160c-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5160c-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="5160c-133">See also</span></span>

- [<span data-ttu-id="5160c-134">合成结构</span><span class="sxs-lookup"><span data-stu-id="5160c-134">Fusion Structures</span></span>](fusion-structures.md)
- [<span data-ttu-id="5160c-135">全局程序集缓存</span><span class="sxs-lookup"><span data-stu-id="5160c-135">Global Assembly Cache</span></span>](../../app-domains/gac.md)
