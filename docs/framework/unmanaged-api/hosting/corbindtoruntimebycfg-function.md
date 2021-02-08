---
description: 了解详细信息： CorBindToRuntimeByCfg 函数
title: CorBindToRuntimeByCfg 函数
ms.date: 03/30/2017
api_name:
- CorBindToRuntimeByCfg
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- CorBindToRuntimeByCfg
helpviewer_keywords:
- CorBindToRuntimeByCfg function [.NET Framework hosting]
ms.assetid: ded1e492-a782-4185-9c66-709e421c1782
topic_type:
- apiref
ms.openlocfilehash: c1acf6a8f1d8637bc2d6cd180016ff51cf500107
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99790069"
---
# <a name="corbindtoruntimebycfg-function"></a><span data-ttu-id="457ff-103">CorBindToRuntimeByCfg 函数</span><span class="sxs-lookup"><span data-stu-id="457ff-103">CorBindToRuntimeByCfg Function</span></span>

<span data-ttu-id="457ff-104">使用从 XML 文件中读取的版本信息，将公共语言运行时 (CLR) 加载到进程中。</span><span class="sxs-lookup"><span data-stu-id="457ff-104">Loads the common language runtime (CLR) into a process by using version information that is read from an XML file.</span></span>  
  
 <span data-ttu-id="457ff-105">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="457ff-105">This function has been deprecated in the .NET Framework 4.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="457ff-106">语法</span><span class="sxs-lookup"><span data-stu-id="457ff-106">Syntax</span></span>  
  
```cpp  
HRESULT CorBindToRuntimeByCfg (  
    [in]  IStream     *pCfgStream,  
    [in]  DWORD        reserved,  
    [in]  DWORD        startupFlags,  
    [in]  REFCLSID     rclsid,  
    [in]  REFIID       riid,
    [out] LPVOID FAR*  ppv  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="457ff-107">参数</span><span class="sxs-lookup"><span data-stu-id="457ff-107">Parameters</span></span>  

 `pCfgStream`  
 <span data-ttu-id="457ff-108">中指向 `IStream` 读取 XML 文件的对象的指针。</span><span class="sxs-lookup"><span data-stu-id="457ff-108">[in] A pointer to an `IStream` object that reads the XML file.</span></span>  
  
 `reserved`  
 <span data-ttu-id="457ff-109">中保留供将来使用。</span><span class="sxs-lookup"><span data-stu-id="457ff-109">[in] Reserved for future use.</span></span> <span data-ttu-id="457ff-110">使用 0 (零) 作为值。</span><span class="sxs-lookup"><span data-stu-id="457ff-110">Use 0 (zero) as value.</span></span>  
  
 `startupFlags`  
 <span data-ttu-id="457ff-111">中 [STARTUP_FLAGS](startup-flags-enumeration.md) 枚举的一个值，该值指定 CLR 的启动行为。</span><span class="sxs-lookup"><span data-stu-id="457ff-111">[in] A value of the [STARTUP_FLAGS](startup-flags-enumeration.md) enumeration that specifies the startup behavior of the CLR.</span></span>  
  
 `rclsid`  
 <span data-ttu-id="457ff-112">中 `CLSID` 用于实现 [ICorRuntimeHost](icorruntimehost-interface.md) 或 [ICLRRuntimeHost](iclrruntimehost-interface.md) 接口的 coclass 的。</span><span class="sxs-lookup"><span data-stu-id="457ff-112">[in] The `CLSID` of the coclass that implements either the [ICorRuntimeHost](icorruntimehost-interface.md) or the [ICLRRuntimeHost](iclrruntimehost-interface.md) interface.</span></span> <span data-ttu-id="457ff-113">支持的值为 CLSID_CorRuntimeHost 或 CLSID_CLRRuntimeHost。</span><span class="sxs-lookup"><span data-stu-id="457ff-113">Supported values are CLSID_CorRuntimeHost or CLSID_CLRRuntimeHost.</span></span>  
  
 `riid`  
 <span data-ttu-id="457ff-114">中 `IID` `ICorRuntimeHost` 或 `ICLRRuntimeHost` 接口的。</span><span class="sxs-lookup"><span data-stu-id="457ff-114">[in] The `IID` of either the `ICorRuntimeHost` or the `ICLRRuntimeHost` interface.</span></span> <span data-ttu-id="457ff-115">支持的值为 IID_ICorRuntimeHost 或 IID_ICLRRuntimeHost。</span><span class="sxs-lookup"><span data-stu-id="457ff-115">Supported values are IID_ICorRuntimeHost or IID_ICLRRuntimeHost.</span></span>  
  
 `ppv`  
 <span data-ttu-id="457ff-116">弄指向返回的接口的地址的指针。</span><span class="sxs-lookup"><span data-stu-id="457ff-116">[out] A pointer to the address of the returned interface.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="457ff-117">备注</span><span class="sxs-lookup"><span data-stu-id="457ff-117">Remarks</span></span>  

 <span data-ttu-id="457ff-118">XML 文件的格式将建模为标准应用程序配置文件。</span><span class="sxs-lookup"><span data-stu-id="457ff-118">The format of the XML file is modeled after the standard application configuration file.</span></span> <span data-ttu-id="457ff-119">有关 XML 文件的详细信息，请参阅 [配置文件架构](../../configure-apps/file-schema/index.md)。</span><span class="sxs-lookup"><span data-stu-id="457ff-119">For more information about XML files, see [Configuration File Schema](../../configure-apps/file-schema/index.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="457ff-120">要求</span><span class="sxs-lookup"><span data-stu-id="457ff-120">Requirements</span></span>  

 <span data-ttu-id="457ff-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="457ff-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="457ff-122">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="457ff-122">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="457ff-123">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="457ff-123">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="457ff-124">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="457ff-124">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="457ff-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="457ff-125">See also</span></span>

- [<span data-ttu-id="457ff-126">CorBindToCurrentRuntime 函数</span><span class="sxs-lookup"><span data-stu-id="457ff-126">CorBindToCurrentRuntime Function</span></span>](corbindtocurrentruntime-function.md)
- [<span data-ttu-id="457ff-127">CorBindToRuntime 函数</span><span class="sxs-lookup"><span data-stu-id="457ff-127">CorBindToRuntime Function</span></span>](corbindtoruntime-function.md)
- [<span data-ttu-id="457ff-128">CorBindToRuntimeEx 函数</span><span class="sxs-lookup"><span data-stu-id="457ff-128">CorBindToRuntimeEx Function</span></span>](corbindtoruntimeex-function.md)
- [<span data-ttu-id="457ff-129">CorBindToRuntimeHost 函数</span><span class="sxs-lookup"><span data-stu-id="457ff-129">CorBindToRuntimeHost Function</span></span>](corbindtoruntimehost-function.md)
- [<span data-ttu-id="457ff-130">ICorRuntimeHost 接口</span><span class="sxs-lookup"><span data-stu-id="457ff-130">ICorRuntimeHost Interface</span></span>](icorruntimehost-interface.md)
- [<span data-ttu-id="457ff-131">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="457ff-131">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
