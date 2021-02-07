---
description: 了解详细信息： ICLRMetaHost：： GetVersionFromFile 方法
title: ICLRMetaHost::GetVersionFromFile 方法
ms.date: 03/30/2017
api_name:
- ICLRMetaHost.GetVersionFromFile
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHost::GetVersionFromFile
helpviewer_keywords:
- ICLRMetaHost::GetVersionFromFile method [.NET Framework hosting]
- GetVersionFromFile method [.NET Framework hosting]
ms.assetid: 55bb3eb4-f665-42fc-973c-465567570e82
topic_type:
- apiref
ms.openlocfilehash: 0122c4aba3b8454a84540b22e815c61a2cb25df8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99689048"
---
# <a name="iclrmetahostgetversionfromfile-method"></a><span data-ttu-id="f89e8-103">ICLRMetaHost::GetVersionFromFile 方法</span><span class="sxs-lookup"><span data-stu-id="f89e8-103">ICLRMetaHost::GetVersionFromFile Method</span></span>

<span data-ttu-id="f89e8-104">获取程序集的原始 .NET Framework 编译版本 (存储在元) 数据中的的文件路径。</span><span class="sxs-lookup"><span data-stu-id="f89e8-104">Gets an assembly's original .NET Framework compilation version (stored in the metadata), given its file path.</span></span> <span data-ttu-id="f89e8-105">此方法取代了 [GetFileVersion](getfileversion-function.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="f89e8-105">This method supersedes the [GetFileVersion](getfileversion-function.md) function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f89e8-106">语法</span><span class="sxs-lookup"><span data-stu-id="f89e8-106">Syntax</span></span>  
  
```cpp  
HRESULT GetVersionFromFile (  
    [in] LPCWSTR pwzFilePath,  
    [out, size_is(*pcchBuffer)] LPWSTR pwzBuffer,  
    [in, out] DWORD *pcchBuffer);  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="f89e8-107">参数</span><span class="sxs-lookup"><span data-stu-id="f89e8-107">Parameters</span></span>  

 `pwzFilePath`  
 <span data-ttu-id="f89e8-108">中完整的程序集文件路径。</span><span class="sxs-lookup"><span data-stu-id="f89e8-108">[in] The complete assembly file path.</span></span>  
  
 `pwzbuffer`  
 <span data-ttu-id="f89e8-109">弄存储在元数据中的 .NET Framework 编译版本，格式为 "v *A*"。*B.*[。*X*] "。</span><span class="sxs-lookup"><span data-stu-id="f89e8-109">[out] The .NET Framework compilation version stored in the metadata, in the format "v *A*.*B*[.*X*]".</span></span> <span data-ttu-id="f89e8-110">*A*、 *B* 和 *X* 是与主版本、次版本和生成号对应的十进制数字。</span><span class="sxs-lookup"><span data-stu-id="f89e8-110">*A*, *B*, and *X* are decimal numbers that correspond to the major version, the minor version, and the build number.</span></span> <span data-ttu-id="f89e8-111">此字符串的长度仅限 MAX_PATH。</span><span class="sxs-lookup"><span data-stu-id="f89e8-111">The length of this string is limited to MAX_PATH.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="f89e8-112">此输出匹配 .NET Framework 版本的目录名称，因为它显示在 C:\Windows\Microsoft.NET\Framework. 下。</span><span class="sxs-lookup"><span data-stu-id="f89e8-112">This output matches the directory name for the .NET Framework version, as it appears under C:\Windows\Microsoft.NET\Framework.</span></span>  
  
 <span data-ttu-id="f89e8-113">示例值为 "v1.0.3705"、"v 1.1.4322"、"v 2.0.50727" 和 "v4.0"。*X*"，其中 *X* 依赖于安装的生成号。</span><span class="sxs-lookup"><span data-stu-id="f89e8-113">Example values are "v1.0.3705", "v1.1.4322", "v2.0.50727", and "v4.0.*X*", where *X* depends on the build number installed.</span></span> <span data-ttu-id="f89e8-114">请注意，"v" 前缀是必需的。</span><span class="sxs-lookup"><span data-stu-id="f89e8-114">Note that the "v" prefix is required.</span></span>  
  
 `pcchBuffer`  
 <span data-ttu-id="f89e8-115">[in，out] `pwzbuffer` 用于避免缓冲区溢出的的大小。</span><span class="sxs-lookup"><span data-stu-id="f89e8-115">[in, out] The size of `pwzbuffer` to avoid buffer overruns.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f89e8-116">返回值</span><span class="sxs-lookup"><span data-stu-id="f89e8-116">Return Value</span></span>  

 <span data-ttu-id="f89e8-117">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="f89e8-117">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="f89e8-118">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f89e8-118">HRESULT</span></span>|<span data-ttu-id="f89e8-119">说明</span><span class="sxs-lookup"><span data-stu-id="f89e8-119">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f89e8-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="f89e8-120">S_OK</span></span>|<span data-ttu-id="f89e8-121">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="f89e8-121">The method completed successfully.</span></span>|  
|<span data-ttu-id="f89e8-122">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="f89e8-122">E_POINTER</span></span>|<span data-ttu-id="f89e8-123">`pwzbuffer` 或 `pcchBuffer` 为 null。</span><span class="sxs-lookup"><span data-stu-id="f89e8-123">`pwzbuffer` or `pcchBuffer` is null.</span></span>|  
|<span data-ttu-id="f89e8-124">HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</span><span class="sxs-lookup"><span data-stu-id="f89e8-124">HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</span></span>|<span data-ttu-id="f89e8-125">缓冲区太小。</span><span class="sxs-lookup"><span data-stu-id="f89e8-125">The buffer is too small.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="f89e8-126">要求</span><span class="sxs-lookup"><span data-stu-id="f89e8-126">Requirements</span></span>  

 <span data-ttu-id="f89e8-127">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="f89e8-127">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f89e8-128">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="f89e8-128">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="f89e8-129">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f89e8-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f89e8-130">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f89e8-130">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f89e8-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="f89e8-131">See also</span></span>

- [<span data-ttu-id="f89e8-132">ICLRMetaHost 接口</span><span class="sxs-lookup"><span data-stu-id="f89e8-132">ICLRMetaHost Interface</span></span>](iclrmetahost-interface.md)
- [<span data-ttu-id="f89e8-133">承载</span><span class="sxs-lookup"><span data-stu-id="f89e8-133">Hosting</span></span>](index.md)
