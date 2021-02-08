---
description: 了解详细信息： ICLRMetaHostPolicy：： GetRequestedRuntime 方法
title: ICLRMetaHostPolicy::GetRequestedRuntime 方法
ms.date: 03/30/2017
api_name:
- ICLRMetaHostPolicy.GetRequestedRuntime
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRMetaHostPolicy::GetRequestedRuntime
helpviewer_keywords:
- GetRequestedRuntime method [.NET Framework hosting]
- ICLRMetaHostPolicy::GetRequestedRuntime method [.NET Framework hosting]
ms.assetid: 59ec1832-9cc1-4b5c-983d-03407e51de56
topic_type:
- apiref
ms.openlocfilehash: 0e11694b0cb66ad7fc28abf7bb9f7fc8c6931a19
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99789835"
---
# <a name="iclrmetahostpolicygetrequestedruntime-method"></a><span data-ttu-id="79a9b-103">ICLRMetaHostPolicy::GetRequestedRuntime 方法</span><span class="sxs-lookup"><span data-stu-id="79a9b-103">ICLRMetaHostPolicy::GetRequestedRuntime Method</span></span>

<span data-ttu-id="79a9b-104">提供基于宿主策略、托管程序集、版本字符串和配置流的公共语言运行时 (CLR) 的首选版本的接口。</span><span class="sxs-lookup"><span data-stu-id="79a9b-104">Provides an interface to a preferred version of the common language runtime (CLR) based on a hosting policy, managed assembly, version string, and configuration stream.</span></span> <span data-ttu-id="79a9b-105">此方法实际上不会加载或激活 CLR，只是返回表示策略结果的 [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) 接口。</span><span class="sxs-lookup"><span data-stu-id="79a9b-105">This method does not actually load or activate the CLR, but simply returns the [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) interface that represents the policy result.</span></span> <span data-ttu-id="79a9b-106">此方法取代了 [GetRequestedRuntimeInfo](getrequestedruntimeinfo-function.md)、 [GetRequestedRuntimeVersion](getrequestedruntimeversion-function.md)、 [CorBindToRuntimeHost](corbindtoruntimehost-function.md)、 [CorBindToRuntimeByCfg](corbindtoruntimebycfg-function.md)和 [GetCORRequiredVersion](getcorrequiredversion-function.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="79a9b-106">This method supersedes the [GetRequestedRuntimeInfo](getrequestedruntimeinfo-function.md), [GetRequestedRuntimeVersion](getrequestedruntimeversion-function.md), [CorBindToRuntimeHost](corbindtoruntimehost-function.md), [CorBindToRuntimeByCfg](corbindtoruntimebycfg-function.md), and [GetCORRequiredVersion](getcorrequiredversion-function.md) methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="79a9b-107">语法</span><span class="sxs-lookup"><span data-stu-id="79a9b-107">Syntax</span></span>

```cpp
HRESULT GetRequestedRuntime(
    [in]  METAHOST_POLICY_FLAGS dwPolicyFlags,
    [in]  LPCWSTR pwzBinary,
    [in]  IStream *pCfgStream,
    [in, out, size_is(*pcchVersion)] LPWSTR pwzVersion,
    [in, out]  DWORD *pcchVersion,
    [out, size_is(*pcchImageVersion)] LPWSTR pwzImageVersion,
    [in, out]  DWORD *pcchImageVersion,
    [out] DWORD *pdwConfigFlags,
    [in]  REFIID  riid
    [out, iid_is(riid), retval] LPVOID *ppRuntime);
```

## <a name="parameters"></a><span data-ttu-id="79a9b-108">参数</span><span class="sxs-lookup"><span data-stu-id="79a9b-108">Parameters</span></span>

|<span data-ttu-id="79a9b-109">名称</span><span class="sxs-lookup"><span data-stu-id="79a9b-109">Name</span></span>|<span data-ttu-id="79a9b-110">说明</span><span class="sxs-lookup"><span data-stu-id="79a9b-110">Description</span></span>|
|----------|-----------------|
|`dwPolicyFlags`|<span data-ttu-id="79a9b-111">[in] 必需。</span><span class="sxs-lookup"><span data-stu-id="79a9b-111">[in] Required.</span></span> <span data-ttu-id="79a9b-112">指定 [METAHOST_POLICY_FLAGS](metahost-policy-flags-enumeration.md) 枚举的成员，它表示一个绑定策略和任意数量的修饰符。</span><span class="sxs-lookup"><span data-stu-id="79a9b-112">Specifies a member of the [METAHOST_POLICY_FLAGS](metahost-policy-flags-enumeration.md) enumeration, representing a binding policy, and any number of modifiers.</span></span> <span data-ttu-id="79a9b-113">当前可用的唯一策略是 [METAHOST_POLICY_HIGHCOMPAT](metahost-policy-flags-enumeration.md)。</span><span class="sxs-lookup"><span data-stu-id="79a9b-113">The only policy that is currently available is [METAHOST_POLICY_HIGHCOMPAT](metahost-policy-flags-enumeration.md).</span></span><br /><br /> <span data-ttu-id="79a9b-114">修饰符包括 [METAHOST_POLICY_EMULATE_EXE_LAUNCH](metahost-policy-flags-enumeration.md)、 [METAHOST_POLICY_APPLY_UPGRADE_POLICY](metahost-policy-flags-enumeration.md)、 [METAHOST_POLICY_SHOW_ERROR_DIALOG](metahost-policy-flags-enumeration.md)、 [METAHOST_POLICY_USE_PROCESS_IMAGE_PATH](metahost-policy-flags-enumeration.md)和 [METAHOST_POLICY_ENSURE_SKU_SUPPORTED](metahost-policy-flags-enumeration.md)。</span><span class="sxs-lookup"><span data-stu-id="79a9b-114">Modifiers include [METAHOST_POLICY_EMULATE_EXE_LAUNCH](metahost-policy-flags-enumeration.md), [METAHOST_POLICY_APPLY_UPGRADE_POLICY](metahost-policy-flags-enumeration.md), [METAHOST_POLICY_SHOW_ERROR_DIALOG](metahost-policy-flags-enumeration.md), [METAHOST_POLICY_USE_PROCESS_IMAGE_PATH](metahost-policy-flags-enumeration.md), and [METAHOST_POLICY_ENSURE_SKU_SUPPORTED](metahost-policy-flags-enumeration.md).</span></span>|
|`pwzBinary`|<span data-ttu-id="79a9b-115">[in] 可选。</span><span class="sxs-lookup"><span data-stu-id="79a9b-115">[in] Optional.</span></span> <span data-ttu-id="79a9b-116">指定程序集文件路径。</span><span class="sxs-lookup"><span data-stu-id="79a9b-116">Specifies the assembly file path.</span></span>|
|`pCfgStream`|<span data-ttu-id="79a9b-117">[in] 可选。</span><span class="sxs-lookup"><span data-stu-id="79a9b-117">[in] Optional.</span></span> <span data-ttu-id="79a9b-118">指定配置文件作为 <xref:System.Runtime.InteropServices.ComTypes.IStream?displayProperty=nameWithType>。</span><span class="sxs-lookup"><span data-stu-id="79a9b-118">Specifies the configuration file as a <xref:System.Runtime.InteropServices.ComTypes.IStream?displayProperty=nameWithType>.</span></span>|
|`pwzVersion`|<span data-ttu-id="79a9b-119">[in, out] 可选。</span><span class="sxs-lookup"><span data-stu-id="79a9b-119">[in, out] Optional.</span></span> <span data-ttu-id="79a9b-120">指定或返回要加载的首选 CLR 版本。</span><span class="sxs-lookup"><span data-stu-id="79a9b-120">Specifies or returns the preferred CLR version to be loaded.</span></span>|
|`pcchVersion`|<span data-ttu-id="79a9b-121">[in, out] 必需。</span><span class="sxs-lookup"><span data-stu-id="79a9b-121">[in, out] Required.</span></span> <span data-ttu-id="79a9b-122">输入时指定 `pwzVersion` 的预期的大小，以避免缓冲区溢出。</span><span class="sxs-lookup"><span data-stu-id="79a9b-122">Specifies the expected size of `pwzVersion` as input, to avoid buffer overruns.</span></span> <span data-ttu-id="79a9b-123">如果 `pwzVersion` 为 null，则当 `GetRequestedRuntime` 返回时，`pcchVersion` 包含 `pwzVersion` 的预期的大小以允许预分配；否则为 `pcchVersion` 包含写入 `pwzVersion` 的字符数量。</span><span class="sxs-lookup"><span data-stu-id="79a9b-123">If `pwzVersion` is null, `pcchVersion` contains the expected size of `pwzVersion` when `GetRequestedRuntime` returns, to allow pre-allocation; otherwise, `pcchVersion` contains the number of characters written to `pwzVersion`.</span></span>|
|`pwzImageVersion`|<span data-ttu-id="79a9b-124">[out] 可选。</span><span class="sxs-lookup"><span data-stu-id="79a9b-124">[out] Optional.</span></span> <span data-ttu-id="79a9b-125">`GetRequestedRuntime`返回时，包含对应于返回的[ICLRRuntimeInfo](iclrruntimeinfo-interface.md)接口的 CLR 版本。</span><span class="sxs-lookup"><span data-stu-id="79a9b-125">When `GetRequestedRuntime` returns, contains the CLR version corresponding to the [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) interface that is returned.</span></span>|
|`pcchImageVersion`|<span data-ttu-id="79a9b-126">[in, out] 可选。</span><span class="sxs-lookup"><span data-stu-id="79a9b-126">[in, out] Optional.</span></span> <span data-ttu-id="79a9b-127">输入时指定 `pwzImageVersion` 的预期的大小以避免缓冲区溢出。</span><span class="sxs-lookup"><span data-stu-id="79a9b-127">Specifies the size of `pwzImageVersion` as input to avoid buffer overruns.</span></span> <span data-ttu-id="79a9b-128">如果 `pwzImageVersion` 为 null，则当 `GetRequestedRuntime` 返回时，`pcchImageVersion` 包含 `pwzImageVersion` 的所需大小，以允许预分配。</span><span class="sxs-lookup"><span data-stu-id="79a9b-128">If `pwzImageVersion` is null, `pcchImageVersion` contains the required size of `pwzImageVersion` when `GetRequestedRuntime` returns, to allow pre-allocation.</span></span>|
|`pdwConfigFlags`|<span data-ttu-id="79a9b-129">[out] 可选。</span><span class="sxs-lookup"><span data-stu-id="79a9b-129">[out] Optional.</span></span> <span data-ttu-id="79a9b-130">如果在 `GetRequestedRuntime` 绑定过程中使用配置文件，则在它返回时， `pdwConfigFlags` 将包含一个 [METAHOST_CONFIG_FLAGS](metahost-config-flags-enumeration.md) 值，该值指示 [\<startup>](../../configure-apps/file-schema/startup/startup-element.md) 元素是否具有 `useLegacyV2RuntimeActivationPolicy` 属性集和属性的值。</span><span class="sxs-lookup"><span data-stu-id="79a9b-130">If `GetRequestedRuntime` uses a configuration file during the binding process, when it returns, `pdwConfigFlags` contains a [METAHOST_CONFIG_FLAGS](metahost-config-flags-enumeration.md) value that indicates whether the [\<startup>](../../configure-apps/file-schema/startup/startup-element.md) element has the `useLegacyV2RuntimeActivationPolicy` attribute set, and the value of the attribute.</span></span> <span data-ttu-id="79a9b-131">将 [METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_MASK](metahost-config-flags-enumeration.md) 掩码应用到 `pdwConfigFlags` ，以获取与相关的值 `useLegacyV2RuntimeActivationPolicy` 。</span><span class="sxs-lookup"><span data-stu-id="79a9b-131">Apply the [METAHOST_CONFIG_FLAGS_LEGACY_V2_ACTIVATION_POLICY_MASK](metahost-config-flags-enumeration.md) mask to `pdwConfigFlags` to get the values relevant to `useLegacyV2RuntimeActivationPolicy`.</span></span>|
|`riid`|<span data-ttu-id="79a9b-132">中为请求的 [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) 接口指定接口标识符 IID_ICLRRuntimeInfo。</span><span class="sxs-lookup"><span data-stu-id="79a9b-132">[in] Specifies the interface identifier IID_ICLRRuntimeInfo for the requested [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) interface.</span></span>|
|`ppRuntime`|<span data-ttu-id="79a9b-133">弄当 `GetRequestedRuntime` 返回时，包含指向对应的 [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) 接口的指针。</span><span class="sxs-lookup"><span data-stu-id="79a9b-133">[out] When `GetRequestedRuntime` returns, contains a pointer to the corresponding [ICLRRuntimeInfo](iclrruntimeinfo-interface.md) interface.</span></span>|

## <a name="remarks"></a><span data-ttu-id="79a9b-134">备注</span><span class="sxs-lookup"><span data-stu-id="79a9b-134">Remarks</span></span>

<span data-ttu-id="79a9b-135">如果此方法成功，当且仅当一个或多个以下元素存在于 `<configuration><runtime>` 部分内的配置流中时，该方法具有将其他标志与返回运行时接口的当前默认启动标志结合的副作用：</span><span class="sxs-lookup"><span data-stu-id="79a9b-135">When this method succeeds, it has the side effect of combining additional flags with the current default startup flags of the returned runtime interface, if and only if one or more of the following elements exist in the configuration stream within the `<configuration><runtime>` section:</span></span>

- <span data-ttu-id="79a9b-136">`<gcServer enabled="true"/>` 导致 `STARTUP_SERVER_GC` 将被设置。</span><span class="sxs-lookup"><span data-stu-id="79a9b-136">`<gcServer enabled="true"/>` causes `STARTUP_SERVER_GC` to be set.</span></span>

- <span data-ttu-id="79a9b-137">`<etwEnable enabled="true"/>` 导致 `STARTUP_ETW` 将被设置。</span><span class="sxs-lookup"><span data-stu-id="79a9b-137">`<etwEnable enabled="true"/>` causes `STARTUP_ETW` to be set.</span></span>

- <span data-ttu-id="79a9b-138">`<appDomainResourceMonitoring enabled="true"/>` 导致 `STARTUP_ARM` 将被设置。</span><span class="sxs-lookup"><span data-stu-id="79a9b-138">`<appDomainResourceMonitoring enabled="true"/>` causes `STARTUP_ARM` to be set.</span></span>

<span data-ttu-id="79a9b-139">产生的默认 `STARTUP_FLAGS` 值是从前述列表设置的值与默认启动标志的按位“或”组合。</span><span class="sxs-lookup"><span data-stu-id="79a9b-139">The resulting default `STARTUP_FLAGS` value is the bitwise OR combination of the values that are set from the preceding list with the default startup flags.</span></span>

## <a name="return-value"></a><span data-ttu-id="79a9b-140">返回值</span><span class="sxs-lookup"><span data-stu-id="79a9b-140">Return Value</span></span>

<span data-ttu-id="79a9b-141">此方法返回以下特定 HRESULT 以及表示方法失败的 HRESULT 错误。</span><span class="sxs-lookup"><span data-stu-id="79a9b-141">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>

|<span data-ttu-id="79a9b-142">HRESULT</span><span class="sxs-lookup"><span data-stu-id="79a9b-142">HRESULT</span></span>|<span data-ttu-id="79a9b-143">说明</span><span class="sxs-lookup"><span data-stu-id="79a9b-143">Description</span></span>|
|-------------|-----------------|
|<span data-ttu-id="79a9b-144">S_OK</span><span class="sxs-lookup"><span data-stu-id="79a9b-144">S_OK</span></span>|<span data-ttu-id="79a9b-145">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="79a9b-145">The method completed successfully.</span></span>|
|<span data-ttu-id="79a9b-146">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="79a9b-146">E_POINTER</span></span>|<span data-ttu-id="79a9b-147">`pwzVersion` 不为 null 且 `pcchVersion` 为 null。</span><span class="sxs-lookup"><span data-stu-id="79a9b-147">`pwzVersion` is not null and `pcchVersion` is null.</span></span><br /><br /> <span data-ttu-id="79a9b-148">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="79a9b-148">-or-</span></span><br /><br /> <span data-ttu-id="79a9b-149">`pwzImageVersion` 不为 null 且 `pcchImageVersion` 为 null。</span><span class="sxs-lookup"><span data-stu-id="79a9b-149">`pwzImageVersion` is not null and `pcchImageVersion` is null.</span></span>|
|<span data-ttu-id="79a9b-150">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="79a9b-150">E_INVALIDARG</span></span>|<span data-ttu-id="79a9b-151">`dwPolicyFlags` 未指定 `METAHOST_POLICY_HIGHCOMPAT`。</span><span class="sxs-lookup"><span data-stu-id="79a9b-151">`dwPolicyFlags` does not specify `METAHOST_POLICY_HIGHCOMPAT`.</span></span>|
|<span data-ttu-id="79a9b-152">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="79a9b-152">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="79a9b-153">分配给 `pwzVersion` 的内存不足。</span><span class="sxs-lookup"><span data-stu-id="79a9b-153">The memory allocated to `pwzVersion` is inadequate.</span></span><br /><br /> <span data-ttu-id="79a9b-154">\- 或 -</span><span class="sxs-lookup"><span data-stu-id="79a9b-154">-or-</span></span><br /><br /> <span data-ttu-id="79a9b-155">分配给 `pwzImageVersion` 的内存不足。</span><span class="sxs-lookup"><span data-stu-id="79a9b-155">The memory allocated to `pwzImageVersion` is inadequate.</span></span>|
|<span data-ttu-id="79a9b-156">CLR_E_SHIM_RUNTIMELOAD</span><span class="sxs-lookup"><span data-stu-id="79a9b-156">CLR_E_SHIM_RUNTIMELOAD</span></span>|<span data-ttu-id="79a9b-157">`dwPolicyFlags` 包括 METAHOST_POLICY_APPLY_UPGRADE_POLICY，并且 `pwzVersion` 和 `pcchVersion` 均为 null。</span><span class="sxs-lookup"><span data-stu-id="79a9b-157">`dwPolicyFlags` includes METAHOST_POLICY_APPLY_UPGRADE_POLICY, and both `pwzVersion` and `pcchVersion` are null.</span></span>|

## <a name="requirements"></a><span data-ttu-id="79a9b-158">要求</span><span class="sxs-lookup"><span data-stu-id="79a9b-158">Requirements</span></span>

<span data-ttu-id="79a9b-159">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="79a9b-159">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>

<span data-ttu-id="79a9b-160">**标头：** MetaHost</span><span class="sxs-lookup"><span data-stu-id="79a9b-160">**Header:** MetaHost.h</span></span>

<span data-ttu-id="79a9b-161">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="79a9b-161">**Library:** Included as a resource in MSCorEE.dll</span></span>

<span data-ttu-id="79a9b-162">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="79a9b-162">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>

## <a name="see-also"></a><span data-ttu-id="79a9b-163">请参阅</span><span class="sxs-lookup"><span data-stu-id="79a9b-163">See also</span></span>

- [<span data-ttu-id="79a9b-164">ICLRMetaHostPolicy 接口</span><span class="sxs-lookup"><span data-stu-id="79a9b-164">ICLRMetaHostPolicy Interface</span></span>](iclrmetahostpolicy-interface.md)
- [<span data-ttu-id="79a9b-165">.NET Framework 4 和 4.5 中添加的 CLR 承载接口</span><span class="sxs-lookup"><span data-stu-id="79a9b-165">CLR Hosting Interfaces Added in the .NET Framework 4 and 4.5</span></span>](clr-hosting-interfaces-added-in-the-net-framework-4-and-4-5.md)
- [<span data-ttu-id="79a9b-166">承载接口</span><span class="sxs-lookup"><span data-stu-id="79a9b-166">Hosting Interfaces</span></span>](hosting-interfaces.md)
- [<span data-ttu-id="79a9b-167">承载</span><span class="sxs-lookup"><span data-stu-id="79a9b-167">Hosting</span></span>](index.md)
