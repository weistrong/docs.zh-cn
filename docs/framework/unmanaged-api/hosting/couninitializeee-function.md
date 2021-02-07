---
description: 了解详细信息： CoUninitializeEE 函数
title: CoUninitializeEE 函数
ms.date: 03/30/2017
api_name:
- CoUninitializeEE
api_location:
- mscoree.dll
- mscorsvr.dll
api_type:
- DLLExport
f1_keywords:
- CoUninitializeEE
helpviewer_keywords:
- CoUninitializeEE function [.NET Framework hosting]
ms.assetid: 5f5a311a-839a-465f-89d9-ff1c74da9736
topic_type:
- apiref
ms.openlocfilehash: e356135ea027bd52520eff9084ad2f7f09e1fe0b
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99746160"
---
# <a name="couninitializeee-function"></a><span data-ttu-id="c3e12-103">CoUninitializeEE 函数</span><span class="sxs-lookup"><span data-stu-id="c3e12-103">CoUninitializeEE Function</span></span>

<span data-ttu-id="c3e12-104">`CoUninitializeEE` 已过时，不提供任何功能。</span><span class="sxs-lookup"><span data-stu-id="c3e12-104">`CoUninitializeEE` is obsolete and provides no functionality.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c3e12-105">语法</span><span class="sxs-lookup"><span data-stu-id="c3e12-105">Syntax</span></span>  
  
```cpp  
void CoUninitializeEE (  
    BOOL fFlags  
);  
```  
  
## <a name="remarks"></a><span data-ttu-id="c3e12-106">备注</span><span class="sxs-lookup"><span data-stu-id="c3e12-106">Remarks</span></span>  

 <span data-ttu-id="c3e12-107">不能从进程中卸载公共语言运行时的执行引擎。</span><span class="sxs-lookup"><span data-stu-id="c3e12-107">The common language runtime execution engine cannot be unloaded from a process.</span></span> <span data-ttu-id="c3e12-108">若要关闭执行引擎，请调用 [CorExitProcess](corexitprocess-function.md)。</span><span class="sxs-lookup"><span data-stu-id="c3e12-108">To shut down the execution engine call [CorExitProcess](corexitprocess-function.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c3e12-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="c3e12-109">See also</span></span>

- [<span data-ttu-id="c3e12-110">CoInitializeEE 函数</span><span class="sxs-lookup"><span data-stu-id="c3e12-110">CoInitializeEE Function</span></span>](coinitializeee-function.md)
- [<span data-ttu-id="c3e12-111">元数据全局静态函数</span><span class="sxs-lookup"><span data-stu-id="c3e12-111">Metadata Global Static Functions</span></span>](../metadata/metadata-global-static-functions.md)
