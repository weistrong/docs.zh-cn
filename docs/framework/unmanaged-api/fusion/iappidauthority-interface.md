---
description: 了解详细信息： IAppIdAuthority 接口
title: IAppIdAuthority 接口
ms.date: 03/30/2017
api_name:
- IAppIdAuthority
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAppIdAuthority
helpviewer_keywords:
- IAppIdAuthority interface [.NET Framework fusion]
ms.assetid: ec354fa1-1efd-41b0-bc43-b90597b6e253
topic_type:
- apiref
ms.openlocfilehash: 238885c7f080571b414511c24f9772dbc19b4683
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760991"
---
# <a name="iappidauthority-interface"></a><span data-ttu-id="b1d8d-103">IAppIdAuthority 接口</span><span class="sxs-lookup"><span data-stu-id="b1d8d-103">IAppIdAuthority Interface</span></span>

<span data-ttu-id="b1d8d-104">提供一些方法，这些方法可为应用程序标识和引用生成和比较键。</span><span class="sxs-lookup"><span data-stu-id="b1d8d-104">Provides methods that generate and compare keys for application identities and references.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b1d8d-105">方法</span><span class="sxs-lookup"><span data-stu-id="b1d8d-105">Methods</span></span>  
  
|<span data-ttu-id="b1d8d-106">方法</span><span class="sxs-lookup"><span data-stu-id="b1d8d-106">Method</span></span>|<span data-ttu-id="b1d8d-107">说明</span><span class="sxs-lookup"><span data-stu-id="b1d8d-107">Description</span></span>|  
|------------|-----------------|  
|`IAppIdAuthority::AreDefinitionsEqual`|<span data-ttu-id="b1d8d-108">获取一个值，该值指示两个指定的 [IDefinitionAppId](idefinitionappid-interface.md) 实例是否相等。</span><span class="sxs-lookup"><span data-stu-id="b1d8d-108">Gets a value that indicates whether the two specified [IDefinitionAppId](idefinitionappid-interface.md) instances are equal.</span></span> <span data-ttu-id="b1d8d-109">可以将标志值 IAPPIDAUTHORITY_ARE_DEFINITIONS_EQUAL_FLAG_IGNORE_VERSION 传递给，以忽略其各自的版本信息。</span><span class="sxs-lookup"><span data-stu-id="b1d8d-109">You can pass the flag value IAPPIDAUTHORITY_ARE_DEFINITIONS_EQUAL_FLAG_IGNORE_VERSION to ignore their respective version information.</span></span>|  
|`IAppIdAuthority::AreReferencesEqual`|<span data-ttu-id="b1d8d-110">获取一个值，该值指示两个指定的 [IReferenceAppId](ireferenceappid-interface.md) 实例是否相等。</span><span class="sxs-lookup"><span data-stu-id="b1d8d-110">Gets a value that indicates whether the two specified [IReferenceAppId](ireferenceappid-interface.md) instances are equal.</span></span> <span data-ttu-id="b1d8d-111">可以将标志值 IAPPIDAUTHORITY_ARE_REFERENCES_EQUAL_FLAG_IGNORE_VERSION 传递给，以忽略其各自的版本信息。</span><span class="sxs-lookup"><span data-stu-id="b1d8d-111">You can pass the flag value IAPPIDAUTHORITY_ARE_REFERENCES_EQUAL_FLAG_IGNORE_VERSION to ignore their respective version information.</span></span>|  
|`IAppIdAuthority::AreTextualDefinitionsEqual`|<span data-ttu-id="b1d8d-112">获取一个值，该值指示两个指定的字符串定义是否相等。</span><span class="sxs-lookup"><span data-stu-id="b1d8d-112">Gets a value that indicates whether the two specified string definitions are equal.</span></span> <span data-ttu-id="b1d8d-113">可以将标志值 IAPPIDAUTHORITY_ARE_DEFINITIONS_EQUAL_FLAG_IGNORE_VERSION 传递给，以忽略其各自的版本信息。</span><span class="sxs-lookup"><span data-stu-id="b1d8d-113">You can pass the flag value IAPPIDAUTHORITY_ARE_DEFINITIONS_EQUAL_FLAG_IGNORE_VERSION to ignore their respective version information.</span></span>|  
|`IAppIdAuthority::AreTextualReferencesEqual`|<span data-ttu-id="b1d8d-114">获取一个值，该值指示两个指定的字符串引用是否相等。</span><span class="sxs-lookup"><span data-stu-id="b1d8d-114">Gets a value that indicates whether the two specified string references are equal.</span></span> <span data-ttu-id="b1d8d-115">可以将标志值 IAPPIDAUTHORITY_ARE_REFERENCES_EQUAL_FLAG_IGNORE_VERSION 传递给，以忽略其各自的版本信息。</span><span class="sxs-lookup"><span data-stu-id="b1d8d-115">You can pass the flag value IAPPIDAUTHORITY_ARE_REFERENCES_EQUAL_FLAG_IGNORE_VERSION to ignore their respective version information.</span></span>|  
|`IAppIdAuthority::CreateDefinition`|<span data-ttu-id="b1d8d-116">获取一个接口指针，该指针指向 `IDefinitionAppId` 表示当前范围内的程序集的新生成的实例。</span><span class="sxs-lookup"><span data-stu-id="b1d8d-116">Gets an interface pointer to a newly generated `IDefinitionAppId` instance that represents the assembly in the current scope.</span></span>|  
|`IAppIdAuthority::CreateReference`|<span data-ttu-id="b1d8d-117">获取一个接口指针，该指针指向 `IReferenceAppId` 表示当前范围内的程序集的新创建的。</span><span class="sxs-lookup"><span data-stu-id="b1d8d-117">Gets an interface pointer to a newly created `IReferenceAppId` that represents the assembly in the current scope.</span></span>|  
|`IAppIdAuthority::DefinitionToText`|<span data-ttu-id="b1d8d-118">使用指定的标志值获取指定的的字符串版本 `IDefinitionAppId` 。</span><span class="sxs-lookup"><span data-stu-id="b1d8d-118">Gets a string version of the specified `IDefinitionAppId`, using the specified flag values.</span></span>|  
|`IAppIdAuthority::DoesDefinitionMatchReference`|<span data-ttu-id="b1d8d-119">获取一个值，该值指示指定的 `IDefinitionAppId` 是否 `IReferenceAppId` 表示相同的程序集。</span><span class="sxs-lookup"><span data-stu-id="b1d8d-119">Gets a value that indicates whether the specified `IDefinitionAppId` and `IReferenceAppId` represent the same assembly.</span></span>|  
|`IAppIdAuthority::DoesTextualDefinitionMatchTextualReference`|<span data-ttu-id="b1d8d-120">获取一个值，该值指示指定的定义字符串和引用字符串是否表示相同的程序集。</span><span class="sxs-lookup"><span data-stu-id="b1d8d-120">Gets a value that indicates whether the specified definition string and reference string represent the same assembly.</span></span>|  
|`IAppIdAuthority::GenerateDefinitionKey`|<span data-ttu-id="b1d8d-121">获取表示指定实例的字符串键 `IDefinitionAppId` 。</span><span class="sxs-lookup"><span data-stu-id="b1d8d-121">Gets a string key that represents the specified `IDefinitionAppId` instance.</span></span>|  
|`IAppIdAuthority::GenerateReferenceKey`|<span data-ttu-id="b1d8d-122">获取表示指定实例的字符串键 `IReferenceAppId` 。</span><span class="sxs-lookup"><span data-stu-id="b1d8d-122">Gets a string key that represents the specified `IReferenceAppId` instance.</span></span>|  
|`IAppIdAuthority::HashDefinition`|<span data-ttu-id="b1d8d-123">获取指定实例的哈希键 `IDefinitionAppId` 。</span><span class="sxs-lookup"><span data-stu-id="b1d8d-123">Gets a hash key for the specified `IDefinitionAppId` instance.</span></span>|  
|`IAppIdAuthority::HashReference`|<span data-ttu-id="b1d8d-124">获取指定实例的哈希键 `IReferenceAppId` 。</span><span class="sxs-lookup"><span data-stu-id="b1d8d-124">Gets a hash key for the specified `IReferenceAppId` instance.</span></span>|  
|`IAppIdAuthority::ReferenceToText`|<span data-ttu-id="b1d8d-125">使用指定的标志值获取指定的的字符串版本 `IReferenceAppId` 。</span><span class="sxs-lookup"><span data-stu-id="b1d8d-125">Gets a string version of the specified `IReferenceAppId`, using the specified flag values.</span></span>|  
|`IAppIdAuthority::TextToDefinition`|<span data-ttu-id="b1d8d-126">获取一个接口指针，该指针指向 `IDefinitionAppId` 表示指定字符串键所引用的程序集的实例。</span><span class="sxs-lookup"><span data-stu-id="b1d8d-126">Gets an interface pointer to an `IDefinitionAppId` instance that represents the assembly referenced by the specified string key.</span></span>|  
|`IAppIdAuthority::TextToReference`|<span data-ttu-id="b1d8d-127">获取一个接口指针，该指针指向 `IReferenceAppId` 表示指定字符串键所引用的程序集的实例。</span><span class="sxs-lookup"><span data-stu-id="b1d8d-127">Gets an interface pointer to an `IReferenceAppId` instance that represents the assembly referenced by the specified string key.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b1d8d-128">要求</span><span class="sxs-lookup"><span data-stu-id="b1d8d-128">Requirements</span></span>  

 <span data-ttu-id="b1d8d-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b1d8d-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b1d8d-130">**标头：** 隔离。h</span><span class="sxs-lookup"><span data-stu-id="b1d8d-130">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="b1d8d-131">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b1d8d-131">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b1d8d-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="b1d8d-132">See also</span></span>

- [<span data-ttu-id="b1d8d-133">合成接口</span><span class="sxs-lookup"><span data-stu-id="b1d8d-133">Fusion Interfaces</span></span>](fusion-interfaces.md)
