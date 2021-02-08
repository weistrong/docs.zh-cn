---
description: 了解详细信息：行为安全性
title: 行为安全
ms.date: 03/30/2017
ms.assetid: 19710ae3-f197-4d28-ba9d-52e465006819
ms.openlocfilehash: ba245a2c9558d40f22b9126ee0cf1560ed700ce8
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99778706"
---
# <a name="behavior-security"></a><span data-ttu-id="32109-103">行为安全</span><span class="sxs-lookup"><span data-stu-id="32109-103">Behavior Security</span></span>

<span data-ttu-id="32109-104">本节包含演示服务行为的配置安全的示例。</span><span class="sxs-lookup"><span data-stu-id="32109-104">This section includes samples that demonstrate configuring security for service behaviors.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="32109-105">本节内容</span><span class="sxs-lookup"><span data-stu-id="32109-105">In This Section</span></span>  

 [<span data-ttu-id="32109-106">服务审核行为</span><span class="sxs-lookup"><span data-stu-id="32109-106">Service Auditing Behavior</span></span>](service-auditing-behavior.md)  
 <span data-ttu-id="32109-107">此示例演示如何在服务操作过程中使用 <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior> 来启用对安全事件的审核。</span><span class="sxs-lookup"><span data-stu-id="32109-107">This sample demonstrates how to use the <xref:System.ServiceModel.Description.ServiceSecurityAuditBehavior> to enable auditing of security events during service operations.</span></span>  
  
 [<span data-ttu-id="32109-108">成员资格和角色提供程序</span><span class="sxs-lookup"><span data-stu-id="32109-108">Membership and Role Provider</span></span>](membership-and-role-provider.md)  
 <span data-ttu-id="32109-109">此示例演示服务如何使用 ASP.NET 成员资格和角色提供程序来对客户端进行身份验证和授权。</span><span class="sxs-lookup"><span data-stu-id="32109-109">This sample demonstrates how a service can use the ASP.NET membership and role providers to authenticate and authorize clients.</span></span>  
  
 [<span data-ttu-id="32109-110">授予对服务操作的访问权限</span><span class="sxs-lookup"><span data-stu-id="32109-110">Authorizing Access to Service Operations</span></span>](authorizing-access-to-service-operations.md)  
 <span data-ttu-id="32109-111">此示例演示如何使用 [\<serviceAuthorization>](../../configure-apps/file-schema/wcf/serviceauthorization-element.md) 来允许使用 <xref:System.Security.Permissions.PrincipalPermissionAttribute> 属性来授予对服务操作的访问权限。</span><span class="sxs-lookup"><span data-stu-id="32109-111">This sample demonstrates how to use the [\<serviceAuthorization>](../../configure-apps/file-schema/wcf/serviceauthorization-element.md) to enable use of the <xref:System.Security.Permissions.PrincipalPermissionAttribute> attribute to authorize access to service operations.</span></span>  
  
 [<span data-ttu-id="32109-112">模拟客户端</span><span class="sxs-lookup"><span data-stu-id="32109-112">Impersonating the Client</span></span>](impersonating-the-client.md)  
 <span data-ttu-id="32109-113">此示例演示如何在服务中模拟调用方应用程序，以便服务可以代表调用方访问系统资源。</span><span class="sxs-lookup"><span data-stu-id="32109-113">This sample demonstrates how to impersonate the caller application at the service so that the service can access system resources on behalf of the caller.</span></span>
