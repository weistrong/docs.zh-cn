---
description: 了解详细信息：使用 WS-AtomicTransaction
title: 使用 WS-AtomicTransaction
ms.date: 03/30/2017
helpviewer_keywords:
- WS-AT protocol [WCF]
ms.assetid: 04a4c200-0af0-4c5d-a3d9-87cb7339e054
ms.openlocfilehash: c79a5912289d0dca9f671e614e69e54b82bba854
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99756027"
---
# <a name="using-ws-atomictransaction"></a><span data-ttu-id="97576-103">使用 WS-AtomicTransaction</span><span class="sxs-lookup"><span data-stu-id="97576-103">Using WS-AtomicTransaction</span></span>

<span data-ttu-id="97576-104">WS-AtomicTransaction (WS-AT) 是一种可互操作的事务协议。</span><span class="sxs-lookup"><span data-stu-id="97576-104">WS-AtomicTransaction (WS-AT) is an interoperable transaction protocol.</span></span> <span data-ttu-id="97576-105">它使您能够使用 Web 服务消息对分布式事务进行流处理并以可互操作的方式在异类事务基础结构之间进行协调。</span><span class="sxs-lookup"><span data-stu-id="97576-105">It enables you to flow distributed transactions by using Web service messages, and coordinate in an interoperable manner between heterogeneous transaction infrastructures.</span></span> <span data-ttu-id="97576-106">WS-AT 使用两阶段提交协议在分布式应用程序、事务管理器和资源管理器之间驱动原子结果的生成。</span><span class="sxs-lookup"><span data-stu-id="97576-106">WS-AT uses the two-phase commit protocol to drive an atomic outcome between distributed applications, transaction managers, and resource managers.</span></span>  
  
 <span data-ttu-id="97576-107"> (WCF) 提供的 WS-AT 实现 Windows Communication Foundation 提供的协议服务内置于 Microsoft 分布式事务处理协调器 (MSDTC) 事务管理器中。</span><span class="sxs-lookup"><span data-stu-id="97576-107">The WS-AT implementation Windows Communication Foundation (WCF) provides includes a protocol service built into the Microsoft Distributed Transaction Coordinator (MSDTC) transaction manager.</span></span> <span data-ttu-id="97576-108">使用 WS-AT，WCF 应用程序可将事务流式传输到其他应用程序，包括使用第三方技术生成的可互操作的 Web 服务。</span><span class="sxs-lookup"><span data-stu-id="97576-108">Using WS-AT, WCF applications can flow transactions to other applications, including interoperable Web services built using third-party technology.</span></span>  
  
 <span data-ttu-id="97576-109">在客户端应用程序和服务器应用程序之间流动事务时，使用的事务协议由服务器在终结点上公开的绑定确定，而该终结点由客户端选择。</span><span class="sxs-lookup"><span data-stu-id="97576-109">When flowing a transaction between a client application and a server application, the transaction protocol used is determined by the binding that the server exposes on the endpoint the client selected.</span></span> <span data-ttu-id="97576-110">某些 WCF 系统提供的绑定默认为将 `OleTransactions` 协议指定为事务传播格式，而另一些则默认为指定 ws-at。</span><span class="sxs-lookup"><span data-stu-id="97576-110">Some WCF system-provided bindings default to specifying the `OleTransactions` protocol as the transaction propagation format, while others default to specifying WS-AT.</span></span> <span data-ttu-id="97576-111">您也可以以编程方式修改给定绑定内所选的事务协议。</span><span class="sxs-lookup"><span data-stu-id="97576-111">You can also programmatically modify the choice of transaction protocol inside a given binding.</span></span>  
  
 <span data-ttu-id="97576-112">协议的选择可影响以下内容：</span><span class="sxs-lookup"><span data-stu-id="97576-112">The choice of protocol influences:</span></span>  
  
- <span data-ttu-id="97576-113">使事务从客户端流动到服务器所使用的消息头的格式。</span><span class="sxs-lookup"><span data-stu-id="97576-113">The format of the message headers used to flow the transaction from client to server.</span></span>  
  
- <span data-ttu-id="97576-114">用于在客户端的事务管理器和服务器的事务之间运行两阶段提交协议以便解析事务结果的网络协议。</span><span class="sxs-lookup"><span data-stu-id="97576-114">The network protocol used to run the two-phase commit protocol between the client's transaction manager and the server's transaction, in order to resolve the outcome of the transaction.</span></span>  
  
 <span data-ttu-id="97576-115">如果使用 WCF 编写服务器和客户端，则无需使用 WS-AT。</span><span class="sxs-lookup"><span data-stu-id="97576-115">If the server and client are written using WCF, you do not need to use WS-AT.</span></span> <span data-ttu-id="97576-116">可以改为使用 `NetTcpBinding` 的默认设置并启用 `TransactionFlow` 属性，此设置将使用 `OleTransactions` 协议。</span><span class="sxs-lookup"><span data-stu-id="97576-116">Instead, you can use the default settings of `NetTcpBinding` with the `TransactionFlow` attribute enabled, which will use the `OleTransactions` protocol instead.</span></span> <span data-ttu-id="97576-117">有关详细信息，请参阅 [\<netTcpBinding>](../../configure-apps/file-schema/wcf/nettcpbinding.md)。</span><span class="sxs-lookup"><span data-stu-id="97576-117">For more information, see [\<netTcpBinding>](../../configure-apps/file-schema/wcf/nettcpbinding.md).</span></span> <span data-ttu-id="97576-118">否则，如果你要使事务流动到使用第三方技术生成的 Web 服务，则必须使用 WS-AT。</span><span class="sxs-lookup"><span data-stu-id="97576-118">Otherwise, if you are flowing transactions to Web services built on third-party technologies, you must use WS-AT.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="97576-119">请参阅</span><span class="sxs-lookup"><span data-stu-id="97576-119">See also</span></span>

- [<span data-ttu-id="97576-120">配置 WS-Atomic 事务支持</span><span class="sxs-lookup"><span data-stu-id="97576-120">Configuring WS-Atomic Transaction Support</span></span>](configuring-ws-atomic-transaction-support.md)
