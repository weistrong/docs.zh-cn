---
description: 了解详细信息： WCF 中的授权
title: WCF 中的授权
ms.date: 03/30/2017
helpviewer_keywords:
- authorization [WCF]
- security [WCF], authorization
ms.assetid: 8ea0b552-af65-45b0-a157-c6c111b8ce5e
ms.openlocfilehash: 3fda699a33d8b512d047232398e9cfac63661a85
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99643704"
---
# <a name="authorization-in-wcf"></a><span data-ttu-id="f2987-103">WCF 中的授权</span><span class="sxs-lookup"><span data-stu-id="f2987-103">Authorization in WCF</span></span>

<span data-ttu-id="f2987-104">授权是控制对资源（例如服务或文件）的访问和权限的过程。</span><span class="sxs-lookup"><span data-stu-id="f2987-104">Authorization is the process of controlling access and rights to resources, such as services or files.</span></span> <span data-ttu-id="f2987-105">本部分中的主题介绍如何以各种方式在 Windows Communication Foundation (WCF) 中执行此基本任务。</span><span class="sxs-lookup"><span data-stu-id="f2987-105">The topics in this section show you how to perform this basic task in Windows Communication Foundation (WCF) in a variety of ways.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="f2987-106">本节内容</span><span class="sxs-lookup"><span data-stu-id="f2987-106">In This Section</span></span>  

 [<span data-ttu-id="f2987-107">访问控制机制</span><span class="sxs-lookup"><span data-stu-id="f2987-107">Access Control Mechanisms</span></span>](access-control-mechanisms.md)  
 <span data-ttu-id="f2987-108">简要概述 WCF 中的授权机制，并提供建议的用法。</span><span class="sxs-lookup"><span data-stu-id="f2987-108">Provides a brief outline of the authorization mechanisms in WCF, and suggested uses.</span></span>  
  
 [<span data-ttu-id="f2987-109">如何：使用 PrincipalPermissionAttribute 类限制访问</span><span class="sxs-lookup"><span data-stu-id="f2987-109">How to: Restrict Access with the PrincipalPermissionAttribute Class</span></span>](../how-to-restrict-access-with-the-principalpermissionattribute-class.md)  
 <span data-ttu-id="f2987-110">演示使用 <xref:System.Security.Permissions.PrincipalPermissionAttribute> 限制对服务的访问的过程。</span><span class="sxs-lookup"><span data-stu-id="f2987-110">Shows the process of restricting access to a service with the <xref:System.Security.Permissions.PrincipalPermissionAttribute>.</span></span>  
  
 [<span data-ttu-id="f2987-111">如何：将 ASP.NET 角色提供程序与服务一起使用</span><span class="sxs-lookup"><span data-stu-id="f2987-111">How to: Use the ASP.NET Role Provider with a Service</span></span>](how-to-use-the-aspnet-role-provider-with-a-service.md)  
 <span data-ttu-id="f2987-112">演练服务的配置，使其能够使用 ASP.NET 的角色提供程序功能。</span><span class="sxs-lookup"><span data-stu-id="f2987-112">Walks through the configuration of a service to enable it to use the role provider feature of ASP.NET.</span></span>  
  
 [<span data-ttu-id="f2987-113">如何：将 ASP.NET 授权管理器角色提供程序与服务一起使用</span><span class="sxs-lookup"><span data-stu-id="f2987-113">How to: Use the ASP.NET Authorization Manager Role Provider with a Service</span></span>](how-to-use-the-aspnet-authorization-manager-role-provider-with-a-service.md)  
 <span data-ttu-id="f2987-114">ASP.NET 可以使用授权管理器来管理网站的授权。</span><span class="sxs-lookup"><span data-stu-id="f2987-114">ASP.NET can use the Authorization Manager to manage authorization for a Web site.</span></span> <span data-ttu-id="f2987-115">WCF 可以同样利用 ASP.NET/Authorization Manager 组合来授权客户端。</span><span class="sxs-lookup"><span data-stu-id="f2987-115">WCF can similarly leverage the ASP.NET/Authorization Manager combination for authorization of clients.</span></span>  
  
 [<span data-ttu-id="f2987-116">使用标识模型管理声明和授权</span><span class="sxs-lookup"><span data-stu-id="f2987-116">Managing Claims and Authorization with the Identity Model</span></span>](managing-claims-and-authorization-with-the-identity-model.md)  
 <span data-ttu-id="f2987-117">说明将标识模型基础结构用于基于声明的授权的基础知识。</span><span class="sxs-lookup"><span data-stu-id="f2987-117">Explains the basics of using the Identity Model infrastructure for claims-based authorization.</span></span>  
  
 [<span data-ttu-id="f2987-118">委托和模拟</span><span class="sxs-lookup"><span data-stu-id="f2987-118">Delegation and Impersonation</span></span>](delegation-and-impersonation-with-wcf.md)  
 <span data-ttu-id="f2987-119">说明委托和模拟之间的区别。</span><span class="sxs-lookup"><span data-stu-id="f2987-119">Explains the difference between delegation and impersonation.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="f2987-120">参考</span><span class="sxs-lookup"><span data-stu-id="f2987-120">Reference</span></span>  

 <xref:System.ServiceModel.Security>  
  
 <xref:System.ServiceModel.Description.PrincipalPermissionMode>  
  
 <xref:System.ServiceModel.Description.ServiceAuthorizationBehavior>  
  
 <xref:System.Security.Permissions.PrincipalPermissionAttribute>  
  
## <a name="related-sections"></a><span data-ttu-id="f2987-121">相关章节</span><span class="sxs-lookup"><span data-stu-id="f2987-121">Related Sections</span></span>  

 [<span data-ttu-id="f2987-122">身份验证</span><span class="sxs-lookup"><span data-stu-id="f2987-122">Authentication</span></span>](authentication-in-wcf.md)  
  
## <a name="see-also"></a><span data-ttu-id="f2987-123">请参阅</span><span class="sxs-lookup"><span data-stu-id="f2987-123">See also</span></span>

- [<span data-ttu-id="f2987-124">安全性概述</span><span class="sxs-lookup"><span data-stu-id="f2987-124">Security Overview</span></span>](security-overview.md)
- <span data-ttu-id="f2987-125">[Windows Server App Fabric 的安全模型](/previous-versions/appfabric/ee677202(v=azure.10))</span><span class="sxs-lookup"><span data-stu-id="f2987-125">[Security Model for Windows Server App Fabric](/previous-versions/appfabric/ee677202(v=azure.10))</span></span>
