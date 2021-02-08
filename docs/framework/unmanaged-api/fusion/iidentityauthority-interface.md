---
description: 了解详细信息： IIdentityAuthority 接口
title: IIdentityAuthority 接口
ms.date: 03/30/2017
api_name:
- IIdentityAuthority
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IIdentityAuthority
helpviewer_keywords:
- IIdentityAuthority interface [.NET Framework fusion]
ms.assetid: 6277f914-51a8-49be-bec6-52d6d648527d
topic_type:
- apiref
ms.openlocfilehash: 3064a3d95ebe9a098a7cac0766f18654c6fab8b9
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800131"
---
# <a name="iidentityauthority-interface"></a><span data-ttu-id="c515e-103">IIdentityAuthority 接口</span><span class="sxs-lookup"><span data-stu-id="c515e-103">IIdentityAuthority Interface</span></span>

<span data-ttu-id="c515e-104">管理代码对象的标识键。</span><span class="sxs-lookup"><span data-stu-id="c515e-104">Manages identity keys for code objects.</span></span>

## <a name="methods"></a><span data-ttu-id="c515e-105">方法</span><span class="sxs-lookup"><span data-stu-id="c515e-105">Methods</span></span>

|<span data-ttu-id="c515e-106">方法</span><span class="sxs-lookup"><span data-stu-id="c515e-106">Method</span></span>|<span data-ttu-id="c515e-107">说明</span><span class="sxs-lookup"><span data-stu-id="c515e-107">Description</span></span>|
|------------|-----------------|
|`IIdentityAuthority::AreDefinitionsEqual`|<span data-ttu-id="c515e-108">获取一个值，该值指示两个指定的 [IDefinitionIdentity](idefinitionidentity-interface.md) 实例是否相等。</span><span class="sxs-lookup"><span data-stu-id="c515e-108">Gets a value that indicates whether the two specified [IDefinitionIdentity](idefinitionidentity-interface.md) instances are equal.</span></span>|
|`IIdentityAuthority::AreReferencesEqual`|<span data-ttu-id="c515e-109">获取一个值，该值指示两个指定的 [IReferenceIdentity](ireferenceidentity-interface.md) 实例是否相等。</span><span class="sxs-lookup"><span data-stu-id="c515e-109">Gets a value that indicates whether the two specified [IReferenceIdentity](ireferenceidentity-interface.md) instances are equal.</span></span>|
|`IIdentityAuthority::AreTextualDefinitionsEqual`|<span data-ttu-id="c515e-110">获取一个值，该值指示两个指定的字符串定义标识表示形式是否相等。</span><span class="sxs-lookup"><span data-stu-id="c515e-110">Gets a value that indicates whether the two specified string definition identity representations are equal.</span></span>|
|`IIdentityAuthority::AreTextualReferencesEqual`|<span data-ttu-id="c515e-111">获取一个值，该值指示两个指定的字符串引用标识表示形式是否相等。</span><span class="sxs-lookup"><span data-stu-id="c515e-111">Gets a value that indicates whether the two specified string reference identity representations are equal.</span></span>|
|`IIdentityAuthority::CreateDefinition`|<span data-ttu-id="c515e-112">获取一个指针，该指针指向 `IDefinitionIdentity` 表示当前范围内的代码对象的新实例。</span><span class="sxs-lookup"><span data-stu-id="c515e-112">Gets a pointer to a new `IDefinitionIdentity` instance that represents the code object in the current scope.</span></span>|
|`IIdentityAuthority::CreateReference`|<span data-ttu-id="c515e-113">获取一个指针，该指针指向 `IReferenceIdentity` 表示当前范围内的代码对象的新实例。</span><span class="sxs-lookup"><span data-stu-id="c515e-113">Gets a pointer to a new `IReferenceIdentity` instance that represents the code object in the current scope.</span></span>|
|`IIdentityAuthority::DefinitionToText`|<span data-ttu-id="c515e-114">获取指定的格式化字符串版本 `IDefinitionIdentity` 。</span><span class="sxs-lookup"><span data-stu-id="c515e-114">Gets a formatted string version of the specified `IDefinitionIdentity`.</span></span>|
|`IIdentityAuthority::DefinitionToTextBuffer`|<span data-ttu-id="c515e-115">使用指定的字符串版本填充指定的宽字符缓冲区 `IDefinitionIdentity` 。</span><span class="sxs-lookup"><span data-stu-id="c515e-115">Fills the specified wide character buffer with a string version of the specified `IDefinitionIdentity`.</span></span>|
|`IIdentityAuthority::DoesDefinitionMatchReference`|<span data-ttu-id="c515e-116">获取一个值，该值指示指定的 `IDefinitionIdentity` 和 `IReferenceIdentity` 实例是否引用同一代码对象。</span><span class="sxs-lookup"><span data-stu-id="c515e-116">Gets a value that indicates whether the specified `IDefinitionIdentity` and `IReferenceIdentity` instances refer to the same code object.</span></span>|
|`IIdentityAuthority::DoesTextualDefinitionMatchTextualReference`|<span data-ttu-id="c515e-117">获取一个值，该值指示指定的字符串是否引用同一代码对象。</span><span class="sxs-lookup"><span data-stu-id="c515e-117">Gets a value that indicates whether the specified strings refer to the same code object.</span></span>|
|`IIdentityAuthority::GenerateDefinitionKey`|<span data-ttu-id="c515e-118">获取一个指针，该指针指向指定的新创建的字符串键 `IDefinitionIdentity` 。</span><span class="sxs-lookup"><span data-stu-id="c515e-118">Gets a pointer to a newly created string key for the specified `IDefinitionIdentity`.</span></span>|
|`IIdentityAuthority::GenerateReferenceKey`|<span data-ttu-id="c515e-119">获取一个指针，该指针指向指定的新创建的字符串键 `IReferenceIdentity` 。</span><span class="sxs-lookup"><span data-stu-id="c515e-119">Gets a pointer to a newly created string key for the specified `IReferenceIdentity`.</span></span>|
|`IIdentityAuthority::HashDefinition`|<span data-ttu-id="c515e-120">获取指定的的哈希值 `IDefinitionIdentity` 。</span><span class="sxs-lookup"><span data-stu-id="c515e-120">Gets a hash value for the specified `IDefinitionIdentity`.</span></span>|
|`IIdentityAuthority::HashReference`|<span data-ttu-id="c515e-121">获取指定的的哈希值 `IReferenceIdentity` 。</span><span class="sxs-lookup"><span data-stu-id="c515e-121">Gets a hash value for the specified `IReferenceIdentity`.</span></span>|
|`IIdentityAuthority::ReferenceToText`|<span data-ttu-id="c515e-122">获取指定的格式化字符串版本 `IReferenceIdentity` 。</span><span class="sxs-lookup"><span data-stu-id="c515e-122">Gets a formatted string version of the specified `IReferenceIdentity`.</span></span>|
|`IIdentityAuthority::ReferenceToTextBuffer`|<span data-ttu-id="c515e-123">使用指定的字符串版本填充指定的宽字符缓冲区 `IReferenceIdentity` 。</span><span class="sxs-lookup"><span data-stu-id="c515e-123">Fills the specified wide character buffer with a string version of the specified `IReferenceIdentity`.</span></span>|
|`IIdentityAuthority::TextToDefinition`|<span data-ttu-id="c515e-124">获取一个接口指针，该指针指向 `IDefinitionIdentity` 从指定的格式化字符串生成的实例。</span><span class="sxs-lookup"><span data-stu-id="c515e-124">Gets an interface pointer to an `IDefinitionIdentity` instance generated from the specified formatted string.</span></span>|
|`IIdentityAuthority::TextToReference`|<span data-ttu-id="c515e-125">获取一个接口指针，该指针指向 `IReferenceIdentity` 从指定的格式化字符串生成的实例。</span><span class="sxs-lookup"><span data-stu-id="c515e-125">Gets an interface pointer to an `IReferenceIdentity` instance generated from the specified formatted string.</span></span>|

## <a name="requirements"></a><span data-ttu-id="c515e-126">要求</span><span class="sxs-lookup"><span data-stu-id="c515e-126">Requirements</span></span>

<span data-ttu-id="c515e-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="c515e-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="c515e-128">**标头：** 隔离。h</span><span class="sxs-lookup"><span data-stu-id="c515e-128">**Header:** Isolation.h</span></span>

<span data-ttu-id="c515e-129">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c515e-129">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="c515e-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="c515e-130">See also</span></span>

- [<span data-ttu-id="c515e-131">合成接口</span><span class="sxs-lookup"><span data-stu-id="c515e-131">Fusion Interfaces</span></span>](fusion-interfaces.md)
