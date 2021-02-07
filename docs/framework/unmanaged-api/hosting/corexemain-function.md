---
description: 了解详细信息： _CorExeMain 函数
title: _CorExeMain 函数
ms.date: 03/30/2017
api_name:
- _CorExeMain
api_location:
- mscoree.dll
- clr.dll
- mscorwks.dll
- mscoreei.dll
api_type:
- DLLExport
f1_keywords:
- _CorExeMain
helpviewer_keywords:
- _CorExeMain function [.NET Framework hosting]
ms.assetid: 898f76e2-16f4-4a63-b7d9-dad2d3824d8a
topic_type:
- apiref
ms.openlocfilehash: f94197598d01255c35712aa682f83ca9be1fb377
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99717116"
---
# <a name="_corexemain-function"></a><span data-ttu-id="9d905-103">_CorExeMain 函数</span><span class="sxs-lookup"><span data-stu-id="9d905-103">_CorExeMain Function</span></span>

<span data-ttu-id="9d905-104"> (CLR) 初始化公共语言运行时，找到可执行程序集的 CLR 标头中的托管入口点，然后开始执行。</span><span class="sxs-lookup"><span data-stu-id="9d905-104">Initializes the common language runtime (CLR), locates the managed entry point in the executable assembly's CLR header, and begins execution.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9d905-105">语法</span><span class="sxs-lookup"><span data-stu-id="9d905-105">Syntax</span></span>  
  
```cpp  
__int32 STDMETHODCALLTYPE _CorExeMain ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="9d905-106">备注</span><span class="sxs-lookup"><span data-stu-id="9d905-106">Remarks</span></span>  

 <span data-ttu-id="9d905-107">此函数由加载程序在从托管可执行程序集创建的进程中调用。</span><span class="sxs-lookup"><span data-stu-id="9d905-107">This function is called by the loader in processes created from managed executable assemblies.</span></span> <span data-ttu-id="9d905-108">对于 DLL 程序集，加载程序将改为调用 [_CorDllMain](cordllmain-function.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="9d905-108">For DLL assemblies, the loader calls the [_CorDllMain](cordllmain-function.md) function instead.</span></span>  
  
 <span data-ttu-id="9d905-109">操作系统加载程序将调用此方法，而不考虑映像文件中指定的入口点。</span><span class="sxs-lookup"><span data-stu-id="9d905-109">The operating system loader calls this method regardless of the entry point specified in the image file.</span></span>  
  
 <span data-ttu-id="9d905-110">在 Windows 98、Windows ME、Windows NT 和 Windows 2000 中， `_CorExeMain` 通过操作系统加载程序中的修正间接调用该函数。</span><span class="sxs-lookup"><span data-stu-id="9d905-110">In Windows 98, Windows ME, Windows NT, and Windows 2000, the `_CorExeMain` function is called indirectly through a fixup in the operating system loader.</span></span> <span data-ttu-id="9d905-111">在所有其他版本的 Windows 中，操作系统加载程序直接调用它。</span><span class="sxs-lookup"><span data-stu-id="9d905-111">In all other versions of Windows, it is called directly by the operating system loader.</span></span>  
  
 <span data-ttu-id="9d905-112">有关其他信息，请参阅 [_CorValidateImage](corvalidateimage-function.md) 主题中的 "备注" 部分。</span><span class="sxs-lookup"><span data-stu-id="9d905-112">For additional information, see the Remarks section in the [_CorValidateImage](corvalidateimage-function.md) topic.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9d905-113">要求</span><span class="sxs-lookup"><span data-stu-id="9d905-113">Requirements</span></span>  

 <span data-ttu-id="9d905-114">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="9d905-114">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9d905-115">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="9d905-115">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="9d905-116">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9d905-116">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="9d905-117">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9d905-117">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9d905-118">请参阅</span><span class="sxs-lookup"><span data-stu-id="9d905-118">See also</span></span>

- [<span data-ttu-id="9d905-119">元数据全局静态函数</span><span class="sxs-lookup"><span data-stu-id="9d905-119">Metadata Global Static Functions</span></span>](../metadata/metadata-global-static-functions.md)
