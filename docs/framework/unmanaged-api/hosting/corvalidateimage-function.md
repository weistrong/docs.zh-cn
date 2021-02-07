---
description: 了解详细信息： _CorValidateImage 函数
title: _CorValidateImage 函数
ms.date: 03/30/2017
api_name:
- _CorValidateImage
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- _CorValidateImage
helpviewer_keywords:
- _CorValidateImage function [.NET Framework hosting]
ms.assetid: 0117e080-05f9-4772-885d-e1847230947c
topic_type:
- apiref
ms.openlocfilehash: f3d91c2d7e05786f7bfb0ab94b64e2cfb84a21d3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99746238"
---
# <a name="_corvalidateimage-function"></a><span data-ttu-id="abf37-103">_CorValidateImage 函数</span><span class="sxs-lookup"><span data-stu-id="abf37-103">_CorValidateImage Function</span></span>

<span data-ttu-id="abf37-104">验证托管模块映像，并在加载后通知操作系统加载程序。</span><span class="sxs-lookup"><span data-stu-id="abf37-104">Validates managed module images, and notifies the operating system loader after they have been loaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="abf37-105">语法</span><span class="sxs-lookup"><span data-stu-id="abf37-105">Syntax</span></span>  
  
```cpp  
STDAPI _CorValidateImage (
   [in] PVOID* ImageBase,  
   [in] LPCWSTR FileName  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="abf37-106">参数</span><span class="sxs-lookup"><span data-stu-id="abf37-106">Parameters</span></span>  

 `ImageBase`  
 <span data-ttu-id="abf37-107">中一个指针，指向要作为托管代码验证的图像的起始位置。</span><span class="sxs-lookup"><span data-stu-id="abf37-107">[in] A pointer to the starting location of the image to validate as managed code.</span></span> <span data-ttu-id="abf37-108">必须已将该映像加载到内存中。</span><span class="sxs-lookup"><span data-stu-id="abf37-108">The image must already be loaded into memory.</span></span>  
  
 `FileName`  
 <span data-ttu-id="abf37-109">中图像的文件名。</span><span class="sxs-lookup"><span data-stu-id="abf37-109">[in] The file name of the image.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="abf37-110">返回值</span><span class="sxs-lookup"><span data-stu-id="abf37-110">Return Value</span></span>  

 <span data-ttu-id="abf37-111">此函数返回标准值 `E_INVALIDARG` 、、 `E_OUTOFMEMORY` `E_UNEXPECTED` 和，以及 `E_FAIL` 以下值。</span><span class="sxs-lookup"><span data-stu-id="abf37-111">This function returns the standard values `E_INVALIDARG`, `E_OUTOFMEMORY`, `E_UNEXPECTED`, and `E_FAIL`, as well as the following values.</span></span>  
  
|<span data-ttu-id="abf37-112">返回值</span><span class="sxs-lookup"><span data-stu-id="abf37-112">Return value</span></span>|<span data-ttu-id="abf37-113">说明</span><span class="sxs-lookup"><span data-stu-id="abf37-113">Description</span></span>|  
|------------------|-----------------|  
|`STATUS_INVALID_IMAGE_FORMAT`|<span data-ttu-id="abf37-114">图像无效。</span><span class="sxs-lookup"><span data-stu-id="abf37-114">The image is invalid.</span></span> <span data-ttu-id="abf37-115">此值具有 HRESULT 0xC000007BL。</span><span class="sxs-lookup"><span data-stu-id="abf37-115">This value has the HRESULT 0xC000007BL.</span></span>|  
|`STATUS_SUCCESS`|<span data-ttu-id="abf37-116">图像有效。</span><span class="sxs-lookup"><span data-stu-id="abf37-116">The image is valid.</span></span> <span data-ttu-id="abf37-117">此值具有 HRESULT 0x00000000L。</span><span class="sxs-lookup"><span data-stu-id="abf37-117">This value has the HRESULT 0x00000000L.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="abf37-118">备注</span><span class="sxs-lookup"><span data-stu-id="abf37-118">Remarks</span></span>  

 <span data-ttu-id="abf37-119">在 Windows XP 和更高版本中，操作系统加载程序通过检查公共对象文件格式 (COFF) 标头的 COM 描述符目录位来检查托管模块。</span><span class="sxs-lookup"><span data-stu-id="abf37-119">In Windows XP and later versions, the operating system loader checks for managed modules by examining the COM Descriptor Directory bit in the common object file format (COFF) header.</span></span> <span data-ttu-id="abf37-120">设置位表示托管模块。</span><span class="sxs-lookup"><span data-stu-id="abf37-120">A set bit indicates a managed module.</span></span> <span data-ttu-id="abf37-121">如果加载程序检测到托管模块，它将加载 MsCorEE.dll 和调用 `_CorValidateImage` ，这会执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="abf37-121">If the loader detects a managed module, it loads MsCorEE.dll and calls `_CorValidateImage`, which performs the following actions:</span></span>  
  
- <span data-ttu-id="abf37-122">确认映像是有效的托管模块。</span><span class="sxs-lookup"><span data-stu-id="abf37-122">Confirms that the image is a valid managed module.</span></span>  
  
- <span data-ttu-id="abf37-123">将映像中的入口点更改为公共语言运行时中的入口点 (CLR) 。</span><span class="sxs-lookup"><span data-stu-id="abf37-123">Changes the entry point in the image to an entry point in the common language runtime (CLR).</span></span>  
  
- <span data-ttu-id="abf37-124">对于64位版本的 Windows，通过将其从 PE32 转换为 PE32 + 格式修改内存中的映像。</span><span class="sxs-lookup"><span data-stu-id="abf37-124">For 64-bit versions of Windows, modifies the image that is in memory by transforming it from PE32 to PE32+ format.</span></span>  
  
- <span data-ttu-id="abf37-125">加载托管模块映像时返回到加载程序。</span><span class="sxs-lookup"><span data-stu-id="abf37-125">Returns to the loader when the managed module images are loaded.</span></span>  
  
 <span data-ttu-id="abf37-126">对于可执行映像，操作系统加载器会调用 [_CorExeMain](corexemain-function.md) 函数，而不考虑可执行文件中指定的入口点。</span><span class="sxs-lookup"><span data-stu-id="abf37-126">For executable images, the operating system loader then calls the [_CorExeMain](corexemain-function.md) function, regardless of the entry point specified in the executable.</span></span> <span data-ttu-id="abf37-127">对于 DLL 程序集映像，加载程序将调用 [_CorDllMain](cordllmain-function.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="abf37-127">For DLL assembly images, the loader calls the [_CorDllMain](cordllmain-function.md) function.</span></span>  
  
 <span data-ttu-id="abf37-128">`_CorExeMain` 或 `_CorDllMain` 执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="abf37-128">`_CorExeMain` or `_CorDllMain` performs the following actions:</span></span>  
  
- <span data-ttu-id="abf37-129">初始化 CLR。</span><span class="sxs-lookup"><span data-stu-id="abf37-129">Initializes the CLR.</span></span>  
  
- <span data-ttu-id="abf37-130">定位程序集的 CLR 头中的托管入口点。</span><span class="sxs-lookup"><span data-stu-id="abf37-130">Locates the managed entry point from the assembly's CLR header.</span></span>  
  
- <span data-ttu-id="abf37-131">开始执行。</span><span class="sxs-lookup"><span data-stu-id="abf37-131">Begins execution.</span></span>  
  
 <span data-ttu-id="abf37-132">卸载托管模块映像时，加载程序将调用 [_CorImageUnloading](corimageunloading-function.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="abf37-132">The loader calls the [_CorImageUnloading](corimageunloading-function.md) function when managed module images are unloaded.</span></span> <span data-ttu-id="abf37-133">但是，此函数不执行任何操作;它仅返回。</span><span class="sxs-lookup"><span data-stu-id="abf37-133">However, this function does not perform any action; it just returns.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="abf37-134">要求</span><span class="sxs-lookup"><span data-stu-id="abf37-134">Requirements</span></span>  

 <span data-ttu-id="abf37-135">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="abf37-135">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="abf37-136">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="abf37-136">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="abf37-137">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="abf37-137">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="abf37-138">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="abf37-138">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="abf37-139">请参阅</span><span class="sxs-lookup"><span data-stu-id="abf37-139">See also</span></span>

- [<span data-ttu-id="abf37-140">元数据全局静态函数</span><span class="sxs-lookup"><span data-stu-id="abf37-140">Metadata Global Static Functions</span></span>](../metadata/metadata-global-static-functions.md)
