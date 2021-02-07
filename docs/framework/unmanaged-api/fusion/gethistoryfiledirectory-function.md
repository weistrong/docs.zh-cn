---
description: 了解详细信息： GetHistoryFileDirectory 函数
title: GetHistoryFileDirectory 函数
ms.date: 03/30/2017
api_name:
- GetHistoryFileDirectory
api_location:
- fusion.dll
api_type:
- DLLExport
f1_keywords:
- GetHistoryFileDirectory
helpviewer_keywords:
- GetHistoryFileDirectory function [.NET Framework fusion]
ms.assetid: 93232222-926e-42ac-b85d-8a6d33977672
topic_type:
- apiref
ms.openlocfilehash: 960bc75d69f4be6d1639e109d6327b5e65d3e129
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760961"
---
# <a name="gethistoryfiledirectory-function"></a><span data-ttu-id="1af5e-103">GetHistoryFileDirectory 函数</span><span class="sxs-lookup"><span data-stu-id="1af5e-103">GetHistoryFileDirectory Function</span></span>

<span data-ttu-id="1af5e-104">检索应用程序历史记录目录的路径。</span><span class="sxs-lookup"><span data-stu-id="1af5e-104">Retrieves the path of the application history directory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1af5e-105">语法</span><span class="sxs-lookup"><span data-stu-id="1af5e-105">Syntax</span></span>  
  
```cpp  
HRESULT GetHistoryFileDirectory (  
    [in]      LPWSTR      wzDir,  
    [in,out]  LPCWSTR  *pdwsize,  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="1af5e-106">参数</span><span class="sxs-lookup"><span data-stu-id="1af5e-106">Parameters</span></span>  

 `wzDir`  
 <span data-ttu-id="1af5e-107">弄用于保存应用程序历史记录目录路径的缓冲区。</span><span class="sxs-lookup"><span data-stu-id="1af5e-107">[out] A buffer to hold the path to the application history directory.</span></span>  
  
 `pdwSize`  
 <span data-ttu-id="1af5e-108">[in，out]缓冲区的长度。</span><span class="sxs-lookup"><span data-stu-id="1af5e-108">[in, out] The length of the buffer.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="1af5e-109">返回值</span><span class="sxs-lookup"><span data-stu-id="1af5e-109">Return Value</span></span>  

 <span data-ttu-id="1af5e-110">除以下值外，此方法还返回 Winerror.h 文件中定义的标准 COM 错误代码。</span><span class="sxs-lookup"><span data-stu-id="1af5e-110">This method returns standard COM error codes, as defined in the WinError.h file in addition to the following values.</span></span>  
  
|<span data-ttu-id="1af5e-111">返回代码</span><span class="sxs-lookup"><span data-stu-id="1af5e-111">Return code</span></span>|<span data-ttu-id="1af5e-112">说明</span><span class="sxs-lookup"><span data-stu-id="1af5e-112">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="1af5e-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="1af5e-113">S_OK</span></span>|<span data-ttu-id="1af5e-114">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="1af5e-114">The method completed successfully.</span></span>|  
|<span data-ttu-id="1af5e-115">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="1af5e-115">E_INVALIDARG</span></span>|<span data-ttu-id="1af5e-116">`wzDir` 或 `pdwSize` 为 null，或者版本字符串不正确。</span><span class="sxs-lookup"><span data-stu-id="1af5e-116">`wzDir` or `pdwSize` is null, or the version string is incorrect.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="1af5e-117">备注</span><span class="sxs-lookup"><span data-stu-id="1af5e-117">Remarks</span></span>  

 <span data-ttu-id="1af5e-118">成功完成 `pdwSize` 后，参数设置为路径字符串的长度。</span><span class="sxs-lookup"><span data-stu-id="1af5e-118">On successful completion, the `pdwSize` argument is set to the length of the path string.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1af5e-119">要求</span><span class="sxs-lookup"><span data-stu-id="1af5e-119">Requirements</span></span>  

 <span data-ttu-id="1af5e-120">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="1af5e-120">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1af5e-121">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="1af5e-121">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="1af5e-122">**库：** Fusion.dll 和 Mscorwks.dll。</span><span class="sxs-lookup"><span data-stu-id="1af5e-122">**Library:** Fusion.dll and Mscorwks.dll.</span></span> <span data-ttu-id="1af5e-123">使用 Fusion.dll 而不是 Mscorwks.dll 确保以正确的 .NET Framework 版本为目标。</span><span class="sxs-lookup"><span data-stu-id="1af5e-123">Use Fusion.dll instead of Mscorwks.dll to ensure that you target the correct version of the .NET Framework.</span></span>  
  
 <span data-ttu-id="1af5e-124">**.NET Framework 版本：**[!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1af5e-124">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1af5e-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="1af5e-125">See also</span></span>

- [<span data-ttu-id="1af5e-126">CreateHistoryReader 函数</span><span class="sxs-lookup"><span data-stu-id="1af5e-126">CreateHistoryReader Function</span></span>](createhistoryreader-function.md)
- [<span data-ttu-id="1af5e-127">NukeDownloadedCache 函数</span><span class="sxs-lookup"><span data-stu-id="1af5e-127">NukeDownloadedCache Function</span></span>](nukedownloadedcache-function.md)
- [<span data-ttu-id="1af5e-128">合成全局静态函数</span><span class="sxs-lookup"><span data-stu-id="1af5e-128">Fusion Global Static Functions</span></span>](fusion-global-static-functions.md)
