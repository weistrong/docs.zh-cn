---
description: 详细了解：应用程序开发中的 PNRP
title: 应用程序开发中的 PNRP
ms.date: 03/30/2017
ms.assetid: 265615d6-4423-4b5d-8626-752e456f4f4e
ms.openlocfilehash: d3e6e9a329f292d3cde7fb906b28452a4e67fb1c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99794879"
---
# <a name="pnrp-in-application-development"></a><span data-ttu-id="75e3d-103">应用程序开发中的 PNRP</span><span class="sxs-lookup"><span data-stu-id="75e3d-103">PNRP in Application Development</span></span>

<span data-ttu-id="75e3d-104">Windows Vista 中，网络应用程序可以通过简化的 PNRP 应用程序编程接口 (API) 访问名称发布和解析函数。</span><span class="sxs-lookup"><span data-stu-id="75e3d-104">In Windows Vista, networking applications can access name publication and resolution functions through a simplified PNRP application programming interface (API).</span></span>  
  
## <a name="implementing-the-peer-name-resolution-protocol"></a><span data-ttu-id="75e3d-105">执行对等名称解析协议</span><span class="sxs-lookup"><span data-stu-id="75e3d-105">Implementing the Peer Name Resolution Protocol</span></span>  

 <span data-ttu-id="75e3d-106">借助简化的 PNRP API，无需显式指定云注册名称和地址，PNRP 组件自动决定要加入的合适的云以及要在云中发布的地址。</span><span class="sxs-lookup"><span data-stu-id="75e3d-106">With the simplified PNRP API, clouds are not explicitly specified to register the name and addresses; the PNRP component automatically determines the appropriate clouds to join and the addresses to publish within the clouds.</span></span>  
  
 <span data-ttu-id="75e3d-107">对于 Windows Vista 中高度简化的 PNRP 名称解析, PNRP 名称现已集成到 getaddrinfo() Windows 套接字函数。</span><span class="sxs-lookup"><span data-stu-id="75e3d-107">For highly simplified PNRP name resolution in Windows Vista, PNRP names are now integrated into the getaddrinfo() Windows Sockets function.</span></span> <span data-ttu-id="75e3d-108">若要使用 PNRP 将名称解析为 IPv6 地址，应用程序可以使用 getaddrinfo() 函数解析完全限定的域名 (FQDN) name.prnp.net，其中名称是正在解析的对等名称。</span><span class="sxs-lookup"><span data-stu-id="75e3d-108">To use PNRP to resolve a name to an IPv6 address, applications can use the getaddrinfo() function to resolve the Fully Qualified Domain Name (FQDN) name.prnp.net, in which name is peer name being resolved.</span></span> <span data-ttu-id="75e3d-109">pnrp.net 域是 Windows Vista 中保留用于 PNRP 名称解析的域。</span><span class="sxs-lookup"><span data-stu-id="75e3d-109">The pnrp.net domain is a reserved domain in Windows Vista for PNRP name resolution.</span></span>  
  
 <span data-ttu-id="75e3d-110">PeerToPeer 应用程序之间传递的消息仍由基础体系结构处理，例如 PeerChannel 和 WCF [大型数据和流](../wcf/feature-details/large-data-and-streaming.md)。</span><span class="sxs-lookup"><span data-stu-id="75e3d-110">Message passing between PeerToPeer applications is still handled by underlying architectures such as PeerChannel and WCF [Large Data and Streaming](../wcf/feature-details/large-data-and-streaming.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="75e3d-111">另请参阅</span><span class="sxs-lookup"><span data-stu-id="75e3d-111">See also</span></span>

- <xref:System.Net.PeerToPeer>
