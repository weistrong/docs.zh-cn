---
description: 了解详细信息： GetRequestedRuntimeInfo 函数
title: GetRequestedRuntimeInfo 函数
ms.date: 03/30/2017
api_name:
- GetRequestedRuntimeInfo
api_location:
- mscoree.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- GetRequestedRuntimeInfo
helpviewer_keywords:
- GetRequestedRuntimeInfo function [.NET Framework hosting]
ms.assetid: 0dfd7cdc-c116-4e25-b56a-ac7b0378c942
topic_type:
- apiref
ms.openlocfilehash: 63d0bdcd07be5727cddc0acc352e8358b5ff0090
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785284"
---
# <a name="getrequestedruntimeinfo-function"></a><span data-ttu-id="9befb-103">GetRequestedRuntimeInfo 函数</span><span class="sxs-lookup"><span data-stu-id="9befb-103">GetRequestedRuntimeInfo Function</span></span>

<span data-ttu-id="9befb-104">获取有关应用程序请求的公共语言运行时 (CLR) 的版本和目录信息。</span><span class="sxs-lookup"><span data-stu-id="9befb-104">Gets version and directory information about the common language runtime (CLR) requested by an application.</span></span>  
  
 <span data-ttu-id="9befb-105">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="9befb-105">This function has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9befb-106">语法</span><span class="sxs-lookup"><span data-stu-id="9befb-106">Syntax</span></span>  
  
```cpp  
HRESULT GetRequestedRuntimeInfo (  
    [in]  LPCWSTR  pExe,
    [in]  LPCWSTR  pwszVersion,
    [in]  LPCWSTR  pConfigurationFile,
    [in]  DWORD    startupFlags,
    [in]  DWORD    runtimeInfoFlags,
    [out] LPWSTR   pDirectory,
    [in]  DWORD    dwDirectory,
    [out] DWORD   *dwDirectoryLength,
    [out] LPWSTR   pVersion,
    [in]  DWORD    cchBuffer,
    [out] DWORD   *dwlength  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="9befb-107">参数</span><span class="sxs-lookup"><span data-stu-id="9befb-107">Parameters</span></span>  

 `pExe`  
 <span data-ttu-id="9befb-108">中应用程序的名称。</span><span class="sxs-lookup"><span data-stu-id="9befb-108">[in] The name of the application.</span></span>  
  
 `pwszVersion`  
 <span data-ttu-id="9befb-109">中一个字符串，指定运行时的版本号。</span><span class="sxs-lookup"><span data-stu-id="9befb-109">[in] A string specifying the version number of the runtime.</span></span>  
  
 `pConfigurationFile`  
 <span data-ttu-id="9befb-110">中与相关联的配置文件的名称 `pExe` 。</span><span class="sxs-lookup"><span data-stu-id="9befb-110">[in] The name of the configuration file that is associated with `pExe`.</span></span>  
  
 `startupFlags`  
 <span data-ttu-id="9befb-111">中一个或多个 [STARTUP_FLAGS](startup-flags-enumeration.md) 枚举值。</span><span class="sxs-lookup"><span data-stu-id="9befb-111">[in] One or more of the [STARTUP_FLAGS](startup-flags-enumeration.md) enumeration values.</span></span>  
  
 `runtimeInfoFlags`  
 <span data-ttu-id="9befb-112">中一个或多个 [RUNTIME_INFO_FLAGS](runtime-info-flags-enumeration.md) 枚举值。</span><span class="sxs-lookup"><span data-stu-id="9befb-112">[in] One or more of the [RUNTIME_INFO_FLAGS](runtime-info-flags-enumeration.md) enumeration values.</span></span>  
  
 `pDirectory`  
 <span data-ttu-id="9befb-113">弄一个缓冲区，其中包含成功完成后运行时的目录路径。</span><span class="sxs-lookup"><span data-stu-id="9befb-113">[out] A buffer that contains the directory path to the runtime upon successful completion.</span></span>  
  
 `dwDirectory`  
 <span data-ttu-id="9befb-114">中目录缓冲区的长度。</span><span class="sxs-lookup"><span data-stu-id="9befb-114">[in] The length of the directory buffer.</span></span>  
  
 `dwDirectoryLength`  
 <span data-ttu-id="9befb-115">弄指向目录路径字符串长度的指针。</span><span class="sxs-lookup"><span data-stu-id="9befb-115">[out] A pointer to the length of the directory path string.</span></span>  
  
 `pVersion`  
 <span data-ttu-id="9befb-116">弄一个缓冲区，其中包含成功完成后运行时的版本号。</span><span class="sxs-lookup"><span data-stu-id="9befb-116">[out] A buffer that contains the version number of the runtime upon successful completion.</span></span>  
  
 `cchBuffer`  
 <span data-ttu-id="9befb-117">中版本字符串缓冲区的长度。</span><span class="sxs-lookup"><span data-stu-id="9befb-117">[in] The length of the version string buffer.</span></span>  
  
 `dwlength`  
 <span data-ttu-id="9befb-118">弄指向版本字符串长度的指针。</span><span class="sxs-lookup"><span data-stu-id="9befb-118">[out] A pointer to the length of the version string.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9befb-119">返回值</span><span class="sxs-lookup"><span data-stu-id="9befb-119">Return Value</span></span>  

 <span data-ttu-id="9befb-120">除以下值外，此方法还 (COM) 错误代码（如 Winerror.h 中所定义）返回标准组件对象模型。</span><span class="sxs-lookup"><span data-stu-id="9befb-120">This method returns standard Component Object Model (COM) error codes, as defined in WinError.h, in addition to the following values.</span></span>  
  
|<span data-ttu-id="9befb-121">返回代码</span><span class="sxs-lookup"><span data-stu-id="9befb-121">Return code</span></span>|<span data-ttu-id="9befb-122">说明</span><span class="sxs-lookup"><span data-stu-id="9befb-122">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="9befb-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="9befb-123">S_OK</span></span>|<span data-ttu-id="9befb-124">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="9befb-124">The method completed successfully.</span></span>|  
|<span data-ttu-id="9befb-125">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="9befb-125">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="9befb-126">目录缓冲区不够大，无法存储目录路径。</span><span class="sxs-lookup"><span data-stu-id="9befb-126">The directory buffer is not large enough to store the directory path.</span></span><br /><br /> <span data-ttu-id="9befb-127">- 或 -</span><span class="sxs-lookup"><span data-stu-id="9befb-127">- or -</span></span><br /><br /> <span data-ttu-id="9befb-128">版本缓冲区不够大，无法存储版本字符串。</span><span class="sxs-lookup"><span data-stu-id="9befb-128">The version buffer is not large enough to store the version string.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9befb-129">备注</span><span class="sxs-lookup"><span data-stu-id="9befb-129">Remarks</span></span>  

 <span data-ttu-id="9befb-130">`GetRequestedRuntimeInfo`方法返回有关加载到进程中的版本的运行时信息，这不一定是计算机上安装的最新版本。</span><span class="sxs-lookup"><span data-stu-id="9befb-130">The `GetRequestedRuntimeInfo` method returns run-time information about the version loaded into the process, which is not necessarily the latest version installed on the computer.</span></span>  
  
 <span data-ttu-id="9befb-131">在 .NET Framework 版本2.0 中，可以通过使用方法获取有关最新安装的版本的信息，如下所示 `GetRequestedRuntimeInfo` ：</span><span class="sxs-lookup"><span data-stu-id="9befb-131">In the .NET Framework version 2.0, you can get information about the latest installed version by using the `GetRequestedRuntimeInfo` method as follows:</span></span>  
  
- <span data-ttu-id="9befb-132">将 `pExe` 、 `pwszVersion` 和参数指定 `pConfigurationFile` 为 null。</span><span class="sxs-lookup"><span data-stu-id="9befb-132">Specify the `pExe`, `pwszVersion`, and `pConfigurationFile` parameters as null.</span></span>  
  
- <span data-ttu-id="9befb-133">指定参数的枚举中的 RUNTIME_INFO_UPGRADE_VERSION 标志 `RUNTIME_INFO_FLAGS` `runtimeInfoFlags` 。</span><span class="sxs-lookup"><span data-stu-id="9befb-133">Specify the RUNTIME_INFO_UPGRADE_VERSION flag in the `RUNTIME_INFO_FLAGS` enumerations for the `runtimeInfoFlags` parameter.</span></span>  
  
 <span data-ttu-id="9befb-134">此 `GetRequestedRuntimeInfo` 方法在以下情况下不会返回最新的 CLR 版本：</span><span class="sxs-lookup"><span data-stu-id="9befb-134">The `GetRequestedRuntimeInfo` method does not return the latest CLR version in the following circumstances:</span></span>  
  
- <span data-ttu-id="9befb-135">指定加载特定 CLR 版本的应用程序配置文件存在。</span><span class="sxs-lookup"><span data-stu-id="9befb-135">An application configuration file that specifies loading a particular CLR version exists.</span></span> <span data-ttu-id="9befb-136">请注意，.NET Framework 将使用配置文件，即使为参数指定 null 也是如此 `pConfigurationFile` 。</span><span class="sxs-lookup"><span data-stu-id="9befb-136">Note that the .NET Framework will use the configuration file even if you specify null for the `pConfigurationFile` parameter.</span></span>  
  
- <span data-ttu-id="9befb-137">将 [CorBindToRuntimeEx](corbindtoruntimeex-function.md) 方法指定为指定较早的 CLR 版本。</span><span class="sxs-lookup"><span data-stu-id="9befb-137">The [CorBindToRuntimeEx](corbindtoruntimeex-function.md) method was called specifying an earlier CLR version.</span></span>  
  
- <span data-ttu-id="9befb-138">为早期 CLR 版本编译的应用程序当前正在运行。</span><span class="sxs-lookup"><span data-stu-id="9befb-138">An application that was compiled for an earlier CLR version is currently running.</span></span>  
  
 <span data-ttu-id="9befb-139">对于 `runtimeInfoFlags` 参数，可以一次仅指定枚举的一个体系结构常量 `RUNTIME_INFO_FLAGS` ：</span><span class="sxs-lookup"><span data-stu-id="9befb-139">For the `runtimeInfoFlags` parameter, you can specify only one of the architecture constants of the `RUNTIME_INFO_FLAGS` enumeration at a time:</span></span>  
  
- <span data-ttu-id="9befb-140">RUNTIME_INFO_REQUEST_IA64</span><span class="sxs-lookup"><span data-stu-id="9befb-140">RUNTIME_INFO_REQUEST_IA64</span></span>  
  
- <span data-ttu-id="9befb-141">RUNTIME_INFO_REQUEST_AMD64</span><span class="sxs-lookup"><span data-stu-id="9befb-141">RUNTIME_INFO_REQUEST_AMD64</span></span>  
  
- <span data-ttu-id="9befb-142">RUNTIME_INFO_REQUEST_X86</span><span class="sxs-lookup"><span data-stu-id="9befb-142">RUNTIME_INFO_REQUEST_X86</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9befb-143">要求</span><span class="sxs-lookup"><span data-stu-id="9befb-143">Requirements</span></span>  

 <span data-ttu-id="9befb-144">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9befb-144">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9befb-145">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="9befb-145">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9befb-146">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9befb-146">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9befb-147">**.NET Framework 版本：**[!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9befb-147">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9befb-148">请参阅</span><span class="sxs-lookup"><span data-stu-id="9befb-148">See also</span></span>

- [<span data-ttu-id="9befb-149">GetRequestedRuntimeVersion 函数</span><span class="sxs-lookup"><span data-stu-id="9befb-149">GetRequestedRuntimeVersion Function</span></span>](getrequestedruntimeversion-function.md)
- [<span data-ttu-id="9befb-150">GetVersionFromProcess 函数</span><span class="sxs-lookup"><span data-stu-id="9befb-150">GetVersionFromProcess Function</span></span>](getversionfromprocess-function.md)
- [<span data-ttu-id="9befb-151">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="9befb-151">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
