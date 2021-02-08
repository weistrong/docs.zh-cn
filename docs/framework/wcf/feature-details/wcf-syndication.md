---
description: 了解详细信息： WCF 联合
title: WCF 联合
ms.date: 03/30/2017
helpviewer_keywords:
- syndication [WCF]
ms.assetid: ebf80384-0fc9-4919-a1e8-23ca2a13e300
ms.openlocfilehash: 4bf4dcd40c1b764fd937c03244460c726be94a49
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99779499"
---
# <a name="wcf-syndication"></a><span data-ttu-id="83d2d-103">WCF 联合</span><span class="sxs-lookup"><span data-stu-id="83d2d-103">WCF Syndication</span></span>

<span data-ttu-id="83d2d-104">Windows Communication Foundation (WCF) 提供了在 Atom、RSS 或其他自定义格式中轻松使用联合源的支持，这允许你读取和创建它们，并在服务终结点上公开它们。</span><span class="sxs-lookup"><span data-stu-id="83d2d-104">Windows Communication Foundation (WCF) provides support to easily work with syndication feeds in Atom, RSS or other custom formats, which allows you to read and create them as well as expose them on a service endpoint.</span></span> <span data-ttu-id="83d2d-105">本节中的主题详细描述用于联合的此种编程模型。</span><span class="sxs-lookup"><span data-stu-id="83d2d-105">The topics in this section describe this programming model for syndication in detail.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="83d2d-106">本节内容</span><span class="sxs-lookup"><span data-stu-id="83d2d-106">In This Section</span></span>  

 [<span data-ttu-id="83d2d-107">WCF 联合概述</span><span class="sxs-lookup"><span data-stu-id="83d2d-107">WCF Syndication Overview</span></span>](wcf-syndication-overview.md)  
 <span data-ttu-id="83d2d-108">概述 WCF 提供的联合支持。</span><span class="sxs-lookup"><span data-stu-id="83d2d-108">Provides an overview of syndication support provided by WCF.</span></span>  
  
 [<span data-ttu-id="83d2d-109">联合体系结构</span><span class="sxs-lookup"><span data-stu-id="83d2d-109">Architecture of Syndication</span></span>](architecture-of-syndication.md)  
 <span data-ttu-id="83d2d-110">描述对象模型中的类和联合的扩展性。</span><span class="sxs-lookup"><span data-stu-id="83d2d-110">Describes the classes in the object model and the extensibility of syndication.</span></span>  
  
 [<span data-ttu-id="83d2d-111">WCF 联合对象模型如何映射到 Atom 和 RSS</span><span class="sxs-lookup"><span data-stu-id="83d2d-111">How the WCF Syndication Object Model Maps to Atom and RSS</span></span>](how-the-wcf-syndication-object-model-maps-to-atom-and-rss.md)  
 <span data-ttu-id="83d2d-112">描述源在 WCF 联合对象模型中的表示方式以及如何将它们转换为 RSS 和 Atom 源。</span><span class="sxs-lookup"><span data-stu-id="83d2d-112">Describes how feeds are represented within the WCF Syndication Object Model and how they are converted to RSS and Atom feeds.</span></span>  
  
 [<span data-ttu-id="83d2d-113">如何：创建基本 RSS 源</span><span class="sxs-lookup"><span data-stu-id="83d2d-113">How to: Create a Basic RSS Feed</span></span>](how-to-create-a-basic-rss-feed.md)  
 <span data-ttu-id="83d2d-114">演示如何创建可使基本 RSS 源可用的服务。</span><span class="sxs-lookup"><span data-stu-id="83d2d-114">Shows how to create a service that makes a basic RSS feed available.</span></span>  
  
 [<span data-ttu-id="83d2d-115">如何：创建基本 Atom 源</span><span class="sxs-lookup"><span data-stu-id="83d2d-115">How to: Create a Basic Atom Feed</span></span>](how-to-create-a-basic-atom-feed.md)  
 <span data-ttu-id="83d2d-116">演示如何创建可使基本 ATOM 源可用的服务。</span><span class="sxs-lookup"><span data-stu-id="83d2d-116">Shows how to create a service that makes a basic ATOM feed available.</span></span>  
  
 [<span data-ttu-id="83d2d-117">如何：作为 Atom 和 RSS 公开源</span><span class="sxs-lookup"><span data-stu-id="83d2d-117">How to: Expose a Feed as Both Atom and RSS</span></span>](how-to-expose-a-feed-as-both-atom-and-rss.md)  
 <span data-ttu-id="83d2d-118">演示如何创建可将同一个源用于 ATOM 和 RSS 的服务。</span><span class="sxs-lookup"><span data-stu-id="83d2d-118">Shows how to create a service that makes the same feed available with ATOM and RSS.</span></span>  
  
 [<span data-ttu-id="83d2d-119">联合扩展性</span><span class="sxs-lookup"><span data-stu-id="83d2d-119">Syndication Extensibility</span></span>](syndication-extensibility.md)  
 <span data-ttu-id="83d2d-120">描述向联合源添加自定义元素和属性的方法。</span><span class="sxs-lookup"><span data-stu-id="83d2d-120">Describes the methods of adding custom elements and attributes to a syndication feed.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="83d2d-121">参考</span><span class="sxs-lookup"><span data-stu-id="83d2d-121">Reference</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="83d2d-122">相关章节</span><span class="sxs-lookup"><span data-stu-id="83d2d-122">Related Sections</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="83d2d-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="83d2d-123">See also</span></span>

- [<span data-ttu-id="83d2d-124">WCF Web HTTP 编程模型</span><span class="sxs-lookup"><span data-stu-id="83d2d-124">WCF Web HTTP Programming Model</span></span>](wcf-web-http-programming-model.md)
- [<span data-ttu-id="83d2d-125">部分信任</span><span class="sxs-lookup"><span data-stu-id="83d2d-125">Partial Trust</span></span>](partial-trust.md)
