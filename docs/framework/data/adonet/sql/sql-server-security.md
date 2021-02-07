---
description: 了解详细信息： SQL Server 安全性
title: SQL Server 安全性
ms.date: 03/30/2017
ms.assetid: 9053724d-a1fb-4f0f-b9dc-7f6dd893e8ff
ms.openlocfilehash: 73e5d72dfacb1f856056ba733c4ff06823ae08d7
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99767201"
---
# <a name="sql-server-security"></a><span data-ttu-id="74a4c-103">SQL Server 安全性</span><span class="sxs-lookup"><span data-stu-id="74a4c-103">SQL Server Security</span></span>

<span data-ttu-id="74a4c-104">SQL Server 具有许多支持创建安全数据库应用程序的功能。</span><span class="sxs-lookup"><span data-stu-id="74a4c-104">SQL Server has many features that support creating secure database applications.</span></span>  
  
 <span data-ttu-id="74a4c-105">无论要使用哪个版本的 SQL Server，通用安全注意事项（如数据盗窃和蓄意破坏）都适用。</span><span class="sxs-lookup"><span data-stu-id="74a4c-105">Common security considerations, such as data theft or vandalism, apply regardless of the version of SQL Server you are using.</span></span> <span data-ttu-id="74a4c-106">数据完整性也应视为安全问题。</span><span class="sxs-lookup"><span data-stu-id="74a4c-106">Data integrity should also be considered as a security issue.</span></span> <span data-ttu-id="74a4c-107">如果数据不受保护，且允许临时数据操作，只要数据被无意或恶意地修改为不正确的值或被完全删除，数据就可能变得毫无价值。</span><span class="sxs-lookup"><span data-stu-id="74a4c-107">If data is not protected, it is possible that it could become worthless if ad hoc data manipulation is permitted and the data is inadvertently or maliciously modified with incorrect values or deleted entirely.</span></span> <span data-ttu-id="74a4c-108">此外，通常还必须遵守法律要求，如正确存储机密信息。</span><span class="sxs-lookup"><span data-stu-id="74a4c-108">In addition, there are often legal requirements that must be adhered to, such as the correct storage of confidential information.</span></span> <span data-ttu-id="74a4c-109">存储某些类型的个人数据是完全禁止的，具体取决于适用于特定管辖权地的法律。</span><span class="sxs-lookup"><span data-stu-id="74a4c-109">Storing some kinds of personal data is proscribed entirely, depending on the laws that apply in a particular jurisdiction.</span></span>  
  
 <span data-ttu-id="74a4c-110">与每个版本的 Windows 一样，每个版本的 SQL Server 都具有不同的安全功能，版本越高，功能越强。</span><span class="sxs-lookup"><span data-stu-id="74a4c-110">Each version of SQL Server has different security features, as does each version of Windows, with later versions having enhanced functionality over earlier ones.</span></span> <span data-ttu-id="74a4c-111">请务必了解，单靠安全功能并不能保证数据库应用程序的安全。</span><span class="sxs-lookup"><span data-stu-id="74a4c-111">It is important to understand that security features alone cannot guarantee a secure database application.</span></span> <span data-ttu-id="74a4c-112">每个数据库应用程序都有独特的要求、执行环境、部署模型、物理位置和用户群体。</span><span class="sxs-lookup"><span data-stu-id="74a4c-112">Each database application is unique in its requirements, execution environment, deployment model, physical location, and user population.</span></span> <span data-ttu-id="74a4c-113">某些本地范围内的应用程序可能只需要最低限度的安全措施，而其他本地应用程序或通过 Internet 部署的应用程序可能需要严格的安全措施以及持续监视和评估。</span><span class="sxs-lookup"><span data-stu-id="74a4c-113">Some applications that are local in scope may need only minimal security whereas other local applications or applications deployed over the Internet may require stringent security measures and ongoing monitoring and evaluation.</span></span>  
  
 <span data-ttu-id="74a4c-114">SQL Server 数据库应用程序的安全要求应该在设计时就加以考虑，而不应事后再考虑。</span><span class="sxs-lookup"><span data-stu-id="74a4c-114">The security requirements of a SQL Server database application should be considered at design time, not as an afterthought.</span></span> <span data-ttu-id="74a4c-115">在开发周期的早期评估威胁，让你有机会在检测到漏洞的任意位置缓解潜在损害。</span><span class="sxs-lookup"><span data-stu-id="74a4c-115">Evaluating threats early in the development cycle gives you the opportunity to mitigate potential damage wherever a vulnerability is detected.</span></span>  
  
 <span data-ttu-id="74a4c-116">即使应用程序的初始设计是合理的，但随着系统不断发展，可能也会出现新的威胁。</span><span class="sxs-lookup"><span data-stu-id="74a4c-116">Even if the initial design of an application is sound, new threats may emerge as the system evolves.</span></span> <span data-ttu-id="74a4c-117">通过在数据库周围布建多道防线，可以最大限度地减少安全漏洞造成的损害。</span><span class="sxs-lookup"><span data-stu-id="74a4c-117">By creating multiple lines of defense around your database, you can minimize the damage inflicted by a security breach.</span></span> <span data-ttu-id="74a4c-118">第一道防线是，通过永不授予超过绝对必要的权限来减少攻击面。</span><span class="sxs-lookup"><span data-stu-id="74a4c-118">Your first line of defense is to reduce the attack surface area by never to granting more permissions than are absolutely necessary.</span></span>  
  
 <span data-ttu-id="74a4c-119">本节中的主题简要说明了 SQL Server 中开发人员相关的安全功能，并提供了指向 SQL Server 联机丛书中相关主题以及提供更详细说明的其他资源的链接。</span><span class="sxs-lookup"><span data-stu-id="74a4c-119">The topics in this section briefly describe the security features in SQL Server that are relevant for developers, with links to relevant topics in SQL Server Books Online and other resources that provide more detailed coverage.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="74a4c-120">本节内容</span><span class="sxs-lookup"><span data-stu-id="74a4c-120">In This Section</span></span>  

 [<span data-ttu-id="74a4c-121">SQL Server 安全性概述</span><span class="sxs-lookup"><span data-stu-id="74a4c-121">Overview of SQL Server Security</span></span>](overview-of-sql-server-security.md)  
 <span data-ttu-id="74a4c-122">说明 SQL Server 的体系结构和安全功能。</span><span class="sxs-lookup"><span data-stu-id="74a4c-122">Describes the architecture and security features of SQL Server.</span></span>  
  
 [<span data-ttu-id="74a4c-123">SQL Server 中的应用程序安全方案</span><span class="sxs-lookup"><span data-stu-id="74a4c-123">Application Security Scenarios in SQL Server</span></span>](application-security-scenarios-in-sql-server.md)  
 <span data-ttu-id="74a4c-124">包含对 ADO.NET 和 SQL Server 应用程序的各种应用程序安全方案进行讨论的主题。</span><span class="sxs-lookup"><span data-stu-id="74a4c-124">Contains topics discussing various application security scenarios for ADO.NET and SQL Server applications.</span></span>  
  
 [<span data-ttu-id="74a4c-125">SQL Server Express 安全性</span><span class="sxs-lookup"><span data-stu-id="74a4c-125">SQL Server Express Security</span></span>](sql-server-express-security.md)  
 <span data-ttu-id="74a4c-126">介绍 SQL Server Express 的安全注意事项。</span><span class="sxs-lookup"><span data-stu-id="74a4c-126">Describes security considerations for SQL Server Express.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="74a4c-127">相关章节</span><span class="sxs-lookup"><span data-stu-id="74a4c-127">Related Sections</span></span>  

[<span data-ttu-id="74a4c-128">SQL Server 数据库引擎和 Azure SQL Database 的安全中心</span><span class="sxs-lookup"><span data-stu-id="74a4c-128">Security Center for SQL Server Database Engine and Azure SQL Database</span></span>](/sql/relational-databases/security/security-center-for-sql-server-database-engine-and-azure-sql-database)  
<span data-ttu-id="74a4c-129">介绍了 SQL Server 和 Azure SQL 数据库的安全注意事项。</span><span class="sxs-lookup"><span data-stu-id="74a4c-129">Describes security considerations for SQL Server and Azure SQL Database.</span></span>

[<span data-ttu-id="74a4c-130">安装 SQL Server 的安全注意事项</span><span class="sxs-lookup"><span data-stu-id="74a4c-130">Security Considerations for a SQL Server Installation</span></span>](/sql/sql-server/install/security-considerations-for-a-sql-server-installation)  
<span data-ttu-id="74a4c-131">介绍了在安装 SQL Server 之前要注意的安全事项。</span><span class="sxs-lookup"><span data-stu-id="74a4c-131">Describes security concerns to consider before installing SQL Server.</span></span>

## <a name="see-also"></a><span data-ttu-id="74a4c-132">请参阅</span><span class="sxs-lookup"><span data-stu-id="74a4c-132">See also</span></span>

- [<span data-ttu-id="74a4c-133">保证 ADO.NET 应用程序的安全</span><span class="sxs-lookup"><span data-stu-id="74a4c-133">Securing ADO.NET Applications</span></span>](../securing-ado-net-applications.md)
- [<span data-ttu-id="74a4c-134">SQL Server 和 ADO.NET</span><span class="sxs-lookup"><span data-stu-id="74a4c-134">SQL Server and ADO.NET</span></span>](index.md)
