---
title: SQL Server 中的身份验证
description: 了解 SQL Server ADO.NET 的身份验证，包括 Windows 身份验证模式和混合模式。
ms.date: 05/22/2018
ms.assetid: 646ddbf5-dd4e-4285-8e4a-f565f666c5cc
ms.openlocfilehash: a1ecc0debd584797f72a89318aadc6ccc8a41062
ms.sourcegitcommit: f0fc5db7bcbf212e46933e9cf2d555bb82666141
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "100581923"
---
# <a name="authentication-in-sql-server"></a><span data-ttu-id="6a3c7-103">SQL Server 中的身份验证</span><span class="sxs-lookup"><span data-stu-id="6a3c7-103">Authentication in SQL Server</span></span>

<span data-ttu-id="6a3c7-104">SQL Server 支持两种身份验证模式，即 Windows 身份验证模式和混合模式。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-104">SQL Server supports two authentication modes, Windows authentication mode and mixed mode.</span></span>  
  
- <span data-ttu-id="6a3c7-105">Windows 身份验证是默认模式（通常称为集成安全），因为此 SQL Server 安全模型与 Windows 紧密集成。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-105">Windows authentication is the default, and is often referred to as integrated security because this SQL Server security model is tightly integrated with Windows.</span></span> <span data-ttu-id="6a3c7-106">特定的 Windows 用户和组帐户可信任，可以登录 SQL Server。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-106">Specific Windows user and group accounts are trusted to log in to SQL Server.</span></span> <span data-ttu-id="6a3c7-107">已经过身份验证的 Windows 用户无需提供其他凭据。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-107">Windows users who have already been authenticated do not have to present additional credentials.</span></span>  
  
- <span data-ttu-id="6a3c7-108">混合模式支持由 Windows 和 SQL Server 进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-108">Mixed mode supports authentication both by Windows and by SQL Server.</span></span> <span data-ttu-id="6a3c7-109">用户名和密码保留在 SQL Server 内。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-109">User name and password pairs are maintained within SQL Server.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="6a3c7-110">建议尽可能使用 Windows 身份验证。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-110">We recommend using Windows authentication wherever possible.</span></span> <span data-ttu-id="6a3c7-111">Windows 身份验证使用一系列加密消息来验证 SQL Server 中的用户。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-111">Windows authentication uses a series of encrypted messages to authenticate users in SQL Server.</span></span> <span data-ttu-id="6a3c7-112">使用 SQL Server 登录时，会通过网络传递 SQL Server 登录名和加密的密码，这样会降低它们的安全性。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-112">When SQL Server logins are used, SQL Server login names and encrypted passwords are passed across the network, which makes them less secure.</span></span>  
  
 <span data-ttu-id="6a3c7-113">使用 Windows 身份验证时，用户已登录到 Windows，无需另外登录到 SQL Server。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-113">With Windows authentication, users are already logged onto Windows and do not have to log on separately to SQL Server.</span></span> <span data-ttu-id="6a3c7-114">下面的 `SqlConnection.ConnectionString` 可指定 Windows 身份验证，而无需用户提供用户名或密码。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-114">The following `SqlConnection.ConnectionString` specifies Windows authentication without requiring users to provide a user name or password.</span></span>  
  
```csharp  
"Server=MSSQL1;Database=AdventureWorks;Integrated Security=true;"
```  
  
> [!NOTE]
> <span data-ttu-id="6a3c7-115">登录名不同于数据库用户。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-115">Logins are distinct from database users.</span></span> <span data-ttu-id="6a3c7-116">必须在单独的操作中将登录名或 Windows 组映射到数据库用户或角色。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-116">You must map logins or Windows groups to database users or roles in a separate operation.</span></span> <span data-ttu-id="6a3c7-117">然后，向用户或角色授予对数据库对象的访问权限。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-117">You then grant permissions to users or roles to access database objects.</span></span>  
  
## <a name="authentication-scenarios"></a><span data-ttu-id="6a3c7-118">身份验证方案</span><span class="sxs-lookup"><span data-stu-id="6a3c7-118">Authentication Scenarios</span></span>  

 <span data-ttu-id="6a3c7-119">在以下情况下，Windows 身份验证通常是最佳选择：</span><span class="sxs-lookup"><span data-stu-id="6a3c7-119">Windows authentication is usually the best choice in the following situations:</span></span>  
  
- <span data-ttu-id="6a3c7-120">有域控制器。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-120">There is a domain controller.</span></span>  
  
- <span data-ttu-id="6a3c7-121">应用程序和数据库位于同一台计算机上。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-121">The application and the database are on the same computer.</span></span>  
  
- <span data-ttu-id="6a3c7-122">你正在使用 SQL Server Express 或 LocalDB 的实例。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-122">You are using an instance of SQL Server Express or LocalDB.</span></span>  
  
 <span data-ttu-id="6a3c7-123">SQL Server 登录通常用于以下情况：</span><span class="sxs-lookup"><span data-stu-id="6a3c7-123">SQL Server logins are often used in the following situations:</span></span>  
  
- <span data-ttu-id="6a3c7-124">有工作组。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-124">If you have a workgroup.</span></span>  
  
- <span data-ttu-id="6a3c7-125">用户从不受信任的其他域连接。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-125">Users connect from different, non-trusted domains.</span></span>  
  
- <span data-ttu-id="6a3c7-126">Internet 应用程序（如 ASP.NET）。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-126">Internet applications, such as ASP.NET.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="6a3c7-127">指定 Windows 身份验证不会禁用 SQL Server 登录。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-127">Specifying Windows authentication does not disable SQL Server logins.</span></span> <span data-ttu-id="6a3c7-128">使用 ALTER LOGIN DISABLE Transact-SQL 语句会禁用具有高级权限的 SQL Server 登录。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-128">Use the ALTER LOGIN DISABLE Transact-SQL statement to disable highly-privileged SQL Server logins.</span></span>  
  
## <a name="login-types"></a><span data-ttu-id="6a3c7-129">登录类型</span><span class="sxs-lookup"><span data-stu-id="6a3c7-129">Login Types</span></span>  

 <span data-ttu-id="6a3c7-130">SQL Server 支持三种登录类型：</span><span class="sxs-lookup"><span data-stu-id="6a3c7-130">SQL Server supports three types of logins:</span></span>  
  
- <span data-ttu-id="6a3c7-131">本地 Windows 用户帐户或受信任的域帐户。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-131">A local Windows user account or trusted domain account.</span></span> <span data-ttu-id="6a3c7-132">SQL Server 依靠 Windows 来对 Windows 用户帐户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-132">SQL Server relies on Windows to authenticate the Windows user accounts.</span></span>  
  
- <span data-ttu-id="6a3c7-133">Windows 组。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-133">Windows group.</span></span> <span data-ttu-id="6a3c7-134">向 Windows 组授予访问权限会向作为组成员的所有 Windows 用户登录名授予访问权限。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-134">Granting access to a Windows group grants access to all Windows user logins that are members of the group.</span></span>  
  
- <span data-ttu-id="6a3c7-135">SQL Server 登录。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-135">SQL Server login.</span></span> <span data-ttu-id="6a3c7-136">SQL Server 将用户名和密码的哈希都存储在 master 数据库中，使用内部身份验证方法来验证登录尝试。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-136">SQL Server stores both the username and a hash of the password in the master database, by using internal authentication methods to verify login attempts.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="6a3c7-137">SQL Server 提供了从证书或非对称密钥创建的登录名，仅用于代码签名。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-137">SQL Server provides logins created from certificates or asymmetric keys that are used only for code signing.</span></span> <span data-ttu-id="6a3c7-138">不能用于连接到 SQL Server。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-138">They cannot be used to connect to SQL Server.</span></span>  
  
## <a name="mixed-mode-authentication"></a><span data-ttu-id="6a3c7-139">混合模式身份验证</span><span class="sxs-lookup"><span data-stu-id="6a3c7-139">Mixed Mode Authentication</span></span>  

 <span data-ttu-id="6a3c7-140">如果必须使用混合模式身份验证，则必须创建 SQL Server 登录名，这些登录名存储在 SQL Server 中。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-140">If you must use mixed mode authentication, you must create SQL Server logins, which are stored in SQL Server.</span></span> <span data-ttu-id="6a3c7-141">然后，必须在运行时提供 SQL Server 用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-141">You then have to supply the SQL Server user name and password at run time.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="6a3c7-142">SQL Server 安装有名为 `sa`（“系统管理员”的首字母缩写）的 SQL Server 登录名。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-142">SQL Server installs with a SQL Server login named `sa` (an abbreviation of "system administrator").</span></span> <span data-ttu-id="6a3c7-143">请向 `sa` 登录名分配强密码，并且不在应用程序中使用 `sa` 登录名。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-143">Assign a strong password to the `sa` login and do not use the `sa` login in your application.</span></span> <span data-ttu-id="6a3c7-144">`sa` 登录名映射到 `sysadmin` 固定服务器角色，此角色在整个服务器上具有不可撤销的管理凭据。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-144">The `sa` login maps to the `sysadmin` fixed server role, which has irrevocable administrative credentials on the whole server.</span></span> <span data-ttu-id="6a3c7-145">如果攻击者以系统管理员身份获得访问权限，潜在损害是无限的。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-145">There are no limits to the potential damage if an attacker gains access as a system administrator.</span></span>
  
 <span data-ttu-id="6a3c7-146">SQL Server 提供 SQL Server 登录名的 Windows 密码策略机制。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-146">SQL Server provides Windows password policy mechanisms for SQL Server logins.</span></span> <span data-ttu-id="6a3c7-147">密码复杂性策略通过增加可能密码的数量来阻止强力攻击。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-147">Password complexity policies are designed to deter brute force attacks by increasing the number of possible passwords.</span></span> <span data-ttu-id="6a3c7-148">SQL Server 可以将相同的复杂性和过期策略应用于 SQL Server 内使用的密码。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-148">SQL Server can apply the same complexity and expiration policies to passwords used inside SQL Server.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="6a3c7-149">连接用户输入中的连接字符串可能会让你易受到连接字符串注入攻击。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-149">Concatenating connection strings from user input can leave you vulnerable to a connection string injection attack.</span></span> <span data-ttu-id="6a3c7-150">请使用 <xref:System.Data.SqlClient.SqlConnectionStringBuilder> 在运行时创建语法有效的连接字符串。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-150">Use the <xref:System.Data.SqlClient.SqlConnectionStringBuilder> to create syntactically valid connection strings at run time.</span></span> <span data-ttu-id="6a3c7-151">有关详细信息，请参阅[连接字符串生成器](../connection-string-builders.md)。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-151">For more information, see [Connection String Builders](../connection-string-builders.md).</span></span>  
  
## <a name="external-resources"></a><span data-ttu-id="6a3c7-152">外部资源</span><span class="sxs-lookup"><span data-stu-id="6a3c7-152">External Resources</span></span>  

 <span data-ttu-id="6a3c7-153">有关详细信息，请参阅以下资源。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-153">For more information, see the following resources.</span></span>  
  
|<span data-ttu-id="6a3c7-154">资源</span><span class="sxs-lookup"><span data-stu-id="6a3c7-154">Resource</span></span>|<span data-ttu-id="6a3c7-155">说明</span><span class="sxs-lookup"><span data-stu-id="6a3c7-155">Description</span></span>|  
|--------------|-----------------|  
|[<span data-ttu-id="6a3c7-156">主体</span><span class="sxs-lookup"><span data-stu-id="6a3c7-156">Principals</span></span>](/sql/relational-databases/security/authentication-access/principals-database-engine)|<span data-ttu-id="6a3c7-157">描述 SQL Server 中的登录名和其他安全主体。</span><span class="sxs-lookup"><span data-stu-id="6a3c7-157">Describes logins and other security principals in SQL Server.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="6a3c7-158">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6a3c7-158">See also</span></span>

- [<span data-ttu-id="6a3c7-159">保证 ADO.NET 应用程序的安全</span><span class="sxs-lookup"><span data-stu-id="6a3c7-159">Securing ADO.NET Applications</span></span>](../securing-ado-net-applications.md)
- [<span data-ttu-id="6a3c7-160">SQL Server 中的应用程序安全方案</span><span class="sxs-lookup"><span data-stu-id="6a3c7-160">Application Security Scenarios in SQL Server</span></span>](application-security-scenarios-in-sql-server.md)
- [<span data-ttu-id="6a3c7-161">连接到数据源</span><span class="sxs-lookup"><span data-stu-id="6a3c7-161">Connecting to a Data Source</span></span>](../connecting-to-a-data-source.md)
- [<span data-ttu-id="6a3c7-162">连接字符串</span><span class="sxs-lookup"><span data-stu-id="6a3c7-162">Connection Strings</span></span>](../connection-strings.md)
- [<span data-ttu-id="6a3c7-163">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="6a3c7-163">ADO.NET Overview</span></span>](../ado-net-overview.md)
