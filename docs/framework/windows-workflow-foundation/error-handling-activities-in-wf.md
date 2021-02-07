---
description: 了解详细信息： WF 中的错误处理活动
title: WF 中的错误处理活动
ms.date: 03/30/2017
ms.assetid: 24b68bd3-cef5-4413-ab82-2e2625f209aa
ms.openlocfilehash: ef26c47d8d99f2d2186ef02820f9bebe691c2ff8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99742441"
---
# <a name="error-handling-activities-in-wf"></a><span data-ttu-id="13144-103">WF 中的错误处理活动</span><span class="sxs-lookup"><span data-stu-id="13144-103">Error Handling Activities in WF</span></span>

[!INCLUDE[netfx_current_long](../../../includes/netfx-current-long-md.md)]<span data-ttu-id="13144-104">提供多个系统提供的活动，用于实现错误处理和恢复。</span><span class="sxs-lookup"><span data-stu-id="13144-104">provides several system-provided activities for implementing error handling and recovery.</span></span> <span data-ttu-id="13144-105">有关更多信息，请参见 [异常](exceptions.md)中定义的接口的私有 C++ 特定实现。</span><span class="sxs-lookup"><span data-stu-id="13144-105">For more information, see [Exceptions](exceptions.md).</span></span>  
  
## <a name="error-handling-activities"></a><span data-ttu-id="13144-106">错误处理活动</span><span class="sxs-lookup"><span data-stu-id="13144-106">Error handling activities</span></span>  
  
|||  
|-|-|  
|<xref:System.Activities.Statements.Rethrow>|<span data-ttu-id="13144-107">重新引发从 `TryCatch` 活动中引发的最后一个异常。</span><span class="sxs-lookup"><span data-stu-id="13144-107">Rethrows the last exception thrown from within a `TryCatch` activity.</span></span>|  
|<xref:System.Activities.Statements.Throw>|<span data-ttu-id="13144-108">引发异常。</span><span class="sxs-lookup"><span data-stu-id="13144-108">Throws an exception.</span></span>|  
|<xref:System.Activities.Statements.TryCatch>|<span data-ttu-id="13144-109">实现异常处理。</span><span class="sxs-lookup"><span data-stu-id="13144-109">Implements exception handling.</span></span>|
