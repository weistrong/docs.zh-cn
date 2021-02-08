---
description: 了解详细信息： NukeDownloadedCache 函数
title: NukeDownloadedCache 函数
ms.date: 03/30/2017
api_name:
- NukeDownloadedCache
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- NukeDownloadedCache
helpviewer_keywords:
- NukeDownloadedCache function [.NET Framework fusion]
ms.assetid: fac2b1c6-6fa3-4818-805b-b63972024c86
topic_type:
- apiref
ms.openlocfilehash: 2239473b8e6e43a539b0507c8255d40f87e72043
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99800027"
---
# <a name="nukedownloadedcache-function"></a><span data-ttu-id="163a3-103">NukeDownloadedCache 函数</span><span class="sxs-lookup"><span data-stu-id="163a3-103">NukeDownloadedCache Function</span></span>

<span data-ttu-id="163a3-104">删除公共语言运行时 (CLR) 下载缓存。</span><span class="sxs-lookup"><span data-stu-id="163a3-104">Deletes the common language runtime (CLR) download cache.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="163a3-105">语法</span><span class="sxs-lookup"><span data-stu-id="163a3-105">Syntax</span></span>  
  
```cpp  
HRESULT NukeDownloadedCache();  
```  
  
## <a name="return-value"></a><span data-ttu-id="163a3-106">返回值</span><span class="sxs-lookup"><span data-stu-id="163a3-106">Return Value</span></span>  

 <span data-ttu-id="163a3-107">此方法返回 Winerror.h 中定义的标准 COM 错误代码。</span><span class="sxs-lookup"><span data-stu-id="163a3-107">This method returns standard COM error codes, as defined in WinError.h.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="163a3-108">备注</span><span class="sxs-lookup"><span data-stu-id="163a3-108">Remarks</span></span>  

 <span data-ttu-id="163a3-109">CLR 下载缓存是存储从 URL 下载的具有强名称的程序集以便可以重复使用的区域。</span><span class="sxs-lookup"><span data-stu-id="163a3-109">The CLR download cache is the area where strong-named assemblies that are downloaded from a URL are stored for possible reuse.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="163a3-110">要求</span><span class="sxs-lookup"><span data-stu-id="163a3-110">Requirements</span></span>  

 <span data-ttu-id="163a3-111">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="163a3-111">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="163a3-112">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="163a3-112">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="163a3-113">**库：** Fusion.dll 和 Mscorwks.dll。</span><span class="sxs-lookup"><span data-stu-id="163a3-113">**Library:** Fusion.dll and Mscorwks.dll.</span></span> <span data-ttu-id="163a3-114">使用 Fusion.dll 而不是 Mscorwks.dll 确保以正确的 .NET Framework 版本为目标。</span><span class="sxs-lookup"><span data-stu-id="163a3-114">Use Fusion.dll instead of Mscorwks.dll to ensure that you target the correct version of the .NET Framework.</span></span>  
  
 <span data-ttu-id="163a3-115">**.NET Framework 版本：**[!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="163a3-115">**.NET Framework Versions:** [!INCLUDE[net_current_v11plus](../../../../includes/net-current-v11plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="163a3-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="163a3-116">See also</span></span>

- [<span data-ttu-id="163a3-117">CreateHistoryReader 函数</span><span class="sxs-lookup"><span data-stu-id="163a3-117">CreateHistoryReader Function</span></span>](createhistoryreader-function.md)
- [<span data-ttu-id="163a3-118">GetHistoryFileDirectory 函数</span><span class="sxs-lookup"><span data-stu-id="163a3-118">GetHistoryFileDirectory Function</span></span>](gethistoryfiledirectory-function.md)
- [<span data-ttu-id="163a3-119">合成全局静态函数</span><span class="sxs-lookup"><span data-stu-id="163a3-119">Fusion Global Static Functions</span></span>](fusion-global-static-functions.md)
