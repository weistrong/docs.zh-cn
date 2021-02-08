---
description: 了解详细信息： GetVersionFromProcess 函数
title: GetVersionFromProcess 函数
ms.date: 03/30/2017
api_name:
- GetVersionFromProcess
api_location:
- mscoree.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- GetVersionFromProcess
helpviewer_keywords:
- GetVersionFromProcess function [.NET Framework hosting]
ms.assetid: a9f7f824-64a1-408d-8607-91c7f19d21fe
topic_type:
- apiref
ms.openlocfilehash: ab665d2984f79baf049009690b36782528094937
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785245"
---
# <a name="getversionfromprocess-function"></a><span data-ttu-id="13542-103">GetVersionFromProcess 函数</span><span class="sxs-lookup"><span data-stu-id="13542-103">GetVersionFromProcess Function</span></span>

<span data-ttu-id="13542-104">获取与指定的进程句柄关联 (CLR) 的公共语言运行时的版本号。</span><span class="sxs-lookup"><span data-stu-id="13542-104">Gets the version number of the common language runtime (CLR) that is associated with the specified process handle.</span></span>  
  
 <span data-ttu-id="13542-105">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="13542-105">This function has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="13542-106">语法</span><span class="sxs-lookup"><span data-stu-id="13542-106">Syntax</span></span>  
  
```cpp  
HRESULT GetVersionFromProcess (  
    [in]  HANDLE  hProcess,
    [out] LPWSTR  pVersion,
    [in]  DWORD   cchBuffer,
    [out] DWORD  *dwLength  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="13542-107">参数</span><span class="sxs-lookup"><span data-stu-id="13542-107">Parameters</span></span>  

 `hProcess`  
 <span data-ttu-id="13542-108">中进程的句柄。</span><span class="sxs-lookup"><span data-stu-id="13542-108">[in] A handle to a process.</span></span>  
  
 `pVersion`  
 <span data-ttu-id="13542-109">弄一个缓冲区，其中包含成功完成方法后的版本号字符串。</span><span class="sxs-lookup"><span data-stu-id="13542-109">[out] A buffer that contains the version number string upon successful completion of the method.</span></span>  
  
 `cchBuffer`  
 <span data-ttu-id="13542-110">中版本缓冲区的长度。</span><span class="sxs-lookup"><span data-stu-id="13542-110">[in] The length of the version buffer.</span></span>  
  
 `pdwLength`  
 <span data-ttu-id="13542-111">弄指向版本号字符串长度的指针。</span><span class="sxs-lookup"><span data-stu-id="13542-111">[out] A pointer to the length of the version number string.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="13542-112">返回值</span><span class="sxs-lookup"><span data-stu-id="13542-112">Return Value</span></span>  

 <span data-ttu-id="13542-113">除以下值外，此方法还 (COM) 错误代码（如 Winerror.h 中所定义）返回标准组件对象模型。</span><span class="sxs-lookup"><span data-stu-id="13542-113">This method returns standard Component Object Model (COM) error codes, as defined in WinError.h, in addition to the following values.</span></span>  
  
|<span data-ttu-id="13542-114">返回代码</span><span class="sxs-lookup"><span data-stu-id="13542-114">Return code</span></span>|<span data-ttu-id="13542-115">说明</span><span class="sxs-lookup"><span data-stu-id="13542-115">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="13542-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="13542-116">S_OK</span></span>|<span data-ttu-id="13542-117">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="13542-117">The method completed successfully.</span></span>|  
|<span data-ttu-id="13542-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="13542-118">E_INVALIDARG</span></span>|<span data-ttu-id="13542-119">`pVersion` 为 null 且不为 `cchBuffer` null，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="13542-119">`pVersion` is null and `cchBuffer` is not null, or vice versa.</span></span><br /><br /> <span data-ttu-id="13542-120">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="13542-120">-or-</span></span><br /><br /> <span data-ttu-id="13542-121">`hProcess` 不是进程的有效句柄。</span><span class="sxs-lookup"><span data-stu-id="13542-121">`hProcess` is not a valid handle to a process.</span></span><br /><br /> <span data-ttu-id="13542-122">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="13542-122">-or-</span></span><br /><br /> <span data-ttu-id="13542-123">未加载 CLR。</span><span class="sxs-lookup"><span data-stu-id="13542-123">The CLR is not loaded.</span></span>|  
|<span data-ttu-id="13542-124">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="13542-124">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="13542-125">`cchBuffer` 为 null 或小于版本字符串的长度。</span><span class="sxs-lookup"><span data-stu-id="13542-125">`cchBuffer` is null or less than the length of the version string.</span></span>|  
|<span data-ttu-id="13542-126">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="13542-126">E_NOTIMPL</span></span>|<span data-ttu-id="13542-127">此方法在 Microsoft Windows 95、Microsoft Windows 98 或 Microsoft Windows Millennium Edition 操作系统上不可用。</span><span class="sxs-lookup"><span data-stu-id="13542-127">This method is not available on the Microsoft Windows 95, Microsoft Windows 98, or Microsoft Windows Millennium Edition operating system.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="13542-128">要求</span><span class="sxs-lookup"><span data-stu-id="13542-128">Requirements</span></span>  

 <span data-ttu-id="13542-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="13542-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="13542-130">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="13542-130">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="13542-131">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="13542-131">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="13542-132">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="13542-132">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="13542-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="13542-133">See also</span></span>

- [<span data-ttu-id="13542-134">GetRequestedRuntimeInfo 函数</span><span class="sxs-lookup"><span data-stu-id="13542-134">GetRequestedRuntimeInfo Function</span></span>](getrequestedruntimeinfo-function.md)
- [<span data-ttu-id="13542-135">GetRequestedRuntimeVersion 函数</span><span class="sxs-lookup"><span data-stu-id="13542-135">GetRequestedRuntimeVersion Function</span></span>](getrequestedruntimeversion-function.md)
- [<span data-ttu-id="13542-136">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="13542-136">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
