---
description: 了解详细信息： SQL Server 中的应用程序安全方案
title: SQL Server 中的应用程序安全性方案
ms.date: 03/30/2017
ms.assetid: 0164f3a4-406e-4693-bec3-03c8e18b46d7
ms.openlocfilehash: 8a0e055c3afa1590a74516505d513992bca8b952
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99718650"
---
# <a name="application-security-scenarios-in-sql-server"></a><span data-ttu-id="3ac60-103">SQL Server 中的应用程序安全性方案</span><span class="sxs-lookup"><span data-stu-id="3ac60-103">Application Security Scenarios in SQL Server</span></span>

<span data-ttu-id="3ac60-104">创建安全的 SQL Server 客户端应用程序没有唯一正确的方法。</span><span class="sxs-lookup"><span data-stu-id="3ac60-104">There is no single correct way to create a secure SQL Server client application.</span></span> <span data-ttu-id="3ac60-105">每个应用程序都具有独特的要求、部署环境和用户群体。</span><span class="sxs-lookup"><span data-stu-id="3ac60-105">Every application is unique in its requirements, deployment environment, and user population.</span></span> <span data-ttu-id="3ac60-106">即便应用程序的最初部署具有合理的安全性，但在一段时间后，安全性可能会降低。</span><span class="sxs-lookup"><span data-stu-id="3ac60-106">An application that is reasonably secure when it is initially deployed can become less secure over time.</span></span> <span data-ttu-id="3ac60-107">没有办法准确地预测未来可能出现的威胁。</span><span class="sxs-lookup"><span data-stu-id="3ac60-107">It is impossible to predict with any accuracy what threats may emerge in the future.</span></span>  
  
 <span data-ttu-id="3ac60-108">作为一种产品，SQL Server 已在许多版本的基础上进行了改进，以合并最新的安全功能，使开发人员能够创建安全的数据库应用程序。</span><span class="sxs-lookup"><span data-stu-id="3ac60-108">SQL Server, as a product, has evolved over many versions to incorporate the latest security features that enable developers to create secure database applications.</span></span> <span data-ttu-id="3ac60-109">但是，安全性并不是与生俱来的，需要不断进行监视和更新。</span><span class="sxs-lookup"><span data-stu-id="3ac60-109">However, security doesn't come in the box; it requires continual monitoring and updating.</span></span>  
  
## <a name="common-threats"></a><span data-ttu-id="3ac60-110">常见威胁</span><span class="sxs-lookup"><span data-stu-id="3ac60-110">Common Threats</span></span>  

 <span data-ttu-id="3ac60-111">开发人员需要了解安全威胁、为应对这些威胁而提供的工具以及如何避免自身造成的安全漏洞。</span><span class="sxs-lookup"><span data-stu-id="3ac60-111">Developers need to understand security threats, the tools provided to counter them, and how to avoid self-inflicted security holes.</span></span> <span data-ttu-id="3ac60-112">最好将安全性视为一条链，其中任何一个链接的中断都会削弱整体实力。</span><span class="sxs-lookup"><span data-stu-id="3ac60-112">Security can best be thought of as a chain, where a break in any one link compromises the strength of the whole.</span></span> <span data-ttu-id="3ac60-113">下面列出了一些常见的安全威胁，本节中的主题将对此进行详细讨论。</span><span class="sxs-lookup"><span data-stu-id="3ac60-113">The following list includes some common security threats that are discussed in more detail in the topics in this section.</span></span>  
  
### <a name="sql-injection"></a><span data-ttu-id="3ac60-114">SQL 注入</span><span class="sxs-lookup"><span data-stu-id="3ac60-114">SQL Injection</span></span>  

 <span data-ttu-id="3ac60-115">SQL 注入是恶意用户输入 Transact-SQL 语句而不是有效输入的过程。</span><span class="sxs-lookup"><span data-stu-id="3ac60-115">SQL Injection is the process by which a malicious user enters Transact-SQL statements instead of valid input.</span></span> <span data-ttu-id="3ac60-116">如果输入未经验证直接传递到服务器，并且应用程序无意中执行了注入的代码，攻击可能会损坏或破坏数据。</span><span class="sxs-lookup"><span data-stu-id="3ac60-116">If the input is passed directly to the server without being validated and if the application inadvertently executes the injected code, then the attack has the potential to damage or destroy data.</span></span> <span data-ttu-id="3ac60-117">使用存储过程和参数化命令，避免使用动态 SQL，并限制所有用户的权限，可以防止受到 SQL Server 注入攻击。</span><span class="sxs-lookup"><span data-stu-id="3ac60-117">You can thwart SQL Server injection attacks by using stored procedures and parameterized commands, avoiding dynamic SQL, and restricting permissions on all users.</span></span>  
  
### <a name="elevation-of-privilege"></a><span data-ttu-id="3ac60-118">权限提升</span><span class="sxs-lookup"><span data-stu-id="3ac60-118">Elevation of Privilege</span></span>  

 <span data-ttu-id="3ac60-119">当用户能够获得可信帐户（所有者或管理员）的特权时，就会发生特权提升攻击。</span><span class="sxs-lookup"><span data-stu-id="3ac60-119">Elevation of privilege attacks occur when a user is able to assume the privileges of a trusted account, such as an owner or administrator.</span></span> <span data-ttu-id="3ac60-120">始终在最低特权的用户帐户下运行，并仅分配所需的权限。</span><span class="sxs-lookup"><span data-stu-id="3ac60-120">Always run under least-privileged user accounts and assign only needed permissions.</span></span> <span data-ttu-id="3ac60-121">避免使用管理帐户或所有者帐户来执行代码。</span><span class="sxs-lookup"><span data-stu-id="3ac60-121">Avoid using administrative or owner accounts for executing code.</span></span> <span data-ttu-id="3ac60-122">这可以限制攻击成功后可能发生的破坏程度。</span><span class="sxs-lookup"><span data-stu-id="3ac60-122">This limits the amount of damage that can occur if an attack succeeds.</span></span> <span data-ttu-id="3ac60-123">执行需要附加权限的任务时，请仅在任务期间使用过程签名或模拟。</span><span class="sxs-lookup"><span data-stu-id="3ac60-123">When performing tasks that require additional permissions, use procedure signing or impersonation only for the duration of the task.</span></span> <span data-ttu-id="3ac60-124">你可以使用证书为存储过程签名，或使用模拟来临时分配权限。</span><span class="sxs-lookup"><span data-stu-id="3ac60-124">You can sign stored procedures with certificates or use impersonation to temporarily assign permissions.</span></span>  
  
### <a name="probing-and-intelligent-observation"></a><span data-ttu-id="3ac60-125">探测和智能观测</span><span class="sxs-lookup"><span data-stu-id="3ac60-125">Probing and Intelligent Observation</span></span>  

 <span data-ttu-id="3ac60-126">探测攻击可以使用应用程序生成的错误消息来搜索安全漏洞。</span><span class="sxs-lookup"><span data-stu-id="3ac60-126">A probing attack can use error messages generated by an application to search for security vulnerabilities.</span></span> <span data-ttu-id="3ac60-127">在所有过程代码中实现错误处理，以防止向最终用户返回 SQL Server 错误信息。</span><span class="sxs-lookup"><span data-stu-id="3ac60-127">Implement error handling in all procedural code to prevent SQL Server error information from being returned to the end user.</span></span>  
  
### <a name="authentication"></a><span data-ttu-id="3ac60-128">身份验证</span><span class="sxs-lookup"><span data-stu-id="3ac60-128">Authentication</span></span>  

 <span data-ttu-id="3ac60-129">如果在运行时构造了基于用户输入的连接字符串，则在使用 SQL Server 登录名时可能会发生连接字符串注入攻击。</span><span class="sxs-lookup"><span data-stu-id="3ac60-129">A connection string injection attack can occur when using SQL Server logins if a connection string based on user input is constructed at run time.</span></span> <span data-ttu-id="3ac60-130">如果未检查连接字符串中是否有有效的关键字对，则攻击者可以插入其他字符，从而有可能访问服务器上的敏感数据或其他资源。</span><span class="sxs-lookup"><span data-stu-id="3ac60-130">If the connection string is not checked for valid keyword pairs, an attacker can insert extra characters, potentially accessing sensitive data or other resources on the server.</span></span> <span data-ttu-id="3ac60-131">尽可能使用 Windows 身份验证。</span><span class="sxs-lookup"><span data-stu-id="3ac60-131">Use Windows authentication wherever possible.</span></span> <span data-ttu-id="3ac60-132">如果必须使用 SQL Server 登录名，请在运行时使用 <xref:System.Data.SqlClient.SqlConnectionStringBuilder> 创建和验证连接字符串。</span><span class="sxs-lookup"><span data-stu-id="3ac60-132">If you must use SQL Server logins, use the <xref:System.Data.SqlClient.SqlConnectionStringBuilder> to create and validate connection strings at run time.</span></span>  
  
### <a name="passwords"></a><span data-ttu-id="3ac60-133">密码</span><span class="sxs-lookup"><span data-stu-id="3ac60-133">Passwords</span></span>  

 <span data-ttu-id="3ac60-134">许多攻击成功是因为入侵者能够获取或猜出特权用户的密码。</span><span class="sxs-lookup"><span data-stu-id="3ac60-134">Many attacks succeed because an intruder was able to obtain or guess a password for a privileged user.</span></span> <span data-ttu-id="3ac60-135">密码是抵御入侵者的第一道防线，因此设置强密码对于系统安全是绝对必要的。</span><span class="sxs-lookup"><span data-stu-id="3ac60-135">Passwords are your first line of defense against intruders, so setting strong passwords is essential to the security of your system.</span></span> <span data-ttu-id="3ac60-136">创建并强制实施用于混合模式身份验证的密码策略。</span><span class="sxs-lookup"><span data-stu-id="3ac60-136">Create and enforce password policies for mixed mode authentication.</span></span>  
  
 <span data-ttu-id="3ac60-137">即使使用 Windows 身份验证，也请始终为 `sa` 帐户分配一个强密码。</span><span class="sxs-lookup"><span data-stu-id="3ac60-137">Always assign a strong password to the `sa` account, even when using Windows Authentication.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="3ac60-138">本节内容</span><span class="sxs-lookup"><span data-stu-id="3ac60-138">In This Section</span></span>  

 [<span data-ttu-id="3ac60-139">在 SQL Server 中使用存储过程管理权限</span><span class="sxs-lookup"><span data-stu-id="3ac60-139">Managing Permissions with Stored Procedures in SQL Server</span></span>](managing-permissions-with-stored-procedures-in-sql-server.md)  
 <span data-ttu-id="3ac60-140">描述如何使用存储过程来管理权限和控制数据访问。</span><span class="sxs-lookup"><span data-stu-id="3ac60-140">Describes how to use stored procedures to manage permissions and control data access.</span></span> <span data-ttu-id="3ac60-141">使用存储过程是应对许多安全威胁的一种有效方法。</span><span class="sxs-lookup"><span data-stu-id="3ac60-141">Using stored procedures is an effective way to respond to many security threats.</span></span>  
  
 [<span data-ttu-id="3ac60-142">在 SQL Server 中编写安全动态 SQL</span><span class="sxs-lookup"><span data-stu-id="3ac60-142">Writing Secure Dynamic SQL in SQL Server</span></span>](writing-secure-dynamic-sql-in-sql-server.md)  
 <span data-ttu-id="3ac60-143">介绍使用存储过程编写安全动态 SQL 的技术。</span><span class="sxs-lookup"><span data-stu-id="3ac60-143">Describes techniques for writing secure dynamic SQL using stored procedures.</span></span>  
  
 [<span data-ttu-id="3ac60-144">SQL Server 中的签名存储过程</span><span class="sxs-lookup"><span data-stu-id="3ac60-144">Signing Stored Procedures in SQL Server</span></span>](signing-stored-procedures-in-sql-server.md)  
 <span data-ttu-id="3ac60-145">描述如何使用证书为存储过程签名，以使用户可以使用其无直接访问权限的数据。</span><span class="sxs-lookup"><span data-stu-id="3ac60-145">Describes how to sign a stored procedure with a certificate to enable users to work with data they do not have direct access to.</span></span> <span data-ttu-id="3ac60-146">这就使存储过程可执行调用方无直接执行权限的操作。</span><span class="sxs-lookup"><span data-stu-id="3ac60-146">This enables stored procedures to perform operations that the caller does not have permissions to perform directly.</span></span>  
  
 [<span data-ttu-id="3ac60-147">在 SQL Server 中使用模拟自定义权限</span><span class="sxs-lookup"><span data-stu-id="3ac60-147">Customizing Permissions with Impersonation in SQL Server</span></span>](customizing-permissions-with-impersonation-in-sql-server.md)  
 <span data-ttu-id="3ac60-148">描述如何使用 EXECUTE AS 子句来模拟另一用户。</span><span class="sxs-lookup"><span data-stu-id="3ac60-148">Describes how to use the EXECUTE AS clause to impersonate another user.</span></span> <span data-ttu-id="3ac60-149">模拟将执行上下文从调用方切换到指定用户。</span><span class="sxs-lookup"><span data-stu-id="3ac60-149">Impersonation switches the execution context from the caller to the specified user.</span></span>  
  
 [<span data-ttu-id="3ac60-150">在 SQL Server 中授予行级权限</span><span class="sxs-lookup"><span data-stu-id="3ac60-150">Granting Row-Level Permissions in SQL Server</span></span>](granting-row-level-permissions-in-sql-server.md)  
 <span data-ttu-id="3ac60-151">描述如何实现行级权限以限制数据访问。</span><span class="sxs-lookup"><span data-stu-id="3ac60-151">Describes how to implement row-level permissions to restrict data access.</span></span>  
  
 [<span data-ttu-id="3ac60-152">在 SQL Server 中创建应用程序角色</span><span class="sxs-lookup"><span data-stu-id="3ac60-152">Creating Application Roles in SQL Server</span></span>](creating-application-roles-in-sql-server.md)  
 <span data-ttu-id="3ac60-153">描述应用程序角色的功能。</span><span class="sxs-lookup"><span data-stu-id="3ac60-153">Describes features and functionality of application roles.</span></span>  
  
 [<span data-ttu-id="3ac60-154">在 SQL Server 中启用跨数据库访问</span><span class="sxs-lookup"><span data-stu-id="3ac60-154">Enabling Cross-Database Access in SQL Server</span></span>](enabling-cross-database-access-in-sql-server.md)  
 <span data-ttu-id="3ac60-155">描述如何在不损害安全性的情况启用跨数据库访问。</span><span class="sxs-lookup"><span data-stu-id="3ac60-155">Describes how to enable cross-database access without jeopardizing security.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3ac60-156">请参阅</span><span class="sxs-lookup"><span data-stu-id="3ac60-156">See also</span></span>

- [<span data-ttu-id="3ac60-157">SQL Server 安全性</span><span class="sxs-lookup"><span data-stu-id="3ac60-157">SQL Server Security</span></span>](sql-server-security.md)
- [<span data-ttu-id="3ac60-158">SQL Server 安全性概述</span><span class="sxs-lookup"><span data-stu-id="3ac60-158">Overview of SQL Server Security</span></span>](overview-of-sql-server-security.md)
- [<span data-ttu-id="3ac60-159">保证 ADO.NET 应用程序的安全</span><span class="sxs-lookup"><span data-stu-id="3ac60-159">Securing ADO.NET Applications</span></span>](../securing-ado-net-applications.md)
- [<span data-ttu-id="3ac60-160">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="3ac60-160">ADO.NET Overview</span></span>](../ado-net-overview.md)
