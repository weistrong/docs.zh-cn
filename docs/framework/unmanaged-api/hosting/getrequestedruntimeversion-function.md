---
description: 了解详细信息： GetRequestedRuntimeVersion 函数
title: GetRequestedRuntimeVersion 函数
ms.date: 03/30/2017
api_name:
- GetRequestedRuntimeVersion
api_location:
- mscoree.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- GetRequestedRuntimeVersion
helpviewer_keywords:
- GetRequestedRuntimeVersion function [.NET Framework hosting]
ms.assetid: 82f596a4-483d-4509-b0c5-a84c53c3da1b
topic_type:
- apiref
ms.openlocfilehash: 836cc4b875ddc427c6779950f5b68d2df8b6ef75
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785271"
---
# <a name="getrequestedruntimeversion-function"></a><span data-ttu-id="ccbca-103">GetRequestedRuntimeVersion 函数</span><span class="sxs-lookup"><span data-stu-id="ccbca-103">GetRequestedRuntimeVersion Function</span></span>

<span data-ttu-id="ccbca-104">获取指定应用程序 (CLR) 的公共语言运行时的版本号。</span><span class="sxs-lookup"><span data-stu-id="ccbca-104">Gets the version number of the common language runtime (CLR) requested by the specified application.</span></span> <span data-ttu-id="ccbca-105">如果未安装该版本，则获取在请求版本之前安装的最新版本。</span><span class="sxs-lookup"><span data-stu-id="ccbca-105">If that version is not installed, gets the most recent version that is installed before the requested version.</span></span>  
  
 <span data-ttu-id="ccbca-106">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="ccbca-106">This function has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ccbca-107">语法</span><span class="sxs-lookup"><span data-stu-id="ccbca-107">Syntax</span></span>  
  
```cpp  
HRESULT GetRequestedRuntimeVersion (  
    [in]  LPWSTR  pExe,
    [out] LPWSTR  pVersion,
    [in]  DWORD   cchBuffer,
    [out] DWORD  *pdwLength  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="ccbca-108">参数</span><span class="sxs-lookup"><span data-stu-id="ccbca-108">Parameters</span></span>  

 `pExe`  
 <span data-ttu-id="ccbca-109">中应用程序的名称。</span><span class="sxs-lookup"><span data-stu-id="ccbca-109">[in] The name of the application.</span></span>  
  
 `pVersion`  
 <span data-ttu-id="ccbca-110">弄一个缓冲区，其中包含成功完成后的版本号字符串。</span><span class="sxs-lookup"><span data-stu-id="ccbca-110">[out] A buffer that contains the version number string upon successful completion.</span></span>  
  
 `cchBuffer`  
 <span data-ttu-id="ccbca-111">中版本缓冲区的长度。</span><span class="sxs-lookup"><span data-stu-id="ccbca-111">[in] The length of the version buffer.</span></span>  
  
 `pdwLength`  
 <span data-ttu-id="ccbca-112">弄指向版本号字符串长度的指针。</span><span class="sxs-lookup"><span data-stu-id="ccbca-112">[out] A pointer to the length of the version number string.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ccbca-113">返回值</span><span class="sxs-lookup"><span data-stu-id="ccbca-113">Return Value</span></span>  

 <span data-ttu-id="ccbca-114">除以下值外，此方法还 (COM) 错误代码（如 Winerror.h 中所定义）返回标准组件对象模型。</span><span class="sxs-lookup"><span data-stu-id="ccbca-114">This method returns standard Component Object Model (COM) error codes, as defined in WinError.h, in addition to the following values.</span></span>  
  
|<span data-ttu-id="ccbca-115">返回代码</span><span class="sxs-lookup"><span data-stu-id="ccbca-115">Return code</span></span>|<span data-ttu-id="ccbca-116">说明</span><span class="sxs-lookup"><span data-stu-id="ccbca-116">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="ccbca-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="ccbca-117">S_OK</span></span>|<span data-ttu-id="ccbca-118">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="ccbca-118">The method completed successfully.</span></span>|  
|<span data-ttu-id="ccbca-119">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="ccbca-119">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="ccbca-120">版本缓冲区不够大，无法存储版本字符串。</span><span class="sxs-lookup"><span data-stu-id="ccbca-120">The version buffer is not large enough to store the version string.</span></span>|  
|<span data-ttu-id="ccbca-121">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="ccbca-121">E_POINTER</span></span>|<span data-ttu-id="ccbca-122">`pdwLength` 为 null。</span><span class="sxs-lookup"><span data-stu-id="ccbca-122">`pdwLength` is null.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ccbca-123">要求</span><span class="sxs-lookup"><span data-stu-id="ccbca-123">Requirements</span></span>  

 <span data-ttu-id="ccbca-124">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="ccbca-124">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ccbca-125">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="ccbca-125">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="ccbca-126">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ccbca-126">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="ccbca-127">**.NET Framework 版本：**[!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ccbca-127">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ccbca-128">请参阅</span><span class="sxs-lookup"><span data-stu-id="ccbca-128">See also</span></span>

- [<span data-ttu-id="ccbca-129">GetRequestedRuntimeInfo 函数</span><span class="sxs-lookup"><span data-stu-id="ccbca-129">GetRequestedRuntimeInfo Function</span></span>](getrequestedruntimeinfo-function.md)
- [<span data-ttu-id="ccbca-130">GetVersionFromProcess 函数</span><span class="sxs-lookup"><span data-stu-id="ccbca-130">GetVersionFromProcess Function</span></span>](getversionfromprocess-function.md)
- [<span data-ttu-id="ccbca-131">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="ccbca-131">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
