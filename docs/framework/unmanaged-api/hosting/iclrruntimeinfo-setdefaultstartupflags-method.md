---
description: 了解详细信息： ICLRRuntimeInfo：： SetDefaultStartupFlags 方法
title: ICLRRuntimeInfo::SetDefaultStartupFlags 方法
ms.date: 03/30/2017
api_name:
- ICLRRuntimeInfo.SetDefaultStartupFlags
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::SetDefaultStartupFlags
helpviewer_keywords:
- ICLRRuntimeInfo::SetDefaultStartupFlags method [.NET Framework hosting]
- SetDefaultStartupFlags method [.NET Framework hosting]
ms.assetid: 98ae174f-bff0-48f1-9e05-6cb63b451824
topic_type:
- apiref
ms.openlocfilehash: eb839b2ff71836adc1b3858092f7caf5787275b1
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785037"
---
# <a name="iclrruntimeinfosetdefaultstartupflags-method"></a><span data-ttu-id="be3df-103">ICLRRuntimeInfo::SetDefaultStartupFlags 方法</span><span class="sxs-lookup"><span data-stu-id="be3df-103">ICLRRuntimeInfo::SetDefaultStartupFlags Method</span></span>

<span data-ttu-id="be3df-104">设置启动标志和将用于启动运行时的主机配置文件。</span><span class="sxs-lookup"><span data-stu-id="be3df-104">Sets the startup flags and the host configuration file that will be used to start the runtime.</span></span> <span data-ttu-id="be3df-105">此方法取代了 `startupFlags` [CorBindToRuntimeEx](corbindtoruntimeex-function.md) 和 [CorBindToRuntimeHost](corbindtoruntimehost-function.md) 函数中的参数使用。</span><span class="sxs-lookup"><span data-stu-id="be3df-105">This method supersedes the use of the `startupFlags` parameter in the [CorBindToRuntimeEx](corbindtoruntimeex-function.md) and [CorBindToRuntimeHost](corbindtoruntimehost-function.md) functions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="be3df-106">语法</span><span class="sxs-lookup"><span data-stu-id="be3df-106">Syntax</span></span>  
  
```cpp  
HRESULT SetDefaultStartupFlags(  
           [in]  DWORD dwStartupFlags,  
           [in]  LPCWSTR pwzHostConfigFile);  
```  
  
## <a name="parameters"></a><span data-ttu-id="be3df-107">参数</span><span class="sxs-lookup"><span data-stu-id="be3df-107">Parameters</span></span>  

 `dwStartupFlags`  
 <span data-ttu-id="be3df-108">中要设置的主机启动标志。</span><span class="sxs-lookup"><span data-stu-id="be3df-108">[in] The host startup flags to set.</span></span> <span data-ttu-id="be3df-109">使用与 [CorBindToRuntimeEx](corbindtoruntimeex-function.md) 和 [CorBindToRuntimeHost](corbindtoruntimehost-function.md) 函数相同的标志。</span><span class="sxs-lookup"><span data-stu-id="be3df-109">Use the same flags as with the [CorBindToRuntimeEx](corbindtoruntimeex-function.md) and [CorBindToRuntimeHost](corbindtoruntimehost-function.md) functions.</span></span>  
  
 `pwzHostConfigFile`  
 <span data-ttu-id="be3df-110">中要设置的主机配置文件的目录路径。</span><span class="sxs-lookup"><span data-stu-id="be3df-110">[in] The directory path of the host configuration file to set.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="be3df-111">返回值</span><span class="sxs-lookup"><span data-stu-id="be3df-111">Return Value</span></span>  

 <span data-ttu-id="be3df-112">此方法返回以下特定的 HRESULT 以及指示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="be3df-112">This method returns the following specific HRESULT as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="be3df-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="be3df-113">HRESULT</span></span>|<span data-ttu-id="be3df-114">说明</span><span class="sxs-lookup"><span data-stu-id="be3df-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="be3df-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="be3df-115">S_OK</span></span>|<span data-ttu-id="be3df-116">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="be3df-116">The method completed successfully.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="be3df-117">备注</span><span class="sxs-lookup"><span data-stu-id="be3df-117">Remarks</span></span>  

 <span data-ttu-id="be3df-118">多线程主机应同步对此方法的调用。</span><span class="sxs-lookup"><span data-stu-id="be3df-118">A multithreaded host should synchronize calls to this method.</span></span> <span data-ttu-id="be3df-119">否则，线程 A 可能会 `SetStartupFlags` 在线程 b 完成对的调用 `SetStartupFlags` 和线程 b 启动运行时之前调用方法。</span><span class="sxs-lookup"><span data-stu-id="be3df-119">Otherwise, thread A might call the `SetStartupFlags` method after thread B completes a call to `SetStartupFlags` and before thread B starts the runtime.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="be3df-120">要求</span><span class="sxs-lookup"><span data-stu-id="be3df-120">Requirements</span></span>  

 <span data-ttu-id="be3df-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="be3df-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="be3df-122">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="be3df-122">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="be3df-123">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="be3df-123">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="be3df-124">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="be3df-124">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="be3df-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="be3df-125">See also</span></span>

- [<span data-ttu-id="be3df-126">ICLRRuntimeInfo 接口</span><span class="sxs-lookup"><span data-stu-id="be3df-126">ICLRRuntimeInfo Interface</span></span>](iclrruntimeinfo-interface.md)
- [<span data-ttu-id="be3df-127">承载接口</span><span class="sxs-lookup"><span data-stu-id="be3df-127">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="be3df-128">承载</span><span class="sxs-lookup"><span data-stu-id="be3df-128">Hosting</span></span>](index.md)
