---
description: 了解详细信息：如何：创建通道工厂并使用它来创建和管理通道
title: 如何：创建通道工厂并用它创建和管理通道
ms.date: 03/30/2017
ms.assetid: 018dcc30-9f61-419e-af8e-412a85e8d282
ms.openlocfilehash: 4e76e5ea0c6776e5623a2e716a3702e628f146f6
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99643470"
---
# <a name="how-to-create-a-channel-factory-and-use-it-to-create-and-manage-channels"></a><span data-ttu-id="f23f4-103">如何：创建通道工厂并用它创建和管理通道</span><span class="sxs-lookup"><span data-stu-id="f23f4-103">How to: Create a Channel Factory and Use it to Create and Manage Channels</span></span>

<span data-ttu-id="f23f4-104">通过 <xref:System.ServiceModel.DuplexChannelFactory%601> 类可以创建和管理不同类型的双工通道，客户端可以使用这些通道在服务终结点之间发送和接收消息。</span><span class="sxs-lookup"><span data-stu-id="f23f4-104">The <xref:System.ServiceModel.DuplexChannelFactory%601> class provides the means to create and manage duplex channels of different types that clients use to send and receive messages to and from service endpoints.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f23f4-105">示例</span><span class="sxs-lookup"><span data-stu-id="f23f4-105">Example</span></span>  

 <span data-ttu-id="f23f4-106">下面的代码演示如何创建通道工厂并用它来创建和管理通道。</span><span class="sxs-lookup"><span data-stu-id="f23f4-106">The following code shows how to create a channel factory and use it to create and manage channels.</span></span>  
  
 [!code-csharp[S_CustomAuthentication#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_customauthentication/cs/instance.cs#1)]  
  
## <a name="see-also"></a><span data-ttu-id="f23f4-107">请参阅</span><span class="sxs-lookup"><span data-stu-id="f23f4-107">See also</span></span>

- <xref:System.ServiceModel.DuplexChannelFactory%601>
