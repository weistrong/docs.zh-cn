---
description: 了解有关以下内容的详细信息： TransactionBridge. VolatileParticipantInDoubt
title: Microsoft.Transactions.TransactionBridge.VolatileParticipantInDoubt
ms.date: 03/30/2017
ms.assetid: 3e8fc825-9f22-47e7-9c16-d64ef291c932
ms.openlocfilehash: c9d95285e09d017aa82c86e7c5c6f9fd758b9f80
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99803238"
---
# <a name="microsofttransactionstransactionbridgevolatileparticipantindoubt"></a><span data-ttu-id="b9e80-103">Microsoft.Transactions.TransactionBridge.VolatileParticipantInDoubt</span><span class="sxs-lookup"><span data-stu-id="b9e80-103">Microsoft.Transactions.TransactionBridge.VolatileParticipantInDoubt</span></span>

<span data-ttu-id="b9e80-104">协议服务从无法识别的可变参与者接收到已准备或重播消息。</span><span class="sxs-lookup"><span data-stu-id="b9e80-104">The WS-AT protocol service received a Prepared or Replay message from an unrecognized volatile participant.</span></span> <span data-ttu-id="b9e80-105">已向参与者返回错误，声明事务的结果不确定。</span><span class="sxs-lookup"><span data-stu-id="b9e80-105">A fault was returned to the participant, declares that the transaction's outcome is in doubt.</span></span>  
  
## <a name="description"></a><span data-ttu-id="b9e80-106">说明</span><span class="sxs-lookup"><span data-stu-id="b9e80-106">Description</span></span>  

 <span data-ttu-id="b9e80-107">在本地事务管理器从它已经忘记的可变参与者接收到已准备或重播消息时进行跟踪。</span><span class="sxs-lookup"><span data-stu-id="b9e80-107">Traced when the local Transaction Manager receives a Prepared or Replay message from a Volatile enlistment that it has already forgotten.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="b9e80-108">疑难解答</span><span class="sxs-lookup"><span data-stu-id="b9e80-108">Troubleshooting</span></span>  

 <span data-ttu-id="b9e80-109">调查来自可变参与者的最新消息的可能原因。</span><span class="sxs-lookup"><span data-stu-id="b9e80-109">Investigate potential causes of late messages coming from the Volatile participant.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b9e80-110">请参阅</span><span class="sxs-lookup"><span data-stu-id="b9e80-110">See also</span></span>

- [<span data-ttu-id="b9e80-111">跟踪</span><span class="sxs-lookup"><span data-stu-id="b9e80-111">Tracing</span></span>](index.md)
- [<span data-ttu-id="b9e80-112">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="b9e80-112">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="b9e80-113">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="b9e80-113">Administration and Diagnostics</span></span>](../index.md)
