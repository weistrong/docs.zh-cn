---
description: 了解详细信息：可靠会话
title: 可靠会话
ms.date: 03/30/2017
f1_keywords:
- Windows Communication Foundation, sessions and instances
- WCF, sessions and instances
- sessions and instances [WCF]
helpviewer_keywords:
- instances [WCF]
- sessions [WCF]
ms.assetid: 143951b3-3aa0-4540-b4b7-d33e77e874a1
ms.openlocfilehash: 86df4ccf9c1fd52d162ad7272ece5591f0ca7482
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99632875"
---
# <a name="reliable-sessions"></a><span data-ttu-id="2171a-103">可靠会话</span><span class="sxs-lookup"><span data-stu-id="2171a-103">Reliable Sessions</span></span>

<span data-ttu-id="2171a-104">本部分介绍了 Windows Communication Foundation (WCF) 可靠会话的内容、它的用途、使用方式以及使用方式的方式、支持它的绑定配置以及最佳实践的指针。</span><span class="sxs-lookup"><span data-stu-id="2171a-104">This section describes what a Windows Communication Foundation (WCF) reliable session is, what it's used for, how and when to use one, what binding configurations support it, and pointers on best practices.</span></span> <span data-ttu-id="2171a-105">下表汇总了有关本节中要点和相关主题的详细信息。</span><span class="sxs-lookup"><span data-stu-id="2171a-105">The following table summarizes details about the essential points and related topics in this section.</span></span>

<span data-ttu-id="2171a-106">可靠会话 WCF 提供的功能可确保在终结点之间发送的消息在 SOAP 或传输中介之间传输，并且只传递一次，并根据发送的相同顺序进行传递。</span><span class="sxs-lookup"><span data-stu-id="2171a-106">The reliable session WCF provides features ensuring that messages sent between endpoints are transferred across SOAP or transport intermediaries and are delivered only once and, optionally, in the same order in which they were sent.</span></span>

<span data-ttu-id="2171a-107">若要对 WCF 应用程序使用可靠会话，请使用 WCF 中某个系统提供的绑定（默认情况下支持可靠会话）或作为选项，或创建你自己的支持会话的自定义绑定。</span><span class="sxs-lookup"><span data-stu-id="2171a-107">To use a reliable session with a WCF application, either use one of the system-provided bindings in WCF that support a reliable session by default or as an option, or create your own custom binding that supports the session.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2171a-108">本节内容</span><span class="sxs-lookup"><span data-stu-id="2171a-108">In This Section</span></span>

<span data-ttu-id="2171a-109">[可靠会话概述](reliable-sessions-overview.md) 介绍可靠会话、何时使用它们、支持可靠会话的不同绑定，以及它们的工作方式。</span><span class="sxs-lookup"><span data-stu-id="2171a-109">[Reliable Sessions Overview](reliable-sessions-overview.md) Describes reliable sessions, when to use them, the different bindings that support reliable sessions, and how they work.</span></span>

<span data-ttu-id="2171a-110">[如何：在可靠会话内交换消息](how-to-exchange-messages-within-a-reliable-session.md) 介绍如何使用配置中指定的自定义绑定通过 HTTP 创建可靠会话。</span><span class="sxs-lookup"><span data-stu-id="2171a-110">[How to: Exchange Messages Within a Reliable Session](how-to-exchange-messages-within-a-reliable-session.md) Describes how to create a reliable session over HTTP using a custom binding specified in the configuration.</span></span>

<span data-ttu-id="2171a-111">[如何：在可靠会话内保护消息](how-to-secure-messages-within-reliable-sessions.md) 介绍如何保护可靠会话。</span><span class="sxs-lookup"><span data-stu-id="2171a-111">[How to: Secure Messages within Reliable Sessions](how-to-secure-messages-within-reliable-sessions.md) Describes how to secure a reliable session.</span></span>

<span data-ttu-id="2171a-112">[如何：使用 HTTPS 创建自定义可靠会话绑定](how-to-create-a-custom-reliable-session-binding-with-https.md) 介绍如何通过 HTTPS 创建可靠会话。</span><span class="sxs-lookup"><span data-stu-id="2171a-112">[How to: Create a Custom Reliable Session Binding with HTTPS](how-to-create-a-custom-reliable-session-binding-with-https.md) Describes how to create a reliable session over HTTPS.</span></span>

<span data-ttu-id="2171a-113">[可靠会话的最佳做法](best-practices-for-reliable-sessions.md) 介绍与使用可靠会话相关的一些最佳实践。</span><span class="sxs-lookup"><span data-stu-id="2171a-113">[Best Practices for Reliable Sessions](best-practices-for-reliable-sessions.md) Describes some of the best practices associated with using a reliable session.</span></span>

## <a name="reference"></a><span data-ttu-id="2171a-114">参考</span><span class="sxs-lookup"><span data-stu-id="2171a-114">Reference</span></span>

<xref:System.ServiceModel.ReliableSession>

## <a name="see-also"></a><span data-ttu-id="2171a-115">请参阅</span><span class="sxs-lookup"><span data-stu-id="2171a-115">See also</span></span>

- [<span data-ttu-id="2171a-116">队列和可靠会话</span><span class="sxs-lookup"><span data-stu-id="2171a-116">Queues and Reliable Sessions</span></span>](queues-and-reliable-sessions.md)
- [<span data-ttu-id="2171a-117">会话、实例化和并发</span><span class="sxs-lookup"><span data-stu-id="2171a-117">Sessions, Instancing, and Concurrency</span></span>](sessions-instancing-and-concurrency.md)
