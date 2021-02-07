---
description: 了解详细信息： WebHostServiceCloseFailed
title: System.ServiceModel.Activation.WebHostServiceCloseFailed
ms.date: 03/30/2017
ms.assetid: 3cab9856-a5cf-4f0e-a0cb-89425e368f8e
ms.openlocfilehash: fae41b72e2eb9aba76993081769afc42c0ec8975
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99720444"
---
# <a name="systemservicemodelactivationwebhostserviceclosefailed"></a><span data-ttu-id="23103-103">System.ServiceModel.Activation.WebHostServiceCloseFailed</span><span class="sxs-lookup"><span data-stu-id="23103-103">System.ServiceModel.Activation.WebHostServiceCloseFailed</span></span>

<span data-ttu-id="23103-104">当服务无法正常关闭并中止时发生。</span><span class="sxs-lookup"><span data-stu-id="23103-104">Occurs when a service cannot be closed gracefully and is aborted.</span></span>  
  
## <a name="description"></a><span data-ttu-id="23103-105">说明</span><span class="sxs-lookup"><span data-stu-id="23103-105">Description</span></span>  

 <span data-ttu-id="23103-106">此错误代码仅出现在日志文件中。</span><span class="sxs-lookup"><span data-stu-id="23103-106">This error code only appears in the log file.</span></span> <span data-ttu-id="23103-107">它通常指示编程错误，例如，在已经调用 Abort 之后尝试关闭服务的时候。</span><span class="sxs-lookup"><span data-stu-id="23103-107">It usually indicates a programming error, for example, when you try to close a service after Abort has already been called.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="23103-108">疑难解答</span><span class="sxs-lookup"><span data-stu-id="23103-108">Troubleshooting</span></span>  

 <span data-ttu-id="23103-109">请检查应用程序源代码。</span><span class="sxs-lookup"><span data-stu-id="23103-109">Check the application source code.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="23103-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="23103-110">See also</span></span>

- [<span data-ttu-id="23103-111">跟踪</span><span class="sxs-lookup"><span data-stu-id="23103-111">Tracing</span></span>](index.md)
- [<span data-ttu-id="23103-112">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="23103-112">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="23103-113">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="23103-113">Administration and Diagnostics</span></span>](../index.md)
