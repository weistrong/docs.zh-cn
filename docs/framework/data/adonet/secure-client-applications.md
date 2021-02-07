---
description: 了解详细信息：保护客户端应用程序
title: 保证客户端应用程序的安全
ms.date: 03/30/2017
ms.assetid: 6239592e-fa7d-4dea-9f00-d296d0048b01
ms.openlocfilehash: a40a6444c2e317b03f03688ca46de157ded6f0ac
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99718949"
---
# <a name="secure-client-applications"></a><span data-ttu-id="4f4f2-103">保证客户端应用程序的安全</span><span class="sxs-lookup"><span data-stu-id="4f4f2-103">Secure Client Applications</span></span>

<span data-ttu-id="4f4f2-104">应用程序通常由多个部件组成，所有这些部件均不能包含漏洞，否则可能导致数据丢失或以其他方式危害系统。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-104">Applications typically consist of many parts that must all be protected from vulnerabilities that could result in data loss or otherwise compromise the system.</span></span> <span data-ttu-id="4f4f2-105">在攻击者可访问数据或系统资源之前将其阻止，以此可创建安全的用户界面来防止出现许多问题。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-105">Creating secure user interfaces can prevent many problems by blocking attackers before they can access data or system resources.</span></span>  
  
## <a name="validate-user-input"></a><span data-ttu-id="4f4f2-106">验证用户输入</span><span class="sxs-lookup"><span data-stu-id="4f4f2-106">Validate User Input</span></span>  

 <span data-ttu-id="4f4f2-107">在构建访问数据的应用程序时，除非能够证明其不为恶意输入，否则您应该假定所有用户输入均为恶意输入。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-107">When constructing an application that accesses data, you should assume that all user input is malicious until proven otherwise.</span></span> <span data-ttu-id="4f4f2-108">如果未能实现此目的，则可能会使您的应用程序易于受到攻击。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-108">Failure to do so can leave your application vulnerable to attack.</span></span> <span data-ttu-id="4f4f2-109">.NET Framework 包含的类可帮助您约束输入控件的值的域，如限制可输入字符的数目。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-109">The .NET Framework contains classes to help you enforce a domain of values for input controls, such as limiting the number of characters that can be entered.</span></span> <span data-ttu-id="4f4f2-110">使用事件挂钩，您可以编写用于检查值的有效性的程序。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-110">Event hooks allow you to write procedures to check the validity of values.</span></span> <span data-ttu-id="4f4f2-111">可验证和强类型化用户输入数据，从而限制应用程序对脚本和 SQL 注入攻击的公开程度。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-111">User input data can be validated and strongly typed, limiting an application's exposure to script and SQL injection exploits.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="4f4f2-112">您还必须验证数据源和客户端应用程序中的用户输入。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-112">You must also validate user input at the data source as well as in the client application.</span></span> <span data-ttu-id="4f4f2-113">因为攻击者可能选择避开应用程序，而直接攻击数据源。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-113">An attacker may choose to circumvent your application and attack the data source directly.</span></span>  
  
 [<span data-ttu-id="4f4f2-114">安全性和用户输入</span><span class="sxs-lookup"><span data-stu-id="4f4f2-114">Security and User Input</span></span>](../../../standard/security/security-and-user-input.md)  
 <span data-ttu-id="4f4f2-115">描述如何处理与用户输入相关的细微和潜在危险缺陷。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-115">Describes how to handle subtle and potentially dangerous bugs involving user input.</span></span>  
  
 <span data-ttu-id="4f4f2-116">[验证 ASP.NET 网页中的用户输入](/previous-versions/aspnet/7kh55542(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="4f4f2-116">[Validating User Input in ASP.NET Web Pages](/previous-versions/aspnet/7kh55542(v=vs.100))</span></span>  
 <span data-ttu-id="4f4f2-117">概述如何使用 ASP.NET 验证控件验证用户输入。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-117">Overview of validating user input using ASP.NET validation controls.</span></span>  
  
 [<span data-ttu-id="4f4f2-118">Windows 窗体中的用户输入</span><span class="sxs-lookup"><span data-stu-id="4f4f2-118">User Input in Windows Forms</span></span>](/dotnet/desktop/winforms/user-input-in-windows-forms)  
 <span data-ttu-id="4f4f2-119">提供用于验证 Windows 窗体应用程序中鼠标和键盘输入的链接和信息。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-119">Provides links and information for validating mouse and keyboard input in a Windows Forms application.</span></span>  
  
 [<span data-ttu-id="4f4f2-120">.NET Framework 正则表达式</span><span class="sxs-lookup"><span data-stu-id="4f4f2-120">.NET Framework Regular Expressions</span></span>](../../../standard/base-types/regular-expressions.md)  
 <span data-ttu-id="4f4f2-121">描述如何使用 <xref:System.Text.RegularExpressions.Regex> 类检查用户输入的有效性。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-121">Describes how to use the <xref:System.Text.RegularExpressions.Regex> class to check the validity of user input.</span></span>  
  
## <a name="windows-applications"></a><span data-ttu-id="4f4f2-122">Windows 应用程序</span><span class="sxs-lookup"><span data-stu-id="4f4f2-122">Windows Applications</span></span>  

 <span data-ttu-id="4f4f2-123">过去，Windows 应用程序通常使用完全权限运行。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-123">In the past, Windows applications generally ran with full permissions.</span></span> <span data-ttu-id="4f4f2-124">通过使用代码启用安全性 (CAS)，.NET Framework 可提供限制在 Windows 应用程序中执行代码的基础结构。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-124">The .NET Framework provides the infrastructure to restrict code executing in a Windows application by using code access security (CAS).</span></span> <span data-ttu-id="4f4f2-125">但是，仅使用 CAS 是不足以保护应用程序的。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-125">However, CAS alone is not enough to protect your application.</span></span>  
  
 [<span data-ttu-id="4f4f2-126">Windows 窗体安全</span><span class="sxs-lookup"><span data-stu-id="4f4f2-126">Windows Forms Security</span></span>](/dotnet/desktop/winforms/windows-forms-security)  
 <span data-ttu-id="4f4f2-127">讨论如何保证 Windows 窗体应用程序的安全并提供相关主题的链接。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-127">Discusses how to secure Windows Forms applications and provides links to related topics.</span></span>  
  
 [<span data-ttu-id="4f4f2-128">Windows 窗体和非托管应用程序</span><span class="sxs-lookup"><span data-stu-id="4f4f2-128">Windows Forms and Unmanaged Applications</span></span>](/dotnet/desktop/winforms/advanced/windows-forms-and-unmanaged-applications)  
 <span data-ttu-id="4f4f2-129">描述如何与 Windows 窗体应用程序中的非托管应用程序进行交互。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-129">Describes how to interact with unmanaged applications in a Windows Forms application.</span></span>  
  
 [<span data-ttu-id="4f4f2-130">Windows 窗体的 ClickOnce 部署</span><span class="sxs-lookup"><span data-stu-id="4f4f2-130">ClickOnce Deployment for Windows Forms</span></span>](/dotnet/desktop/winforms/clickonce-deployment-for-windows-forms)  
 <span data-ttu-id="4f4f2-131">描述如何在 Windows 窗体应用程序中使用 `ClickOnce` 部署，并讨论安全含义。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-131">Describes how to use `ClickOnce` deployment in a Windows Forms application and discusses the security implications.</span></span>  
  
## <a name="aspnet-and-xml-web-services"></a><span data-ttu-id="4f4f2-132">ASP.NET 和 XML Web services</span><span class="sxs-lookup"><span data-stu-id="4f4f2-132">ASP.NET and XML Web Services</span></span>  

 <span data-ttu-id="4f4f2-133">ASP.NET 应用程序通常需要限制对 Web 站点某些部分的访问，并提供其他数据保护机制和站点安全机制。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-133">ASP.NET applications generally need to restrict access to some portions of the Web site and provide other mechanisms for data protection and site security.</span></span> <span data-ttu-id="4f4f2-134">这些链接可提供用于保护 ASP.NET 应用程序的有用信息。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-134">These links provide useful information for securing your ASP.NET application.</span></span>  
  
 <span data-ttu-id="4f4f2-135">XML Web services 能够提供可由 ASP.NET 应用程序、Windows 窗体应用程序或其他 Web 服务使用的数据。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-135">An XML Web service provides data that can be consumed by an ASP.NET application, a Windows Forms application, or another Web service.</span></span> <span data-ttu-id="4f4f2-136">你需要管理 Web 服务自身的安全性以及客户端应用程序的安全性。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-136">You need to manage security for the Web service itself as well as security for the client application.</span></span>  
  
 <span data-ttu-id="4f4f2-137">有关详细信息，请参阅以下资源。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-137">For more information, see the following resources.</span></span>  
  
|<span data-ttu-id="4f4f2-138">资源</span><span class="sxs-lookup"><span data-stu-id="4f4f2-138">Resource</span></span>|<span data-ttu-id="4f4f2-139">说明</span><span class="sxs-lookup"><span data-stu-id="4f4f2-139">Description</span></span>|  
|--------------|-----------------|  
|<span data-ttu-id="4f4f2-140">[保护 ASP.NET 网站](/previous-versions/aspnet/91f66yxt(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="4f4f2-140">[Securing ASP.NET Web Sites](/previous-versions/aspnet/91f66yxt(v=vs.100))</span></span>|<span data-ttu-id="4f4f2-141">讨论如何保证 ASP.NET 应用程序的安全。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-141">Discusses how to secure ASP.NET applications.</span></span>|  
|<span data-ttu-id="4f4f2-142">[保证使用 ASP.NET 创建的 XML Web services 的安全](/previous-versions/dotnet/netframework-4.0/w67h0dw7(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="4f4f2-142">[Securing XML Web Services Created Using ASP.NET](/previous-versions/dotnet/netframework-4.0/w67h0dw7(v=vs.100))</span></span>|<span data-ttu-id="4f4f2-143">讨论如何实现 ASP.NET Web 服务的安全性。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-143">Discusses how to implement security for an ASP.NET Web Service.</span></span>|  
|<span data-ttu-id="4f4f2-144">[脚本攻击概述](/previous-versions/aspnet/w1sw53ds(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="4f4f2-144">[Script Exploits Overview](/previous-versions/aspnet/w1sw53ds(v=vs.100))</span></span>|<span data-ttu-id="4f4f2-145">讨论如何抵御脚本攻击，该攻击会尝试将恶意字符插入网页。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-145">Discusses how to guard against a script exploit attack, which attempts to insert malicious characters into a Web page.</span></span>|  
|<span data-ttu-id="4f4f2-146">[Basic Security Practices for Web Applications（Web 应用程序的基本安全实践）](/previous-versions/aspnet/zdh19h94(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="4f4f2-146">[Basic Security Practices for Web Applications](/previous-versions/aspnet/zdh19h94(v=vs.100))</span></span>|<span data-ttu-id="4f4f2-147">常规安全信息和指向更多讨论的链接，</span><span class="sxs-lookup"><span data-stu-id="4f4f2-147">General security information and links to further discussion,</span></span>|  
  
## <a name="remoting"></a><span data-ttu-id="4f4f2-148">远程处理</span><span class="sxs-lookup"><span data-stu-id="4f4f2-148">Remoting</span></span>  

 <span data-ttu-id="4f4f2-149">利用 .NET 远程处理，可以方便地生成广泛分布的应用程序，而不论应用程序组件是全部集中在一台计算机上，还是分布在世界各地。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-149">.NET remoting enables you to build widely distributed applications easily, whether the application components are all on one computer or spread out across the entire world.</span></span> <span data-ttu-id="4f4f2-150">生成的客户端应用程序可以使用同一台计算机（或可通过其网络连接到的任何其他计算机）上其他进程中的对象。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-150">You can build client applications that use objects in other processes on the same computer or on any other computer that is reachable over its network.</span></span> <span data-ttu-id="4f4f2-151">您还可以在同一进程中使用 .NET 远程处理与其他应用程序域进行通信。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-151">You can also use .NET remoting to communicate with other application domains in the same process.</span></span>  
  
|<span data-ttu-id="4f4f2-152">资源</span><span class="sxs-lookup"><span data-stu-id="4f4f2-152">Resource</span></span>|<span data-ttu-id="4f4f2-153">说明</span><span class="sxs-lookup"><span data-stu-id="4f4f2-153">Description</span></span>|  
|--------------|-----------------|  
|<span data-ttu-id="4f4f2-154">[远程应用程序的配置](/previous-versions/dotnet/netframework-4.0/b8tysty8(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="4f4f2-154">[Configuration of Remote Applications](/previous-versions/dotnet/netframework-4.0/b8tysty8(v=vs.100))</span></span>|<span data-ttu-id="4f4f2-155">讨论如何配置远程处理应用程序以避免出现常见问题。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-155">Discusses how to configure remoting applications in order to avoid common problems.</span></span>|  
|<span data-ttu-id="4f4f2-156">[远程处理中的安全性](/previous-versions/dotnet/netframework-4.0/9hwst9th(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="4f4f2-156">[Security in Remoting](/previous-versions/dotnet/netframework-4.0/9hwst9th(v=vs.100))</span></span>|<span data-ttu-id="4f4f2-157">描述身份验证和加密以及与远程处理相关的其他安全主题。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-157">Describes authentication and encryption as well as additional security topics relevant to remoting.</span></span>|  
|[<span data-ttu-id="4f4f2-158">安全性和远程处理注意事项</span><span class="sxs-lookup"><span data-stu-id="4f4f2-158">Security and Remoting Considerations</span></span>](../../misc/security-and-remoting-considerations.md)|<span data-ttu-id="4f4f2-159">描述与受保护对象和应用程序域交叉相关的安全问题。</span><span class="sxs-lookup"><span data-stu-id="4f4f2-159">Describes security issues with protected objects and application domain crossing.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="4f4f2-160">请参阅</span><span class="sxs-lookup"><span data-stu-id="4f4f2-160">See also</span></span>

- [<span data-ttu-id="4f4f2-161">保证 ADO.NET 应用程序的安全</span><span class="sxs-lookup"><span data-stu-id="4f4f2-161">Securing ADO.NET Applications</span></span>](securing-ado-net-applications.md)
- <span data-ttu-id="4f4f2-162">[数据访问策略的建议](/previous-versions/visualstudio/visual-studio-2008/8fxztkff(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="4f4f2-162">[Recommendations for Data Access Strategies](/previous-versions/visualstudio/visual-studio-2008/8fxztkff(v=vs.90))</span></span>
- [<span data-ttu-id="4f4f2-163">保护应用程序</span><span class="sxs-lookup"><span data-stu-id="4f4f2-163">Securing Applications</span></span>](/visualstudio/ide/securing-applications)
- [<span data-ttu-id="4f4f2-164">保护连接信息</span><span class="sxs-lookup"><span data-stu-id="4f4f2-164">Protecting Connection Information</span></span>](protecting-connection-information.md)
- [<span data-ttu-id="4f4f2-165">ADO.NET 概述</span><span class="sxs-lookup"><span data-stu-id="4f4f2-165">ADO.NET Overview</span></span>](ado-net-overview.md)
