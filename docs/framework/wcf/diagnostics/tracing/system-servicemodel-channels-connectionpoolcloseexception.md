---
description: 了解有关以下方面的详细信息： ConnectionPoolCloseException
title: System.ServiceModel.Channels.ConnectionPoolCloseException
ms.date: 03/30/2017
ms.assetid: 8358898e-129e-4fac-a6bf-bf3aa4293ae2
ms.openlocfilehash: a65739cc872f3cd175d76e9113380f9f4185d498
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99644627"
---
# <a name="systemservicemodelchannelsconnectionpoolcloseexception"></a><span data-ttu-id="53078-103">System.ServiceModel.Channels.ConnectionPoolCloseException</span><span class="sxs-lookup"><span data-stu-id="53078-103">System.ServiceModel.Channels.ConnectionPoolCloseException</span></span>

<span data-ttu-id="53078-104">关闭此连接池中的连接时发生异常。</span><span class="sxs-lookup"><span data-stu-id="53078-104">An exception occurred while closing the connections in this connection pool.</span></span>  
  
## <a name="description"></a><span data-ttu-id="53078-105">说明</span><span class="sxs-lookup"><span data-stu-id="53078-105">Description</span></span>  

 <span data-ttu-id="53078-106">此错误级别跟踪表明关闭 Windows Communication Foundation (WCF) 的连接池功能所使用的连接池时出错。</span><span class="sxs-lookup"><span data-stu-id="53078-106">This error level trace indicates that an error has occurred while closing the connection pools used by Windows Communication Foundation (WCF)’s connection pooling feature.</span></span> <span data-ttu-id="53078-107">一种可能的原因是一个池连接或一组池连接在 CloseTimeout 内未成功关闭。</span><span class="sxs-lookup"><span data-stu-id="53078-107">One possible reason for this is an unsuccessful closure of a pooled connection, or a set of pooled connections within the CloseTimeout.</span></span> <span data-ttu-id="53078-108">当引发此异常时，将中止该池内所有剩余的未关闭连接，并放弃其他池内的未关闭连接。</span><span class="sxs-lookup"><span data-stu-id="53078-108">When this exception is thrown, any remaining unclosed connections within that pool are aborted; unclosed connections within other pools are abandoned.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="53078-109">请参阅</span><span class="sxs-lookup"><span data-stu-id="53078-109">See also</span></span>

- [<span data-ttu-id="53078-110">跟踪</span><span class="sxs-lookup"><span data-stu-id="53078-110">Tracing</span></span>](index.md)
- [<span data-ttu-id="53078-111">使用跟踪来排除应用程序故障</span><span class="sxs-lookup"><span data-stu-id="53078-111">Using Tracing to Troubleshoot Your Application</span></span>](using-tracing-to-troubleshoot-your-application.md)
- [<span data-ttu-id="53078-112">管理和诊断</span><span class="sxs-lookup"><span data-stu-id="53078-112">Administration and Diagnostics</span></span>](../index.md)
