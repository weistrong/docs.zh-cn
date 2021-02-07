---
description: 了解详细信息：如何：使用相同类型的多个安全令牌
title: 如何：使用相同类型的多个安全令牌
ms.date: 03/30/2017
ms.assetid: cf179f48-4ed4-4caa-86a5-ef8eecc231cd
ms.openlocfilehash: 0cbf831c82fdc2aee5a09237c586286a5776d234
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99734251"
---
# <a name="how-to-use-multiple-security-tokens-of-the-same-type"></a><span data-ttu-id="071c8-103">如何：使用相同类型的多个安全令牌</span><span class="sxs-lookup"><span data-stu-id="071c8-103">How to: Use Multiple Security Tokens of the Same Type</span></span>

- <span data-ttu-id="071c8-104">在 .NET Framework 3.0 中，客户端消息只包含任何给定类型的一个令牌。</span><span class="sxs-lookup"><span data-stu-id="071c8-104">In .NET Framework 3.0, a client message only contained one token of any given type.</span></span> <span data-ttu-id="071c8-105">现在，客户端消息可以包含某种类型的多个令牌。</span><span class="sxs-lookup"><span data-stu-id="071c8-105">Now client messages can contain multiple tokens of a type.</span></span> <span data-ttu-id="071c8-106">本主题演示如何将同一类型的多个令牌包含在客户端消息中。</span><span class="sxs-lookup"><span data-stu-id="071c8-106">This topic shows how to include multiple tokens of the same type in a client message.</span></span>  
  
- <span data-ttu-id="071c8-107">请注意，不能以这种方式配置服务：一个服务只能包含一个支持令牌。</span><span class="sxs-lookup"><span data-stu-id="071c8-107">Note that you cannot configure a service in this way: a service can contain only one supporting token.</span></span>  
  
### <a name="to-use-multiple-security-tokens-of-the-same-type"></a><span data-ttu-id="071c8-108">使用相同类型的多个安全令牌</span><span class="sxs-lookup"><span data-stu-id="071c8-108">To use multiple security tokens of the same type</span></span>  
  
1. <span data-ttu-id="071c8-109">创建要填充的空绑定元素集合。</span><span class="sxs-lookup"><span data-stu-id="071c8-109">Create an empty binding element collection to be populated.</span></span>  
  
     [!code-csharp[C_CustomBinding#9](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_custombinding/cs/c_custombinding.cs#9)]  
  
2. <span data-ttu-id="071c8-110">通过调用 <xref:System.ServiceModel.Channels.SecurityBindingElement> 创建 <xref:System.ServiceModel.Channels.SecurityBindingElement.CreateMutualCertificateBindingElement%2A>。</span><span class="sxs-lookup"><span data-stu-id="071c8-110">Create a <xref:System.ServiceModel.Channels.SecurityBindingElement> by calling <xref:System.ServiceModel.Channels.SecurityBindingElement.CreateMutualCertificateBindingElement%2A>.</span></span>  
  
     [!code-csharp[C_CustomBinding#10](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_custombinding/cs/c_custombinding.cs#10)]  
  
3. <span data-ttu-id="071c8-111">创建一个 <xref:System.ServiceModel.Security.Tokens.SupportingTokenParameters> 集合。</span><span class="sxs-lookup"><span data-stu-id="071c8-111">Create a <xref:System.ServiceModel.Security.Tokens.SupportingTokenParameters> collection.</span></span>  
  
     [!code-csharp[C_CustomBinding#11](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_custombinding/cs/c_custombinding.cs#11)]  
  
4. <span data-ttu-id="071c8-112">将 SAML 令牌添加到集合中。</span><span class="sxs-lookup"><span data-stu-id="071c8-112">Add SAML tokens to the collection.</span></span>  
  
     [!code-csharp[C_CustomBinding#12](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_custombinding/cs/c_custombinding.cs#12)]  
  
5. <span data-ttu-id="071c8-113">将集合添加到 <xref:System.ServiceModel.Channels.SecurityBindingElement> 中。</span><span class="sxs-lookup"><span data-stu-id="071c8-113">Add the collection to the <xref:System.ServiceModel.Channels.SecurityBindingElement>.</span></span>  
  
     [!code-csharp[C_CustomBinding#13](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_custombinding/cs/c_custombinding.cs#13)]  
  
6. <span data-ttu-id="071c8-114">将绑定元素添加到绑定元素集合中。</span><span class="sxs-lookup"><span data-stu-id="071c8-114">Add binding elements to the binding element collection.</span></span>  
  
     [!code-csharp[C_CustomBinding#14](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_custombinding/cs/c_custombinding.cs#14)]  
  
7. <span data-ttu-id="071c8-115">返回从绑定元素集合创建的新自定义绑定。</span><span class="sxs-lookup"><span data-stu-id="071c8-115">Return a new custom binding created from the binding element collection.</span></span>  
  
     [!code-csharp[C_CustomBinding#15](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_custombinding/cs/c_custombinding.cs#15)]  
  
## <a name="example"></a><span data-ttu-id="071c8-116">示例</span><span class="sxs-lookup"><span data-stu-id="071c8-116">Example</span></span>  

 <span data-ttu-id="071c8-117">下面是前面的过程所描述的整个方法。</span><span class="sxs-lookup"><span data-stu-id="071c8-117">The following is the entire method described by the preceding procedure.</span></span>  
  
 [!code-csharp[C_CustomBinding#7](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_custombinding/cs/c_custombinding.cs#7)]  
