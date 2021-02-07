---
description: 了解详细信息：保护 ADO.NET 应用程序
title: 保证应用程序的安全
ms.date: 03/30/2017
ms.assetid: 005a1d43-6ee5-471e-ad98-1d30a44d49d5
ms.openlocfilehash: 4e4d219d1f4249846943d019e174abd6d43687c7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99718871"
---
# <a name="securing-adonet-applications"></a><span data-ttu-id="9d131-103">保护 ADO.NET 应用程序</span><span class="sxs-lookup"><span data-stu-id="9d131-103">Securing ADO.NET applications</span></span>

<span data-ttu-id="9d131-104">编写安全 ADO.NET 应用程序不仅仅是避免常见的编码缺陷（如不验证用户输入）。</span><span class="sxs-lookup"><span data-stu-id="9d131-104">Writing a secure ADO.NET application involves more than avoiding common coding pitfalls such as not validating user input.</span></span> <span data-ttu-id="9d131-105">访问数据的应用程序具有许多潜在的故障点，攻击者可以利用它们检索、操纵或破坏敏感数据。</span><span class="sxs-lookup"><span data-stu-id="9d131-105">An application that accesses data has many potential points of failure that an attacker can exploit to retrieve, manipulate, or destroy sensitive data.</span></span> <span data-ttu-id="9d131-106">因此，了解安全性的各个方面（从应用程序设计阶段期间的威胁建模过程到应用程序的最终部署和不断的维护）非常重要。</span><span class="sxs-lookup"><span data-stu-id="9d131-106">It is therefore important to understand all aspects of security, from the process of threat modeling during the design phase of your application, to its eventual deployment and ongoing maintenance.</span></span>  
  
<span data-ttu-id="9d131-107">.NET Framework 提供了很多有用的类、服务和工具，以用于保证数据库应用程序的安全和对其进行管理。</span><span class="sxs-lookup"><span data-stu-id="9d131-107">The .NET Framework provides many useful classes, services, and tools for securing and administering database applications.</span></span> <span data-ttu-id="9d131-108">公共语言运行库 (CLR) 提供了供代码在其中运行的类型安全环境，以及用于进一步限制托管代码权限的代码访问安全性 (CAS)。</span><span class="sxs-lookup"><span data-stu-id="9d131-108">The common language runtime (CLR) provides a type-safe environment for code to run in, with code access security (CAS) to restrict further the permissions of managed code.</span></span> <span data-ttu-id="9d131-109">遵循安全数据访问编码惯例可降低由潜在攻击者造成的损坏。</span><span class="sxs-lookup"><span data-stu-id="9d131-109">Following secure data access coding practices limits the damage that can be inflicted by a potential attacker.</span></span>  
  
<span data-ttu-id="9d131-110">编写安全代码不会阻止在使用非托管资源（如数据库）时自己造成的安全漏洞。</span><span class="sxs-lookup"><span data-stu-id="9d131-110">Writing secure code does not guard against self-inflicted security holes when working with unmanaged resources such as databases.</span></span> <span data-ttu-id="9d131-111">多数服务器数据库（如 SQL Server）拥有其各自的安全系统，正确实现这些安全系统可增强安全性。</span><span class="sxs-lookup"><span data-stu-id="9d131-111">Most server databases, such as SQL Server, have their own security systems, which enhance security when implemented correctly.</span></span> <span data-ttu-id="9d131-112">但是，即使是具有可靠安全系统的数据源，如果未适当配置，也可能受到攻击。</span><span class="sxs-lookup"><span data-stu-id="9d131-112">However, even a data source with a robust security system can be victimized in an attack if it is not configured appropriately.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="9d131-113">本节内容</span><span class="sxs-lookup"><span data-stu-id="9d131-113">In this section</span></span>

 [<span data-ttu-id="9d131-114">安全性概述</span><span class="sxs-lookup"><span data-stu-id="9d131-114">Security Overview</span></span>](security-overview.md)  
 <span data-ttu-id="9d131-115">提供对设计安全 ADO.NET 应用程序的建议。</span><span class="sxs-lookup"><span data-stu-id="9d131-115">Provides recommendations for designing secure ADO.NET applications.</span></span>  
  
 [<span data-ttu-id="9d131-116">安全数据访问</span><span class="sxs-lookup"><span data-stu-id="9d131-116">Secure Data Access</span></span>](secure-data-access.md)  
 <span data-ttu-id="9d131-117">描述如何使用受保护数据源中的数据。</span><span class="sxs-lookup"><span data-stu-id="9d131-117">Describes how to work with data from a secured data source.</span></span>  
  
 [<span data-ttu-id="9d131-118">保证客户端应用程序的安全</span><span class="sxs-lookup"><span data-stu-id="9d131-118">Secure Client Applications</span></span>](secure-client-applications.md)  
 <span data-ttu-id="9d131-119">描述客户端应用程序的安全注意事项。</span><span class="sxs-lookup"><span data-stu-id="9d131-119">Describes security considerations for client applications.</span></span>  
  
 [<span data-ttu-id="9d131-120">代码访问安全性和 ADO.NET</span><span class="sxs-lookup"><span data-stu-id="9d131-120">Code Access Security and ADO.NET</span></span>](code-access-security.md)  
 <span data-ttu-id="9d131-121">描述 CAS 如何帮助保护 ADO.NET 代码，</span><span class="sxs-lookup"><span data-stu-id="9d131-121">Describes how CAS can help protect ADO.NET code.</span></span> <span data-ttu-id="9d131-122">还讨论如何使用部分信任。</span><span class="sxs-lookup"><span data-stu-id="9d131-122">Also discusses how to work with partial trust.</span></span>  
  
 [<span data-ttu-id="9d131-123">隐私和数据安全性</span><span class="sxs-lookup"><span data-stu-id="9d131-123">Privacy and Data Security</span></span>](privacy-and-data-security.md)  
 <span data-ttu-id="9d131-124">描述 ADO.NET 应用程序的加密选项。</span><span class="sxs-lookup"><span data-stu-id="9d131-124">Describes encryption options for ADO.NET applications.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="9d131-125">相关章节</span><span class="sxs-lookup"><span data-stu-id="9d131-125">Related sections</span></span>

 [<span data-ttu-id="9d131-126">数据集和 DataTable 安全指南</span><span class="sxs-lookup"><span data-stu-id="9d131-126">DataSet and DataTable security guidance</span></span>](dataset-datatable-dataview/security-guidance.md)  
 <span data-ttu-id="9d131-127">提供和的安全 <xref:System.Data.DataSet> 指南 <xref:System.Data.DataTable> 。</span><span class="sxs-lookup"><span data-stu-id="9d131-127">Provides security guidance for <xref:System.Data.DataSet> and <xref:System.Data.DataTable>.</span></span>

 [<span data-ttu-id="9d131-128">SQL Server 安全性</span><span class="sxs-lookup"><span data-stu-id="9d131-128">SQL Server Security</span></span>](./sql/sql-server-security.md)  
 <span data-ttu-id="9d131-129">描述从开发人员角度来讲的 SQL Server 安全功能。</span><span class="sxs-lookup"><span data-stu-id="9d131-129">Describes SQL Server security features from a developer's perspective.</span></span>  
  
 [<span data-ttu-id="9d131-130">安全注意事项</span><span class="sxs-lookup"><span data-stu-id="9d131-130">Security Considerations</span></span>](./ef/security-considerations.md)  
 <span data-ttu-id="9d131-131">描述实体框架应用程序的安全性。</span><span class="sxs-lookup"><span data-stu-id="9d131-131">Describes security for Entity Framework applications.</span></span>  
  
 [<span data-ttu-id="9d131-132">安全性</span><span class="sxs-lookup"><span data-stu-id="9d131-132">Security</span></span>](../../../standard/security/index.md)  
 <span data-ttu-id="9d131-133">包含一些链接，这些链接指向介绍 .NET 中的所有安全方面的文章。</span><span class="sxs-lookup"><span data-stu-id="9d131-133">Contains links to articles describing all aspects of security in .NET.</span></span>  
  
 <span data-ttu-id="9d131-134">[安全性工具](/previous-versions/visualstudio/visual-studio-2008/7w3fd0wb(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="9d131-134">[Security Tools](/previous-versions/visualstudio/visual-studio-2008/7w3fd0wb(v=vs.90))</span></span>  
 <span data-ttu-id="9d131-135">用于保证安全策略的安全和对其进行管理的 .NET Framework 工具。</span><span class="sxs-lookup"><span data-stu-id="9d131-135">.NET Framework tools for securing and administering security policy.</span></span>  
  
 <span data-ttu-id="9d131-136">[创建安全应用程序的资源](/previous-versions/visualstudio/visual-studio-2010/ms165101(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="9d131-136">[Resources for Creating Secure Applications](/previous-versions/visualstudio/visual-studio-2010/ms165101(v=vs.100))</span></span>  
 <span data-ttu-id="9d131-137">提供指向用于创建安全应用程序的文章的链接。</span><span class="sxs-lookup"><span data-stu-id="9d131-137">Provides links to articles for creating secure applications.</span></span>  
  
 [<span data-ttu-id="9d131-138">安全参考书目</span><span class="sxs-lookup"><span data-stu-id="9d131-138">Security Bibliography</span></span>](/visualstudio/ide/securing-applications)  
 <span data-ttu-id="9d131-139">提供联机和印刷资料中提供的外部资源的链接。</span><span class="sxs-lookup"><span data-stu-id="9d131-139">Provides links to external resources available online and in print.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9d131-140">请参阅</span><span class="sxs-lookup"><span data-stu-id="9d131-140">See also</span></span>

- [<span data-ttu-id="9d131-141">ADO.NET</span><span class="sxs-lookup"><span data-stu-id="9d131-141">ADO.NET</span></span>](index.md)
- [<span data-ttu-id="9d131-142">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="9d131-142">ADO.NET Overview</span></span>](ado-net-overview.md)
