---
description: 了解有关以下方面的详细信息： TxFailedToNegotiateOleTx
title: System.ServiceModel.TxFailedToNegotiateOleTx
ms.date: 03/30/2017
ms.assetid: 3f0f0b4b-a1ad-4704-8329-455daf54892d
ms.openlocfilehash: c7f18ef73ff9c09cc51ad3aa6c54c2bd672d0cc3
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99735564"
---
# <a name="systemservicemodeltxfailedtonegotiateoletx"></a><span data-ttu-id="76dc8-103">System.ServiceModel.TxFailedToNegotiateOleTx</span><span class="sxs-lookup"><span data-stu-id="76dc8-103">System.ServiceModel.TxFailedToNegotiateOleTx</span></span>

<span data-ttu-id="76dc8-104">对指定协调上下文的 OleTransactions 协议协商失败。</span><span class="sxs-lookup"><span data-stu-id="76dc8-104">The OleTransactions protocol negotiation failed to complete for the specified coordination context.</span></span>  
  
## <a name="description"></a><span data-ttu-id="76dc8-105">说明</span><span class="sxs-lookup"><span data-stu-id="76dc8-105">Description</span></span>  

 <span data-ttu-id="76dc8-106">当带有 OleTx 信息的传入事务无法使用附加的 OleTx 信息，将回退并改用 WS-AT 时进行跟踪。</span><span class="sxs-lookup"><span data-stu-id="76dc8-106">Traced when an incoming transaction with OleTx information is unable to use the attached OleTx information, and will fall-back to using WS-AT instead.</span></span>  
  
## <a name="troubleshooting"></a><span data-ttu-id="76dc8-107">疑难解答</span><span class="sxs-lookup"><span data-stu-id="76dc8-107">Troubleshooting</span></span>  

 <span data-ttu-id="76dc8-108">指示计算机之间的 MSDTC RPC 通信所具有的一个潜在问题。</span><span class="sxs-lookup"><span data-stu-id="76dc8-108">Indicates a potential problem with MSDTC RPC communication between the machines.</span></span> <span data-ttu-id="76dc8-109">如果日志中出现许多此类跟踪，则可能导致性能急剧下降。</span><span class="sxs-lookup"><span data-stu-id="76dc8-109">If many of these traces appear in the log, a drastic decrease in performance can result.</span></span>  <span data-ttu-id="76dc8-110">如果不希望使用 OleTx，请在 WS-AT 注册表配置中将 `OleTxUpgradeEnabled` 设置为 0。</span><span class="sxs-lookup"><span data-stu-id="76dc8-110">If OleTx is not desired, set `OleTxUpgradeEnabled` to 0 in the WS-AT registry configuration.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="76dc8-111">请参阅</span><span class="sxs-lookup"><span data-stu-id="76dc8-111">See also</span></span>

- [<span data-ttu-id="76dc8-112">跟踪</span><span class="sxs-lookup"><span data-stu-id="76dc8-112">Tracing</span></span>](index.md)
- [<span data-ttu-id="76dc8-113">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="76dc8-113">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="76dc8-114">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="76dc8-114">Administration and Diagnostics</span></span>](../index.md)
