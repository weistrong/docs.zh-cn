---
description: 了解详细信息：如何：创建要求会话的服务
title: 如何：创建要求会话的服务
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 8a7613ef-0df9-47c3-b8dc-47f42cb1fd8b
ms.openlocfilehash: 362aee23437bb7f45af5a265a9d3ef47bf62915c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99734459"
---
# <a name="how-to-create-a-service-that-requires-sessions"></a><span data-ttu-id="857b0-103">如何：创建要求会话的服务</span><span class="sxs-lookup"><span data-stu-id="857b0-103">How to: Create a Service That Requires Sessions</span></span>

<span data-ttu-id="857b0-104">会话在两个或更多终结点之间创建一个共享状态，从而启用一些有用的功能，例如回调、多跳安全性以及客户端和服务实例之间的关联。</span><span class="sxs-lookup"><span data-stu-id="857b0-104">Sessions create a shared state between two or more endpoints that enables useful features such as callbacks, multi-hop security, and associations between clients and service instances.</span></span> <span data-ttu-id="857b0-105">有关 Windows Communication Foundation 中的会话 (WCF) 应用程序的详细信息，请参阅 [使用会话](../using-sessions.md)。</span><span class="sxs-lookup"><span data-stu-id="857b0-105">For more information about sessions in Windows Communication Foundation (WCF) applications, see [Using Sessions](../using-sessions.md).</span></span>  
  
### <a name="to-specify-that-a-contract-require-its-binding-to-support-sessions"></a><span data-ttu-id="857b0-106">指定协定需要其绑定来支持会话</span><span class="sxs-lookup"><span data-stu-id="857b0-106">To specify that a contract require its binding to support sessions</span></span>  
  
1. <span data-ttu-id="857b0-107">创建至少包含一个操作的服务协定。</span><span class="sxs-lookup"><span data-stu-id="857b0-107">Create a service contract with at least one operation.</span></span> <span data-ttu-id="857b0-108">有关如何创建服务协定的示例，请参阅 [如何：定义服务协定](../how-to-define-a-wcf-service-contract.md)。</span><span class="sxs-lookup"><span data-stu-id="857b0-108">For an example of how to create a service contract, see [How to: Define a Service Contract](../how-to-define-a-wcf-service-contract.md).</span></span>  
  
2. <span data-ttu-id="857b0-109">修改声明协定的 <xref:System.ServiceModel.ServiceContractAttribute?displayProperty=nameWithType>，将 <xref:System.ServiceModel.ServiceContractAttribute.SessionMode%2A?displayProperty=nameWithType> 属性设置为：</span><span class="sxs-lookup"><span data-stu-id="857b0-109">Modify the <xref:System.ServiceModel.ServiceContractAttribute?displayProperty=nameWithType> that declares the contract by setting the <xref:System.ServiceModel.ServiceContractAttribute.SessionMode%2A?displayProperty=nameWithType> property to either:</span></span>  
  
    - <span data-ttu-id="857b0-110"><xref:System.ServiceModel.SessionMode.Required?displayProperty=nameWithType>（如果必须在会话中运行此协定）。</span><span class="sxs-lookup"><span data-stu-id="857b0-110"><xref:System.ServiceModel.SessionMode.Required?displayProperty=nameWithType> if this contract must be run within a session.</span></span>  
  
    - <span data-ttu-id="857b0-111"><xref:System.ServiceModel.SessionMode.Allowed?displayProperty=nameWithType>（如果可以在会话中运行此协定）。</span><span class="sxs-lookup"><span data-stu-id="857b0-111"><xref:System.ServiceModel.SessionMode.Allowed?displayProperty=nameWithType> if this contract can be run within a session.</span></span>  
  
    - <span data-ttu-id="857b0-112"><xref:System.ServiceModel.SessionMode.NotAllowed?displayProperty=nameWithType>（如果不得在会话中运行此协定）。</span><span class="sxs-lookup"><span data-stu-id="857b0-112"><xref:System.ServiceModel.SessionMode.NotAllowed?displayProperty=nameWithType> if this contract must not be run within a session.</span></span>  
  
3. <span data-ttu-id="857b0-113">配置服务终结点以使用支持会话的绑定。</span><span class="sxs-lookup"><span data-stu-id="857b0-113">Configure your service endpoint to use a binding that supports sessions.</span></span> <span data-ttu-id="857b0-114">下面的配置示例演示了支持 WS<xref:System.ServiceModel.WSDualHttpBinding?displayProperty=nameWithType>ReliableMessaging 会话的 `-` 的用法。</span><span class="sxs-lookup"><span data-stu-id="857b0-114">The following configuration example shows the use of the <xref:System.ServiceModel.WSDualHttpBinding?displayProperty=nameWithType>, which supports a WS`-`ReliableMessaging session.</span></span>  
  
     [!code-xml[SCA.Session#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/sca.session/cs/hostapplication.exe.config#2)]
  
## <a name="example"></a><span data-ttu-id="857b0-115">示例</span><span class="sxs-lookup"><span data-stu-id="857b0-115">Example</span></span>  

 <span data-ttu-id="857b0-116">下面的示例代码演示如何指定协定级别会话需求并使用配置文件来支持 <xref:System.ServiceModel.WSDualHttpBinding?displayProperty=nameWithType> 绑定的需求。</span><span class="sxs-lookup"><span data-stu-id="857b0-116">The following example code shows how to specify a contract-level session requirement and use a configuration file to support that requirement with the <xref:System.ServiceModel.WSDualHttpBinding?displayProperty=nameWithType> binding.</span></span>  
  
 [!code-csharp[SCA.Session#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/sca.session/cs/services.cs#1)]
 [!code-vb[SCA.Session#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/sca.session/vb/services.vb#1)]
 [!code-xml[SCA.Session#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/sca.session/cs/hostapplication.exe.config#2)]
  
## <a name="see-also"></a><span data-ttu-id="857b0-117">请参阅</span><span class="sxs-lookup"><span data-stu-id="857b0-117">See also</span></span>

- <xref:System.ServiceModel.ServiceContractAttribute?displayProperty=nameWithType>
- <xref:System.ServiceModel.ServiceContractAttribute.SessionMode%2A?displayProperty=nameWithType>
- <xref:System.ServiceModel.SessionMode?displayProperty=nameWithType>
