---
description: 了解详细信息：绑定扩展性
title: 绑定扩展性
ms.date: 03/30/2017
ms.assetid: cabdd583-ddf5-493e-9dba-c6c31cde8f65
ms.openlocfilehash: 638d19fd0d6d4d7123f8b5e0c5702f6d34d70ff5
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99704168"
---
# <a name="binding-extensibility"></a><span data-ttu-id="5b6ab-103">绑定扩展性</span><span class="sxs-lookup"><span data-stu-id="5b6ab-103">Binding Extensibility</span></span>

<span data-ttu-id="5b6ab-104">本节包含演示 Windows Communication Foundation (WCF) 中的自定义绑定的示例。</span><span class="sxs-lookup"><span data-stu-id="5b6ab-104">This section contains samples that demonstrate custom binding in Windows Communication Foundation (WCF).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="5b6ab-105">本节内容</span><span class="sxs-lookup"><span data-stu-id="5b6ab-105">In This Section</span></span>  

 <xref:System.ServiceModel.NetHttpBinding>  
 <span data-ttu-id="5b6ab-106">演示如何实现在 <xref:System.ServiceModel.Channels.HttpTransportBindingElement> 之上堆积 <xref:System.ServiceModel.Channels.HttpsTransportBindingElement> 或 <xref:System.ServiceModel.Channels.BinaryMessageEncodingBindingElement> 的绑定。</span><span class="sxs-lookup"><span data-stu-id="5b6ab-106">Demonstrates how to implement a binding that stacks <xref:System.ServiceModel.Channels.HttpTransportBindingElement> or the <xref:System.ServiceModel.Channels.HttpsTransportBindingElement> on top of the <xref:System.ServiceModel.Channels.BinaryMessageEncodingBindingElement>.</span></span>  
  
 [<span data-ttu-id="5b6ab-107">WSStreamedHttpBinding</span><span class="sxs-lookup"><span data-stu-id="5b6ab-107">WSStreamedHttpBinding</span></span>](wsstreamedhttpbinding.md)  
 <span data-ttu-id="5b6ab-108">演示如何创建一个绑定，该绑定用于在使用 HTTP 传输时支持件流式传送方案。</span><span class="sxs-lookup"><span data-stu-id="5b6ab-108">Demonstrates how to create a binding that is designed to support streaming scenarios when the HTTP transport is used.</span></span>  
