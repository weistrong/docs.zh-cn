---
description: 了解详细信息： AssemblyFlags 枚举
title: AssemblyFlags 枚举
ms.date: 03/30/2017
api_name:
- AssemblyFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- AssemblyFlags
helpviewer_keywords:
- AssemblyFlags enumeration [.NET Framework metadata]
ms.assetid: 40f9bd9e-16ec-447e-81b0-168c875e9866
topic_type:
- apiref
ms.openlocfilehash: 17cc0dec305c21d21693fe8f4f8d82c039f73278
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99678999"
---
# <a name="assemblyflags-enumeration"></a><span data-ttu-id="278fe-103">AssemblyFlags 枚举</span><span class="sxs-lookup"><span data-stu-id="278fe-103">AssemblyFlags Enumeration</span></span>

<span data-ttu-id="278fe-104">包含用于描述程序集的运行时功能的值。</span><span class="sxs-lookup"><span data-stu-id="278fe-104">Contains values that describe run-time features of an assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="278fe-105">语法</span><span class="sxs-lookup"><span data-stu-id="278fe-105">Syntax</span></span>  
  
```cpp  
typedef enum {  
    afImplicitExportedTypes = 0x0001,  
    afImplicitResources = 0x0002,  
    afNonSideBySideAppDomain = 0x0010,  
    afNonSideBySideProcess = 0x0020,  
    afNonSideBySideMachine = 0x0030  
} AssemblyFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="278fe-106">成员</span><span class="sxs-lookup"><span data-stu-id="278fe-106">Members</span></span>  
  
|<span data-ttu-id="278fe-107">成员</span><span class="sxs-lookup"><span data-stu-id="278fe-107">Member</span></span>|<span data-ttu-id="278fe-108">说明</span><span class="sxs-lookup"><span data-stu-id="278fe-108">Description</span></span>|  
|------------|-----------------|  
|`afImplicitExportedTypes`|<span data-ttu-id="278fe-109">指定导出的类型定义在构成程序集的文件中是隐式的。</span><span class="sxs-lookup"><span data-stu-id="278fe-109">Specifies that exported type definitions are implicit within the files that comprise the assembly.</span></span> <span data-ttu-id="278fe-110">在 .NET Framework 版本1.0 和1.1 中，始终假定此值已设置。</span><span class="sxs-lookup"><span data-stu-id="278fe-110">In the .NET Framework versions 1.0 and 1.1, this value is always assumed to be set.</span></span>|  
|`afImplicitResources`|<span data-ttu-id="278fe-111">指定资源定义在构成程序集的文件中是隐式的。</span><span class="sxs-lookup"><span data-stu-id="278fe-111">Specifies that resource definitions are implicit within the files that comprise the assembly.</span></span> <span data-ttu-id="278fe-112">在 .NET Framework 1.0 和1.1 中，始终假定此值已设置。</span><span class="sxs-lookup"><span data-stu-id="278fe-112">In the .NET Framework 1.0 and 1.1, this value is always assumed to be set.</span></span>|  
|`afNonSideBySideAppDomain`|<span data-ttu-id="278fe-113">指定程序集不能与其他版本在同一应用程序域中一起执行。</span><span class="sxs-lookup"><span data-stu-id="278fe-113">Specifies that the assembly cannot execute with other versions if they are running in the same application domain.</span></span>|  
|`afNonSideBySideProcess`|<span data-ttu-id="278fe-114">指定程序集不能与其他版本在同一进程中一起执行。</span><span class="sxs-lookup"><span data-stu-id="278fe-114">Specifies that the assembly cannot execute with other versions if they are running in the same process.</span></span>|  
|`afNonSideBySideMachine`|<span data-ttu-id="278fe-115">如果程序集在同一台计算机上运行，则指定该程序集无法与其他版本一起执行。</span><span class="sxs-lookup"><span data-stu-id="278fe-115">Specifies that the assembly cannot execute with other versions if they are running on the same computer.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="278fe-116">备注</span><span class="sxs-lookup"><span data-stu-id="278fe-116">Remarks</span></span>  

 <span data-ttu-id="278fe-117">0x0010 和0x0070 （含）之间的值用于描述所引用程序集的并行兼容性功能。</span><span class="sxs-lookup"><span data-stu-id="278fe-117">The values between 0x0010 and 0x0070, inclusive, are used to describe side-by-side compatibility features of the referenced assembly.</span></span> <span data-ttu-id="278fe-118">如果未设置这些值，则假定程序集是并行兼容的。</span><span class="sxs-lookup"><span data-stu-id="278fe-118">If none of these values are set, the assembly is assumed to be side-by-side compatible.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="278fe-119">要求</span><span class="sxs-lookup"><span data-stu-id="278fe-119">Requirements</span></span>  

 <span data-ttu-id="278fe-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="278fe-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="278fe-121">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="278fe-121">**Header:** MsCorEE.h</span></span>  
  
 <span data-ttu-id="278fe-122">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="278fe-122">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="278fe-123">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="278fe-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="278fe-124">请参阅</span><span class="sxs-lookup"><span data-stu-id="278fe-124">See also</span></span>

- [<span data-ttu-id="278fe-125">元数据枚举</span><span class="sxs-lookup"><span data-stu-id="278fe-125">Metadata Enumerations</span></span>](metadata-enumerations.md)
- [<span data-ttu-id="278fe-126">IMetaDataAssemblyEmit 接口</span><span class="sxs-lookup"><span data-stu-id="278fe-126">IMetaDataAssemblyEmit Interface</span></span>](imetadataassemblyemit-interface.md)
