---
description: 了解详细信息： WCF 发现
title: WCF Discovery
ms.date: 03/30/2017
helpviewer_keywords:
- WCF [WCF], discovery
- Windows Communication Foundation [WCF], discovery
- discovery [WCF]
ms.assetid: 462c4913-f388-45a9-9042-28ae96a4e735
ms.openlocfilehash: 67fa5800209676b11e9e49171483bf514b6a190a
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99779629"
---
# <a name="wcf-discovery"></a><span data-ttu-id="0376d-103">WCF Discovery</span><span class="sxs-lookup"><span data-stu-id="0376d-103">WCF Discovery</span></span>

<span data-ttu-id="0376d-104">Windows Communication Foundation (WCF) 允许在运行时使用 WS-Discovery 协议以可互操作的方式在运行时发现服务。</span><span class="sxs-lookup"><span data-stu-id="0376d-104">Windows Communication Foundation (WCF) provides support to enable services to be discoverable at runtime in an interoperable way using the WS-Discovery protocol.</span></span> <span data-ttu-id="0376d-105">WCF 服务可以使用多播消息或发现代理服务器向网络公布其可用性。</span><span class="sxs-lookup"><span data-stu-id="0376d-105">WCF services can announce their availability to the network using a multicast message or to a discovery proxy server.</span></span> <span data-ttu-id="0376d-106">客户端应用程序可以搜索网络或发现代理服务器来查找满足一组条件的服务。</span><span class="sxs-lookup"><span data-stu-id="0376d-106">Client applications can search the network or a discovery proxy server to find services that meet a set of criteria.</span></span> <span data-ttu-id="0376d-107">本节中的主题分别概述和详细介绍了此功能的编程模型。</span><span class="sxs-lookup"><span data-stu-id="0376d-107">The topics in this section provide an overview and describe the programming model for this feature in detail.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="0376d-108">本节内容</span><span class="sxs-lookup"><span data-stu-id="0376d-108">In This Section</span></span>  

 [<span data-ttu-id="0376d-109">WCF Discovery 概述</span><span class="sxs-lookup"><span data-stu-id="0376d-109">WCF Discovery Overview</span></span>](wcf-discovery-overview.md)  
 <span data-ttu-id="0376d-110">概述 WCF 提供的 WS-Discovery 支持。</span><span class="sxs-lookup"><span data-stu-id="0376d-110">Provides an overview of WS-Discovery support provided by WCF.</span></span>  
  
 [<span data-ttu-id="0376d-111">WCF Discovery 对象模型</span><span class="sxs-lookup"><span data-stu-id="0376d-111">WCF Discovery Object Model</span></span>](wcf-discovery-object-model.md)  
 <span data-ttu-id="0376d-112">描述对象模型中的类和 WS-Discovery 支持的扩展性。</span><span class="sxs-lookup"><span data-stu-id="0376d-112">Describes the classes in the object model and extensibility of WS-Discovery support.</span></span>  
  
 [<span data-ttu-id="0376d-113">如何：以编程方式向 WCF 服务和客户端添加可发现性</span><span class="sxs-lookup"><span data-stu-id="0376d-113">How to: Programmatically Add Discoverability to a WCF Service and Client</span></span>](how-to-programmatically-add-discoverability-to-a-wcf-service-and-client.md)  
 <span data-ttu-id="0376d-114">演示如何使 Windows Communication Foundation (WCF) 服务可发现。</span><span class="sxs-lookup"><span data-stu-id="0376d-114">Shows how to make a Windows Communication Foundation (WCF) service discoverable.</span></span>  
  
 [<span data-ttu-id="0376d-115">实现发现代理</span><span class="sxs-lookup"><span data-stu-id="0376d-115">Implementing a Discovery Proxy</span></span>](implementing-a-discovery-proxy.md)  
 <span data-ttu-id="0376d-116">描述一些必需步骤，这些步骤用于实现发现代理、注册到发现代理的可检测服务以及使用发现代理查找可检测服务的客户端。</span><span class="sxs-lookup"><span data-stu-id="0376d-116">Describes the steps required to implement a discovery proxy, a discoverable service that registers with the discovery proxy, and a client that uses the discovery proxy to find the discoverable service.</span></span>  
  
 [<span data-ttu-id="0376d-117">发现版本控制</span><span class="sxs-lookup"><span data-stu-id="0376d-117">Discovery Versioning</span></span>](discovery-versioning.md)  
 <span data-ttu-id="0376d-118">简要概述了一些新发现功能的原型实现，</span><span class="sxs-lookup"><span data-stu-id="0376d-118">Provides a brief overview of a prototype implementation of some new discovery features.</span></span> <span data-ttu-id="0376d-119">还概述了如何选择要使用的发现版本。</span><span class="sxs-lookup"><span data-stu-id="0376d-119">It also gives an overview on how to select the discovery version to use.</span></span>  
  
 [<span data-ttu-id="0376d-120">在配置文件中配置发现</span><span class="sxs-lookup"><span data-stu-id="0376d-120">Configuring Discovery in a Configuration File</span></span>](configuring-discovery-in-a-configuration-file.md)  
 <span data-ttu-id="0376d-121">演示如何在配置中配置 Discovery。</span><span class="sxs-lookup"><span data-stu-id="0376d-121">Shows how to configure Discovery in configuration.</span></span>  
  
 [<span data-ttu-id="0376d-122">使用 Discovery 客户端通道</span><span class="sxs-lookup"><span data-stu-id="0376d-122">Using the Discovery Client Channel</span></span>](using-the-discovery-client-channel.md)  
 <span data-ttu-id="0376d-123">演示如何在编写 WCF 客户端应用程序时使用发现客户端通道。</span><span class="sxs-lookup"><span data-stu-id="0376d-123">Shows how to use a Discovery Client Channel when writing a WCF client application.</span></span>
