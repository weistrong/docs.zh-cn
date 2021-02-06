---
description: 了解详细信息： AssemblyOptions 枚举
title: AssemblyOptions 枚举
ms.date: 03/30/2017
api_name:
- AssemblyOptions
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- AssemblyOptions
helpviewer_keywords:
- Alink API, AssemblyOptions enumeration
- AssemblyOptions enumeration
ms.assetid: 84f83921-64cb-49e3-ac8b-22a0b77b18a8
topic_type:
- apiref
ms.openlocfilehash: aba9ecb3176f533e2d53e2e45fef3d1dc4e55077
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99638413"
---
# <a name="assemblyoptions-enumeration"></a><span data-ttu-id="1036a-103">AssemblyOptions 枚举</span><span class="sxs-lookup"><span data-stu-id="1036a-103">AssemblyOptions Enumeration</span></span>

<span data-ttu-id="1036a-104">枚举程序集选项。</span><span class="sxs-lookup"><span data-stu-id="1036a-104">Enumerates the assembly options.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1036a-105">语法</span><span class="sxs-lookup"><span data-stu-id="1036a-105">Syntax</span></span>  
  
```cpp  
typedef enum _AssemblyOptions {  
    optAssemTitle = 0,  
    optAssemDescription,  
    optAssemConfig,  
    optAssemOS,  
    optAssemProcessor,  
    optAssemLocale,  
    optAssemVersion,  
    optAssemCompany,  
    optAssemProduct,  
    optAssemProductVersion,  
    optAssemCopyright,  
    optAssemTrademark,  
    optAssemKeyFile,  
    optAssemKeyName,  
    optAssemAlgID,  
    optAssemFlags,  
    optAssemHalfSign,  
    optAssemFileVersion,  
    optAssemSatelliteVer,  
    optLastAssemOption  
}   AssemblyOptions;  
```  
  
## <a name="fields"></a><span data-ttu-id="1036a-106">字段</span><span class="sxs-lookup"><span data-stu-id="1036a-106">Fields</span></span>  
  
|<span data-ttu-id="1036a-107">字段</span><span class="sxs-lookup"><span data-stu-id="1036a-107">Field</span></span>|<span data-ttu-id="1036a-108">说明</span><span class="sxs-lookup"><span data-stu-id="1036a-108">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="1036a-109">optAssemTitle</span><span class="sxs-lookup"><span data-stu-id="1036a-109">optAssemTitle</span></span>|<span data-ttu-id="1036a-110">String-表示程序集标题。</span><span class="sxs-lookup"><span data-stu-id="1036a-110">String - Represents the assembly title.</span></span>|  
|<span data-ttu-id="1036a-111">optAssemDescription</span><span class="sxs-lookup"><span data-stu-id="1036a-111">optAssemDescription</span></span>|<span data-ttu-id="1036a-112">String-包含程序集说明。</span><span class="sxs-lookup"><span data-stu-id="1036a-112">String - Contains the assembly description.</span></span>|  
|<span data-ttu-id="1036a-113">optAssemConfig</span><span class="sxs-lookup"><span data-stu-id="1036a-113">optAssemConfig</span></span>|<span data-ttu-id="1036a-114">String-包含程序集配置。</span><span class="sxs-lookup"><span data-stu-id="1036a-114">String - Contains the assembly configuration.</span></span>|  
|<span data-ttu-id="1036a-115">optAssemOS</span><span class="sxs-lookup"><span data-stu-id="1036a-115">optAssemOS</span></span>|<span data-ttu-id="1036a-116">字符串编码为： "dwOSPlatformId. dwOSMajorVersion. dwOSMinorVersion"。</span><span class="sxs-lookup"><span data-stu-id="1036a-116">String - Encoded as: "dwOSPlatformId.dwOSMajorVersion.dwOSMinorVersion".</span></span>|  
|<span data-ttu-id="1036a-117">optAssemProcessor</span><span class="sxs-lookup"><span data-stu-id="1036a-117">optAssemProcessor</span></span>|<span data-ttu-id="1036a-118">ULONG</span><span class="sxs-lookup"><span data-stu-id="1036a-118">ULONG</span></span>|  
|<span data-ttu-id="1036a-119">optAssemLocale</span><span class="sxs-lookup"><span data-stu-id="1036a-119">optAssemLocale</span></span>|<span data-ttu-id="1036a-120">String-包含程序集的区域设置。</span><span class="sxs-lookup"><span data-stu-id="1036a-120">String - Contains the assembly locale.</span></span>|  
|<span data-ttu-id="1036a-121">optAssemVersion</span><span class="sxs-lookup"><span data-stu-id="1036a-121">optAssemVersion</span></span>|<span data-ttu-id="1036a-122">字符串编码为： "主要版本. 次要版本. 内部版本. 修订版本"。</span><span class="sxs-lookup"><span data-stu-id="1036a-122">String - Encoded as: "Major.Minor.Build.Revision".</span></span>|  
|<span data-ttu-id="1036a-123">optAssemCompany</span><span class="sxs-lookup"><span data-stu-id="1036a-123">optAssemCompany</span></span>|<span data-ttu-id="1036a-124">String-包含公司。</span><span class="sxs-lookup"><span data-stu-id="1036a-124">String - Contains the company.</span></span>|  
|<span data-ttu-id="1036a-125">optAssemProduct</span><span class="sxs-lookup"><span data-stu-id="1036a-125">optAssemProduct</span></span>|<span data-ttu-id="1036a-126">String-包含产品名称。</span><span class="sxs-lookup"><span data-stu-id="1036a-126">String - Contains the product name.</span></span>|  
|<span data-ttu-id="1036a-127">optAssemProductVersion</span><span class="sxs-lookup"><span data-stu-id="1036a-127">optAssemProductVersion</span></span>|<span data-ttu-id="1036a-128">String (也称为 InformationalVersion) 。</span><span class="sxs-lookup"><span data-stu-id="1036a-128">String (also known as InformationalVersion).</span></span>|  
|<span data-ttu-id="1036a-129">optAssemCopyright</span><span class="sxs-lookup"><span data-stu-id="1036a-129">optAssemCopyright</span></span>|<span data-ttu-id="1036a-130">String-包含版权信息。</span><span class="sxs-lookup"><span data-stu-id="1036a-130">String - Contains the copyright information.</span></span>|  
|<span data-ttu-id="1036a-131">optAssemTrademark</span><span class="sxs-lookup"><span data-stu-id="1036a-131">optAssemTrademark</span></span>|<span data-ttu-id="1036a-132">String-包含商标信息。</span><span class="sxs-lookup"><span data-stu-id="1036a-132">String - Contains the trademark information.</span></span>|  
|<span data-ttu-id="1036a-133">optAssemKeyFile</span><span class="sxs-lookup"><span data-stu-id="1036a-133">optAssemKeyFile</span></span>|<span data-ttu-id="1036a-134"> (文件名) 字符串。</span><span class="sxs-lookup"><span data-stu-id="1036a-134">String (file name).</span></span>|  
|<span data-ttu-id="1036a-135">optAssemKeyName</span><span class="sxs-lookup"><span data-stu-id="1036a-135">optAssemKeyName</span></span>|<span data-ttu-id="1036a-136"> (项名称) 的字符串。</span><span class="sxs-lookup"><span data-stu-id="1036a-136">String (The key name).</span></span>|  
|<span data-ttu-id="1036a-137">optAssemAlgID</span><span class="sxs-lookup"><span data-stu-id="1036a-137">optAssemAlgID</span></span>|<span data-ttu-id="1036a-138">ULONG</span><span class="sxs-lookup"><span data-stu-id="1036a-138">ULONG</span></span>|  
|<span data-ttu-id="1036a-139">optAssemFlags</span><span class="sxs-lookup"><span data-stu-id="1036a-139">optAssemFlags</span></span>|<span data-ttu-id="1036a-140">ULONG</span><span class="sxs-lookup"><span data-stu-id="1036a-140">ULONG</span></span>|  
|<span data-ttu-id="1036a-141">optAssemHalfSign</span><span class="sxs-lookup"><span data-stu-id="1036a-141">optAssemHalfSign</span></span>|<span data-ttu-id="1036a-142">Bool (也称为 DelaySign) 。</span><span class="sxs-lookup"><span data-stu-id="1036a-142">Bool (Also known as DelaySign).</span></span>|  
|<span data-ttu-id="1036a-143">optAssemFileVersion</span><span class="sxs-lookup"><span data-stu-id="1036a-143">optAssemFileVersion</span></span>|<span data-ttu-id="1036a-144">编码为 "ProductVersion" 的字符串，与 "" 相同。</span><span class="sxs-lookup"><span data-stu-id="1036a-144">String - Encoded as "Major.Minor.Build.Revision"--same as ProductVersion.</span></span>|  
|<span data-ttu-id="1036a-145">optAssemSatelliteVer</span><span class="sxs-lookup"><span data-stu-id="1036a-145">optAssemSatelliteVer</span></span>|<span data-ttu-id="1036a-146">字符串编码为 "主要版本. 次要版本. 内部版本. 内部版本. 修订版本"。</span><span class="sxs-lookup"><span data-stu-id="1036a-146">String - Encoded as "Major.Minor.Build.Revision".</span></span>|  
|<span data-ttu-id="1036a-147">optLastAssemOption</span><span class="sxs-lookup"><span data-stu-id="1036a-147">optLastAssemOption</span></span>|<span data-ttu-id="1036a-148">元素数的计数器。</span><span class="sxs-lookup"><span data-stu-id="1036a-148">A counter of the number of elements.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="1036a-149">要求</span><span class="sxs-lookup"><span data-stu-id="1036a-149">Requirements</span></span>  

 <span data-ttu-id="1036a-150">**标头：** alink。h</span><span class="sxs-lookup"><span data-stu-id="1036a-150">**Header:** alink.h</span></span>  
  
 <span data-ttu-id="1036a-151">**库**： alink.dll</span><span class="sxs-lookup"><span data-stu-id="1036a-151">**Library**: alink.dll</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1036a-152">请参阅</span><span class="sxs-lookup"><span data-stu-id="1036a-152">See also</span></span>

- [<span data-ttu-id="1036a-153">Al.exe（程序集链接器）</span><span class="sxs-lookup"><span data-stu-id="1036a-153">Al.exe (Assembly Linker)</span></span>](../../tools/al-exe-assembly-linker.md)
