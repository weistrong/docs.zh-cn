---
description: 详细了解：NetworkInformation
title: NetworkInformation
ms.date: 03/30/2017
helpviewer_keywords:
- Network
ms.assetid: 31b44dd3-b903-4a48-8419-40419a3e4038
ms.openlocfilehash: 9092fd0593d9046f419018b882c08066a6bc654c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99785700"
---
# <a name="networkinformation"></a><span data-ttu-id="a07e9-103">NetworkInformation</span><span class="sxs-lookup"><span data-stu-id="a07e9-103">NetworkInformation</span></span>

<span data-ttu-id="a07e9-104"><xref:System.Net.NetworkInformation> 命名空间使你能够收集有关网络事件、更改、统计信息和属性的信息。</span><span class="sxs-lookup"><span data-stu-id="a07e9-104">The <xref:System.Net.NetworkInformation> namespace enables you to gather information about network events, changes, statistics, and properties.</span></span> <span data-ttu-id="a07e9-105">还可使用 <xref:System.Net.NetworkInformation.Ping?displayProperty=nameWithType> 类来确定是否可以访问远程主机。</span><span class="sxs-lookup"><span data-stu-id="a07e9-105">You can also determine whether a remote host is reachable by using the <xref:System.Net.NetworkInformation.Ping?displayProperty=nameWithType> class.</span></span>  
  
## <a name="network-availability-and-events"></a><span data-ttu-id="a07e9-106">网络可用性和事件</span><span class="sxs-lookup"><span data-stu-id="a07e9-106">Network Availability and Events</span></span>  

 <span data-ttu-id="a07e9-107"><xref:System.Net.NetworkInformation.NetworkChange?displayProperty=nameWithType> 类使你能确定是否已更改网络地址或可用性。</span><span class="sxs-lookup"><span data-stu-id="a07e9-107">The <xref:System.Net.NetworkInformation.NetworkChange?displayProperty=nameWithType> class enables you to determine whether the network address or availability has changed.</span></span> <span data-ttu-id="a07e9-108">若要使用此类，请创建事件处理程序来处理更改，并将其与 <xref:System.Net.NetworkInformation.NetworkAddressChangedEventHandler> 或 <xref:System.Net.NetworkInformation.NetworkAvailabilityChangedEventHandler> 关联。</span><span class="sxs-lookup"><span data-stu-id="a07e9-108">To use this class, create an event handler to process the change, and associate it with a <xref:System.Net.NetworkInformation.NetworkAddressChangedEventHandler> or a <xref:System.Net.NetworkInformation.NetworkAvailabilityChangedEventHandler>.</span></span> <span data-ttu-id="a07e9-109">有关详细信息，请参阅[如何：检测网络可用性和地址更改](how-to-detect-network-availability-and-address-changes.md)。</span><span class="sxs-lookup"><span data-stu-id="a07e9-109">For more information, see [How to: Detect Network Availability and Address Changes](how-to-detect-network-availability-and-address-changes.md).</span></span>  
  
## <a name="network-statistics-and-properties"></a><span data-ttu-id="a07e9-110">网络统计信息和属性</span><span class="sxs-lookup"><span data-stu-id="a07e9-110">Network Statistics and Properties</span></span>  

 <span data-ttu-id="a07e9-111">可在接口或协议基础上收集网络统计信息和属性。</span><span class="sxs-lookup"><span data-stu-id="a07e9-111">You can gather network statistics and properties on an interface or protocol basis.</span></span> <span data-ttu-id="a07e9-112"><xref:System.Net.NetworkInformation.NetworkInterface>、<xref:System.Net.NetworkInformation.NetworkInterfaceType> 和 <xref:System.Net.NetworkInformation.PhysicalAddress> 类提供有关特定网络接口的信息，而 <xref:System.Net.NetworkInformation.IPInterfaceProperties>、<xref:System.Net.NetworkInformation.IPGlobalProperties>、<xref:System.Net.NetworkInformation.IPGlobalStatistics>、<xref:System.Net.NetworkInformation.TcpStatistics> 和 <xref:System.Net.NetworkInformation.UdpStatistics> 类提供有关第 3 层和第 4 层数据包的信息。</span><span class="sxs-lookup"><span data-stu-id="a07e9-112">The <xref:System.Net.NetworkInformation.NetworkInterface>, <xref:System.Net.NetworkInformation.NetworkInterfaceType>, and <xref:System.Net.NetworkInformation.PhysicalAddress> classes give information about a particular network interface, while the <xref:System.Net.NetworkInformation.IPInterfaceProperties>, <xref:System.Net.NetworkInformation.IPGlobalProperties>, <xref:System.Net.NetworkInformation.IPGlobalStatistics>, <xref:System.Net.NetworkInformation.TcpStatistics>, and <xref:System.Net.NetworkInformation.UdpStatistics> classes give information about layer 3 and layer 4 packets.</span></span> <span data-ttu-id="a07e9-113">有关详细信息，请参阅[如何：获取接口和协议信息](how-to-get-interface-and-protocol-information.md)。</span><span class="sxs-lookup"><span data-stu-id="a07e9-113">For more information, see [How to: Get Interface and Protocol Information](how-to-get-interface-and-protocol-information.md).</span></span>  
  
## <a name="determine-if-a-remote-host-is-reachable"></a><span data-ttu-id="a07e9-114">确定是否可访问远程主机</span><span class="sxs-lookup"><span data-stu-id="a07e9-114">Determine if a Remote Host is Reachable</span></span>  

 <span data-ttu-id="a07e9-115">可使用 <xref:System.Net.NetworkInformation.Ping> 类来确定远程主机是否运行、是否在线及是否可访问。</span><span class="sxs-lookup"><span data-stu-id="a07e9-115">You can use the <xref:System.Net.NetworkInformation.Ping> class to determine whether a Remote Host is up, on the network, and reachable.</span></span> <span data-ttu-id="a07e9-116">有关详细信息，请参阅[如何：Ping 主机](how-to-ping-a-host.md)。</span><span class="sxs-lookup"><span data-stu-id="a07e9-116">For more information, see [How to: Ping a Host](how-to-ping-a-host.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a07e9-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="a07e9-117">See also</span></span>

- [<span data-ttu-id="a07e9-118">网络编程示例</span><span class="sxs-lookup"><span data-stu-id="a07e9-118">Network Programming Samples</span></span>](network-programming-samples.md)

<!-- to-do: review sample links
- [Network Information Technology Sample](https://archive.msdn.microsoft.com/nclsamples/Wiki/View.aspx?title=Network%20Information)
- [NetStat Tool Technology Sample](https://archive.msdn.microsoft.com/nclsamples/Wiki/View.aspx?title=NetStat%20Tool)
- [Ping Client Technology Sample](https://archive.msdn.microsoft.com/nclsamples/Wiki/View.aspx?title=Ping%20Client)
-->
