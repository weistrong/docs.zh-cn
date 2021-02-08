---
description: 了解详细信息： IMetaDataAssemblyImport：： FindAssembliesByName 方法
title: IMetaDataAssemblyImport::FindAssembliesByName 方法
ms.date: 03/30/2017
api_name:
- IMetaDataAssemblyImport.FindAssembliesByName
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataAssemblyImport::FindAssembliesByName
helpviewer_keywords:
- FindAssembliesByName method [.NET Framework metadata]
- IMetaDataAssemblyImport::FindAssembliesByName method [.NET Framework metadata]
ms.assetid: 4db97cf9-e4c1-4233-8efa-cbdc0e14a8e4
topic_type:
- apiref
ms.openlocfilehash: f9c25392cc2c70a0ebc17181b876cf9c6ba03c78
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789289"
---
# <a name="imetadataassemblyimportfindassembliesbyname-method"></a><span data-ttu-id="e6297-103">IMetaDataAssemblyImport::FindAssembliesByName 方法</span><span class="sxs-lookup"><span data-stu-id="e6297-103">IMetaDataAssemblyImport::FindAssembliesByName Method</span></span>

<span data-ttu-id="e6297-104">`szAssemblyName`使用由公共语言运行时使用的标准规则 (CLR) 来解析引用，获取具有指定参数的程序集的数组。</span><span class="sxs-lookup"><span data-stu-id="e6297-104">Gets an array of assemblies with the specified `szAssemblyName` parameter, using the standard rules employed by the common language runtime (CLR) for resolving references.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e6297-105">语法</span><span class="sxs-lookup"><span data-stu-id="e6297-105">Syntax</span></span>  
  
```cpp  
HRESULT FindAssembliesByName (  
    [in]  LPCWSTR     szAppBase,
    [in]  LPCWSTR     szPrivateBin,
    [in]  LPCWSTR     szAssemblyName,
    [out] IUnknown    *ppIUnk[],
    [in]  ULONG       cMax,
    [out] ULONG       *pcAssemblies  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e6297-106">参数</span><span class="sxs-lookup"><span data-stu-id="e6297-106">Parameters</span></span>  

 `szAppBase`  
 <span data-ttu-id="e6297-107">中要在其中搜索给定程序集的根目录。</span><span class="sxs-lookup"><span data-stu-id="e6297-107">[in] The root directory in which to search for the given assembly.</span></span> <span data-ttu-id="e6297-108">如果此值设置为 `null` ， `FindAssembliesByName` 则将仅在程序集的全局程序集缓存中查找。</span><span class="sxs-lookup"><span data-stu-id="e6297-108">If this value is set to `null`, `FindAssembliesByName` will look only in the global assembly cache for the assembly.</span></span>  
  
 `szPrivateBin`  
 <span data-ttu-id="e6297-109">中要在其中搜索程序集的根目录下的以分号分隔的子目录列表 (例如 "bin; bin2" ) 。</span><span class="sxs-lookup"><span data-stu-id="e6297-109">[in] A list of semicolon-delimited subdirectories (for example, "bin;bin2"), under the root directory, in which to search for the assembly.</span></span> <span data-ttu-id="e6297-110">除了在默认探测规则中指定的目录之外，还会探测这些目录。</span><span class="sxs-lookup"><span data-stu-id="e6297-110">These directories are probed in addition to those specified in the default probing rules.</span></span>  
  
 `szAssemblyName`  
 <span data-ttu-id="e6297-111">中要查找的程序集的名称。</span><span class="sxs-lookup"><span data-stu-id="e6297-111">[in] The name of the assembly to find.</span></span> <span data-ttu-id="e6297-112">此字符串的格式在的 "类引用" 页中定义 <xref:System.Reflection.AssemblyName> 。</span><span class="sxs-lookup"><span data-stu-id="e6297-112">The format of this string is defined in the class reference page for <xref:System.Reflection.AssemblyName>.</span></span>  
  
 `ppIUnk`  
 <span data-ttu-id="e6297-113">中要在其中放置接口指针的 [IUnknown](/cpp/atl/iunknown) 类型的数组 `IMetadataAssemblyImport` 。</span><span class="sxs-lookup"><span data-stu-id="e6297-113">[in] An array of type [IUnknown](/cpp/atl/iunknown) in which to put the `IMetadataAssemblyImport` interface pointers.</span></span>  
  
 `cMax`  
 <span data-ttu-id="e6297-114">弄可放置的接口指针的最大数目 `ppIUnk` 。</span><span class="sxs-lookup"><span data-stu-id="e6297-114">[out] The maximum number of interface pointers that can be placed in `ppIUnk`.</span></span>  
  
 `pcAssemblies`  
 <span data-ttu-id="e6297-115">弄返回的接口指针的数目。</span><span class="sxs-lookup"><span data-stu-id="e6297-115">[out] The number of interface pointers returned.</span></span> <span data-ttu-id="e6297-116">即，实际置于中的接口指针的数目 `ppIUnk` 。</span><span class="sxs-lookup"><span data-stu-id="e6297-116">That is, the number of interface pointers actually placed in `ppIUnk`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e6297-117">返回值</span><span class="sxs-lookup"><span data-stu-id="e6297-117">Return Value</span></span>  
  
|<span data-ttu-id="e6297-118">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e6297-118">HRESULT</span></span>|<span data-ttu-id="e6297-119">说明</span><span class="sxs-lookup"><span data-stu-id="e6297-119">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="e6297-120">`FindAssembliesByName` 已成功返回。</span><span class="sxs-lookup"><span data-stu-id="e6297-120">`FindAssembliesByName` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="e6297-121">没有程序集。</span><span class="sxs-lookup"><span data-stu-id="e6297-121">There are no assemblies.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e6297-122">备注</span><span class="sxs-lookup"><span data-stu-id="e6297-122">Remarks</span></span>  

 <span data-ttu-id="e6297-123">在给定程序集名称的 `FindAssembliesByName` 情况下，方法通过遵循用于解析程序集引用的标准规则查找程序集。</span><span class="sxs-lookup"><span data-stu-id="e6297-123">Given an assembly name, the `FindAssembliesByName` method finds the assembly by following the standard rules for resolving assembly references.</span></span> <span data-ttu-id="e6297-124"> (有关详细信息，请参阅 [运行时如何定位程序集](../../deployment/how-the-runtime-locates-assemblies.md)。 ) `FindAssembliesByName` 使调用方可以配置程序集解析程序上下文的各个方面，例如应用程序基和专用搜索路径。</span><span class="sxs-lookup"><span data-stu-id="e6297-124">(For more information, see [How the Runtime Locates Assemblies](../../deployment/how-the-runtime-locates-assemblies.md).) `FindAssembliesByName` allows the caller to configure various aspects of the assembly resolver context, such as application base and private search path.</span></span>  
  
 <span data-ttu-id="e6297-125">`FindAssembliesByName`方法要求在进程中初始化 CLR，以便调用程序集解析逻辑。</span><span class="sxs-lookup"><span data-stu-id="e6297-125">The `FindAssembliesByName` method requires the CLR to be initialized in the process in order to invoke the assembly resolution logic.</span></span> <span data-ttu-id="e6297-126">因此，在调用之前，必须先调用 [CoInitializeEE](../hosting/coinitializeee-function.md) (传递 COINITEE_DEFAULT) `FindAssembliesByName` ，然后再调用 [CoUninitializeCor](../hosting/couninitializecor-function.md)。</span><span class="sxs-lookup"><span data-stu-id="e6297-126">Therefore, you must call [CoInitializeEE](../hosting/coinitializeee-function.md) (passing COINITEE_DEFAULT) before calling `FindAssembliesByName`, and then follow with a call to [CoUninitializeCor](../hosting/couninitializecor-function.md).</span></span>  
  
 <span data-ttu-id="e6297-127">`FindAssembliesByName` 返回一个 [IMetaDataImport](imetadataimport-interface.md) 指针，该指针指向包含传入的程序集名称的程序集清单的文件。</span><span class="sxs-lookup"><span data-stu-id="e6297-127">`FindAssembliesByName` returns an [IMetaDataImport](imetadataimport-interface.md) pointer to the file containing the assembly manifest for the assembly name that is passed in.</span></span> <span data-ttu-id="e6297-128">如果未完全指定给定的程序集名称 (例如，如果不包含版本) ，则可能会返回多个程序集。</span><span class="sxs-lookup"><span data-stu-id="e6297-128">If the given assembly name is not fully specified (for example, if it does not include a version), multiple assemblies might be returned.</span></span>  
  
 <span data-ttu-id="e6297-129">`FindAssembliesByName` 在编译时尝试查找引用的程序集的编译器通常使用。</span><span class="sxs-lookup"><span data-stu-id="e6297-129">`FindAssembliesByName` is commonly used by a compiler that attempts to find a referenced assembly at compile time.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e6297-130">要求</span><span class="sxs-lookup"><span data-stu-id="e6297-130">Requirements</span></span>  

 <span data-ttu-id="e6297-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e6297-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e6297-132">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="e6297-132">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e6297-133">**库：** 用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="e6297-133">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e6297-134">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e6297-134">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e6297-135">请参阅</span><span class="sxs-lookup"><span data-stu-id="e6297-135">See also</span></span>

- [<span data-ttu-id="e6297-136">运行时如何定位程序集</span><span class="sxs-lookup"><span data-stu-id="e6297-136">How the Runtime Locates Assemblies</span></span>](../../deployment/how-the-runtime-locates-assemblies.md)
- [<span data-ttu-id="e6297-137">IMetaDataAssemblyImport 接口</span><span class="sxs-lookup"><span data-stu-id="e6297-137">IMetaDataAssemblyImport Interface</span></span>](imetadataassemblyimport-interface.md)
