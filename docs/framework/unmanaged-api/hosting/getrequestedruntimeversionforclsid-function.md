---
description: 了解详细信息： GetRequestedRuntimeVersionForCLSID 函数
title: GetRequestedRuntimeVersionForCLSID 函数
ms.date: 03/30/2017
api_name:
- GetRequestedRuntimeVersionForCLSID
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetRequestedRuntimeVersionForCLSID
helpviewer_keywords:
- GetRequestedRuntimeVersionForCLSID function [.NET Framework hosting]
ms.assetid: 5bb12f9a-0612-434b-b4ed-2db636a20bec
topic_type:
- apiref
ms.openlocfilehash: 10fdc947181d3f1fa12b33f11cf31b68fc4285cd
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785258"
---
# <a name="getrequestedruntimeversionforclsid-function"></a><span data-ttu-id="e9304-103">GetRequestedRuntimeVersionForCLSID 函数</span><span class="sxs-lookup"><span data-stu-id="e9304-103">GetRequestedRuntimeVersionForCLSID Function</span></span>

<span data-ttu-id="e9304-104">获取具有指定的类的相应公共语言运行时 (CLR) 版本信息 `CLSID` 。</span><span class="sxs-lookup"><span data-stu-id="e9304-104">Gets the appropriate common language runtime (CLR) version information for the class with the specified `CLSID`.</span></span>  
  
 <span data-ttu-id="e9304-105">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="e9304-105">This function has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e9304-106">语法</span><span class="sxs-lookup"><span data-stu-id="e9304-106">Syntax</span></span>  
  
```cpp  
HRESULT GetRequestedRuntimeVersionForCLSID (  
    [in]  REFCLSID   rclsid,
    [out]  LPWSTR     pVersion,
    [in]  DWORD      cchBuffer,
    [out] DWORD*     dwLength,
    [in]  CLSID_RESOLUTION_FLAGS dwResolutionFlags  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="e9304-107">参数</span><span class="sxs-lookup"><span data-stu-id="e9304-107">Parameters</span></span>  

 `rclsid`  
 <span data-ttu-id="e9304-108">中 `CLSID` 组件的。</span><span class="sxs-lookup"><span data-stu-id="e9304-108">[in]  The `CLSID` of the component.</span></span>  
  
 `pVersion`  
 <span data-ttu-id="e9304-109">弄 一个缓冲区，其中包含成功完成后的版本号字符串。</span><span class="sxs-lookup"><span data-stu-id="e9304-109">[out]  A buffer that contains the version number string upon successful completion.</span></span>  
  
 `cchBuffer`  
 <span data-ttu-id="e9304-110">中 缓冲区的大小（宽字符） `pVersion` 。</span><span class="sxs-lookup"><span data-stu-id="e9304-110">[in]  The size, in wide characters, of the `pVersion` buffer.</span></span>  
  
 `dwLength`  
 <span data-ttu-id="e9304-111">弄返回的缓冲区的长度（以字节为单位）。</span><span class="sxs-lookup"><span data-stu-id="e9304-111">[out] The length, in bytes, of the returned buffer.</span></span>  
  
 `dwResolutionFlags`  
 <span data-ttu-id="e9304-112">中 CLSID_RESOLUTION_FLAGS 值之一。</span><span class="sxs-lookup"><span data-stu-id="e9304-112">[in]  One of the CLSID_RESOLUTION_FLAGS values.</span></span> <span data-ttu-id="e9304-113">支持以下值：</span><span class="sxs-lookup"><span data-stu-id="e9304-113">The following values are supported:</span></span>  
  
- <span data-ttu-id="e9304-114">CLSID_RESOLUTION_DEFAULT： (0x0) 指定应使用默认互操作行为。</span><span class="sxs-lookup"><span data-stu-id="e9304-114">CLSID_RESOLUTION_DEFAULT: (0x0) Specifies that default interop behavior should be used.</span></span>  
  
- <span data-ttu-id="e9304-115">CLSID_RESOLUTION_REGISTERED： (0x1) 指定应搜索注册表并应用填充程序策略。</span><span class="sxs-lookup"><span data-stu-id="e9304-115">CLSID_RESOLUTION_REGISTERED: (0x1) Specifies that the registry should be searched and shim policy should be applied.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="e9304-116">返回值</span><span class="sxs-lookup"><span data-stu-id="e9304-116">Return Value</span></span>  
  
|<span data-ttu-id="e9304-117">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e9304-117">HRESULT</span></span>|<span data-ttu-id="e9304-118">说明</span><span class="sxs-lookup"><span data-stu-id="e9304-118">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="e9304-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="e9304-119">S_OK</span></span>|<span data-ttu-id="e9304-120">函数已成功返回。</span><span class="sxs-lookup"><span data-stu-id="e9304-120">The function returned successfully.</span></span>|  
|<span data-ttu-id="e9304-121">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="e9304-121">E_INVALIDARG</span></span>|<span data-ttu-id="e9304-122">其中一个参数的类型或格式无效。</span><span class="sxs-lookup"><span data-stu-id="e9304-122">One of the parameters has an invalid type or format.</span></span>|  
|<span data-ttu-id="e9304-123">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="e9304-123">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="e9304-124">`pVersion`缓冲区不够大，无法容纳整个版本字符串。</span><span class="sxs-lookup"><span data-stu-id="e9304-124">The `pVersion` buffer is not large enough to hold the entire version string.</span></span>|  
|<span data-ttu-id="e9304-125">REGDB_E_CLASSNOTREG</span><span class="sxs-lookup"><span data-stu-id="e9304-125">REGDB_E_CLASSNOTREG</span></span>|<span data-ttu-id="e9304-126">没有用指定的注册的类 `CLSID` 。</span><span class="sxs-lookup"><span data-stu-id="e9304-126">There is no class registered with the specified `CLSID`.</span></span>|  
|<span data-ttu-id="e9304-127">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="e9304-127">E_POINTER</span></span>|<span data-ttu-id="e9304-128">`dwLength` 为 null，或 `cchBuffer` 足以容纳版本字符串，但 `pVersion` 为 null。</span><span class="sxs-lookup"><span data-stu-id="e9304-128">`dwLength` is null, or `cchBuffer` is large enough to hold the version string, but `pVersion` is null.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="e9304-129">要求</span><span class="sxs-lookup"><span data-stu-id="e9304-129">Requirements</span></span>  

 <span data-ttu-id="e9304-130">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e9304-130">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e9304-131">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="e9304-131">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e9304-132">**.NET Framework 版本：**[!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e9304-132">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e9304-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="e9304-133">See also</span></span>

- [<span data-ttu-id="e9304-134">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="e9304-134">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
