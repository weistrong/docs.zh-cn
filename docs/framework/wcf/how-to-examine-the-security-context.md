---
description: 了解详细信息：如何：检查安全上下文
title: 如何：检查安全性上下文
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ServiceSecurityContext class
- WCF, security
- Claimset class
ms.assetid: 389b5a57-4175-4bc0-ada0-fc750d51149f
ms.openlocfilehash: e82491a877cf1f741767c91d1e7c304ba7676e6c
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99779395"
---
# <a name="how-to-examine-the-security-context"></a><span data-ttu-id="662fd-103">如何：检查安全性上下文</span><span class="sxs-lookup"><span data-stu-id="662fd-103">How to: Examine the Security Context</span></span>

<span data-ttu-id="662fd-104">在 Windows Communication Foundation (WCF) services 进行编程时，使用服务安全上下文可以确定有关用于向服务进行身份验证的客户端凭据和声明的详细信息。</span><span class="sxs-lookup"><span data-stu-id="662fd-104">When programming Windows Communication Foundation (WCF) services, the service security context enables you to determine details about the client credentials and claims used to authenticate with the service.</span></span> <span data-ttu-id="662fd-105">这是使用 <xref:System.ServiceModel.ServiceSecurityContext> 类的属性进行的。</span><span class="sxs-lookup"><span data-stu-id="662fd-105">This is done by using the properties of the <xref:System.ServiceModel.ServiceSecurityContext> class.</span></span>  
  
 <span data-ttu-id="662fd-106">例如，使用 <xref:System.ServiceModel.ServiceSecurityContext.PrimaryIdentity%2A> 或 <xref:System.ServiceModel.ServiceSecurityContext.WindowsIdentity%2A> 属性可检索当前客户端的标识。</span><span class="sxs-lookup"><span data-stu-id="662fd-106">For example, you can retrieve the identity of the current client by using the <xref:System.ServiceModel.ServiceSecurityContext.PrimaryIdentity%2A> or the <xref:System.ServiceModel.ServiceSecurityContext.WindowsIdentity%2A> property.</span></span> <span data-ttu-id="662fd-107">若要确定客户端是否匿名，请使用 <xref:System.ServiceModel.ServiceSecurityContext.IsAnonymous%2A> 属性。</span><span class="sxs-lookup"><span data-stu-id="662fd-107">To determine whether the client is anonymous, use the <xref:System.ServiceModel.ServiceSecurityContext.IsAnonymous%2A> property.</span></span>  
  
 <span data-ttu-id="662fd-108">通过循环访问 <xref:System.ServiceModel.ServiceSecurityContext.AuthorizationContext%2A> 属性中的声明集合，还可以确定以客户端的名义进行了哪些声明。</span><span class="sxs-lookup"><span data-stu-id="662fd-108">You can also determine what claims are being made on behalf of the client by iterating through the collection of claims in the <xref:System.ServiceModel.ServiceSecurityContext.AuthorizationContext%2A> property.</span></span>  
  
### <a name="to-get-the-current-security-context"></a><span data-ttu-id="662fd-109">获取当前安全上下文</span><span class="sxs-lookup"><span data-stu-id="662fd-109">To get the current security context</span></span>  
  
- <span data-ttu-id="662fd-110">访问静态属性 <xref:System.ServiceModel.ServiceSecurityContext.Current%2A> 以获取当前的安全上下文。</span><span class="sxs-lookup"><span data-stu-id="662fd-110">Access the static property <xref:System.ServiceModel.ServiceSecurityContext.Current%2A> to get the current security context.</span></span> <span data-ttu-id="662fd-111">从参考检查当前上下文的任何属性。</span><span class="sxs-lookup"><span data-stu-id="662fd-111">Examine any of the properties of the current context from the reference.</span></span>  
  
### <a name="to-determine-the-identity-of-the-caller"></a><span data-ttu-id="662fd-112">确定调用方的标识</span><span class="sxs-lookup"><span data-stu-id="662fd-112">To determine the identity of the caller</span></span>  
  
1. <span data-ttu-id="662fd-113">打印 <xref:System.ServiceModel.ServiceSecurityContext.PrimaryIdentity%2A> 和 <xref:System.ServiceModel.ServiceSecurityContext.WindowsIdentity%2A> 属性的值。</span><span class="sxs-lookup"><span data-stu-id="662fd-113">Print the value of the <xref:System.ServiceModel.ServiceSecurityContext.PrimaryIdentity%2A> and <xref:System.ServiceModel.ServiceSecurityContext.WindowsIdentity%2A> properties.</span></span>  
  
### <a name="to-parse-the-claims-of-a-caller"></a><span data-ttu-id="662fd-114">分析调用方的声明</span><span class="sxs-lookup"><span data-stu-id="662fd-114">To parse the claims of a caller</span></span>  
  
1. <span data-ttu-id="662fd-115">返回当前 <xref:System.IdentityModel.Policy.AuthorizationContext> 类。</span><span class="sxs-lookup"><span data-stu-id="662fd-115">Return the current <xref:System.IdentityModel.Policy.AuthorizationContext> class.</span></span> <span data-ttu-id="662fd-116">使用 <xref:System.ServiceModel.ServiceSecurityContext.Current%2A> 属性返回当前服务安全上下文，然后使用 `AuthorizationContext` 属性返回 <xref:System.ServiceModel.ServiceSecurityContext.AuthorizationContext%2A>。</span><span class="sxs-lookup"><span data-stu-id="662fd-116">Use the <xref:System.ServiceModel.ServiceSecurityContext.Current%2A> property to return the current service security context, then return the `AuthorizationContext` using the <xref:System.ServiceModel.ServiceSecurityContext.AuthorizationContext%2A> property.</span></span>  
  
2. <span data-ttu-id="662fd-117">分析由 <xref:System.IdentityModel.Claims.ClaimSet> 类的 <xref:System.IdentityModel.Policy.AuthorizationContext.ClaimSets%2A> 属性返回的 <xref:System.IdentityModel.Policy.AuthorizationContext> 对象的集合。</span><span class="sxs-lookup"><span data-stu-id="662fd-117">Parse the collection of <xref:System.IdentityModel.Claims.ClaimSet> objects returned by the <xref:System.IdentityModel.Policy.AuthorizationContext.ClaimSets%2A> property of the <xref:System.IdentityModel.Policy.AuthorizationContext> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="662fd-118">示例</span><span class="sxs-lookup"><span data-stu-id="662fd-118">Example</span></span>  

 <span data-ttu-id="662fd-119">下面的示例打印当前安全上下文的 <xref:System.ServiceModel.ServiceSecurityContext.WindowsIdentity%2A> 和 <xref:System.ServiceModel.ServiceSecurityContext.PrimaryIdentity%2A> 属性的值及 <xref:System.IdentityModel.Claims.Claim.ClaimType%2A> 属性、声明的资源值，以及当前安全上下文中每个声明的 <xref:System.IdentityModel.Claims.Claim.Right%2A> 属性。</span><span class="sxs-lookup"><span data-stu-id="662fd-119">The following example prints the values of the <xref:System.ServiceModel.ServiceSecurityContext.WindowsIdentity%2A> and <xref:System.ServiceModel.ServiceSecurityContext.PrimaryIdentity%2A> properties of the current security context and the <xref:System.IdentityModel.Claims.Claim.ClaimType%2A> property, the resource value of the claim, and the <xref:System.IdentityModel.Claims.Claim.Right%2A> property of every claim in the current security context.</span></span>  
  
 [!code-csharp[c_PrincipalPermissionAttribute#4](../../../samples/snippets/csharp/VS_Snippets_CFX/c_principalpermissionattribute/cs/source.cs#4)]
 [!code-vb[c_PrincipalPermissionAttribute#4](../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_principalpermissionattribute/vb/source.vb#4)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="662fd-120">编译代码</span><span class="sxs-lookup"><span data-stu-id="662fd-120">Compiling the Code</span></span>  

 <span data-ttu-id="662fd-121">该代码使用以下命名空间：</span><span class="sxs-lookup"><span data-stu-id="662fd-121">The code uses the following namespaces:</span></span>  
  
- <xref:System>  
  
- <xref:System.ServiceModel>  
  
- <xref:System.IdentityModel.Policy>  
  
- <xref:System.IdentityModel.Claims>  
  
## <a name="see-also"></a><span data-ttu-id="662fd-122">请参阅</span><span class="sxs-lookup"><span data-stu-id="662fd-122">See also</span></span>

- [<span data-ttu-id="662fd-123">保证服务的安全</span><span class="sxs-lookup"><span data-stu-id="662fd-123">Securing Services</span></span>](securing-services.md)
- [<span data-ttu-id="662fd-124">服务标识和身份验证</span><span class="sxs-lookup"><span data-stu-id="662fd-124">Service Identity and Authentication</span></span>](./feature-details/service-identity-and-authentication.md)
