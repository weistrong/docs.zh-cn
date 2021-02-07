---
description: 了解详细信息： 4802-DiscoveryClientProtocolExceptionSuppressed
title: 4802 - DiscoveryClientProtocolExceptionSuppressed
ms.date: 03/30/2017
ms.assetid: 568212f7-1060-4f5c-a7a0-1352c7cc743b
ms.openlocfilehash: 5183e9de704e4da4d93376eeb1dbe22f48bad918
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99744534"
---
# <a name="4802---discoveryclientprotocolexceptionsuppressed"></a><span data-ttu-id="071c3-103">4802 - DiscoveryClientProtocolExceptionSuppressed</span><span class="sxs-lookup"><span data-stu-id="071c3-103">4802 - DiscoveryClientProtocolExceptionSuppressed</span></span>

## <a name="properties"></a><span data-ttu-id="071c3-104">属性</span><span class="sxs-lookup"><span data-stu-id="071c3-104">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="071c3-105">ID</span><span class="sxs-lookup"><span data-stu-id="071c3-105">ID</span></span>|<span data-ttu-id="071c3-106">4802</span><span class="sxs-lookup"><span data-stu-id="071c3-106">4802</span></span>|  
|<span data-ttu-id="071c3-107">关键字</span><span class="sxs-lookup"><span data-stu-id="071c3-107">Keywords</span></span>|<span data-ttu-id="071c3-108">发现</span><span class="sxs-lookup"><span data-stu-id="071c3-108">Discovery</span></span>|  
|<span data-ttu-id="071c3-109">级别</span><span class="sxs-lookup"><span data-stu-id="071c3-109">Level</span></span>|<span data-ttu-id="071c3-110">信息</span><span class="sxs-lookup"><span data-stu-id="071c3-110">Information</span></span>|  
|<span data-ttu-id="071c3-111">通道</span><span class="sxs-lookup"><span data-stu-id="071c3-111">Channel</span></span>|<span data-ttu-id="071c3-112">Microsoft-Windows-应用程序服务器-应用程序/调试</span><span class="sxs-lookup"><span data-stu-id="071c3-112">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="071c3-113">说明</span><span class="sxs-lookup"><span data-stu-id="071c3-113">Description</span></span>  

 <span data-ttu-id="071c3-114">当关闭 DiscoveryClient 时，ProtocolException 被禁止，此时发出此事件。</span><span class="sxs-lookup"><span data-stu-id="071c3-114">This event is emitted when the a ProtocolException was suppressed while closing the DiscoveryClient.</span></span>  
  
## <a name="message"></a><span data-ttu-id="071c3-115">消息</span><span class="sxs-lookup"><span data-stu-id="071c3-115">Message</span></span>  

 <span data-ttu-id="071c3-116">关闭 DiscoveryClient 时，ProtocolException 被禁止。</span><span class="sxs-lookup"><span data-stu-id="071c3-116">A ProtocolException was suppressed while closing the DiscoveryClient.</span></span> <span data-ttu-id="071c3-117">这可能是由于 DiscoveryService 仍在尝试向 DiscoveryClient 发送响应。</span><span class="sxs-lookup"><span data-stu-id="071c3-117">This could be because a DiscoveryService is still trying to send response to the DiscoveryClient.</span></span>  
  
## <a name="details"></a><span data-ttu-id="071c3-118">详细信息</span><span class="sxs-lookup"><span data-stu-id="071c3-118">Details</span></span>
