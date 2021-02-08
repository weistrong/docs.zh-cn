---
description: 了解详细信息： CorBindToCurrentRuntime 函数
title: CorBindToCurrentRuntime 函数
ms.date: 03/30/2017
api_name:
- CorBindToCurrentRuntime
api_location:
- mscoree.dll
- mscoreei.dll
api_type:
- HeaderDef
f1_keywords:
- CorBindToCurrentRuntime
helpviewer_keywords:
- CorBindToCurrentRuntime function [.NET Framework hosting]
ms.assetid: 6105c13e-d9cd-44d2-a95a-924e042830c7
topic_type:
- apiref
ms.openlocfilehash: 7dd2ab7febf4b1f87265a670a1af5d54b1e1102e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790108"
---
# <a name="corbindtocurrentruntime-function"></a><span data-ttu-id="4b9a8-103">CorBindToCurrentRuntime 函数</span><span class="sxs-lookup"><span data-stu-id="4b9a8-103">CorBindToCurrentRuntime Function</span></span>

<span data-ttu-id="4b9a8-104">通过使用存储在 XML 文件中的版本信息，将 (CLR) 中的公共语言运行时加载到进程中。</span><span class="sxs-lookup"><span data-stu-id="4b9a8-104">Loads the common language runtime (CLR) into a process by using version information stored in an XML file.</span></span> <span data-ttu-id="4b9a8-105">XML 文件的格式将建模为标准应用程序配置文件。</span><span class="sxs-lookup"><span data-stu-id="4b9a8-105">The format of the XML file is modeled after the standard application configuration file.</span></span> <span data-ttu-id="4b9a8-106">有关配置文件的详细信息，请参阅[配置文件架构](../../configure-apps/file-schema/index.md)。</span><span class="sxs-lookup"><span data-stu-id="4b9a8-106">For more information about configuration files, see [Configuration File Schema](../../configure-apps/file-schema/index.md).</span></span>  
  
 <span data-ttu-id="4b9a8-107">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="4b9a8-107">This function has been deprecated in the .NET Framework 4.</span></span> <span data-ttu-id="4b9a8-108">请参阅将 [公共语言运行时加载到进程中](/previous-versions/dotnet/netframework-4.0/01918c6x(v=vs.100))。</span><span class="sxs-lookup"><span data-stu-id="4b9a8-108">See [Loading the Common Language Runtime into a Process](/previous-versions/dotnet/netframework-4.0/01918c6x(v=vs.100)).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4b9a8-109">语法</span><span class="sxs-lookup"><span data-stu-id="4b9a8-109">Syntax</span></span>  
  
```cpp  
HRESULT CorBindToCurrentRuntime (  
    [in]  LPCWSTR   pwszFileName,  
    [in]  REFCLSID  rclsid,  
    [in]  REFIID    riid,  
    [out] LPVOID    *ppv  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="4b9a8-110">参数</span><span class="sxs-lookup"><span data-stu-id="4b9a8-110">Parameters</span></span>  

 `pwszFileName`  
 <span data-ttu-id="4b9a8-111">中指定要加载的 CLR 版本的应用程序配置文件的名称。</span><span class="sxs-lookup"><span data-stu-id="4b9a8-111">[in] The name of an application configuration file that specifies the version of the CLR to load.</span></span> <span data-ttu-id="4b9a8-112">如果文件名不是完全限定的，则假定它与进行调用的可执行文件位于同一目录中。</span><span class="sxs-lookup"><span data-stu-id="4b9a8-112">If the file name is not fully qualified, it is assumed to be in the same directory as the executable making the call.</span></span>  
  
 <span data-ttu-id="4b9a8-113">配置文件的元素中的 version 特性描述了要加载的运行时的版本 [\<requiredRuntime>](../../configure-apps/file-schema/startup/requiredruntime-element.md) 。</span><span class="sxs-lookup"><span data-stu-id="4b9a8-113">The version of the runtime to be loaded is described by the version attribute in the [\<requiredRuntime>](../../configure-apps/file-schema/startup/requiredruntime-element.md) element of the configuration file.</span></span>  
  
 <span data-ttu-id="4b9a8-114">如果未指定任何版本，或者如果 `<requiredRuntime>` 找不到该元素，则会加载计算机上安装的最新版本的 CLR。</span><span class="sxs-lookup"><span data-stu-id="4b9a8-114">If no version is specified, or if the `<requiredRuntime>` element cannot be found, the latest version of the CLR that is installed on the machine is loaded.</span></span>  
  
 `rclsid`  
 <span data-ttu-id="4b9a8-115">中 `CLSID` 用于实现 [ICorRuntimeHost](icorruntimehost-interface.md) 或 [ICLRRuntimeHost](iclrruntimehost-interface.md) 接口的 coclass 的。</span><span class="sxs-lookup"><span data-stu-id="4b9a8-115">[in] The `CLSID` of the coclass that implements either the [ICorRuntimeHost](icorruntimehost-interface.md) or the [ICLRRuntimeHost](iclrruntimehost-interface.md) interface.</span></span> <span data-ttu-id="4b9a8-116">支持的值为 CLSID_CorRuntimeHost 或 CLSID_CLRRuntimeHost。</span><span class="sxs-lookup"><span data-stu-id="4b9a8-116">Supported values are CLSID_CorRuntimeHost or CLSID_CLRRuntimeHost.</span></span>  
  
 `riid`  
 <span data-ttu-id="4b9a8-117">中 `IID` 你请求的接口的。</span><span class="sxs-lookup"><span data-stu-id="4b9a8-117">[in] The `IID` of the interface you are requesting.</span></span> <span data-ttu-id="4b9a8-118">支持的值为 IID_ICorRuntimeHost 或 IID_ICLRRuntimeHost。</span><span class="sxs-lookup"><span data-stu-id="4b9a8-118">Supported values are IID_ICorRuntimeHost or IID_ICLRRuntimeHost.</span></span>  
  
 `ppv`  
 <span data-ttu-id="4b9a8-119">弄返回的接口指针。</span><span class="sxs-lookup"><span data-stu-id="4b9a8-119">[out] The returned interface pointer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4b9a8-120">要求</span><span class="sxs-lookup"><span data-stu-id="4b9a8-120">Requirements</span></span>  

 <span data-ttu-id="4b9a8-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4b9a8-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4b9a8-122">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="4b9a8-122">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="4b9a8-123">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4b9a8-123">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="4b9a8-124">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4b9a8-124">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4b9a8-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="4b9a8-125">See also</span></span>

- [<span data-ttu-id="4b9a8-126">CorBindToRuntime 函数</span><span class="sxs-lookup"><span data-stu-id="4b9a8-126">CorBindToRuntime Function</span></span>](corbindtoruntime-function.md)
- [<span data-ttu-id="4b9a8-127">CorBindToRuntimeByCfg 函数</span><span class="sxs-lookup"><span data-stu-id="4b9a8-127">CorBindToRuntimeByCfg Function</span></span>](corbindtoruntimebycfg-function.md)
- [<span data-ttu-id="4b9a8-128">CorBindToRuntimeEx 函数</span><span class="sxs-lookup"><span data-stu-id="4b9a8-128">CorBindToRuntimeEx Function</span></span>](corbindtoruntimeex-function.md)
- [<span data-ttu-id="4b9a8-129">CorBindToRuntimeHost 函数</span><span class="sxs-lookup"><span data-stu-id="4b9a8-129">CorBindToRuntimeHost Function</span></span>](corbindtoruntimehost-function.md)
- [<span data-ttu-id="4b9a8-130">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="4b9a8-130">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)
- [<span data-ttu-id="4b9a8-131">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="4b9a8-131">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
