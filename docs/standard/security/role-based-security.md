---
description: 了解详细信息： Role-Based 安全性
title: 基于角色的安全性
ms.date: 07/15/2020
helpviewer_keywords:
- role-based security, about role-based security
- user authentication, principals
- principals [.NET]
- security [.NET], role-based
- permissions [.NET], principals
- authentication [.NET], principals
- role-based security, principals
ms.assetid: 578cc32b-5654-4d8b-9d8c-ebcbc5c75390
ms.openlocfilehash: 66457248ccfaa8535ce150e7654cd5be20fb6a68
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99629521"
---
# <a name="role-based-security"></a><span data-ttu-id="56bb3-103">基于角色的安全性</span><span class="sxs-lookup"><span data-stu-id="56bb3-103">Role-Based Security</span></span>

<span data-ttu-id="56bb3-104">在财务或业务应用程序中经常使用角色来强制执行策略。</span><span class="sxs-lookup"><span data-stu-id="56bb3-104">Roles are often used in financial or business applications to enforce policy.</span></span> <span data-ttu-id="56bb3-105">例如，应用程序可能会根据发出请求的用户是否是指定角色的成员，以限制其所处理事务的大小。</span><span class="sxs-lookup"><span data-stu-id="56bb3-105">For example, an application might impose limits on the size of the transaction being processed depending on whether the user making the request is a member of a specified role.</span></span> <span data-ttu-id="56bb3-106">职员处理事务的授权可能低于所指定阈值，主管可能具有更高的限制，而副总裁可能具有比主管更高的限制（或无限制）。</span><span class="sxs-lookup"><span data-stu-id="56bb3-106">Clerks might have authorization to process transactions that are less than a specified threshold, supervisors might have a higher limit, and vice-presidents might have a still higher limit (or no limit at all).</span></span> <span data-ttu-id="56bb3-107">当应用程序需要多项审批来完成操作时，也可以使用基于角色的安全性。</span><span class="sxs-lookup"><span data-stu-id="56bb3-107">Role-based security can also be used when an application requires multiple approvals to complete an action.</span></span> <span data-ttu-id="56bb3-108">这种情况可能发生在采购系统中，任何员工均可生成采购请求，但只有采购代理可以将此请求转换成可发送给供应商的采购订单。</span><span class="sxs-lookup"><span data-stu-id="56bb3-108">Such a case might be a purchasing system in which any employee can generate a purchase request, but only a purchasing agent can convert that request into a purchase order that can be sent to a supplier.</span></span>  
  
 <span data-ttu-id="56bb3-109">基于 .NET 角色的安全性通过提供有关主体的信息来支持授权，该主体是从关联的标识构造的，可用于当前线程。</span><span class="sxs-lookup"><span data-stu-id="56bb3-109">.NET role-based security supports authorization by making information about the principal, which is constructed from an associated identity, available to the current thread.</span></span> <span data-ttu-id="56bb3-110">标识（和其帮助定义的主体）可以基于 Windows 帐户，或可以为与 Windows 帐户无关的自定义标识。</span><span class="sxs-lookup"><span data-stu-id="56bb3-110">The identity (and the principal it helps to define) can be either based on a Windows account or be a custom identity unrelated to a Windows account.</span></span> <span data-ttu-id="56bb3-111">.NET 应用程序可以基于主体的标识或角色成员资格做出授权决策，也可以同时进行这两项决策。</span><span class="sxs-lookup"><span data-stu-id="56bb3-111">.NET applications can make authorization decisions based on the principal's identity or role membership, or both.</span></span> <span data-ttu-id="56bb3-112">角色是指在安全性方面具有相同特权的一组命名主体（如出纳或经理）。</span><span class="sxs-lookup"><span data-stu-id="56bb3-112">A role is a named set of principals that have the same privileges with respect to security (such as a teller or a manager).</span></span> <span data-ttu-id="56bb3-113">主体可以是一个或多个角色的成员。</span><span class="sxs-lookup"><span data-stu-id="56bb3-113">A principal can be a member of one or more roles.</span></span> <span data-ttu-id="56bb3-114">因此，应用程序可以使用角色成员身份来确定主体是否有权执行所请求的操作。</span><span class="sxs-lookup"><span data-stu-id="56bb3-114">Therefore, applications can use role membership to determine whether a principal is authorized to perform a requested action.</span></span>  
  
 <span data-ttu-id="56bb3-115">为了与代码访问安全性实现易用性和一致性，.NET 基于角色的安全性提供 <xref:System.Security.Permissions.PrincipalPermission?displayProperty=nameWithType> 使公共语言运行时能够以类似于代码访问安全检查的方式执行授权的对象。</span><span class="sxs-lookup"><span data-stu-id="56bb3-115">To provide ease of use and consistency with code access security, .NET role-based security provides <xref:System.Security.Permissions.PrincipalPermission?displayProperty=nameWithType> objects that enable the common language runtime to perform authorization in a way that is similar to code access security checks.</span></span> <span data-ttu-id="56bb3-116"><xref:System.Security.Permissions.PrincipalPermission> 类表示主体必须与之匹配，并且与两种声明性和命令性安全检查相兼容的标识和角色。</span><span class="sxs-lookup"><span data-stu-id="56bb3-116">The <xref:System.Security.Permissions.PrincipalPermission> class represents the identity or role that the principal must match and is compatible with both declarative and imperative security checks.</span></span> <span data-ttu-id="56bb3-117">还可以直接访问主体的标识信息，并在需要时在代码中执行角色和标识检查。</span><span class="sxs-lookup"><span data-stu-id="56bb3-117">You can also access a principal's identity information directly and perform role and identity checks in your code when needed.</span></span>  
  
 <span data-ttu-id="56bb3-118">.NET 提供了基于角色的安全性支持，它具有足够的灵活性和可扩展性，足以满足各种应用程序的需求。</span><span class="sxs-lookup"><span data-stu-id="56bb3-118">.NET provides role-based security support that is flexible and extensible enough to meet the needs of a wide spectrum of applications.</span></span> <span data-ttu-id="56bb3-119">你可以选择与现有身份验证基础结构进行交互操作（如 COM+ 1.0 服务）或创建自定义身份验证系统。</span><span class="sxs-lookup"><span data-stu-id="56bb3-119">You can choose to interoperate with existing authentication infrastructures, such as COM+ 1.0 Services, or to create a custom authentication system.</span></span> <span data-ttu-id="56bb3-120">基于角色的安全性非常适合在主要在服务器上进行处理 ASP.NET Web 应用程序中使用。</span><span class="sxs-lookup"><span data-stu-id="56bb3-120">Role-based security is particularly well-suited for use in ASP.NET Web applications, which are processed primarily on the server.</span></span> <span data-ttu-id="56bb3-121">但是，可以在客户端或服务器上使用基于 .NET 角色的安全性。</span><span class="sxs-lookup"><span data-stu-id="56bb3-121">However, .NET role-based security can be used on either the client or the server.</span></span>  
  
 <span data-ttu-id="56bb3-122">阅读本部分之前，请确保了解 [关键安全概念](key-security-concepts.md)中介绍的内容。</span><span class="sxs-lookup"><span data-stu-id="56bb3-122">Before reading this section, make sure that you understand the material presented in [Key Security Concepts](key-security-concepts.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="56bb3-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="56bb3-123">See also</span></span>
  
- [<span data-ttu-id="56bb3-124">主体和标识对象</span><span class="sxs-lookup"><span data-stu-id="56bb3-124">Principal and Identity Objects</span></span>](principal-and-identity-objects.md)
- [<span data-ttu-id="56bb3-125">安全性的基础概念</span><span class="sxs-lookup"><span data-stu-id="56bb3-125">Key Security Concepts</span></span>](key-security-concepts.md)
- <xref:System.Security.Permissions.PrincipalPermission?displayProperty=nameWithType>
- [<span data-ttu-id="56bb3-126">ASP.NET Core 安全性</span><span class="sxs-lookup"><span data-stu-id="56bb3-126">ASP.NET Core Security</span></span>](/aspnet/core/security/)
