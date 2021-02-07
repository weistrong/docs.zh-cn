---
description: 了解详细信息：发现版本控制
title: 发现版本控制
ms.date: 03/30/2017
ms.assetid: f91c6d0a-3af2-45c5-9a5c-e75390619836
ms.openlocfilehash: 075fefce0477810336c8b857343984070ed89b37
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99743182"
---
# <a name="discovery-versioning"></a><span data-ttu-id="a607d-103">发现版本控制</span><span class="sxs-lookup"><span data-stu-id="a607d-103">Discovery Versioning</span></span>

<span data-ttu-id="a607d-104">本主题简要概述了一些新增发现功能的实现，</span><span class="sxs-lookup"><span data-stu-id="a607d-104">This topic provides a brief overview of the implementation of some new discovery features.</span></span> <span data-ttu-id="a607d-105">还概述了如何选择要使用的发现版本。</span><span class="sxs-lookup"><span data-stu-id="a607d-105">It also gives an overview on how to select the discovery version to use.</span></span>

## <a name="discovery-versioning"></a><span data-ttu-id="a607d-106">发现版本控制</span><span class="sxs-lookup"><span data-stu-id="a607d-106">Discovery Versioning</span></span>

<span data-ttu-id="a607d-107">发现功能包括对 WS_Discovery 协议的三个版本的支持。</span><span class="sxs-lookup"><span data-stu-id="a607d-107">The discovery feature includes support for three versions of the WS_Discovery protocol.</span></span> <span data-ttu-id="a607d-108">使用发现 API，您可以选择要使用的协议版本。</span><span class="sxs-lookup"><span data-stu-id="a607d-108">The discovery APIs allow you to select which version of the protocol you want to use.</span></span> <span data-ttu-id="a607d-109">本文档简要介绍与版本控制相关的设置。</span><span class="sxs-lookup"><span data-stu-id="a607d-109">This document briefly describes the versioning-related settings.</span></span>

<span data-ttu-id="a607d-110">下面的发现类现在具有 <xref:System.ServiceModel.Discovery.DiscoveryVersion> 属性，并在其构造函数中采用 <xref:System.ServiceModel.Discovery.DiscoveryVersion> 参数：</span><span class="sxs-lookup"><span data-stu-id="a607d-110">The following Discovery classes now have a <xref:System.ServiceModel.Discovery.DiscoveryVersion> property and take a <xref:System.ServiceModel.Discovery.DiscoveryVersion> argument in their constructors:</span></span>

- <xref:System.ServiceModel.Discovery.AnnouncementEndpoint>

- <xref:System.ServiceModel.Discovery.DiscoveryEndpoint>

- <xref:System.ServiceModel.Discovery.UdpDiscoveryEndpoint>

- <xref:System.ServiceModel.Discovery.UdpAnnouncementEndpoint>

### <a name="discoveryversionwsdiscoveryapril2005"></a><span data-ttu-id="a607d-111">DiscoveryVersion.WSDiscoveryApril2005</span><span class="sxs-lookup"><span data-stu-id="a607d-111">DiscoveryVersion.WSDiscoveryApril2005</span></span>

<span data-ttu-id="a607d-112"><xref:System.ServiceModel.Discovery.DiscoveryVersion.WSDiscoveryApril2005>作为构造函数参数提供可使实现使用 WS-Discovery 协议的 April2005 版本。</span><span class="sxs-lookup"><span data-stu-id="a607d-112">Providing <xref:System.ServiceModel.Discovery.DiscoveryVersion.WSDiscoveryApril2005> as a constructor parameter makes the implementation use the April2005 version of the WS-Discovery protocol.</span></span> <span data-ttu-id="a607d-113">此版本对应于 WS-Discovery 协议规范的已发布版本。</span><span class="sxs-lookup"><span data-stu-id="a607d-113">This version corresponds to the published version of the WS-Discovery protocol specification.</span></span> <span data-ttu-id="a607d-114">此版本应当用于与使用 April2005 版 WS-Discovery 的旧版应用程序进行互操作。</span><span class="sxs-lookup"><span data-stu-id="a607d-114">This version should be used to interoperate with legacy application utilizing the April2005 version of WS-Discovery.</span></span>

### <a name="discoveryversionwsdiscovery11"></a><span data-ttu-id="a607d-115">DiscoveryVersion.WSDiscovery11</span><span class="sxs-lookup"><span data-stu-id="a607d-115">DiscoveryVersion.WSDiscovery11</span></span>

<span data-ttu-id="a607d-116">Api 使用的默认发现版本是 <xref:System.ServiceModel.Discovery.DiscoveryVersion.WSDiscovery11> 。</span><span class="sxs-lookup"><span data-stu-id="a607d-116">The default discovery version used by the APIs is <xref:System.ServiceModel.Discovery.DiscoveryVersion.WSDiscovery11>.</span></span> <span data-ttu-id="a607d-117">这是 WS-Discovery 协议的当前标准化版本。</span><span class="sxs-lookup"><span data-stu-id="a607d-117">This is the current standardized version of the WS-Discovery protocol.</span></span>

## <a name="discoveryversionwsdiscoverycd1"></a><span data-ttu-id="a607d-118">DiscoveryVersion.WSDiscoveryCD1</span><span class="sxs-lookup"><span data-stu-id="a607d-118">DiscoveryVersion.WSDiscoveryCD1</span></span>

<span data-ttu-id="a607d-119">作为构造函数参数提供 <xref:System.ServiceModel.Discovery.DiscoveryVersion.WSDiscoveryCD1> 可使实现使用 WS-Discovery 协议的委员会草案第 1 版。</span><span class="sxs-lookup"><span data-stu-id="a607d-119">Providing <xref:System.ServiceModel.Discovery.DiscoveryVersion.WSDiscoveryCD1> as a constructor parameter makes the implementation use the committee draft 1 version of the WS-Discovery protocol.</span></span> <span data-ttu-id="a607d-120">此协议版本应当用于与运行 CD1 版 WS-Discovery 协议的实现进行互操作。</span><span class="sxs-lookup"><span data-stu-id="a607d-120">This version of the protocol should be used to interoperate with implementations running the CD1 version of the WS-Discovery protocol.</span></span>

## <a name="supporting-multiple-udp-discovery-endpoints-for-different-discovery-versions-on-a-single-service-host"></a><span data-ttu-id="a607d-121">支持单一服务主机上不同发现版本的多个 UDP 发现终结点</span><span class="sxs-lookup"><span data-stu-id="a607d-121">Supporting Multiple UDP Discovery Endpoints for Different Discovery Versions on a Single Service Host</span></span>

<span data-ttu-id="a607d-122">您可能希望在单一服务主机上对不同发现版本公开多个 UDP 发现终结点。</span><span class="sxs-lookup"><span data-stu-id="a607d-122">You may want to expose multiple UDP Discovery Endpoints for different discovery versions on a single service host.</span></span> <span data-ttu-id="a607d-123">为此，必须为每个 UDP 发现终结点指定唯一的地址。</span><span class="sxs-lookup"><span data-stu-id="a607d-123">To do this you must specify a unique address for each UDP discovery endpoint.</span></span> <span data-ttu-id="a607d-124">以下示例演示如何执行此操作。</span><span class="sxs-lookup"><span data-stu-id="a607d-124">The following example shows how to do this.</span></span>

```csharp
UdpDiscoveryEndpoint newVersionUdpEndpoint = new UdpDiscoveryEndpoint(DiscoveryVersion.WSDiscovery11);
UdpDiscoveryEndpoint oldVersionUdpEndpoint = new UdpDiscoveryEndpoint(DiscoveryVersion.WSDiscoveryApril2005);

newVersionUdpEndpoint.Address = new EndpointAddress(newVersionUdpEndpoint.Address.Uri.ToString() + "/version11");
oldVersionUdpEndpoint.Address = new EndpointAddress(oldVersionUdpEndpoint.Address.Uri.ToString() + "/versionApril2005");

serviceHost.AddServiceEndpoint(newVersionUdpEndpoint);
serviceHost.AddServiceEndpoint(oldVersionUdpEndpoint);
```
