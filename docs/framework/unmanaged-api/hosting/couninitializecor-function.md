---
description: 了解详细信息： CoUninitializeCor 函数
title: CoUninitializeCor 函数
ms.date: 03/30/2017
api_name:
- CoUninitializeCor
api_location:
- mscoree.dll
- mscorsvr.dll
api_type:
- DLLExport
f1_keywords:
- CoUninitializeCor
helpviewer_keywords:
- CoUninitializeCor function [.NET Framework hosting]
ms.assetid: 50a95b8b-9766-470e-bb29-2c7ecddfd4a1
topic_type:
- apiref
ms.openlocfilehash: 1aa3482b6891779b4c85c29079ccd26d7170934e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99746199"
---
# <a name="couninitializecor-function"></a><span data-ttu-id="98a7f-103">CoUninitializeCor 函数</span><span class="sxs-lookup"><span data-stu-id="98a7f-103">CoUninitializeCor Function</span></span>

<span data-ttu-id="98a7f-104">`CoUninitializeCor` 已过时。</span><span class="sxs-lookup"><span data-stu-id="98a7f-104">`CoUninitializeCor` is obsolete.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="98a7f-105">语法</span><span class="sxs-lookup"><span data-stu-id="98a7f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(void) CoUninitializeCor(void);  
```  
  
## <a name="remarks"></a><span data-ttu-id="98a7f-106">备注</span><span class="sxs-lookup"><span data-stu-id="98a7f-106">Remarks</span></span>  

 <span data-ttu-id="98a7f-107">公共语言运行时无法从进程中卸载。</span><span class="sxs-lookup"><span data-stu-id="98a7f-107">The common language runtime cannot be unloaded from a process.</span></span> <span data-ttu-id="98a7f-108">若要从正在运行的进程中完全删除运行时，则必须关闭该进程。</span><span class="sxs-lookup"><span data-stu-id="98a7f-108">To completely remove the runtime from a running process, you must shut down that process.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="98a7f-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="98a7f-109">See also</span></span>

- [<span data-ttu-id="98a7f-110">元数据全局静态函数</span><span class="sxs-lookup"><span data-stu-id="98a7f-110">Metadata Global Static Functions</span></span>](../metadata/metadata-global-static-functions.md)
