---
description: 了解详细信息：数据传输和序列化
title: 数据传输和序列化
ms.date: 03/30/2017
helpviewer_keywords:
- data serialization [WCF]
- data transfer [WCF]
ms.assetid: 0f03c635-f3e7-4c5c-9463-3cb0135e221e
ms.openlocfilehash: 50e5068efc10d706fb9ce2634998408e48037ded
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99756560"
---
# <a name="data-transfer-and-serialization"></a><span data-ttu-id="9d99b-103">数据传输和序列化</span><span class="sxs-lookup"><span data-stu-id="9d99b-103">Data Transfer and Serialization</span></span>

<span data-ttu-id="9d99b-104">在已连接的系统中，服务和客户端依赖于数据交换来完成任何任务。</span><span class="sxs-lookup"><span data-stu-id="9d99b-104">In a connected system, services and clients depend on the exchange of data to accomplish any task.</span></span> <span data-ttu-id="9d99b-105">作为服务或客户端的开发人员，你还必须了解 Windows Communication Foundation (WCF) 如何处理数据和数据序列化，以便创建高效且易于维护的应用程序。</span><span class="sxs-lookup"><span data-stu-id="9d99b-105">As a developer of a service or client, you must also understand how Windows Communication Foundation (WCF) handles data and data serialization in order to create applications that are efficient and easy to maintain.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="9d99b-106">本节内容</span><span class="sxs-lookup"><span data-stu-id="9d99b-106">In This Section</span></span>  

 [<span data-ttu-id="9d99b-107">在服务协定中指定数据传输</span><span class="sxs-lookup"><span data-stu-id="9d99b-107">Specifying Data Transfer in Service Contracts</span></span>](specifying-data-transfer-in-service-contracts.md)  
 <span data-ttu-id="9d99b-108">描述服务中数据传输的基本概念。</span><span class="sxs-lookup"><span data-stu-id="9d99b-108">Describes the basic concepts of data transfer in services.</span></span>  
  
 [<span data-ttu-id="9d99b-109">使用数据协定</span><span class="sxs-lookup"><span data-stu-id="9d99b-109">Using Data Contracts</span></span>](using-data-contracts.md)  
 <span data-ttu-id="9d99b-110">描述什么是数据协定以及如何创建和使用它们。</span><span class="sxs-lookup"><span data-stu-id="9d99b-110">Describes what data contracts are and how to create and use them.</span></span>  
  
 [<span data-ttu-id="9d99b-111">数据协定序列化程序</span><span class="sxs-lookup"><span data-stu-id="9d99b-111">Data Contract Serializer</span></span>](data-contract-serializer.md)  
 <span data-ttu-id="9d99b-112">描述如何通过 <xref:System.Runtime.Serialization.DataContractSerializer> 类或 <xref:System.Runtime.Serialization.XmlObjectSerializer> 类的任何扩展完成数据序列化。</span><span class="sxs-lookup"><span data-stu-id="9d99b-112">Describes how to accomplish serialization of data with the <xref:System.Runtime.Serialization.DataContractSerializer> class or any extension of the <xref:System.Runtime.Serialization.XmlObjectSerializer> class.</span></span>  
  
 [<span data-ttu-id="9d99b-113">使用 XmlSerializer 类</span><span class="sxs-lookup"><span data-stu-id="9d99b-113">Using the XmlSerializer Class</span></span>](using-the-xmlserializer-class.md)  
 <span data-ttu-id="9d99b-114">描述如何使用以及为什么使用 <xref:System.Xml.Serialization.XmlSerializer> 类（<xref:System.Runtime.Serialization.DataContractSerializer> 类的替代类）。</span><span class="sxs-lookup"><span data-stu-id="9d99b-114">Describes how and why to use the <xref:System.Xml.Serialization.XmlSerializer> class, an alternative to the <xref:System.Runtime.Serialization.DataContractSerializer> class.</span></span>  
  
 [<span data-ttu-id="9d99b-115">使用消息约定</span><span class="sxs-lookup"><span data-stu-id="9d99b-115">Using Message Contracts</span></span>](using-message-contracts.md)  
 <span data-ttu-id="9d99b-116">描述消息协定如何允许很好的控制 SOAP 消息。</span><span class="sxs-lookup"><span data-stu-id="9d99b-116">Describes how message contracts allow fine control over SOAP messages.</span></span>  
  
 [<span data-ttu-id="9d99b-117">使用 Message 类</span><span class="sxs-lookup"><span data-stu-id="9d99b-117">Using the Message Class</span></span>](using-the-message-class.md)  
 <span data-ttu-id="9d99b-118">描述如何使用消息类功能。</span><span class="sxs-lookup"><span data-stu-id="9d99b-118">Describes how to use Message class features.</span></span>  
  
 [<span data-ttu-id="9d99b-119">筛选</span><span class="sxs-lookup"><span data-stu-id="9d99b-119">Filtering</span></span>](filtering.md)  
 <span data-ttu-id="9d99b-120">描述基于各种条件启用消息预处理的筛选。</span><span class="sxs-lookup"><span data-stu-id="9d99b-120">Describes filtering, which enables pre-processing of a message based on various criteria.</span></span>  
  
 [<span data-ttu-id="9d99b-121">大型数据和流</span><span class="sxs-lookup"><span data-stu-id="9d99b-121">Large Data and Streaming</span></span>](large-data-and-streaming.md)  
 <span data-ttu-id="9d99b-122">描述如何发送大数据块，如二进制文件。</span><span class="sxs-lookup"><span data-stu-id="9d99b-122">Describes how to send a large block of data, such as a binary file.</span></span>  
  
 [<span data-ttu-id="9d99b-123">数据的安全考虑事项</span><span class="sxs-lookup"><span data-stu-id="9d99b-123">Security Considerations for Data</span></span>](security-considerations-for-data.md)  
 <span data-ttu-id="9d99b-124">描述在对数据传输和序列化进行编程时要注意的项。</span><span class="sxs-lookup"><span data-stu-id="9d99b-124">Describes items to be aware of when programming data transfer and serialization.</span></span>  
  
 [<span data-ttu-id="9d99b-125">数据传输体系结构概述</span><span class="sxs-lookup"><span data-stu-id="9d99b-125">Data Transfer Architectural Overview</span></span>](data-transfer-architectural-overview.md)  
 <span data-ttu-id="9d99b-126">描述 WCF 中数据传输的总体设计。</span><span class="sxs-lookup"><span data-stu-id="9d99b-126">Describes a view of the overall design of data transfer in WCF.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="9d99b-127">参考</span><span class="sxs-lookup"><span data-stu-id="9d99b-127">Reference</span></span>  

 <xref:System.ServiceModel>  
  
 <xref:System.Runtime.Serialization.DataContractSerializer>  
  
 <xref:System.Xml.Serialization.XmlSerializer>  
  
 <xref:System.Runtime.Serialization>  
  
 <xref:System.Xml.Serialization>  
  
## <a name="related-sections"></a><span data-ttu-id="9d99b-128">相关章节</span><span class="sxs-lookup"><span data-stu-id="9d99b-128">Related Sections</span></span>  

 [<span data-ttu-id="9d99b-129">扩展编码器和序列化程序</span><span class="sxs-lookup"><span data-stu-id="9d99b-129">Extending Encoders and Serializers</span></span>](../extending/extending-encoders-and-serializers.md)  
  
## <a name="see-also"></a><span data-ttu-id="9d99b-130">请参阅</span><span class="sxs-lookup"><span data-stu-id="9d99b-130">See also</span></span>

- [<span data-ttu-id="9d99b-131">最佳做法：数据协定版本管理</span><span class="sxs-lookup"><span data-stu-id="9d99b-131">Best Practices: Data Contract Versioning</span></span>](../best-practices-data-contract-versioning.md)
- [<span data-ttu-id="9d99b-132">服务版本控制</span><span class="sxs-lookup"><span data-stu-id="9d99b-132">Service Versioning</span></span>](../service-versioning.md)
