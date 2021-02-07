---
description: 了解详细信息：合成接口
title: 合成接口
ms.date: 03/30/2017
helpviewer_keywords:
- interfaces [.NET Framework fusion]
- fusion interfaces [.NET Framework]
- unmanaged interfaces [.NET Framework], fusion
ms.assetid: e2cf98b7-40c1-4f74-86c7-8a76dd9da677
ms.openlocfilehash: 3b6ca64b40ebc1a7b38129d897059ca628d3914c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761060"
---
# <a name="fusion-interfaces"></a><span data-ttu-id="2dabd-103">合成接口</span><span class="sxs-lookup"><span data-stu-id="2dabd-103">Fusion Interfaces</span></span>

<span data-ttu-id="2dabd-104">本节介绍了合成 API 用于访问应用程序资源属性的非托管接口，并为应用程序定位了这些资源的正确版本。</span><span class="sxs-lookup"><span data-stu-id="2dabd-104">This section describes the unmanaged interfaces that the fusion API uses to access the properties of an application's resources and to locate the correct versions of those resources for the application.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="2dabd-105">本节内容</span><span class="sxs-lookup"><span data-stu-id="2dabd-105">In This Section</span></span>  

 [<span data-ttu-id="2dabd-106">IAppIdAuthority 接口</span><span class="sxs-lookup"><span data-stu-id="2dabd-106">IAppIdAuthority Interface</span></span>](iappidauthority-interface.md)  
 <span data-ttu-id="2dabd-107">提供一些方法，这些方法可为应用程序标识和引用生成和比较键。</span><span class="sxs-lookup"><span data-stu-id="2dabd-107">Provides methods that generate and compare keys for application identities and references.</span></span>  
  
 [<span data-ttu-id="2dabd-108">IAssemblyCache 接口</span><span class="sxs-lookup"><span data-stu-id="2dabd-108">IAssemblyCache Interface</span></span>](iassemblycache-interface.md)  
 <span data-ttu-id="2dabd-109">提供全局程序集缓存的表示形式。</span><span class="sxs-lookup"><span data-stu-id="2dabd-109">Provides a representation of the global assembly cache.</span></span>  
  
 [<span data-ttu-id="2dabd-110">IAssemblyCacheItem 接口</span><span class="sxs-lookup"><span data-stu-id="2dabd-110">IAssemblyCacheItem Interface</span></span>](iassemblycacheitem-interface.md)  
 <span data-ttu-id="2dabd-111">表示全局程序集缓存中的单个程序集。</span><span class="sxs-lookup"><span data-stu-id="2dabd-111">Represents a single assembly in the global assembly cache.</span></span>  
  
 [<span data-ttu-id="2dabd-112">IAssemblyEnum 接口</span><span class="sxs-lookup"><span data-stu-id="2dabd-112">IAssemblyEnum Interface</span></span>](iassemblyenum-interface.md)  
 <span data-ttu-id="2dabd-113">表示对象数组的枚举器 `IAssemblyName` 。</span><span class="sxs-lookup"><span data-stu-id="2dabd-113">Represents an enumerator for an array of `IAssemblyName` objects.</span></span>  
  
 [<span data-ttu-id="2dabd-114">IAssemblyName 接口</span><span class="sxs-lookup"><span data-stu-id="2dabd-114">IAssemblyName Interface</span></span>](iassemblyname-interface.md)  
 <span data-ttu-id="2dabd-115">提供用于描述和处理程序集的唯一标识的方法。</span><span class="sxs-lookup"><span data-stu-id="2dabd-115">Provides methods for describing and working with an assembly's unique identity.</span></span>  
  
 [<span data-ttu-id="2dabd-116">IDefinitionAppId 接口</span><span class="sxs-lookup"><span data-stu-id="2dabd-116">IDefinitionAppId Interface</span></span>](idefinitionappid-interface.md)  
 <span data-ttu-id="2dabd-117">表示定义当前作用域中的应用程序的代码的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="2dabd-117">Represents a unique identifier for the code that defines the application in the current scope.</span></span>  
  
 [<span data-ttu-id="2dabd-118">IDefinitionIdentity 接口</span><span class="sxs-lookup"><span data-stu-id="2dabd-118">IDefinitionIdentity Interface</span></span>](idefinitionidentity-interface.md)  
 <span data-ttu-id="2dabd-119">表示定义当前作用域中的应用程序的代码的唯一签名。</span><span class="sxs-lookup"><span data-stu-id="2dabd-119">Represents the unique signature of the code that defines the application in the current scope.</span></span>  
  
 [<span data-ttu-id="2dabd-120">IEnumDefinitionIdentity 接口</span><span class="sxs-lookup"><span data-stu-id="2dabd-120">IEnumDefinitionIdentity Interface</span></span>](ienumdefinitionidentity-interface.md)  
 <span data-ttu-id="2dabd-121">用作对象集合的枚举器 `IDefinitionIdentity` 。</span><span class="sxs-lookup"><span data-stu-id="2dabd-121">Serves as the enumerator for a collection of `IDefinitionIdentity` objects.</span></span>  
  
 [<span data-ttu-id="2dabd-122">IEnumIDENTITY_ATTRIBUTE 接口</span><span class="sxs-lookup"><span data-stu-id="2dabd-122">IEnumIDENTITY_ATTRIBUTE Interface</span></span>](ienumidentity-attribute-interface.md)  
 <span data-ttu-id="2dabd-123">用作当前范围中代码对象的特性的枚举数。</span><span class="sxs-lookup"><span data-stu-id="2dabd-123">Serves as an enumerator for the attributes of the code object in the current scope.</span></span>  
  
 [<span data-ttu-id="2dabd-124">IEnumReferenceIdentity 接口</span><span class="sxs-lookup"><span data-stu-id="2dabd-124">IEnumReferenceIdentity Interface</span></span>](ienumreferenceidentity-interface.md)  
 <span data-ttu-id="2dabd-125">用作对象集合的枚举器 `IReferenceIdentity` 。</span><span class="sxs-lookup"><span data-stu-id="2dabd-125">Serves as an enumerator for a collection of `IReferenceIdentity` objects.</span></span>  
  
 [<span data-ttu-id="2dabd-126">IIdentityAuthority 接口</span><span class="sxs-lookup"><span data-stu-id="2dabd-126">IIdentityAuthority Interface</span></span>](iidentityauthority-interface.md)  
 <span data-ttu-id="2dabd-127">管理代码对象的标识键。</span><span class="sxs-lookup"><span data-stu-id="2dabd-127">Manages identity keys for code objects.</span></span>  
  
 [<span data-ttu-id="2dabd-128">IInstallReferenceEnum 接口</span><span class="sxs-lookup"><span data-stu-id="2dabd-128">IInstallReferenceEnum Interface</span></span>](iinstallreferenceenum-interface.md)  
 <span data-ttu-id="2dabd-129">表示安装在全局程序集缓存中的被引用程序集的枚举器。</span><span class="sxs-lookup"><span data-stu-id="2dabd-129">Represents an enumerator for the referenced assemblies installed in the global assembly cache.</span></span>  
  
 [<span data-ttu-id="2dabd-130">IInstallReferenceItem 接口</span><span class="sxs-lookup"><span data-stu-id="2dabd-130">IInstallReferenceItem Interface</span></span>](iinstallreferenceitem-interface.md)  
 <span data-ttu-id="2dabd-131">表示安装在全局程序集缓存中的项。</span><span class="sxs-lookup"><span data-stu-id="2dabd-131">Represents an item installed in the global assembly cache.</span></span>  
  
 [<span data-ttu-id="2dabd-132">IReferenceAppId 接口</span><span class="sxs-lookup"><span data-stu-id="2dabd-132">IReferenceAppId Interface</span></span>](ireferenceappid-interface.md)  
 <span data-ttu-id="2dabd-133">表示对当前范围内的应用程序的唯一标识符的引用。</span><span class="sxs-lookup"><span data-stu-id="2dabd-133">Represents a reference to the unique identifier for the application in the current scope.</span></span>  
  
 [<span data-ttu-id="2dabd-134">IReferenceIdentity 接口</span><span class="sxs-lookup"><span data-stu-id="2dabd-134">IReferenceIdentity Interface</span></span>](ireferenceidentity-interface.md)  
 <span data-ttu-id="2dabd-135">表示对代码对象的唯一签名的引用。</span><span class="sxs-lookup"><span data-stu-id="2dabd-135">Represents a reference to the unique signature of a code object.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="2dabd-136">参考</span><span class="sxs-lookup"><span data-stu-id="2dabd-136">Reference</span></span>  

 <xref:System.Reflection>  
  
 <xref:System.Reflection.Emit>  
  
## <a name="related-sections"></a><span data-ttu-id="2dabd-137">相关章节</span><span class="sxs-lookup"><span data-stu-id="2dabd-137">Related Sections</span></span>  

 [<span data-ttu-id="2dabd-138">合成全局静态函数</span><span class="sxs-lookup"><span data-stu-id="2dabd-138">Fusion Global Static Functions</span></span>](fusion-global-static-functions.md)  
  
 [<span data-ttu-id="2dabd-139">合成枚举</span><span class="sxs-lookup"><span data-stu-id="2dabd-139">Fusion Enumerations</span></span>](fusion-enumerations.md)  
  
 [<span data-ttu-id="2dabd-140">合成结构</span><span class="sxs-lookup"><span data-stu-id="2dabd-140">Fusion Structures</span></span>](fusion-structures.md)
