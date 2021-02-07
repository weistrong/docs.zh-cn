---
description: 了解详细信息： _CorDllMain 函数
title: _CorDllMain 函数
ms.date: 03/30/2017
api_name:
- _CorDllMain
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- _CorDllMain
helpviewer_keywords:
- _CorDllMain function [.NET Framework hosting]
ms.assetid: bc7b51cf-39d3-48ec-a5cb-2f179fbefff8
topic_type:
- apiref
ms.openlocfilehash: 442afae3a627eb684a86c02fbc6e546aa804b7a5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99717142"
---
# <a name="_cordllmain-function"></a><span data-ttu-id="acd6e-103">\_CorDllMain 函数</span><span class="sxs-lookup"><span data-stu-id="acd6e-103">\_CorDllMain Function</span></span>

<span data-ttu-id="acd6e-104"> (CLR) 初始化公共语言运行时，查找 DLL 程序集的 CLR 头中的托管入口点，然后开始执行。</span><span class="sxs-lookup"><span data-stu-id="acd6e-104">Initializes the common language runtime (CLR), locates the managed entry point in the DLL assembly's CLR header, and begins execution.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="acd6e-105">语法</span><span class="sxs-lookup"><span data-stu-id="acd6e-105">Syntax</span></span>  
  
```cpp  
BOOL STDMETHODCALLTYPE _CorDllMain (  
   [in] HINSTANCE hInst,  
   [in] DWORD     dwReason,  
   [in] LPVOID    lpReserved  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="acd6e-106">参数</span><span class="sxs-lookup"><span data-stu-id="acd6e-106">Parameters</span></span>  

 `hInst`  
 <span data-ttu-id="acd6e-107">中加载的模块的实例句柄。</span><span class="sxs-lookup"><span data-stu-id="acd6e-107">[in] The instance handle of the loaded module.</span></span>  
  
 `dwReason`  
 <span data-ttu-id="acd6e-108">中指示调用 DLL 入口点函数的原因。</span><span class="sxs-lookup"><span data-stu-id="acd6e-108">[in]Indicates why the DLL entry-point function is being called.</span></span> <span data-ttu-id="acd6e-109">此参数可以是下列值之一： DLL \_ PROCESS_ATTACH、dll \_ 线程 \_ 附加、dll \_ 线程 \_ 附加或 dll \_ 进程 \_ 分离。</span><span class="sxs-lookup"><span data-stu-id="acd6e-109">This parameter can be one of the following values: DLL\_PROCESS_ATTACH, DLL\_THREAD\_ATTACH, DLL\_THREAD\_ATTACH, or DLL\_PROCESS\_DETACH.</span></span> <span data-ttu-id="acd6e-110">有关这些值的说明，请参阅 `DllMain` PLATFORM SDK 中的文档。</span><span class="sxs-lookup"><span data-stu-id="acd6e-110">For descriptions of these values, see the `DllMain` documentation in the Platform SDK.</span></span>  
  
 `lpReserved`  
 <span data-ttu-id="acd6e-111">中用.</span><span class="sxs-lookup"><span data-stu-id="acd6e-111">[in] Unused.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="acd6e-112">返回值</span><span class="sxs-lookup"><span data-stu-id="acd6e-112">Return Value</span></span>  

 <span data-ttu-id="acd6e-113">`true`如果发生错误，则此方法将返回成功 `false` 。</span><span class="sxs-lookup"><span data-stu-id="acd6e-113">This method returns `true` for success and `false` if an error occurs.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="acd6e-114">备注</span><span class="sxs-lookup"><span data-stu-id="acd6e-114">Remarks</span></span>  

 <span data-ttu-id="acd6e-115">此函数由 DLL 程序集的操作系统加载程序调用。</span><span class="sxs-lookup"><span data-stu-id="acd6e-115">This function is called by the operating system loader for DLL assemblies.</span></span> <span data-ttu-id="acd6e-116">对于可执行程序集，加载程序将调用[ \_ CorExeMain](corexemain-function.md)函数。</span><span class="sxs-lookup"><span data-stu-id="acd6e-116">For executable assemblies, the loader calls the [\_CorExeMain](corexemain-function.md) function instead.</span></span>  
  
 <span data-ttu-id="acd6e-117">操作系统加载程序将调用此方法，而不考虑 DLL 文件中指定的入口点。</span><span class="sxs-lookup"><span data-stu-id="acd6e-117">The operating system loader calls this method regardless of the entry point specified in the DLL file.</span></span>  
  
<span data-ttu-id="acd6e-118">`_CorDllMain`函数由操作系统加载程序直接调用。</span><span class="sxs-lookup"><span data-stu-id="acd6e-118">The `_CorDllMain` function is called directly by the operating system loader.</span></span>
  
 <span data-ttu-id="acd6e-119">有关其他信息，请参阅[ \_ CorValidateImage](corvalidateimage-function.md)主题中的 "备注" 部分。</span><span class="sxs-lookup"><span data-stu-id="acd6e-119">For additional information, see the Remarks section in the [\_CorValidateImage](corvalidateimage-function.md) topic.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="acd6e-120">要求</span><span class="sxs-lookup"><span data-stu-id="acd6e-120">Requirements</span></span>  

 <span data-ttu-id="acd6e-121">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="acd6e-121">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="acd6e-122">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="acd6e-122">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="acd6e-123">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="acd6e-123">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="acd6e-124">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="acd6e-124">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="acd6e-125">请参阅</span><span class="sxs-lookup"><span data-stu-id="acd6e-125">See also</span></span>

- [<span data-ttu-id="acd6e-126">元数据全局静态函数</span><span class="sxs-lookup"><span data-stu-id="acd6e-126">Metadata Global Static Functions</span></span>](../metadata/metadata-global-static-functions.md)
