---
description: 了解有关以下方面的详细信息： MessageClosedAgain
title: System.ServiceModel.MessageClosedAgain
ms.date: 03/30/2017
ms.assetid: 24c274d4-65cd-4c91-9869-bc6eb34ef979
ms.openlocfilehash: 40e6dcc8974440bd7d7f10ca30e36447c4ae790a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99716193"
---
# <a name="systemservicemodelmessageclosedagain"></a><span data-ttu-id="70037-103">System.ServiceModel.MessageClosedAgain</span><span class="sxs-lookup"><span data-stu-id="70037-103">System.ServiceModel.MessageClosedAgain</span></span>

<span data-ttu-id="70037-104">System.ServiceModel.MessageClosedAgain</span><span class="sxs-lookup"><span data-stu-id="70037-104">System.ServiceModel.MessageClosedAgain</span></span>  
  
## <a name="description"></a><span data-ttu-id="70037-105">说明</span><span class="sxs-lookup"><span data-stu-id="70037-105">Description</span></span>  

 <span data-ttu-id="70037-106">已再次关闭消息。</span><span class="sxs-lookup"><span data-stu-id="70037-106">A message was closed again.</span></span>  
  
 <span data-ttu-id="70037-107">消息只应关闭一次。</span><span class="sxs-lookup"><span data-stu-id="70037-107">A message should be closed only once.</span></span> <span data-ttu-id="70037-108">如果用户扩展代码发出此跟踪，则指示用户扩展代码正在关闭一个已经关闭的消息。</span><span class="sxs-lookup"><span data-stu-id="70037-108">If this trace is being emitted in user extension code, it indicates that the user extension code is closing a message that has already been closed.</span></span> <span data-ttu-id="70037-109">如果通过产品代码发出此跟踪，则指示用户扩展代码可能正在过早地关闭消息。</span><span class="sxs-lookup"><span data-stu-id="70037-109">If this trace is being emitted through product code, it indicates that the user extension code could potentially be closing a message too early.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="70037-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="70037-110">See also</span></span>

- [<span data-ttu-id="70037-111">跟踪</span><span class="sxs-lookup"><span data-stu-id="70037-111">Tracing</span></span>](index.md)
- [<span data-ttu-id="70037-112">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="70037-112">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="70037-113">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="70037-113">Administration and Diagnostics</span></span>](../index.md)
