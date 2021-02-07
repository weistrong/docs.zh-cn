---
description: 了解有关以下方面的详细信息： TxCompletionStatusCompletedForError
title: System.ServiceModel.TxCompletionStatusCompletedForError
ms.date: 03/30/2017
ms.assetid: 8ade4722-a6d5-471c-b960-1cfea4ea2aa9
ms.openlocfilehash: 83cd5c258b3a60f69cc94426aed7ccc1d27f6013
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99735603"
---
# <a name="systemservicemodeltxcompletionstatuscompletedforerror"></a><span data-ttu-id="1b64a-103">System.ServiceModel.TxCompletionStatusCompletedForError</span><span class="sxs-lookup"><span data-stu-id="1b64a-103">System.ServiceModel.TxCompletionStatusCompletedForError</span></span>

<span data-ttu-id="1b64a-104">由于未处理的执行异常，导致指定操作的指定事务处于完成状态。</span><span class="sxs-lookup"><span data-stu-id="1b64a-104">The specified transaction for the specified operation was completed due to an unhandled execution exception.</span></span>  
  
## <a name="description"></a><span data-ttu-id="1b64a-105">说明</span><span class="sxs-lookup"><span data-stu-id="1b64a-105">Description</span></span>  

 <span data-ttu-id="1b64a-106">在尝试完成当前事务过程中发生错误时跟踪。</span><span class="sxs-lookup"><span data-stu-id="1b64a-106">Traced when an error occurs during an attempt to complete the current transaction.</span></span> <span data-ttu-id="1b64a-107">在将答复或错误发送给调用方之前，会发生此情况。</span><span class="sxs-lookup"><span data-stu-id="1b64a-107">This happens before a reply or fault is sent to the caller.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="1b64a-108">疑难解答</span><span class="sxs-lookup"><span data-stu-id="1b64a-108">Troubleshooting</span></span>  

 <span data-ttu-id="1b64a-109">检查跟踪的消息，以查找异常消息和所有可操作的项。</span><span class="sxs-lookup"><span data-stu-id="1b64a-109">Inspect the traced message for the exception message and any actionable items.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1b64a-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="1b64a-110">See also</span></span>

- [<span data-ttu-id="1b64a-111">跟踪</span><span class="sxs-lookup"><span data-stu-id="1b64a-111">Tracing</span></span>](index.md)
- [<span data-ttu-id="1b64a-112">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="1b64a-112">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="1b64a-113">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="1b64a-113">Administration and Diagnostics</span></span>](../index.md)
