---
description: 了解详细信息： CreateDebuggingInterfaceFromVersion 函数
title: CreateDebuggingInterfaceFromVersion 函数
ms.date: 03/30/2017
api_name:
- CreateDebuggingInterfaceFromVersion
api_location:
- mscoree.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- CreateDebuggingInterfaceFromVersion
helpviewer_keywords:
- CreateDebuggingInterfaceFromVersion function [.NET Framework hosting]
ms.assetid: a746a849-463c-44f5-a2f0-9e812ed8bcc3
topic_type:
- apiref
ms.openlocfilehash: 163ada49f028071b48c93ee3c565152a773782ac
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99760623"
---
# <a name="createdebugginginterfacefromversion-function"></a><span data-ttu-id="3aad0-103">CreateDebuggingInterfaceFromVersion 函数</span><span class="sxs-lookup"><span data-stu-id="3aad0-103">CreateDebuggingInterfaceFromVersion Function</span></span>

<span data-ttu-id="3aad0-104">基于指定的版本信息创建 [ICorDebug](../debugging/icordebug-interface.md) 对象。</span><span class="sxs-lookup"><span data-stu-id="3aad0-104">Creates an [ICorDebug](../debugging/icordebug-interface.md) object based on the specified version information.</span></span>  
  
 <span data-ttu-id="3aad0-105">此函数在 .NET Framework 4 中已过时。</span><span class="sxs-lookup"><span data-stu-id="3aad0-105">This function is obsolete in the .NET Framework 4.</span></span> <span data-ttu-id="3aad0-106">相反，若要获取公共语言运行时的接口 (CLR) 2.0，请使用 [ICLRRuntimeInfo：： GetInterface](iclrruntimeinfo-getinterface-method.md) 方法并指定类标识符 CLSID_CLRDebuggingLegacy 和接口标识符 IID_ICorDebug。</span><span class="sxs-lookup"><span data-stu-id="3aad0-106">Instead, to get an interface for the common language runtime (CLR) 2.0, use the [ICLRRuntimeInfo::GetInterface](iclrruntimeinfo-getinterface-method.md) method and specify the class identifier CLSID_CLRDebuggingLegacy and the interface identifier IID_ICorDebug.</span></span> <span data-ttu-id="3aad0-107">若要获取 CLR 4 或更高版本的接口，请调用 [CLRCreateInstance](clrcreateinstance-function.md) 函数并指定类标识符 CLSID_CLRDebugging 和接口标识符 IID_ICLRDebugging。</span><span class="sxs-lookup"><span data-stu-id="3aad0-107">To get an interface for CLR 4 or later, call the [CLRCreateInstance](clrcreateinstance-function.md) function and specify the class identifier CLSID_CLRDebugging and the interface identifier IID_ICLRDebugging.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3aad0-108">语法</span><span class="sxs-lookup"><span data-stu-id="3aad0-108">Syntax</span></span>  
  
```cpp  
HRESULT CreateDebuggingInterfaceFromVersion (  
    [in]  int      iDebuggerVersion,
    [in]  LPCWSTR  szDebuggeeVersion,
    [out] IUnknown **ppCordb  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="3aad0-109">参数</span><span class="sxs-lookup"><span data-stu-id="3aad0-109">Parameters</span></span>  

 `iDebuggerVersion`  
 <span data-ttu-id="3aad0-110">中调试器所需的的版本 `ICorDebug` 。</span><span class="sxs-lookup"><span data-stu-id="3aad0-110">[in] The version of `ICorDebug` that is expected by the debugger.</span></span> <span data-ttu-id="3aad0-111">有关有效值，请参阅 [CorDebugInterfaceVersion](../debugging/cordebuginterfaceversion-enumeration.md) 枚举。</span><span class="sxs-lookup"><span data-stu-id="3aad0-111">See the [CorDebugInterfaceVersion](../debugging/cordebuginterfaceversion-enumeration.md) enumeration for valid values.</span></span>  
  
 `szDebuggeeVersion`  
 <span data-ttu-id="3aad0-112">中与要调试的应用程序或进程关联的公共语言运行时版本。</span><span class="sxs-lookup"><span data-stu-id="3aad0-112">[in] The common language runtime version associated with the application or process to be debugged.</span></span> <span data-ttu-id="3aad0-113">有关检索此值的信息，请参阅 [GetVersionFromProcess](getversionfromprocess-function.md) 或 [GetRequestedRuntimeVersion](getrequestedruntimeversion-function.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3aad0-113">See the [GetVersionFromProcess](getversionfromprocess-function.md) or [GetRequestedRuntimeVersion](getrequestedruntimeversion-function.md) method for information on retrieving this value.</span></span>  
  
 `ppCordb`  
 <span data-ttu-id="3aad0-114">弄接收指向对象的指针的位置 `ICorDebug` 。</span><span class="sxs-lookup"><span data-stu-id="3aad0-114">[out] The location that receives a pointer to the `ICorDebug` object.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="3aad0-115">返回值</span><span class="sxs-lookup"><span data-stu-id="3aad0-115">Return Value</span></span>  

 <span data-ttu-id="3aad0-116">除以下值外，此方法还返回 Winerror.h 文件中定义的标准 COM 错误代码。</span><span class="sxs-lookup"><span data-stu-id="3aad0-116">This method returns standard COM error codes as defined in the WinError.h file in addition to the following values.</span></span>  
  
|<span data-ttu-id="3aad0-117">返回代码</span><span class="sxs-lookup"><span data-stu-id="3aad0-117">Return code</span></span>|<span data-ttu-id="3aad0-118">说明</span><span class="sxs-lookup"><span data-stu-id="3aad0-118">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="3aad0-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="3aad0-119">S_OK</span></span>|<span data-ttu-id="3aad0-120">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="3aad0-120">The method completed successfully.</span></span>|  
|<span data-ttu-id="3aad0-121">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3aad0-121">E_INVALIDARG</span></span>|<span data-ttu-id="3aad0-122">`szDebuggeeVersion` 或 `ppCordb` 为 null，或者版本字符串不正确。</span><span class="sxs-lookup"><span data-stu-id="3aad0-122">`szDebuggeeVersion` or `ppCordb` is null, or the version string is incorrect.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="3aad0-123">备注</span><span class="sxs-lookup"><span data-stu-id="3aad0-123">Remarks</span></span>  

 <span data-ttu-id="3aad0-124">`szDebuggeeVersion`参数映射到 MSCorDbi.dll 的相应版本。</span><span class="sxs-lookup"><span data-stu-id="3aad0-124">The `szDebuggeeVersion` parameter maps to the corresponding version of MSCorDbi.dll.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3aad0-125">要求</span><span class="sxs-lookup"><span data-stu-id="3aad0-125">Requirements</span></span>  

 <span data-ttu-id="3aad0-126">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="3aad0-126">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3aad0-127">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="3aad0-127">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="3aad0-128">**库：** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="3aad0-128">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="3aad0-129">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3aad0-129">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3aad0-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="3aad0-130">See also</span></span>

- [<span data-ttu-id="3aad0-131">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="3aad0-131">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
