---
description: 了解详细信息： LoadLibraryShim 函数
title: LoadLibraryShim 函数
ms.date: 03/30/2017
api_name:
- LoadLibraryShim
api_location:
- mscoree.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- LoadLibraryShim
helpviewer_keywords:
- LoadLibraryShim function [.NET Framework hosting]
ms.assetid: 30931874-4d0e-4df1-b3d1-e425b50655d1
topic_type:
- apiref
ms.openlocfilehash: 829d64b5215fc21b2d8c8b753f5ad99212267b6a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99680000"
---
# <a name="loadlibraryshim-function"></a><span data-ttu-id="60804-103">LoadLibraryShim 函数</span><span class="sxs-lookup"><span data-stu-id="60804-103">LoadLibraryShim Function</span></span>

<span data-ttu-id="60804-104">加载 .NET Framework 可再发行组件包中包含的 DLL 的指定版本。</span><span class="sxs-lookup"><span data-stu-id="60804-104">Loads a specified version of a DLL that is included in the .NET Framework redistributable package.</span></span>  
  
 <span data-ttu-id="60804-105">此函数已在 .NET Framework 4 中弃用。</span><span class="sxs-lookup"><span data-stu-id="60804-105">This function has been deprecated in the .NET Framework 4.</span></span> <span data-ttu-id="60804-106">改为使用 [ICLRRuntimeInfo：： LoadLibrary](iclrruntimeinfo-loadlibrary-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="60804-106">Use the [ICLRRuntimeInfo::LoadLibrary](iclrruntimeinfo-loadlibrary-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="60804-107">语法</span><span class="sxs-lookup"><span data-stu-id="60804-107">Syntax</span></span>  
  
```cpp  
HRESULT LoadLibraryShim (  
    [in]  LPCWSTR  szDllName,  
    [in]  LPCWSTR  szVersion,  
          LPVOID   pvReserved,  
    [out] HMODULE *phModDll  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="60804-108">参数</span><span class="sxs-lookup"><span data-stu-id="60804-108">Parameters</span></span>  

 `szDllName`  
 <span data-ttu-id="60804-109">中以零结尾的字符串，表示要从 .NET Framework 库中加载的 DLL 的名称。</span><span class="sxs-lookup"><span data-stu-id="60804-109">[in] A zero-terminated string that represents the name of the DLL to be loaded from the .NET Framework library.</span></span>  
  
 `szVersion`  
 <span data-ttu-id="60804-110">中以零结尾的字符串，表示要加载的 DLL 的版本。</span><span class="sxs-lookup"><span data-stu-id="60804-110">[in] A zero-terminated string that represents the version of the DLL to be loaded.</span></span> <span data-ttu-id="60804-111">如果 `szVersion` 为 null，则为加载选择的版本是指定 DLL 的最新版本，该版本低于版本4。</span><span class="sxs-lookup"><span data-stu-id="60804-111">If `szVersion` is null, the version selected for loading is the latest version of the specified DLL that is less than version 4.</span></span> <span data-ttu-id="60804-112">也就是说，如果为 null，则忽略等于或大于版本4的所有版本， `szVersion` 如果未安装低于版本4的版本，则 DLL 无法加载。</span><span class="sxs-lookup"><span data-stu-id="60804-112">That is, all versions equal to or greater than version 4 are ignored if `szVersion` is null, and if no version less than version 4 is installed, the DLL fails to load.</span></span> <span data-ttu-id="60804-113">这是为了确保 .NET Framework 4 的安装不会影响预先存在的应用程序或组件。</span><span class="sxs-lookup"><span data-stu-id="60804-113">This is to ensure that installation of the .NET Framework 4 does not affect pre-existing applications or components.</span></span> <span data-ttu-id="60804-114">请参阅 CLR 团队博客中的 " [进程内 SxS 和迁移快速入门](https://devblogs.microsoft.com/dotnet/in-proc-sxs-and-migration-quick-start/) 条目。</span><span class="sxs-lookup"><span data-stu-id="60804-114">See the entry [In-Proc SxS and Migration Quick Start](https://devblogs.microsoft.com/dotnet/in-proc-sxs-and-migration-quick-start/) in the CLR team blog.</span></span>  
  
 `pvReserved`  
 <span data-ttu-id="60804-115">留待将来使用。</span><span class="sxs-lookup"><span data-stu-id="60804-115">Reserved for future use.</span></span>  
  
 `phModDll`  
 <span data-ttu-id="60804-116">弄指向模块的句柄的指针。</span><span class="sxs-lookup"><span data-stu-id="60804-116">[out] A pointer to the handle of the module.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="60804-117">返回值</span><span class="sxs-lookup"><span data-stu-id="60804-117">Return Value</span></span>  

 <span data-ttu-id="60804-118">除以下值外，此方法还 (COM) 错误代码（如 Winerror.h 中所定义）返回标准组件对象模型。</span><span class="sxs-lookup"><span data-stu-id="60804-118">This method returns standard Component Object Model (COM) error codes, as defined in WinError.h, in addition to the following values.</span></span>  
  
|<span data-ttu-id="60804-119">返回代码</span><span class="sxs-lookup"><span data-stu-id="60804-119">Return code</span></span>|<span data-ttu-id="60804-120">说明</span><span class="sxs-lookup"><span data-stu-id="60804-120">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="60804-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="60804-121">S_OK</span></span>|<span data-ttu-id="60804-122">该方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="60804-122">The method completed successfully.</span></span>|  
|<span data-ttu-id="60804-123">CLR_E_SHIM_RUNTIMELOAD</span><span class="sxs-lookup"><span data-stu-id="60804-123">CLR_E_SHIM_RUNTIMELOAD</span></span>|<span data-ttu-id="60804-124">加载 `szDllName` 需要加载公共语言运行时 (clr) ，而 clr 的必要版本无法加载。</span><span class="sxs-lookup"><span data-stu-id="60804-124">Loading `szDllName` requires loading the common language runtime (CLR), and the necessary version of the CLR cannot be loaded.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="60804-125">备注</span><span class="sxs-lookup"><span data-stu-id="60804-125">Remarks</span></span>  

 <span data-ttu-id="60804-126">此函数用于加载 .NET Framework 可再发行组件包中包含的 Dll。</span><span class="sxs-lookup"><span data-stu-id="60804-126">This function is used to load DLLs that are included in the .NET Framework redistributable package.</span></span> <span data-ttu-id="60804-127">它不会加载用户生成的 Dll。</span><span class="sxs-lookup"><span data-stu-id="60804-127">It does not load user-generated DLLs.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="60804-128">从 .NET Framework 版本2.0 开始，加载 Fusion.dll 会导致加载 CLR。</span><span class="sxs-lookup"><span data-stu-id="60804-128">Beginning with the .NET Framework version 2.0, loading Fusion.dll causes the CLR to be loaded.</span></span> <span data-ttu-id="60804-129">这是因为 Fusion.dll 中的函数现在是由运行时提供其实现的包装器。</span><span class="sxs-lookup"><span data-stu-id="60804-129">This is because the functions in Fusion.dll are now wrappers whose implementations are provided by the runtime.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="60804-130">要求</span><span class="sxs-lookup"><span data-stu-id="60804-130">Requirements</span></span>  

 <span data-ttu-id="60804-131">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="60804-131">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="60804-132">**标头：** Mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="60804-132">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="60804-133">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="60804-133">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="60804-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="60804-134">See also</span></span>

- [<span data-ttu-id="60804-135">弃用的 CLR 承载函数</span><span class="sxs-lookup"><span data-stu-id="60804-135">Deprecated CLR Hosting Functions</span></span>](deprecated-clr-hosting-functions.md)
