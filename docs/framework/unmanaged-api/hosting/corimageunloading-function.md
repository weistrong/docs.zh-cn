---
description: 了解详细信息： _CorImageUnloading 函数
title: _CorImageUnloading 函数
ms.date: 03/30/2017
api_name:
- _CorImageUnloading
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- _CorImageUnloading
helpviewer_keywords:
- _CorImageUnloading function [.NET Framework hosting]
ms.assetid: b4367214-6dac-4280-aa11-fd487ff30bc4
topic_type:
- apiref
ms.openlocfilehash: fe10c97be66aab21793b1ad306aa5d90eaa1ade2
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99716986"
---
# <a name="_corimageunloading-function"></a><span data-ttu-id="81832-103">_CorImageUnloading 函数</span><span class="sxs-lookup"><span data-stu-id="81832-103">_CorImageUnloading Function</span></span>

<span data-ttu-id="81832-104">卸载托管模块映像时通知加载程序。</span><span class="sxs-lookup"><span data-stu-id="81832-104">Notifies the loader when the managed module images are unloaded.</span></span>  
  
 <span data-ttu-id="81832-105">未实现此函数。</span><span class="sxs-lookup"><span data-stu-id="81832-105">This function is not implemented.</span></span> <span data-ttu-id="81832-106">如果调用，它将返回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="81832-106">If called, it returns E_NOTIMPL.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="81832-107">语法</span><span class="sxs-lookup"><span data-stu-id="81832-107">Syntax</span></span>  
  
```cpp  
STDAPI (VOID) _CorImageUnloading(
   [in] PVOID* ImageBase  
);  
```  
  
## <a name="parameters"></a><span data-ttu-id="81832-108">参数</span><span class="sxs-lookup"><span data-stu-id="81832-108">Parameters</span></span>  

 `ImageBase`  
 <span data-ttu-id="81832-109">中一个指针，指向要卸载的图像的起始位置。</span><span class="sxs-lookup"><span data-stu-id="81832-109">[in] A pointer to the starting location of the image to unload.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="81832-110">要求</span><span class="sxs-lookup"><span data-stu-id="81832-110">Requirements</span></span>  

 <span data-ttu-id="81832-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="81832-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="81832-112">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="81832-112">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="81832-113">**库：** 作为中的资源包含 MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="81832-113">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="81832-114">**.NET Framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="81832-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="81832-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="81832-115">See also</span></span>

- [<span data-ttu-id="81832-116">元数据全局静态函数</span><span class="sxs-lookup"><span data-stu-id="81832-116">Metadata Global Static Functions</span></span>](../metadata/metadata-global-static-functions.md)
