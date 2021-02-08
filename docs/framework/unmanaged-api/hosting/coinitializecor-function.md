---
description: 了解详细信息： CoInitializeCor 函数
title: CoInitializeCor 函数
ms.date: 03/30/2017
api_name:
- CoInitializeCor
api_location:
- mscoree.dll
- mscorsvr.dll
api_type:
- DLLExport
f1_keywords:
- CoInitializeCor
helpviewer_keywords:
- CoInitializeCor function [.NET Framework hosting]
ms.assetid: 9b9079fb-579e-4141-b3f0-791072dd40dc
topic_type:
- apiref
ms.openlocfilehash: e1db9914cce8a92cecf78123a2e247d75ec74acf
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99799845"
---
# <a name="coinitializecor-function"></a><span data-ttu-id="a006b-103">CoInitializeCor 函数</span><span class="sxs-lookup"><span data-stu-id="a006b-103">CoInitializeCor Function</span></span>

<span data-ttu-id="a006b-104">`CoInitializeCor` 已过时。</span><span class="sxs-lookup"><span data-stu-id="a006b-104">`CoInitializeCor` is obsolete.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a006b-105">语法</span><span class="sxs-lookup"><span data-stu-id="a006b-105">Syntax</span></span>  
  
```cpp  
STDAPI CoInitializeCor (  
    DWORD fFlags  
);  
```  
  
## <a name="remarks"></a><span data-ttu-id="a006b-106">备注</span><span class="sxs-lookup"><span data-stu-id="a006b-106">Remarks</span></span>  

 <span data-ttu-id="a006b-107">若要初始化公共语言运行时，请使用 [CorBindToRuntimeEx](corbindtoruntimeex-function.md) 或 [CorBindToCurrentRuntime](corbindtocurrentruntime-function.md)。</span><span class="sxs-lookup"><span data-stu-id="a006b-107">To initialize the common language runtime, use either [CorBindToRuntimeEx](corbindtoruntimeex-function.md) or [CorBindToCurrentRuntime](corbindtocurrentruntime-function.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a006b-108">要求</span><span class="sxs-lookup"><span data-stu-id="a006b-108">Requirements</span></span>  

 <span data-ttu-id="a006b-109">**标头：** Cor</span><span class="sxs-lookup"><span data-stu-id="a006b-109">**Header:** Cor.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a006b-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="a006b-110">See also</span></span>

- [<span data-ttu-id="a006b-111">元数据全局静态函数</span><span class="sxs-lookup"><span data-stu-id="a006b-111">Metadata Global Static Functions</span></span>](../metadata/metadata-global-static-functions.md)
