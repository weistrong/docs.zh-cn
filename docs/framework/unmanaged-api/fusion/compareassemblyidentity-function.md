---
description: 了解详细信息： CompareAssemblyIdentity 函数
title: CompareAssemblyIdentity 函数
ms.date: 03/30/2017
api_name:
- CompareAssemblyIdentity
api_location:
- fusion.dll
- clr.dll
api_type:
- COM
f1_keywords:
- CompareAssemblyIdentity
helpviewer_keywords:
- CompareAssemblyIdentity function [.NET Framework fusion]
ms.assetid: 8b364ae1-8efa-4744-a7da-81fd093d84d6
topic_type:
- apiref
ms.openlocfilehash: aa55d1ea0b1968ec4e50106139e154e29e159ec7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761208"
---
# <a name="compareassemblyidentity-function"></a><span data-ttu-id="82a7c-103">CompareAssemblyIdentity 函数</span><span class="sxs-lookup"><span data-stu-id="82a7c-103">CompareAssemblyIdentity Function</span></span>

<span data-ttu-id="82a7c-104">比较两个程序集标识以确定它们是否等效。</span><span class="sxs-lookup"><span data-stu-id="82a7c-104">Compares two assembly identities to determine whether they are equivalent.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="82a7c-105">语法</span><span class="sxs-lookup"><span data-stu-id="82a7c-105">Syntax</span></span>  
  
```cpp  
STDAPI CompareAssemblyIdentity (  
    [in]  LPCWSTR                  pwzAssemblyIdentity1,  
    [in]  BOOL                     fUnified1,  
    [in]  LPCWSTR                  pwzAssemblyIdentity2,  
    [in]  BOOL                     fUnified2,  
    [out] BOOL                     *pfEquivalent,  
    [out] AssemblyComparisonResult *pResult  
 );  
```  
  
## <a name="parameters"></a><span data-ttu-id="82a7c-106">参数</span><span class="sxs-lookup"><span data-stu-id="82a7c-106">Parameters</span></span>  

 `pwzAssemblyIdentity1`  
 <span data-ttu-id="82a7c-107">中比较中第一个程序集的文本标识。</span><span class="sxs-lookup"><span data-stu-id="82a7c-107">[in] The textual identity of the first assembly in the comparison.</span></span>  
  
 `fUnified1`  
 <span data-ttu-id="82a7c-108">中指示的用户指定的统一的布尔标志 `pwzAssemblyIdentity1` 。</span><span class="sxs-lookup"><span data-stu-id="82a7c-108">[in] A Boolean flag that indicates user-specified unification for `pwzAssemblyIdentity1`.</span></span>  
  
 `pwzAssemblyIdentity2`  
 <span data-ttu-id="82a7c-109">中比较中第二个程序集的文本标识。</span><span class="sxs-lookup"><span data-stu-id="82a7c-109">[in] The textual identity of the second assembly in the comparison.</span></span>  
  
 `fUnified2`  
 <span data-ttu-id="82a7c-110">中指示的用户指定的统一的布尔标志 `pwzAssemblyIdentity2` 。</span><span class="sxs-lookup"><span data-stu-id="82a7c-110">[in] A Boolean flag that indicates user-specified unification for `pwzAssemblyIdentity2`.</span></span>  
  
 `pfEquivalent`  
 <span data-ttu-id="82a7c-111">弄指示两个程序集是否等效的布尔型标志。</span><span class="sxs-lookup"><span data-stu-id="82a7c-111">[out] A Boolean flag that indicates whether the two assemblies are equivalent.</span></span>  
  
 `pResult`  
 <span data-ttu-id="82a7c-112">弄 [AssemblyComparisonResult](assemblycomparisonresult-enumeration.md) 枚举，其中包含有关比较的详细信息。</span><span class="sxs-lookup"><span data-stu-id="82a7c-112">[out] An [AssemblyComparisonResult](assemblycomparisonresult-enumeration.md) enumeration that contains detailed information about the comparison.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="82a7c-113">返回值</span><span class="sxs-lookup"><span data-stu-id="82a7c-113">Return Value</span></span>  

 <span data-ttu-id="82a7c-114">`pfEquivalent` 返回一个布尔值，该值指示两个程序集是否等效。</span><span class="sxs-lookup"><span data-stu-id="82a7c-114">`pfEquivalent` returns a Boolean value that indicates whether the two assemblies are equivalent.</span></span> <span data-ttu-id="82a7c-115">`pResult` 返回 `AssemblyComparisonResult` 值之一，以便为的值提供更详细的原因 `pfEquivalent` 。</span><span class="sxs-lookup"><span data-stu-id="82a7c-115">`pResult` returns one of the `AssemblyComparisonResult` values, to give a more detailed reason for the value of `pfEquivalent`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="82a7c-116">备注</span><span class="sxs-lookup"><span data-stu-id="82a7c-116">Remarks</span></span>  

 <span data-ttu-id="82a7c-117">`CompareAssemblyIdentity` 检查 `pwzAssemblyIdentity1` 和是否 `pwzAssemblyIdentity2` 等效。</span><span class="sxs-lookup"><span data-stu-id="82a7c-117">`CompareAssemblyIdentity` checks whether `pwzAssemblyIdentity1` and `pwzAssemblyIdentity2` are equivalent.</span></span> <span data-ttu-id="82a7c-118">`pfEquivalent``true`在以下一个或多个条件下，设置为：</span><span class="sxs-lookup"><span data-stu-id="82a7c-118">`pfEquivalent` is set to `true` under one or more of the following conditions:</span></span>  
  
- <span data-ttu-id="82a7c-119">这两个程序集标识是等效的。</span><span class="sxs-lookup"><span data-stu-id="82a7c-119">The two assembly identities are equivalent.</span></span> <span data-ttu-id="82a7c-120">对于强名称程序集，等效要求程序集名称、版本、公钥标记和区域性完全相同。</span><span class="sxs-lookup"><span data-stu-id="82a7c-120">For strongly named assemblies, equivalency requires the assembly name, version, public key token, and culture to be identical.</span></span> <span data-ttu-id="82a7c-121">对于简单命名的程序集，等效要求程序集名称和区域性匹配。</span><span class="sxs-lookup"><span data-stu-id="82a7c-121">For simply named assemblies, equivalency requires a match on the assembly name and culture.</span></span>  
  
- <span data-ttu-id="82a7c-122">这两个程序集标识都是指在 .NET Framework 上运行的程序集。</span><span class="sxs-lookup"><span data-stu-id="82a7c-122">Both assembly identities refer to assemblies that run on the .NET Framework.</span></span> <span data-ttu-id="82a7c-123">`true`即使程序集版本号不匹配，此条件也将返回。</span><span class="sxs-lookup"><span data-stu-id="82a7c-123">This condition returns `true` even if the assembly version numbers do not match.</span></span>  
  
- <span data-ttu-id="82a7c-124">这两个程序集不是托管程序集，而是 `fUnified1` `fUnified2` 设置为 `true` 。</span><span class="sxs-lookup"><span data-stu-id="82a7c-124">The two assemblies are not managed assemblies, but `fUnified1` or `fUnified2` was set to `true`.</span></span>  
  
 <span data-ttu-id="82a7c-125">该 `fUnified` 标志指示在强名称程序集的版本号之前的所有版本号都被视为等效于强名称程序集。</span><span class="sxs-lookup"><span data-stu-id="82a7c-125">The `fUnified` flag indicates that all version numbers up to the version number of the strongly named assembly are considered equivalent to the strongly named assembly.</span></span> <span data-ttu-id="82a7c-126">例如，如果的值 `pwzAssemblyIndentity1` 为 "MyAssembly，version = 3.0.0.0，culture = 中立，publicKeyToken = ..."，并且的值 `fUnified1` 为 `true` ，则表示从版本0.0.0.0 到3.0.0.0 的 MyAssembly 的所有版本均应视为等效。</span><span class="sxs-lookup"><span data-stu-id="82a7c-126">For example, if the value of `pwzAssemblyIndentity1` is "MyAssembly, version=3.0.0.0, culture=neutral, publicKeyToken=....", and the value of `fUnified1` is `true`, this indicates that all versions of MyAssembly from version 0.0.0.0 to 3.0.0.0 should be treated as equivalent.</span></span> <span data-ttu-id="82a7c-127">在这种情况下，如果 `pwzAssemblyIndentity2` 引用与相同的程序集，则将 `pwzAssemblyIndentity1` 设置为，但该程序集的版本号较低 `pfEquivalent` `true` 。</span><span class="sxs-lookup"><span data-stu-id="82a7c-127">In such a case, if `pwzAssemblyIndentity2` refers to the same assembly as `pwzAssemblyIndentity1`, except that it has a lower version number, `pfEquivalent` is set to `true`.</span></span> <span data-ttu-id="82a7c-128">如果 `pwzAssemblyIdentity2` 引用较高的版本号， `pfEquivalent` 则 `true` 仅当的值为时，才设置为 `fUnified2` `true` 。</span><span class="sxs-lookup"><span data-stu-id="82a7c-128">If `pwzAssemblyIdentity2` refers to a higher version number, `pfEquivalent` is set to `true` only if the value of `fUnified2` is `true`.</span></span>  
  
 <span data-ttu-id="82a7c-129">`pResult`参数包含有关两个程序集被视为等效或不等效的原因的具体信息。</span><span class="sxs-lookup"><span data-stu-id="82a7c-129">The `pResult` parameter includes specific information about why the two assemblies are considered equivalent or not equivalent.</span></span> <span data-ttu-id="82a7c-130">有关详细信息，请参阅 [AssemblyComparisonResult 枚举](assemblycomparisonresult-enumeration.md)。</span><span class="sxs-lookup"><span data-stu-id="82a7c-130">For more information, see [AssemblyComparisonResult Enumeration](assemblycomparisonresult-enumeration.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="82a7c-131">要求</span><span class="sxs-lookup"><span data-stu-id="82a7c-131">Requirements</span></span>  

 <span data-ttu-id="82a7c-132">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="82a7c-132">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="82a7c-133">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="82a7c-133">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="82a7c-134">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="82a7c-134">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="82a7c-135">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="82a7c-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="82a7c-136">请参阅</span><span class="sxs-lookup"><span data-stu-id="82a7c-136">See also</span></span>

- [<span data-ttu-id="82a7c-137">合成全局静态函数</span><span class="sxs-lookup"><span data-stu-id="82a7c-137">Fusion Global Static Functions</span></span>](fusion-global-static-functions.md)
- [<span data-ttu-id="82a7c-138">AssemblyComparisonResult 枚举</span><span class="sxs-lookup"><span data-stu-id="82a7c-138">AssemblyComparisonResult Enumeration</span></span>](assemblycomparisonresult-enumeration.md)
