---
description: 了解详细信息： ICLRRuntimeInfo：： GetVersionString 方法
title: ICLRRuntimeInfo::GetVersionString 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.GetVersionString
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::GetVersionString
helpviewer_keywords:
- ICLRRuntimeInfo::GetVersionString method [.NET Framework hosting]
- GetVersionString method, ICLRRuntimeInfo interface [.NET Framework hosting]
ms.assetid: 98b097ef-2276-4dd9-8551-b03c972e8179
topic_type:
- apiref
ms.openlocfilehash: 1c7603f4e9bb1142c415ba9da7a05a52d2d5e776
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99753869"
---
# <a name="iclrruntimeinfogetversionstring-method"></a><span data-ttu-id="2d5ae-103">ICLRRuntimeInfo::GetVersionString 方法</span><span class="sxs-lookup"><span data-stu-id="2d5ae-103">ICLRRuntimeInfo::GetVersionString Method</span></span>

<span data-ttu-id="2d5ae-104">获取公共语言运行时 (CLR) 版本信息与给定的 [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) 接口相关联。</span><span class="sxs-lookup"><span data-stu-id="2d5ae-104">Gets common language runtime (CLR) version information associated with a given [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) interface.</span></span>  
  
 <span data-ttu-id="2d5ae-105">此方法取代了以下函数：</span><span class="sxs-lookup"><span data-stu-id="2d5ae-105">This method supersedes the following functions:</span></span>  
  
- [<span data-ttu-id="2d5ae-106">GetRequestedRuntimeInfo</span><span class="sxs-lookup"><span data-stu-id="2d5ae-106">GetRequestedRuntimeInfo</span></span>](getrequestedruntimeinfo-function.md)  
  
- [<span data-ttu-id="2d5ae-107">GetRequestedRuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="2d5ae-107">GetRequestedRuntimeVersion</span></span>](getrequestedruntimeversion-function.md)  
  
## <a name="syntax"></a><span data-ttu-id="2d5ae-108">语法</span><span class="sxs-lookup"><span data-stu-id="2d5ae-108">Syntax</span></span>  
  
```cpp  
HRESULT GetVersionString(  
    [out, size_is(*pcchBuffer)] LPWSTR pwzBuffer,  
    [in, out]  DWORD *pcchBuffer);  
```  
  
## <a name="parameters"></a><span data-ttu-id="2d5ae-109">参数</span><span class="sxs-lookup"><span data-stu-id="2d5ae-109">Parameters</span></span>  

 `pwzBuffer`  
 <span data-ttu-id="2d5ae-110">弄"V *A*" 格式的 .NET Framework 编译版本。*B.*[。*X*] "。</span><span class="sxs-lookup"><span data-stu-id="2d5ae-110">[out] The .NET Framework compilation version in the format "v *A*.*B*[.*X*]".</span></span> <span data-ttu-id="2d5ae-111">*A*、 *B* 和 *X* 是与主版本、次版本和生成号对应的十进制数字。</span><span class="sxs-lookup"><span data-stu-id="2d5ae-111">*A*, *B*, and *X* are decimal numbers that correspond to the major version, the minor version, and the build number.</span></span> <span data-ttu-id="2d5ae-112">*X* 是可选的。</span><span class="sxs-lookup"><span data-stu-id="2d5ae-112">*X* is optional.</span></span> <span data-ttu-id="2d5ae-113">如果 *X* 不存在，则没有尾随句点。</span><span class="sxs-lookup"><span data-stu-id="2d5ae-113">If *X* is not present, there is no trailing period.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="2d5ae-114">此参数必须匹配 .NET Framework 版本的目录名称，因为它显示在 C:\Windows\Microsoft.NET\Framework. 下。</span><span class="sxs-lookup"><span data-stu-id="2d5ae-114">This parameter must match the directory name for the .NET Framework version, as it appears under C:\Windows\Microsoft.NET\Framework.</span></span>  
  
 <span data-ttu-id="2d5ae-115">示例值为 "v1.0.3705"、"v 1.1.4322"、"v 2.0.50727" 和 "v4.0"。*x*"，其中 *x* 依赖于安装的生成号。</span><span class="sxs-lookup"><span data-stu-id="2d5ae-115">Example values are "v1.0.3705", "v1.1.4322", "v2.0.50727", and "v4.0.*x*", where *x* depends on the build number installed.</span></span> <span data-ttu-id="2d5ae-116">请注意，"v" 前缀是必需的。</span><span class="sxs-lookup"><span data-stu-id="2d5ae-116">Note that the "v" prefix is mandatory.</span></span>  
  
 `pchBuffer`  
 <span data-ttu-id="2d5ae-117">[in，out]指定的大小 `pwzBuffer` 以避免缓冲区溢出。</span><span class="sxs-lookup"><span data-stu-id="2d5ae-117">[in, out] Specifies the size of `pwzBuffer` to avoid buffer overruns.</span></span> <span data-ttu-id="2d5ae-118">如果 `pwzBuffer` 为 `null` ，则 `pchBuffer` 返回所需的大小 `pwzBuffer` 以允许预先分配。</span><span class="sxs-lookup"><span data-stu-id="2d5ae-118">If `pwzBuffer` is `null`, `pchBuffer` returns the required size of `pwzBuffer` to allow preallocation.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="2d5ae-119">返回值</span><span class="sxs-lookup"><span data-stu-id="2d5ae-119">Return Value</span></span>  

 <span data-ttu-id="2d5ae-120">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="2d5ae-120">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="2d5ae-121">HRESULT</span><span class="sxs-lookup"><span data-stu-id="2d5ae-121">HRESULT</span></span>|<span data-ttu-id="2d5ae-122">说明</span><span class="sxs-lookup"><span data-stu-id="2d5ae-122">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="2d5ae-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="2d5ae-123">S_OK</span></span>|<span data-ttu-id="2d5ae-124">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="2d5ae-124">The method completed successfully.</span></span>|  
|<span data-ttu-id="2d5ae-125">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="2d5ae-125">E_POINTER</span></span>|<span data-ttu-id="2d5ae-126">`pwzBuffer` 或 `pchBuffer` 为 null。</span><span class="sxs-lookup"><span data-stu-id="2d5ae-126">`pwzBuffer` or `pchBuffer` is null.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="2d5ae-127">要求</span><span class="sxs-lookup"><span data-stu-id="2d5ae-127">Requirements</span></span>  

 <span data-ttu-id="2d5ae-128">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="2d5ae-128">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2d5ae-129">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="2d5ae-129">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="2d5ae-130">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="2d5ae-130">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="2d5ae-131">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2d5ae-131">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2d5ae-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="2d5ae-132">See also</span></span>

- [<span data-ttu-id="2d5ae-133">ICLRRuntimeInfo 接口</span><span class="sxs-lookup"><span data-stu-id="2d5ae-133">ICLRRuntimeInfo Interface</span></span>](iclrruntimeinfo-interface.md)
- [<span data-ttu-id="2d5ae-134">承载接口</span><span class="sxs-lookup"><span data-stu-id="2d5ae-134">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="2d5ae-135">.NET Framework 4 和 4.5 中添加的 CLR 承载接口</span><span class="sxs-lookup"><span data-stu-id="2d5ae-135">CLR Hosting Interfaces Added in the .NET Framework 4 and 4.5</span></span>](clr-hosting-interfaces-added-in-the-net-framework-4-and-4-5.md)
- [<span data-ttu-id="2d5ae-136">承载</span><span class="sxs-lookup"><span data-stu-id="2d5ae-136">Hosting</span></span>](index.md)
