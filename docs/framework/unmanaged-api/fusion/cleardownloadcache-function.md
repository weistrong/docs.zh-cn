---
description: 了解详细信息： ClearDownloadCache 函数
title: ClearDownloadCache 函数
ms.date: 03/30/2017
api_name:
- ClearDownloadCache
api_location:
- fusion.dll
- clr.dll
- mscorwks.dll
api_type:
- DLLExport
f1_keywords:
- ClearDownloadCache
helpviewer_keywords:
- ClearDownloadCache function [.NET Framework fusion]
ms.assetid: df7595d1-430f-44b4-8160-4c2ba9df70b1
topic_type:
- apiref
ms.openlocfilehash: e0aecf525051172ea8a21c4941f9dad79b4fc85b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99761221"
---
# <a name="cleardownloadcache-function"></a><span data-ttu-id="a535b-103">ClearDownloadCache 函数</span><span class="sxs-lookup"><span data-stu-id="a535b-103">ClearDownloadCache Function</span></span>

<span data-ttu-id="a535b-104">清除已下载程序集的全局程序集缓存。</span><span class="sxs-lookup"><span data-stu-id="a535b-104">Clears the global assembly cache of downloaded assemblies.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a535b-105">语法</span><span class="sxs-lookup"><span data-stu-id="a535b-105">Syntax</span></span>  
  
```cpp  
HRESULT ClearDownloadCache ();  
```  
  
## <a name="requirements"></a><span data-ttu-id="a535b-106">要求</span><span class="sxs-lookup"><span data-stu-id="a535b-106">Requirements</span></span>  

 <span data-ttu-id="a535b-107">**平台：** 请参阅 [系统要求](../../get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="a535b-107">**Platforms:** See [System Requirements](../../get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a535b-108">**标头：** 合成。h</span><span class="sxs-lookup"><span data-stu-id="a535b-108">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="a535b-109">**库：** Fusion.dll 和 Mscorwks.dll。</span><span class="sxs-lookup"><span data-stu-id="a535b-109">**Library:** Fusion.dll and Mscorwks.dll.</span></span> <span data-ttu-id="a535b-110">使用 Fusion.dll 而不是 Mscorwks.dll 确保以正确的 .NET Framework 版本为目标。</span><span class="sxs-lookup"><span data-stu-id="a535b-110">Use Fusion.dll instead of Mscorwks.dll to ensure that you target the correct version of the .NET Framework.</span></span>  
  
 <span data-ttu-id="a535b-111">**.NET Framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a535b-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a535b-112">请参阅</span><span class="sxs-lookup"><span data-stu-id="a535b-112">See also</span></span>

- [<span data-ttu-id="a535b-113">合成全局静态函数</span><span class="sxs-lookup"><span data-stu-id="a535b-113">Fusion Global Static Functions</span></span>](fusion-global-static-functions.md)
- [<span data-ttu-id="a535b-114">全局程序集缓存</span><span class="sxs-lookup"><span data-stu-id="a535b-114">Global Assembly Cache</span></span>](../../app-domains/gac.md)
