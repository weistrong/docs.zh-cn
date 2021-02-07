---
description: 了解详细信息： AssemblyComparisonResult 枚举
title: AssemblyComparisonResult 枚举
ms.date: 03/30/2017
api_name:
- AssemblyComparisonResult
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- AssemblyComparisonResult
helpviewer_keywords:
- AssemblyComparisonResult enumeration [.NET Framework fusion]
ms.assetid: bd042f89-10b1-40ca-946e-46da082f5263
topic_type:
- apiref
ms.openlocfilehash: 093cff830aa87d28ee86ecaeb6965887279a72d6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761261"
---
# <a name="assemblycomparisonresult-enumeration"></a><span data-ttu-id="b1ce9-103">AssemblyComparisonResult 枚举</span><span class="sxs-lookup"><span data-stu-id="b1ce9-103">AssemblyComparisonResult Enumeration</span></span>

<span data-ttu-id="b1ce9-104">指示由 [CompareAssemblyIdentity](compareassemblyidentity-function.md) 函数确定的两个程序集标识的等效性。</span><span class="sxs-lookup"><span data-stu-id="b1ce9-104">Indicates the equivalence of two assembly identities, as determined by the [CompareAssemblyIdentity](compareassemblyidentity-function.md) function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b1ce9-105">语法</span><span class="sxs-lookup"><span data-stu-id="b1ce9-105">Syntax</span></span>  
  
```cpp  
typedef enum _tagAssemblyComparisonResult {  
    ACR_Unknown,
    ACR_EquivalentFullMatch,  
    ACR_EquivalentWeakNamed,  
    ACR_EquivalentFXUnified,  
    ACR_EquivalentUnified,
    ACR_NonEquivalentVersion,  
    ACR_NonEquivalent,
    ACR_EquivalentPartialMatch,  
    ACR_EquivalentPartialWeakNamed,
    ACR_EquivalentPartialUnified,  
    ACR_EquivalentPartialFXUnified,  
    ACR_NonEquivalentPartialVersion
} AssemblyComparisonResult;  
```  
  
## <a name="members"></a><span data-ttu-id="b1ce9-106">成员</span><span class="sxs-lookup"><span data-stu-id="b1ce9-106">Members</span></span>  
  
|<span data-ttu-id="b1ce9-107">成员名称</span><span class="sxs-lookup"><span data-stu-id="b1ce9-107">Member name</span></span>|<span data-ttu-id="b1ce9-108">描述</span><span class="sxs-lookup"><span data-stu-id="b1ce9-108">Description</span></span>|  
|-----------------|-----------------|  
|`ACR_EquivalentFullMatch`|<span data-ttu-id="b1ce9-109">指示比较匹配项中的所有程序集字段。</span><span class="sxs-lookup"><span data-stu-id="b1ce9-109">Indicates that all assembly fields in the comparison match.</span></span>|  
|`ACR_EquivalentFXUnified`|<span data-ttu-id="b1ce9-110">指示基于公共语言运行时版本，将程序集视为等效 (CLR) .NET Framework 版本2.0 中的程序集版本号。</span><span class="sxs-lookup"><span data-stu-id="b1ce9-110">Indicates that assemblies are considered equivalent based on the common language runtime version (CLR) unification of assembly version numbers in the .NET Framework version 2.0.</span></span>|  
|`ACR_EquivalentPartialFXUnified`|<span data-ttu-id="b1ce9-111">指示程序集的部分匹配，这些程序集基于 .NET Framework 2.0 中的程序集版本号的 CLR 统一。</span><span class="sxs-lookup"><span data-stu-id="b1ce9-111">Indicates a partial match of the assemblies based on the CLR unification of assembly version numbers in the .NET Framework 2.0.</span></span>|  
|`ACR_EquivalentPartialMatch`|<span data-ttu-id="b1ce9-112">指示程序集的部分匹配项。</span><span class="sxs-lookup"><span data-stu-id="b1ce9-112">Indicates a partial match of the assemblies.</span></span>|  
|`ACR_EquivalentPartialUnified`|<span data-ttu-id="b1ce9-113">指示程序集的部分匹配，这些程序集基于旧的版本号。</span><span class="sxs-lookup"><span data-stu-id="b1ce9-113">Indicates a partial match of the assemblies based on legacy unification of version numbers.</span></span>|  
|`ACR_EquivalentPartialWeakNamed`|<span data-ttu-id="b1ce9-114">指示只与命名的程序集进行部分匹配。</span><span class="sxs-lookup"><span data-stu-id="b1ce9-114">Indicates a partial match of simply named assemblies.</span></span>|  
|`ACR_EquivalentUnified`|<span data-ttu-id="b1ce9-115">指示程序集根据 .NET Framework 旧版本中的 CLR 统一版本号被视为等效的。</span><span class="sxs-lookup"><span data-stu-id="b1ce9-115">Indicates that assemblies are considered equivalent based on the CLR unification of version numbers in legacy versions of the .NET Framework.</span></span>|  
|`ACR_EquivalentWeakNamed`|<span data-ttu-id="b1ce9-116">指示两个只命名的程序集的匹配项，这些程序集的版本号被忽略。</span><span class="sxs-lookup"><span data-stu-id="b1ce9-116">Indicates a match between two simply named assemblies whose version numbers were ignored.</span></span>|  
|`ACR_NonEquivalent`|<span data-ttu-id="b1ce9-117">指示两个程序集之间未发生匹配。</span><span class="sxs-lookup"><span data-stu-id="b1ce9-117">Indicates that no match occurred between the two assemblies.</span></span>|  
|`ACR_NonEquivalentPartialVersion`|<span data-ttu-id="b1ce9-118">指示除了仅部分匹配的版本号外，这两个程序集匹配。</span><span class="sxs-lookup"><span data-stu-id="b1ce9-118">Indicates that the two assemblies match except for their version numbers, which match only partially.</span></span>|  
|`ACR_NonEquivalentVersion`|<span data-ttu-id="b1ce9-119">指示两个程序集匹配，但其版本号不匹配。</span><span class="sxs-lookup"><span data-stu-id="b1ce9-119">Indicates that the two assemblies match except for their version numbers, which do not match.</span></span>|  
|`ACR_Unknown`|<span data-ttu-id="b1ce9-120">指示非等效的原因未知。</span><span class="sxs-lookup"><span data-stu-id="b1ce9-120">Indicates that the reason for non-equivalency is not known.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b1ce9-121">要求</span><span class="sxs-lookup"><span data-stu-id="b1ce9-121">Requirements</span></span>  

 <span data-ttu-id="b1ce9-122">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="b1ce9-122">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b1ce9-123">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="b1ce9-123">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="b1ce9-124">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="b1ce9-124">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="b1ce9-125">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b1ce9-125">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b1ce9-126">请参阅</span><span class="sxs-lookup"><span data-stu-id="b1ce9-126">See also</span></span>

- [<span data-ttu-id="b1ce9-127">CompareAssemblyIdentity 函数</span><span class="sxs-lookup"><span data-stu-id="b1ce9-127">CompareAssemblyIdentity Function</span></span>](compareassemblyidentity-function.md)
- [<span data-ttu-id="b1ce9-128">合成枚举</span><span class="sxs-lookup"><span data-stu-id="b1ce9-128">Fusion Enumerations</span></span>](fusion-enumerations.md)
