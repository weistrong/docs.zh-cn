---
description: 了解详细信息： METAHOST_POLICY_FLAGS 枚举
title: METAHOST_POLICY_FLAGS 枚举
ms.date: 03/30/2017
api_name:
- METAHOST_POLICY_FLAGS
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- METAHOST_POLICY_FLAGS
helpviewer_keywords:
- METAHOST_POLICY_FLAGS enumeration [.NET Framework hosting]
ms.assetid: 3bb4b526-0118-42e2-ba59-c95648528ce9
topic_type:
- apiref
ms.openlocfilehash: 3a3ebe602c8f048b7f9fc907f5d4741722bd0ed3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99679616"
---
# <a name="metahost_policy_flags-enumeration"></a><span data-ttu-id="bbee5-103">METAHOST_POLICY_FLAGS 枚举</span><span class="sxs-lookup"><span data-stu-id="bbee5-103">METAHOST_POLICY_FLAGS Enumeration</span></span>

<span data-ttu-id="bbee5-104">提供大多数运行时主机通用的绑定策略。</span><span class="sxs-lookup"><span data-stu-id="bbee5-104">Provides binding policies that are common to most runtime hosts.</span></span> <span data-ttu-id="bbee5-105">此枚举由 [ICLRMetaHostPolicy：： GetRequestedRuntime](iclrmetahostpolicy-getrequestedruntime-method.md) 方法使用。</span><span class="sxs-lookup"><span data-stu-id="bbee5-105">This enumeration is used by the [ICLRMetaHostPolicy::GetRequestedRuntime](iclrmetahostpolicy-getrequestedruntime-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bbee5-106">语法</span><span class="sxs-lookup"><span data-stu-id="bbee5-106">Syntax</span></span>  
  
```cpp  
typedef enum {  
    METAHOST_POLICY_HIGHCOMPAT              = 0x00,  
    METAHOST_POLICY_APPLY_UPGRADE_POLICY    = 0x08,  
    METAHOST_POLICY_EMULATE_EXE_LAUNCH      = 0x10,  
    METAHOST_POLICY_SHOW_ERROR_DIALOG       = 0x20,  
    METAHOST_POLICY_USE_PROCESS_IMAGE_PATH  = 0x40,  
    METAHOST_POLICY_ENSURE_SKU_SUPPORTED    = 0x80,  
    METAHOST_POLICY_IGNORE_ERROR_MODE       = 0x1000  
  
} METAHOST_POLICY_FLAGS;  
```  
  
## <a name="members"></a><span data-ttu-id="bbee5-107">成员</span><span class="sxs-lookup"><span data-stu-id="bbee5-107">Members</span></span>  
  
|<span data-ttu-id="bbee5-108">成员</span><span class="sxs-lookup"><span data-stu-id="bbee5-108">Member</span></span>|<span data-ttu-id="bbee5-109">说明</span><span class="sxs-lookup"><span data-stu-id="bbee5-109">Description</span></span>|  
|------------|-----------------|  
|`METAHOST_POLICY_HIGHCOMPAT`|<span data-ttu-id="bbee5-110">定义高兼容性策略，该策略不考虑加载到当前进程 (CLR) 的任何公共语言运行时。</span><span class="sxs-lookup"><span data-stu-id="bbee5-110">Defines the high-compatibility policy, which does not consider any common language runtime (CLR) that is loaded into the current process.</span></span> <span data-ttu-id="bbee5-111">相反，它仅考虑已安装的 Clr 和组件的首选项，派生自程序集文件本身、声明的生成版本或配置文件。</span><span class="sxs-lookup"><span data-stu-id="bbee5-111">Instead, it considers only the installed CLRs and the preferences of the component, as derived from the assembly file itself, the declared built-against version, or the configuration file.</span></span>|  
|`METAHOST_POLICY_APPLY_UPGRADE_POLICY`|<span data-ttu-id="bbee5-112">当找不到匹配项的内容时，将升级策略应用于版本绑定结果，具体取决于 HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft的内容 \\ 。NETFramework\Policy\Upgrades.</span><span class="sxs-lookup"><span data-stu-id="bbee5-112">Applies upgrade policy to the version bind result when an exact match is not found, based on the contents of HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\\.NETFramework\Policy\Upgrades.</span></span> <span data-ttu-id="bbee5-113">这与 [RUNTIME_INFO_UPGRADE_VERSION](runtime-info-flags-enumeration.md)的效果相同。</span><span class="sxs-lookup"><span data-stu-id="bbee5-113">This has the same effect as [RUNTIME_INFO_UPGRADE_VERSION](runtime-info-flags-enumeration.md).</span></span>|  
|`METAHOST_POLICY_EMULATE_EXE_LAUNCH`|<span data-ttu-id="bbee5-114">返回绑定结果，就好像在新进程中启动了提供给调用的图像一样。</span><span class="sxs-lookup"><span data-stu-id="bbee5-114">Binding results are returned as if the image provided to the call were launched in a new process.</span></span> <span data-ttu-id="bbee5-115">目前，会 `GetRequestedRuntime` 忽略一组可加载的运行时，并将其与已安装的运行时集绑定在一起。</span><span class="sxs-lookup"><span data-stu-id="bbee5-115">Currently, `GetRequestedRuntime` ignores the set of loadable runtimes and binds against the set of installed runtimes.</span></span> <span data-ttu-id="bbee5-116">此标志允许主机在启动时确定 EXE 将绑定到的运行时。</span><span class="sxs-lookup"><span data-stu-id="bbee5-116">This flag allows a host to determine which runtime an EXE will bind to when it is launched.</span></span>|  
|`METAHOST_POLICY_SHOW_ERROR_DIALOG`|<span data-ttu-id="bbee5-117">如果 `GetRequestedRuntime` 找不到与输入参数兼容的运行时，则会显示错误对话框。</span><span class="sxs-lookup"><span data-stu-id="bbee5-117">An error dialog box is displayed if `GetRequestedRuntime` is unable to find a runtime that is compatible with the input parameters.</span></span> <span data-ttu-id="bbee5-118">从 .NET Framework 4.5 开始，此错误对话框可以采用 Windows 功能对话框的形式，该对话框会询问用户是否要启用相应的功能。</span><span class="sxs-lookup"><span data-stu-id="bbee5-118">Beginning with the .NET Framework 4.5, this error dialog box can take the form of a Windows feature dialog box that asks whether the user would like to enable the appropriate feature.</span></span>|  
|`METAHOST_POLICY_USE_PROCESS_IMAGE_PATH`|<span data-ttu-id="bbee5-119">`GetRequestedRuntime` 使用进程图像 (和任何相应的配置文件) 作为绑定过程的附加输入。</span><span class="sxs-lookup"><span data-stu-id="bbee5-119">`GetRequestedRuntime` uses the process image (and any corresponding configuration file) as additional input to the binding process.</span></span> <span data-ttu-id="bbee5-120">默认情况下， `GetRequestedRuntime` 不会回退到进程映像路径 (通常是在确定要绑定到的运行时) 用于启动进程的 EXE。</span><span class="sxs-lookup"><span data-stu-id="bbee5-120">By default, `GetRequestedRuntime` does not fall back to the process image path (typically, the EXE that was used to launch the process) when determining the runtime to bind to.</span></span>|  
|`METAHOST_POLICY_ENSURE_SKU_SUPPORTED`|<span data-ttu-id="bbee5-121">`GetRequestedRuntime` 如果配置文件中没有可用的信息，则必须检查是否安装了相应的 SKU。</span><span class="sxs-lookup"><span data-stu-id="bbee5-121">`GetRequestedRuntime` must check whether the appropriate SKU is installed when no information is available in the configuration file.</span></span> <span data-ttu-id="bbee5-122">这允许不具有配置文件的应用程序在 .NET Framework 的默认安装的较小 Sku 上正常失败。</span><span class="sxs-lookup"><span data-stu-id="bbee5-122">This allows applications that do not have configuration files to fail gracefully on smaller SKUs than the default installation of the .NET Framework.</span></span> <span data-ttu-id="bbee5-123">默认情况下，不 `GetRequestedRuntime` 会检查是否安装了相应的 sku，除非在配置文件元素中指定了 sku 属性 `<supportedRuntime />` 。</span><span class="sxs-lookup"><span data-stu-id="bbee5-123">By default, `GetRequestedRuntime` does not check whether the appropriate SKU is installed unless the SKU attribute is specified in the configuration file `<supportedRuntime />` element.</span></span>|  
|`METAHOST_POLICY_IGNORE_ERROR_MODE`|<span data-ttu-id="bbee5-124">`GetRequestedRuntime` 应忽略 SEM_FAILCRITICALERRORS (通过调用 [SetErrorMode](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) 函数) 设置，并显示错误对话框。</span><span class="sxs-lookup"><span data-stu-id="bbee5-124">`GetRequestedRuntime` should ignore SEM_FAILCRITICALERRORS (which is set by calling the [SetErrorMode](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) function), and show the error dialog box.</span></span> <span data-ttu-id="bbee5-125">默认情况下，SEM_FAILCRITICALERRORS 禁止显示错误对话框。</span><span class="sxs-lookup"><span data-stu-id="bbee5-125">By default, SEM_FAILCRITICALERRORS suppresses the error dialog box.</span></span> <span data-ttu-id="bbee5-126">它可能已被其他进程继承，并且在你的方案中可能不需要此错误。</span><span class="sxs-lookup"><span data-stu-id="bbee5-126">It may have been inherited from another process, and the silent error may be undesirable in your scenario.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bbee5-127">备注</span><span class="sxs-lookup"><span data-stu-id="bbee5-127">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bbee5-128">要求</span><span class="sxs-lookup"><span data-stu-id="bbee5-128">Requirements</span></span>  

 <span data-ttu-id="bbee5-129">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="bbee5-129">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bbee5-130">**标头：** Metahost</span><span class="sxs-lookup"><span data-stu-id="bbee5-130">**Header:** Metahost.h</span></span>  
  
 <span data-ttu-id="bbee5-131">**库：** 作为中的资源包含 MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bbee5-131">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bbee5-132">**.NET Framework 版本：**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bbee5-132">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bbee5-133">请参阅</span><span class="sxs-lookup"><span data-stu-id="bbee5-133">See also</span></span>

- [<span data-ttu-id="bbee5-134">承载枚举</span><span class="sxs-lookup"><span data-stu-id="bbee5-134">Hosting Enumerations</span></span>](hosting-enumerations.md)
- [<span data-ttu-id="bbee5-135">GetRequestedRuntime 方法</span><span class="sxs-lookup"><span data-stu-id="bbee5-135">GetRequestedRuntime Method</span></span>](iclrmetahostpolicy-getrequestedruntime-method.md)
